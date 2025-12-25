## 2.2. Core ideas in Deep Learning [^1]

Machine Learning research is experiencing its biggest growth spurt in the history of the field. With groundbreaking ideas being published several times a year, how can one keep up with the field? The good news is that the useful set of foundational ideas is updated only every few years. Below, we describe a subset of those ideas at an intuitive level, and why they matter for EO.

### 2.2.1. Architectures

#### **2.2.1.1. Convolutional Neural Networks (CNNs)**

 Convolution is the backbone of modern computer vision and remains central to AI4EO applications. CNNs rely on *location invariance*, the idea that features such as a building’s footprint can be recognized regardless of where they appear in an image. This makes CNNs efficient: instead of relearning the same building features across multiple locations, the network generalizes them across the image.

Traditional CNNs operate on 2D images (X and Y), but the approach extends naturally to 3D datacubes. In EO, the extra dimension often represents *time*, enabling 3D CNNs to learn spatio-temporal patterns such as land cover change.

#### **2.2.1.2. Recurrent Neural Networks (RNNs)**

 RNNs introduce a notion of *memory* by feeding outputs back into their own inputs. This allows them to capture temporal or sequential dependencies. An example is seasonal vegetation changes from EO time series. While powerful, RNNs are limited by their ability to retain information over very long sequences. Examples of recurrent neural network structures include LSTM (Long Short Term Memory) blocks or GRU (Gated Recurrent Unit) blocks. Each of them have a temporal element which maintains some historic data and holds that forward to the next timestep, so that the previous values will impact the future outputs.

#### **2.2.1.3. Attention and Transformers**

 Originally developed for natural language processing, Transformers (built on stacked attention layers) are increasingly used in vision tasks. Attention mechanisms dynamically learn *contextual relationships*: e.g., recognizing a road may require connecting distant pixels along a line, whereas recognizing crops may require local context. Unlike CNNs, Transformers can adaptively decide what to focus on. Early adoption in EO was slowed by computational costs. For example, in a 100 x 100 image, the model needs to deal with 10, 000 pixels which does not fit in GPU memory. So, more practical implementations had to be devised for images by limiting the attention span of each pixel to a certain radius. 

### 2.2.2. Degrees of Supervision

**Weakly-supervised learning** — EO datasets rarely fits perfectly into the supervised learning paradigm. Expert annotations are expensive to produce. Weak supervision is effectively a compromise in the level of detail of the ground truths that allows for faster and cheaper annotation. For example, it is pointless to fully annotate and delineate the exact shape of water bodies in a river network for hundreds of kms, when a ML model requires only fragments of it to learn to segment rivers. Another example of weak-supervision is to train segmentation and object detection models with annotation at the image level but not at the pixel level.

**Semi-supervised learning** — It is common for EO datasets to be partially annotated. For example, many crop fields in a region might lack annotation, yet these regions contain temporal spectral signatures that obey the same physical laws. Crop fields with similar spectral signatures are likely to represent the same type of crop, regardless of annotation. The main idea of weak-supervision is that even a non-annotated spectral signature is a valuable feature that can guide the learning and prediction of the annotated ones.

**Active learning** — The problem of learning is not just about ‘what’ to learn, but also ‘when’ to learn it. In the typical supervised learning paradigm, an ML model is allowed to plough through thousands of labelled data points whose individual contribution to the overall learning can be dubious. This is obviously inefficient when time is of the essence. With Active Learning, the labelling process occurs with an ML model in the loop, that tells the human which datapoint to label next. This can speed up the learning process of a model by orders of magnitude.

**Transfer learning** — This type of learning makes sense when there exists a database of general-purpose models pretrained on very large datasets. These might perform well enough on average, but they might not necessarily fit the needs of an individual use-case. For example, an end-user might have a bespoke and probably expensive dataset that they cannot share beyond their local network (for legal reasons). In this case, instead of uploading and adding their data to a bigger corpus, they can download one such pre-trained model and fine-tune its parameters to their data.

**Self-supervised learning** — SSL is the most promising approach to unsupervised learning. To appreciate the simplicity of SSL, it helps to view it in the light of supervised learning. In Computer Vision all images share the same "DNA"—a conglomeration of oriented lines, curves, color gradients, and other low-level spatial configurations—all ubiquitous in what the human eye could reasonably perceive. With that in mind, SSL defines its own ML tasks on a use-case. We can easily do so by altering a dataset of images in a consistent manner while retaining the originals. Then we can train a ML model to ‘repair’ altered images to their original state and because we kept the originals we can do this with good-old supervised learning. Such tasks whose ground-truths are produced programmatically are known as *pretext tasks*, see **Table 2.2.2-1**.

| Pretext task | Image degradation | Reconstruct from |
| ----- | :---- | :---- |
| Inpainting / infilling | remove center patch | rest of the image |
| Spectral interpolation | remove the RED band | other bands |
| Time extrapolation | remove final **revisit** from time-series | past revisits |
| Colour restoration | remove colour / convert to monochrome | monochrome image |
| Super-resolution | reduce spatial resolution | low-resolution image |

**Table 2.2.2-1**: Real examples of pretext tasks in SSL. Each degradation implies a reconstruction task.

The running theme here is to guess the *missing* parts from the *observed* parts, and the best part is that they all depend on ground-truth whose generation is trivial to automate. The point of all this is that regardless of the pretext task, a similar set of low-level visual features will be learned (the hypothetical ‘DNA’). This observation leads to the main hypothesis of self-supervision, written here as a question:

*Since any given ground-truth might not be the exclusive enabler for the learning of low-level features, why allow the absence of expertly annotated ground-truths be the information bottleneck to learning?*

SSL allows us to leverage as much unlabelled data as we can store, to learn ‘jack-of-all-trades’ features useful for common vision tasks, like classification. Then we can specialize (fine-tune) them in a supervised way through our limited ground-truths. Regardless, industry and science practitioners of SSL will be the first to agree on the importance of pretext task design. For example, in agriculture when it comes to classifying crops, we expect seasonality to be a key differentiator of temporal crop signatures\[[1](/reference.md#ref.1)\]. Here, once again the real-world is reminding us that there is no replacement for creativity and subject-matter expertise, and that intuitions gained from ImageNet eventually do hit a wall.

**Foundation Models** — Foundation models are a more recent development within the field of machine learning. They leverage the benefits of self-supervised learning and of transfer learning. In these models, a large scale model is developed using some SSL task, such as a masked auto-encoder, using a massive quantity of data. Once these models are trained, to represent the SSL task, they are then modified and *transferred* to a different task, known as fine-tuning. This fine-tuning is the application of the pre-trained foundation model to a different downstream task, using principles of transfer learning. It has been shown that these foundation models learn the inherent structures within the data they are aiming to represent and can then be fine-tuned on new tasks with much less data that would be required to build a model from scratch, improving the performance on a weakly-supervised task. 

**The role of ground-truth in unsupervised learning** — If there is one takeaway from the success stories of unsupervised learning, it is that an obsession with nailing the end-task alone misses the point of learning and can even hinder a model from reaching its full potential. On the other hand, regardless of the type of unsupervised learning being used, the importance of the availability of expertly annotated ground-truths cannot be overstated. Ultimately, a successful application of ML must be demonstrably predictive of the end-task. This means, ground-truth labels, whether acquired by manual annotation or from expensive bona-fide physics simulations, will always be in high demand. Even if they serve merely as a sanity check, or a unit-test.

[^1]: Content modified and adapted with permission from the [Satellite Applications Catapult Whitepaper by Kalaitzis et al. (2022) : State of AI for Earth Observation.](https://sa.catapult.org.uk/digital-library/white-paper-state-of-ai-for-earth-observation/)

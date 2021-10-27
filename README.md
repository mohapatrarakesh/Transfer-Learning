# Transfer-Learning
Transfer learning is a machine learning method where a model developed for a task is reused as the starting point for a model on a second task.

Most of the time you won't want to train a whole convolutional network yourself. Modern ConvNets training on huge datasets like ImageNet take weeks on multiple GPUs.
Instead, most people use a pretrained network either as a fixed feature extractor, or as an initial network to fine tune.

In this notebook, you'll be using VGGNet trained on the ImageNet dataset as a feature extractor. Below is a diagram of the VGGNet architecture, with a series of convolutional and max-pooling layers, then three fully-connected layers at the end that classify the 1000 classes found in the ImageNet database.
 
VGGNet is great because it's simple and has great performance, coming in second in the ImageNet competition. The idea here is that we keep all the convolutional layers, but replace the final fully-connected layer with our own classifier. This way we can use VGGNet as a fixed feature extractor for our images then easily train a simple classifier on top of that.
•	Use all but the last fully-connected layer as a fixed feature extractor.
•	Define a new, final classification layer and apply it to a task of our choice!
You can read more about transfer learning from the CS231n Stanford course notes.


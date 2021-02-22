## St. Georges classification task
- Original [dataset](https://enterideas.com/testcv)

### Context

This repo contains a notebook with a baseline solution for a generic binary image classification task.
The task is solved by fine-tuning an EfficientNet_B3 using tempered cross entropy loss.
No multi-GPU support or gradient checkpointing is implemented.

### Setup

In order to run this notebook, you'll need to:
 - Install pytorch following instructions in the link below:

https://pytorch.org/get-started/locally/

 - Install Torchelie:

pip install git+https://github.com/vermeille/Torchelie

 - Install Ranger Optimizer

pip install -e git+https://github.com/lessw2020/Ranger-Deep-Learning-Optimizer.git#egg=Ranger

To set up the rest of the prerequisites do in bash:
```bash
pip install requirements.txt
```
macos users (additional step):
```bash
brew install libomp

### Dataset

The provided dataset contains 6047 images which belong to one of two categories:
2681 images containing depictions of St. Georges and 3366 other images.
Images are of various sizes, have varying number of channels, the dataset also has
some noise in it's labels, as images belonging to the positive label also contain
images of people, buildings, flags and other objects that don't contain St. Georges'
depiction.

### Acknowledgements

This dataset was downloaded from:
https://enterideas.com/testcv
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

In order to use GPU, make sure that your pytorch and cuda versions are compatible.
Using GPU as adviced.

 - Install poetry:

https://python-poetry.org/docs/#installation

To install the rest of dependencies, run poetry install command in bash:
```bash
poetry install
```

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
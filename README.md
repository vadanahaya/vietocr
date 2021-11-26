# VietOCR
**Please update to version vietocr>=0.3.5 to avoid errors.**
<p align="center">
<img src="https://github.com/pbcquoc/vietocr/raw/master/image/sample.png" width="1000" height="300">
</p>

In this project, I install Transformer OCR model to recognize handwriting and typed letters for Vietnamese. Model architecture is a great combination between CNN and Transformer models (which is the foundation model of the quite famous BERT). The TransformerOCR model has a lot of advantages compared to the CRNN model that has been installed by me. You can read [at](https://pbcquoc.github.io/vietocr) here about the architecture and how to train the model with different data sets.

VietOCR model has extremely good generality, even has quite high accuracy on a new dataset even though the model has never been trained.

<p align="center">
<img src="https://raw.githubusercontent.com/pbcquoc/vietocr/master/image/vietocr.jpg" width="512" height="614">
</p>

# Setting
To install, type the following command
```
pip install vietocr==0.3.5
```
# Quick Start
Please refer to this notebook [https://github.com/pbcquoc/vietocr/blob/master/vietocr_gettingstart.ipynb) to know how to use it.

# Model Zoo
This library implements both seq models, attention seq2seq and transfomer. Seq2seq has a very fast prediction speed and is used in the industry quite a lot, but transformer is more accurate but prediction is quite slow. Therefore, I provide both types for you to choose from.

This model is trained on a dataset of 10m images, including many different types of images such as self-generated images, handwriting, and actual scanned documents.
Pretrain models are available.

# Test results on 10m tập
| Backbone | Config | Precision full sequence | time |
| ------------- |:-------:| ---:|---:|
| VGG19-bn - Transformer | vgg_transformer | 0.8800 | 86ms @ 1080ti |
| VGG19-bn - Seq2Seq | vgg_seq2seq | 0.8701 | 12ms @ 1080ti |

The prediction time of the vgg-transformer model is too long compared to the seq2seq model, while there is no clear difference between the accuracy of these two architectures.

# Dataset
I only provide a sample data set of about 1m self-generated images. You can download it at [here](https://drive.google.com/file/d/1T0cmkhTgu3ahyMIwGZeby612RpVdDxOR/view).
# License
I release this library under the terms of [Apache 2.0 license]().

# Contact
If you have any problem, please create an issue or contact me at pbcquoc@gmail.com

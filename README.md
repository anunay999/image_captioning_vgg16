# Image Captioning using VGG16
The task of image captioning can be divided into two modules logically – one is an image based model – which extracts the features and nuances out of our image, and the other is a language based model – which translates the features and objects given by our image based model to a natural sentence.

For our image based model (viz encoder) – we usually rely on a Convolutional Neural Network model. And for our language based model (viz decoder) – we rely on a Recurrent Neural Network. The image below summarizes the approach given above.

![alt text](https://raw.githubusercontent.com/yunjey/pytorch-tutorial/master/tutorials/03-advanced/image_captioning/png/model.png)

Here I'm using a pre-trained [VGG16](https://github.com/fchollet/deep-learning-models/releases/download/v0.1/vgg16_weights_tf_dim_ordering_tf_kernels.h5) model with weights as my CNN which will act as an input to my RNN(LSTM)

The Dataset which I used for this project is [Flickr8k](https://www.kaggle.com/srbhshinde/flickr8k-sau), [Flickr30k](http://shannon.cs.illinois.edu/DenotationGraph/) or [MS-COCO](http://cocodataset.org/#download) which is widey used dataset for image captioning can also be applied in this case. I'm limited by resources to train my model on huge datasets so I chose Flickr8k.

Models
============

In VergeML you can find an array of Machine Learning models and we will continue adding new models. 
Currently, we only support image based models: 

* vergeml/densenet           Densenet model, with weights pre-trained on ImageNet.
* vergeml/inceptionresnetv2  InceptionResnetV2 model, with weights pre-trained on ImageNet.
* vergeml/inceptionv3        InceptionV3 model, with weights pre-trained on ImageNet.
* vergeml/mobilenet          MobileNet model, with weights pre-trained on ImageNet.
* vergeml/mobilenetv2        MobilenetV2 model, with weights pre-trained on ImageNet.
* vergeml/nasnet             NASNet model, with weights pre-trained on ImageNet.
* vergeml/resnet50           ResNet50 model, with weights pre-trained on ImageNet.
* vergeml/similar            Image Simililarity Search
* vergeml/vgg16              VGG16 model, with weights pre-trained on ImageNet.
* vergeml/vgg19              VGG19 model, with weights pre-trained on ImageNet.
* vergeml/xception           Xception model, with weights pre-trained on ImageNet.

If you want to contribute by porting new models into VergeML, you can follow these instructions:

How to port a new model to VergeML
============

Porting a model to VergeML has some core benefits: 

  * Other users can easily access your model
  * You can focus on your model, as the peripheral tasks (such as data loading) are handled within VergeML 
  * If you are a researcher, getting peer reviewed will become an easy and grant reproducibility. 

> At the moment we only support models based on TensorFlow. Other frameworks will follow soon!

In order to port a model follow these steps: 

Get rid of peripheral functions
------------




Write this in your model source code
------------


Let us know!
------------

We will include your ported model into our model galery and name you official porting author for this model. 

Wirte us to: models@vergeml.com

You will be named in the section "SourceCode" of your model to give you credits on your great support!


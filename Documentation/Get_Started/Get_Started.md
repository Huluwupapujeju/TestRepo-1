Get Started
============

New to VergeML? No probs, with this guide you will get an easy introduction!
We show you how to built an image classifier and built a rest interface for your possible web app.

Software Requirements
-----------
Before you start, make shure you have the following packages installed: 

> [Python 3.7](https://www.python.org/downloads/)

> [Tensorflow](https://www.tensorflow.org/install/)

> [Cuda 9.1](https://developer.nvidia.com/cuda-toolkit-archive) (for GPU support)

> [cuDNN 7.1](https://developer.nvidia.com/cudnn) (for GPU support, you will need to register @ Nvidia to download)

If you need more help installing VergeML we have a seperate, more detailed [guide](link) to help you through the installation process.

Installing VergeML
-----------

You can directly install VergeML from the Python Package Index with pip:

    pip install vergeml

Or if you want to do it manually you can checkout the current version from git and install it yourself:

    git clone https://github.com/vergeml


Installing your first ML Model
-----------
For this tutorial we will use the image classifier "resnet50", but if you desire a different model, you can check the complete list of supported models here (link. 

Now, start by installing Inception 

    ml install resnet50

> Info: BTW, you can always use "ml help" for detailed information about functions and commands within VergeML.

Creating your first project
-----------
First choose a directory on your machine where you want to use VergeML for your projects. We created a directory called /vergeml

Now navigate to this directory and run the following command in order to setup the structure for your first project "my_cat_dog_classifier": 

    ml --model resnet new my_cat_dog_classifier

In your project directory you will now find the following subdirectories and files:
 
 /samples  --> directory for sample images
 
 vergeml.yaml  --> your project file


Start your training!
-----------

Now we want to sort our training data. A good starting point would be the cats and dogs dataset (200mb), so lets download it.

    ml download cats_and_dogs

Otherwise, you could use your own dataset by simply copying your images into at least two subfolders within the /samples directory. You should have at least 10 images per image category!

Rename the subdirectories based on your image categories (lables) and be shure that the images are placed in their corresponding directories:
* cats
* dogs

Now we simply want to start to train, right? So type: 

    ml train

This will create a new AI (in our case called: @relaxing-doom) in the newly created /training directory. Here all relevant information will be stored, such as checkpoints and stats and it will look something like this:

![example image](\Images\training.jpg "An exemplary image")


Now lean back and let it train...

> Info: Your dataset will as a standard be split into 80% training, 10% validation and 10% test instances.

When your newly AI has now finished training and you are not 100% happy with your results, you can always train again and change your hyperparameters by adding:

    ml train --layers=3 --learning_rate=0.002 --epochs=50

> Info: You can find model relevant hyperparameters by typing: ml help train






Creating a REST service
-----------

Your newly created AI is now finished and you are ready to test it out through a REST API!

For us, we simply type: 

    ml @touchy_automaton rest 

Or for a complete directory with multiple images: 

    ml @touchy_automaton predict --batch /test_directory/*jpg

Use the following command, if you cant remember your trained AI name or want to compare your multiple training instances for performance and accuracy. 

    ml list

You can always further train an instance: 

    ml @touchy_automaton train

Further reads
-----------

Check out these docs:

* [Data Management](http://www.vergeml.com/model/inception_tl)
* [Installation](http://www.vergeml.com/model/inception_tl)
* [Models](http://www.vergeml.com/model/inception_tl)
* [Training](http://www.vergeml.com/model/inception_tl)
* [VergeML](http://www.vergeml.com/model/inception_tl)
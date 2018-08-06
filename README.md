![VergeML](https://github.com/cpalegra/TestRepo/blob/master/Header.png "VergeML")


Introduction
============

VergeML is command line based environment for exploring, training and running state-of-the-Art Machine Learning models. It integrates all necessary tools and services (from preprocessing to REST API) so you can totally focus on creating your ML applications.

Sometimes training a new ML model is as easy as typing:
    
    ml train

Features
============
VergeML is currently handling all tasks for running image based ML models and we are currently on our beta stage. It is under active development and maintenance! Starting with v0.8, VergeML operates on continuous integration, and all releases are tagged in git. If you'd like to contribute, see CONTRIBUTING!

Building Veneur requires Go 1.9 or later.

### ML Projects ###


Each project creates all structures you need from creating the 


### ML Models ###

Currently we only support image based ML models, where we handpicked the most relevant and production ready models currently available. You can see here the list of currently ported models to VergeML. New models will be ported every week, so keep posted!

If you'd like to contribute by porting new models, here are detailed instructions on how to do it. 

### Data Management ###

VergeML handles all data specific workflows, from data loading to preprocessing and augmentations. Here you can find more specific documentation on this chapter.

### Training and Performance ###
Train your models, manage your hyperparameters through the command line or via a config file and compare performancen on your experiments. 


### Plug-In System ###



### REST Interface ###



Get Started
============

Start using VergeML within minutes by following these instructions.

Software Requirements
-----------
Before you can get going with VergeML, make shure you have the following packages installed: 

> Python 3.6 [Hyper](http://www.hyper.is)

> Python 3.6 [Hyper](http://www.hyper.is) (Optional)

If you need more help installing VergeML we have a seperate, more detailed [document](http://www.vergeml.com/docs/installation) to guide you through the installation.

Installing VergeML
-----------

You can directly install VergeML from the Python Package Index with pip:

    pip install vergeml

Or if you want to do it manually you can checkout the current version from git and install it yourself:

    git clone https://github.com/vergeml

First tips before you get started
-----------
Use the command. 

    ml help



Installing your first ML Model
-----------
In this section we will guide you through the whole cycle of installing, training and predicting the image classifier [inception](http://vergeml.com/model/inception). 

Start by installing Inception 

    ml install inception

This will install all necessary components, such as tensorflow, its dependencies and laslty the model itself.


Creating your first project
-----------
First choose a directory on your machine where you want to use VergeML for your projects. We created a directory called /vergeml

Now navigate to this directory and run the following command in order to setup you project structure for your first project "my_inception": 

    ml --model inception_tl new my_inception

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

This will create a new training instance (in our case called: @touchy_automaton) in the newly created /training directory. Here all relevant information will be stored, such as checkpoints and stats and it will look something like this:

![example image](\Images\platzhalter.PNG "An exemplary image")

Now lean back and let it train...


Performance validation
-----------

Your newly created AI has now finished training and you are ready to test it out!

For us, we simply type: 

    ml @touchy_automaton predict --file /test_directory/image1.jpg

Or for a complete directory with multiple images: 

    ml @touchy_automaton predict --batch /test_directory/*jpg

Use the following command, if you cant remember your trained AI name or want to compare your multiple training instances for performance and accuracy. 

    ml list

You can always further train an instance: 

    ml @touchy_automaton train


Documentation
============

We recommend you to read the following docs for in-depth information: 

1. Data Management: [Inception_tl](http://www.vergeml.com/model/inception_tl)
2. Installation: [Inception_tl](http://www.vergeml.com/model/inception_tl)
3. Models: [Inception_tl](http://www.vergeml.com/model/inception_tl)
4. Training: [Inception_tl](http://www.vergeml.com/model/inception_tl)
5. VergeML: [Inception_tl](http://www.vergeml.com/model/inception_tl)

License
============

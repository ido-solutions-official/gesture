# Gesture training model
Machine : MAC Os Mojave ver 10.14.4

Language : python 3.6.8

Packages : see <a href="https://github.com/ido-solutions-official/gesture/blob/master/requirement.txt">requirement.txt</a>
## How to use the notebook
**Step1 : Set up your computer**

This notebook was written in jupyter notebook(.ipynb). If you don't have Python notebook installed on your computer <a href="https://github.com/ido-solutions-official/index/wiki">see more instructions here</a>

**Step2 : Clone repository**

by using git, type 

`git clone https://github.com/ido-solutions-official/gesture.git gesture`

in the terminal. If you don't have Git installed on your computer <a href="https://git-scm.com/downloads">see more instructions here</a>

**Step3 : Install python packages**

install Python packages with requirement.txt in repository. Simply open terminal, go to your python environment, then type

`pip install -r requirement.txt`

---
#### Remarks (18 APR 2019)
This Notebook run using _Keras versions 2.2.4_; however, installing from `pip` resulting in errors when fitting model with validation. We recommend installing Keras directly from their github using `git`.

`git clone https://github.com/keras-team/keras.git`

Then, `cd` to the Keras folder and run the install command:

```
cd keras
sudo python setup.py install
```
---
**Step4 : Prepare Dataset**

In this example, we had already prepare some hand-gesture dataset structured as following;
```
gesture
|_
  raw_images
    |_ train
      |_buff_20.png
      |_...
      |_...
  processed_images
    |_buff
      |_buff_20.png
      |_...
      |_...
    |_luv
    |...
    |...

```
* by running part 1 of Python notebook, It will convert training data(__.png__ images in folder `raw_images/train`) into images in folder `processed images`

* the training images must be named in a format **_catagory_id.xxx_** i.e. __buff_20.png__ or __paper_90.jpg__

* We could prepare new data set by 
  1. Delete all images in a folder `raw_images/train`
  2. Delete a folder `processed_images`
  3. Put new images in a folder `raw_images/train` with specified format.
  4. Run part 1 of Python notebook again
  
**Step5 : Train and Predict a gesture**

By running part 2 of Python notebook, It will created a keras CNN model, save in .h5 format, then predict an in-sample data

* My CNN model is the same as Number classfication based on MNIST database. Credit : <a href="https://github.com/asingh33/CNNGestureRecognizer#cnn-model-used">Abhishek Singh,asingh33/CNNGestureRecognizer: CNNGestureRecognizer (Version 1.3.0),</a>


* Use model to predict images however you like i.e. with OpenCV

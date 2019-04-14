# Gesture training model
Machine : MAC Os Mojave ver 10.14.4

Language : python 3.6.8

Packages : see <a href="https://github.com/ido-solutions-official/gesture/blob/master/requirement.txt">requirement.txt</a>
## How to use notebook
**Step1 : set up your computer**
This notebook wrote in jupyter notebook(.ipynb). If you don't have Python notebook installed on your computer <a href="https://github.com/ido-solutions-official/index/wiki">see more instructions here</a>

**Step2 : clone repository**
by using git, type 

`git clone https://github.com/ido-solutions-official/gesture.git gesture`

in the terminal. If you don't have Git installed on your computer <a href="https://git-scm.com/downloads">see more instructions here</a>

**Step3 : install python packages**
install Python packages with requirement.txt in repository. Simply open terminal and type

`pip install -r requirement.txt`


**Step4 : Prepare Dataset**
In this example, we had already prepare some hand-gesture dataset structured as following;
```
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
* by running part 1 of Python notebook, It will convert train data(.png images in folder `raw_images/train`) into images in processed images

* the training images must be named in a format *catagorial_id.xxx* i.e. _buff_20.png_ or _paper_90.jpg_

* We could prepare new data set by 
  1. Delete all images in `raw_images/train`
  2. Delete folder `processed_images`
  3. Put new images in folder `raw_images/train` with specified format.
  4. Run part 1 of Python notebook again
  
**Step5 : Train and Predict a gesture**
By running part 2 of Python notebook, It will created a keras CNN model, save in .h5 format, then predict an in-sample data

* My CNN model is the same as Number classfication based on MNIST database. Credit : <a href="https://github.com/asingh33/CNNGestureRecognizer#cnn-model-used">Abhishek Singh,asingh33/CNNGestureRecognizer: CNNGestureRecognizer (Version 1.3.0),</a>


* Use model to predict images however you like i.e. with OpenCV

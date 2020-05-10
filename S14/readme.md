Background Images – Streets (A combination of different country streets backgrounds)

Foreground – Footballers (Cuz they are fun)

(Background)[link]

(Footballer)[link]



1)	Downloaded the random images from google.

2)	Resized the different sized images to 224x224 maintaining some aspect ratio.

3)	Have taken images of 100 footballers in different positions

4)	Through powerpoint have removed the background and generated the forground images of said footballers. Also found out the hard way that PNG supports transparency but JPG does not.

5)	Cropped the images manually to make sure they contain the footballers only in the center of image.

6)	Understood that the 4th channel indicates transparency. So through use of this channel wrote a simple code to generate masks for foreground images. 

7)	Written a script to overlay the images, generate the mask, while keeping in mind the forgeound must be embedded within the background. 

8)	Uploaded the images and masks to google drive.

9)	Cloned this repo https://github.com/ialhashim/DenseDepth.git

10)	Loaded the model into colab

11)	Iterated through each of the generated images (resized to 448 as the model was reducing output size by half) and created depth masks as follows.

12)	Calculated the mean and std of the dataset.

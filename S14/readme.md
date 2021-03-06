# Background Images – Streets (A combination of different country streets backgrounds)

![Background](https://github.com/raviteja8484/EVA4/blob/master/S14/bg_012.png)

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/bg_021.png)


# Foreground – Footballers (Cuz they are fun)

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/fg_036.png)

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/fg_037.png)


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

13) PNG supports image transparency so they were used for creating the masks. But the JPEG sizes are smaller hence they have been used for that

14) Image quality was reduced to 65% to reduce the size of the data format. 


# FG Masks

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/fg_mask_036.jpg)

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/fg_mask_037.jpg)

# Depth Model Predictions

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/img_0005.jpg)

![Background2](https://github.com/raviteja8484/EVA4/blob/master/S14/img_0021.jpg)

## BG Calculation

Computing mean: 100%|██████████| 1/1 [00:10<00:00, 10.75s/it]

Computing std:   0%|          | 0/1 [00:00<?, ?it/s]

Mean:  tensor([0.5039, 0.5001, 0.4850])

Computing std: 100%|██████████| 1/1 [00:00<00:00,  1.88it/s]

Std:  tensor([0.2466, 0.2463, 0.2581])





## FG Calculation


Computing mean:   0%|          | 0/1 [00:00<?, ?it/s]

Computing mean: 100%|██████████| 1/1 [00:00<00:00,  2.11it/s]

Computing std:   0%|          | 0/1 [00:00<?, ?it/s]

Mean:  tensor([0.1883, 0.1555, 0.1361])

Computing std: 100%|██████████| 1/1 [00:00<00:00,  1.77it/s]

Std:  tensor([0.3097, 0.2736, 0.2482])


## Mask calculation

Computing mean:   0%|          | 0/1 [00:00<?, ?it/s]

Computing mean: 100%|██████████| 1/1 [00:00<00:00,  2.27it/s]

Computing std:   0%|          | 0/1 [00:00<?, ?it/s]

Mean:  tensor([0.3647, 0.3647, 0.3647])

Computing std: 100%|██████████| 1/1 [00:00<00:00,  1.93it/s]

Std:  tensor([0.4768, 0.4768, 0.4768])

## FG_BG

Computing mean:   0%|          | 0/4 [00:00<?, ?it/s]

Mean:  tensor([0.1727, 0.1361, 0.1439])

Computing std:   0%|          | 0/4 [00:00<?, ?it/s]

Std:  tensor([0.1907, 0.1712, 0.1576])

# Scripts

![Data creation](https://github.com/raviteja8484/EVA4/blob/master/S14/data_creation.ipynb)

![STD and Mean Caluclation](https://github.com/raviteja8484/EVA4/blob/master/S14/Calculation.ipynb)

![DATA SET](https://drive.google.com/drive/folders/1mdsfyT4LXikBSgAsHRD-um8Q1f2gEnRC?usp=sharing)



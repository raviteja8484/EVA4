## Part 1:

1)	Building the code and the model and see whether it’s working properly. 

2)	Coding the model structure properly is important.

3)	 Have to reduce the number of parameters as well

4)	Everything seems to be working well.



## Part 2: 

1)	Write the RF for all the conv blocks

2)	Target : - 

a.	Reduce the number of parameters and work on model architecture

b.	Skeleton code right. Check to see if the model structure is what u want. Once you fix on it you won’t be getting around to change it much.

3)	Changes made

a.	Removed padding of 1

b.	Adding Relu to convolution and transition blocks.

c.	Reducing the number of filters

d.	Changed filter size to 5 for first conv block and then 10 and so on

e.	Changed filter size from 5 to 8 since observed Training and test accuracies had huge gaps (1.2%)

4)	Observations 

a.	The final conv layer has around 5k parameters there itself

b.	Training accuracy – 99.13(8-16 Filter size)

c.	Test Accuracy – 98.53

d.	Training accuracy -99. 10  (10-16 Filter size)

e.	Test Accuracy – 98.70 

f.	Gap between Training and test is not as big but not small as well. Used this model for going ahead with



## Part 3: 

1)	Target

a.	BatchNormalization – Added to improve model accuracy

b.	Use Regularization technique and added dropout value of (0.2)

2)	Changed made

a.	Added batch normalization to every convolution layer.

b.	Added dropout after adding BN



3)	Observations :-

a.	Batch Normalization has added more time for training! And a few parameters!

b.	Training accuracy -99.93% (Only BN)

c.	Test accuracy – 99.36%

d.	Model has scope for improvement.

e.	Model is almost overfitting

f.	Training accuracy – 99.45% ( Dropout-0.2)

g.	Test accuracy – 99.24

h.	Training accuracy – 99.56% (Dropout 0.1)

i.	Testing Accuracy – 99.32% 





## Part 4:

1)	Target : -

a.	Batch normalization and dropout have been added. 

b.	Add GAP 

2)	Changes made

a.	Added gap instead of final convolution layer.

b.	Avoiding code 7 (noted observations)

3)	Observations

a.	Parameters reduced to 6k

b.	Accuracy reduced to 98.83%

c.	GAP seems to have reduced the gap between training and test accuracy very well. Final epoch was 98.83 (both train and test)

4)	Part 4.2

a.	Accuracy is close but we are still not getting to go above 99%

b.	Training acc – 98.74%

c.	Test acc- 98.88%

d.	Lets add one more layer to this model itself only.

## Part 5

# GOAL
*   Image augmentation. 
*   Model finalizing 
*   Changed learning rate to 0.4
*   Maintaining consistent accuracy 
*   Fine tuning out some loose ends

Result 

1) We have achieved the accuracy of 99.42% crossing the threshold of 99.4% in under 15 epochs.

2) Image augmentation has helped us to increase the accuracy very so slightly.

3) Only one epoch was able to achieve above 99.4%. Consistency was maintained around 99.39%




| K,p,s     	| In 	| Out 	| Receptive Field 	| J(out) 	|
|-----------	|----	|-----	|-----------------	|--------	|
| 0         	| 0  	| 28  	| 1               	| 1      	|
| 3,0,1     	| 28 	| 26  	| 3               	| 1      	|
| 3,0,1     	| 26 	| 24  	| 5               	| 1      	|
| 1,0,1     	| 24 	| 24  	| 5               	| 1      	|
| 2,0,2(MP) 	| 24 	| 12  	| 5               	| 1      	|
| 3,0,1     	| 12 	| 10  	| 9               	| 2      	|
| 3,0,1     	| 10 	| 8   	| 13              	| 2      	|
| 3,0,1     	| 8  	| 6   	| 17              	| 2      	|
| 3,1,1     	| 6  	| 6   	| 21              	| 2      	|
| 6,0,6     	| 6  	| 1   	| 31              	| 2      	|
| 1,0,1     	| 1  	| 1   	| 31              	| 12     	|


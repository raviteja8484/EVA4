Session 8
==========

Things done
-----------
1. Proudly written the very first python library. Named ‘Gudiya’ (Named after a friend)
2. Implemented proper utilization of classes in python. 
3. Two classes doing everything. 
  * Model.py (code taken from https://github.com/kuangliu/pytorch-cifar) (Resnet 18)
  * TrainandTestUtils.py (Train, Test and other utilities)
4. Both the classes above are taken from the Library below.
5. [Gudiya](https://pypi.org/project/Gudiya/) (v=0.1.1.4)
6. Have most of the functions available in this library
  * Display model summary
  * Plot training images  
  * Train and test model
  * Plot misclassified images
  * Plot class wise and total accuracy
  * Plotting testing and training accuracy


Parameters
----------
1. Data Augmentations used = {Random Crop, Random Horizontal Flip, To Tensor, Normalize}
2. Optimizer = SGD
  * LR = 0.001
  * Momentum = 0.95
  * Weight decay = 0.0004
 3.	Scheduler = OneCycleLR
  * Max LR = 0.1
  * Total Steps =40
3.	**Epochs = 40**
4.	**Training ACCURACY = 99.66%**
5.	**Testing ACCURACY = 93.76%**

False Positives
---------------


![alt text](https://github.com/raviteja8484/EVA4/blob/master/S8/FP.PNG "False Positives") 



Training vs Validation Accuracy
-------------------------------

![Im](https://github.com/raviteja8484/EVA4/blob/master/S8/PlotGraph.PNG)


Results
-------
1. One cycle LR gave very high results.  Have to see why 
2. Model can be pushed more with more control over the model and the augmentations, LR, optimizers etc.
3. Can implement L1 as well?


Next Steps
----------
  o	 Implement more utilities for control over the parameters and data
  
  o	 Use the predictions to set an API and see if the weights can be saved and used as a service.
  
  o	 Work with and implement best codes ever to be used by self and others.
  
  
How do I feel?
--------------

![Gif failed](https://github.com/raviteja8484/EVA4/blob/master/S8/own.gif)

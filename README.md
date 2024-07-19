# Model performance with and without using relu activation function

In this experiment I am trying see whats the effect of Relu activation function.

## Data set
  I have used make_circles() from sklearn.dataset to create dataset.
  In the dataset of 1000 samples is created.
  This dataset has two features(x0, x1) and one label( y either 0 or 1). x0 and x1 refers to coordinate point in 2-d plane.
  I have split the data in 8:2 ratio for training and testing respectively.
  Here is the dataset in the 2-d plane
  ![image](https://github.com/user-attachments/assets/6f441962-19d5-43d0-8f1d-93854428b298)
  Yellow and voilet are two different datasets

## Models
  In this experiment I have created two different models.
  One with relu activation function and other without Relu activation function.
  One with relu is model_0 and without relu is model0
  ### Architecture of the models
    model0:-
     CircleModelV0(
    (layer1): Linear(in_features=2, out_features=5, bias=True)
    (layer2): Linear(in_features=5, out_features=10, bias=True)
    (layer3): Linear(in_features=10, out_features=1, bias=True)
    )

    model_0:-
    Sequential(
      (0): Linear(in_features=2, out_features=5, bias=True)
      (1): ReLU()
      (2): Linear(in_features=5, out_features=1, bias=True)
    )

  for both the model the loss function is BCEwithlogits() (Binary Cross Entropy), and optimizer is SGD(Standard Gradient Descendent). 

## Training and results
Both models were trained for 10000 epoches, But results are intresting. The model with model with Relu has improved its performance from 50% to 99%.
But the model without relu activation function was struck at around 50%. So on this data set we need non-linear componet which is detected by relu function.
here are the images
![image](https://github.com/user-attachments/assets/1cd24e04-1f7e-4596-ab86-0fc2cd476fb0)
with relu


![image](https://github.com/user-attachments/assets/3d51bdbb-2a14-4889-9305-64ba928b1a89)
without relu


  

  

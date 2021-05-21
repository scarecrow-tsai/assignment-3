# Assigment 3


The notebook contains 4 major parts. 

1. Dataset and DataLoader
2. Model
3. Train Loop 
4. Test Loop and Classification Table


## Data Representation

The images are converted into tensors. After being normalized, they are sent into the network. The random integer to be added is taken as a single number which is passed through an FC layers to generate a latent representation of the same. 


## Data Generation Strategy

The random number tensors are generated on the fly during the training loop. The shape of this tensor is the same as the image-output size.


## Output Combination

Both the image and random number are passed through the network to generate an latent vector of size 20. We choose 20 because it is the maximum sum possible. We then add these two latent representations and calculate the loss. The true value is the sum of image-output + random number genrated. 


## Results Evaluation

The results are evaluated using the `classification_report`, `accuracy_score`, and `confusion_matrix` functions from sklearn. Classification report gives the precision, recall, and F1-score for each class. The average F1 score is 50%. The accuracy is 51%.

## Loss Function

I used the cross-entropy loss because this is a multi-class classification network which means the number of output classes are more than 2. 

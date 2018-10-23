
# Week 9 - Optimal Weightings (Contd.)

We came to a realisation in our weekly meeting with Dilpreet that our genetic algorithm was using the same dataset for training and testing and hence our results were unfairly representating the true accuracy of the model. To fix this, we had to conduct an additional market survey to gather more data. Once we have enough data for both a train and validation set, we can accuractely evaluate our model. I rewrote the genetics algorithm to train itself of half of the training set with it's fitness function as the accuracy on the other half of the training set. Once repeating this process for a certain number of epochs (1000 epochs) we can validate it on our validation set we have gathered.

# DQN_demo_for_SI


This repo contains a notebook of me trying to implement DQN by hand in order to better my understanding of the algorithm. I am using DQN in the space invaders environment.



A summary of DQN

We implement DQN when the environment space is big. Deep Q-learning calculates the loss functions between the Q-target and the predicited Q-value which then updates the weights and bias accordingly. It takes in a state and outputs a Q-value with a corresponding action. A simplified version of architeture of DQN is input -> CNN layer -> fully connected layer -> action with Q-value


Phases of DQN
There is sampling phase in which actions are peformed and the store the observed experience tuples in a replay memory
There is the training phase that takes small batch of tuples randomly from the buffer and, the model learns from this batch by using a gradient descent

The down side of DQN is its instability because we combinie a non-linear Q-value function and updating targets with existing estimates and not an actual complete return. There is also the temporal limitation problem 

To combat this issue we use previous experiences to make sure that we are not lossing prior learnt experience. We also use double DQN which has two networks, a target network and a DQN network, to reduce the overestimation of Q-vaues. Target network gets the Q-Target value of taking that action at the next state while the DQN selects the best action based on the highest Q-value.

Q-Target is calculated by Rt+1 + (gamma * estimate of Q-value in next state) 

Q-loss is calculated by Q-Target - previous Q-value estimation





CNN stands for convolutional nerual network and its able to caputre spatial and Temporal dependencies in an image through the application of relevant filters, i.e it gets the most important information from a image

Fully connectd layers are linear layers that connect the input neuron to every output neuron. 

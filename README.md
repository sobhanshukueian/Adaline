# Adaline
ADALINE (Adaptive Linear Neuron) implementation for predicting X and O characters in python.

Adaline is a single layer neural network with multiple nodes where each node accepts multiple inputs and generates one output.The ADALINE was created by Widrow and Hoff in 1960

![image](https://user-images.githubusercontent.com/47561760/123557610-182c5180-d7a7-11eb-8916-aac5ff99d580.png)

# Architecture
The ADALINE computes the activation potential y by summing up all the contributions from the multiplication of the inputs by the synaptic weights and its threshold.
and adjust the weights and bios as follows (The process of adjusting the weights and threshold of the ADALINE network is based on a learning algorithm named the Delta
rule (Widrow and Hoff 1960) or Widrow-Hoff learning rule, also known as LMS (Least Mean Square) algorithm or Gradient Descent method) :  

![image](https://user-images.githubusercontent.com/47561760/123557906-c389d600-d7a8-11eb-9408-1f82ab7a079a.png)
![image](https://user-images.githubusercontent.com/47561760/123557915-d00e2e80-d7a8-11eb-9a28-a686c5957530.png)

.t represents desired value or target.

.b represents bios.

.w represents weights.

.a represents learning rate

The last step for producing the ADALINE output y is using of an activation function.

# Trainig Model

The idea of the Delta rule, when n training samples are available, is to minimize the difference between the desired output t and the response y
of the linear combiner, considering all n samples, in order to adjust the weights and threshold of the neuron.

The function of the squared error related to the p training samples is defined by:

![image](https://user-images.githubusercontent.com/47561760/123558342-ecab6600-d7aa-11eb-91da-c5e6c619d5f3.png)

The next step consists of the application of the gradient operator on the mean squared error with respect to vector w, in order to search for an optimal value for the squared error function

![image](https://user-images.githubusercontent.com/47561760/123558533-039e8800-d7ac-11eb-97e1-b26c5960266a.png)

![image](https://user-images.githubusercontent.com/47561760/123558512-e073d880-d7ab-11eb-89ea-197632fc89e4.png)

Finally, the steps for adapting the weight vector must be executed in the opposite direction of the gradient,
because the optimization goal is to minimize the squared error(the negative sign of delta E and n cancel each other out ).
In this condition, the variation w to update the ADALINE weight vector is given by :

![image](https://user-images.githubusercontent.com/47561760/123558581-48c2ba00-d7ac-11eb-859e-55453ac500bc.png)

![image](https://user-images.githubusercontent.com/47561760/123558607-71e34a80-d7ac-11eb-813e-b496aff97f2b.png)

To demonstrate the convergence process of the ADALINE, the below figure illustrates a geometric interpretation of the steps needed to update vector w
towards the minimum point w* of the squared error function {E(w)}

![image](https://user-images.githubusercontent.com/47561760/123558634-9b03db00-d7ac-11eb-8b20-118038e2b171.png)







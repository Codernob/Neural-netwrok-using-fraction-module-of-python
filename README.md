# Neural netwrok using fraction module of python
 In this repository I have performed several experiments using the Fraction module of python to see if it has any difference compared to floating point arithmetic.<br>
 I had originally hypothesized that using fractions in stead of floats would result in better accuracy of the model. But it turned out that using fractions has next no effect on the accuracy of the model.<br>
 The results of my experiments are summarized as below:<br>
| Loss function     | Activation  | Accuracy and training time<br> of Floating point Implementation     | Accuracy and training time <br>of Fraction Implementation | 
| :---              |    :----:   |          :---:                                                  |          :---:                                        |
| Log-Loss           | ReLu        | 96.3%,  0.3s                                                       |             96.3% , 7.2s                          |
| MSE                | Sigmoid     |         93.59270609460634%, 0.1s                               |   93.59270609460631%, 15 minutes 36 seconds              |
| L1 Loss            | Sigmoid         |    93.333%, 17s                                            |   93.333% , 17 minutes 49 seconds                         |   <br>
Stochastic Gradient Descent (SGD) optimizer was used in every implementation. <br>
To add insult to injury, using fractions results in long training times. This can be explained by the fact that fraction operations involve gcd calculations which can get computationally costly over time.
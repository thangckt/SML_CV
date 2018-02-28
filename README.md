# Supervised Machine Learning + Enhanced sampling
Using supervised machine learning to build collective variables for accelerated sampling

This repo contains the necessary details for reproducing the results from our manuscript:

Sultan et al: Decision functions from supervised machine learning algorithms as collective
variables for accelerating molecular simulations, arXiv preprint 

The general idea can be summarized using the picture below: 
![SVM boundary](https://github.com/msultan/SML_CV/blob/master/chignolin_example/pic1.png)

Given some sampling in the start and end states, a SML algorithm such as a Support Vector Machine 
can find a hyper plane that maximally divides those states. Then the distance to this plane can be
used as a collective variable in molecular dynamics and enhanced sampling calculations. 

We can use the decision function, which basically measures this distance, in a variety of different 
ways. For example, in logistic regression methods, this is done via a sigmoid of the linear weights. SML based CVs can use non-linearity via kernels or neural network based classifiers. Multiple states can be incorporated via bias-exchange. For more details, please see the manuscript. 

The repo requires several other python and non-python packages including MSMBuilder, MSMExplorer, 
tica_metadynamics, scikit-learn, Plumed, and OpenMM . 

1). The folders contains the ipython notebooks + 
setup scripts needed to reproduce the main results of the paper. It also contains a step-by-step guide on how to generate input files needed for Plumed to able to run Metadynamics using the SML's decision function as the collective variable. 


# Fractal time series noise recognition
Project is dedicated to the study of methods for detecting and classifying noise in fractal time series using convolutional neural networks.
The main focus is on analyzing the trajectories of fractal Brownian motion with different levels of additive noise. As part of the research, a model was created that uses visual images of trajectories to train the neural network and evaluate its effectiveness.
## Fractal time series
Fractal time series, which exhibit self-similarity properties across different scales, are used to model various processes in finance, medicine, ecology, and other fields. An important characteristic of these series is their ability to accurately describe complex systems, enabling understanding of behavior and prediction of future changes.
## Fractal Brownian motion
Fractal Brownian motion is an important concept in many fields because it demonstrates the property of self-similarity across different scales, making it a useful tool for modeling various processes. It should be noted that fractal Brownian motion is a random process that exhibits self-similarity properties across different scales. This means that the structure of the series remains similar when scaled up or down. Fractal Brownian motion is a continuous Gaussian process in random time on the interval [0, ], starting from zero, with zero mean for all and the following covariance function: $E[B_H(t) B_H(s)] = \frac{1}{2} \left( |t|^{2H} + |s|^{2H} - |t - s|^{2H} \right)$


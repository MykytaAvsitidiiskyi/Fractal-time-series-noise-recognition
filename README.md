# Fractal time series noise recognition
Project is dedicated to the study of methods for detecting and classifying noise in fractal time series using convolutional neural networks.
The main focus is on analyzing the trajectories of fractal Brownian motion with different levels of additive noise. As part of the research, a model was created that uses visual images of trajectories to train the neural network and evaluate its effectiveness.
## Fractal time series
Fractal time series, which exhibit self-similarity properties across different scales, are used to model various processes in finance, medicine, ecology, and other fields. An important characteristic of these series is their ability to accurately describe complex systems, enabling understanding of behavior and prediction of future changes.
## Fractal Brownian motion
Fractal Brownian motion is an important concept in many fields because it demonstrates the property of self-similarity across different scales, making it a useful tool for modeling various processes. It should be noted that fractal Brownian motion is a random process that exhibits self-similarity properties across different scales. This means that the structure of the series remains similar when scaled up or down. Fractal Brownian motion is a continuous Gaussian process in random time $B_H(t)$ on the interval $[0, T]$, starting from zero, with zero mean for all $t \in [0, T]$ and the following covariance function: $E[B_H(t) B_H(s)] = \frac{1}{2} \left( |t|^{2H} + |s|^{2H} - |t - s|^{2H} \right)$, where $H$ - s a real number in the interval $(0, 1)$.
The Hurst parameter describes the unevenness of the resulting motion, with higher values leading to smoother motion. The value of $𝐻$ determines the type of process, which is a fractional Brownian motion:
1) If $H = 0.5$, then the process is a standard Brownian motion;
2) If $H < 0.5$, then the increments of the process are negatively correlated;
3) If $H > 0.5$, then the increments of the process are positively correlated.
Additionally, correlated increments of the process indicate the presence of persistence or memory in the process. A persistent process, or a process with memory, is characterized by the fact that changes in the value of the process at one point in time usually cause changes in values at future points in time in the same direction.
## Noise in fractal Brownian motion
Additive noise added to fractal time series is a key aspect in the analysis and modeling of complex systems. It reflects the random variations that occur in the process and can be expressed through a characteristic such as variance. Variance, in turn, is a measure of the distribution of the series values around its mean. In the context of fractal Brownian motion, variance reflects the intensity and variability of the additive noise that affects the underlying process. Analysis of additive noise can help identify interrelationships between different parts of the system and detect potential risk points or weaknesses. This is important for developing risk management strategies and optimizing the overall functioning of the system.
## Dataset
As part of this study, we focus on modeling fractal Brownian motion and generating training data for further analysis and classification. Our approach is based on creating several datasets, each containing different classes of fractal Brownian motion with various Hurst exponent indicators and additive noise in the form of variance.
It is important to note that we do not work directly with the fractal Brownian motions themselves. Instead, we work with their representations. This is a crucial aspect of our methodology, as it allows us to apply powerful image processing and deep learning tools to analyze and classify these random processes.
Two datasets were generated as part of the study: representations of fractal Brownian motion with Hurst exponent values of $\( H = 0.7 \)$ and $\( H = 0.9 \)$. This allowed us to obtain various series that differ in the degree of correlation between process increments and to evaluate the quality of classification with different Hurst exponent values.
Both datasets are divided into four classes. In each class, we add additive noise in the form of variance. This allows us to study the impact of different noise levels on the characteristics and behavior of fractal Brownian motion. Each class corresponds to a certain level of noise variance: $\( \sigma^2 = 0 \)$, $\( \sigma^2 = 0.2 \)$, $\( \sigma^2 = 0.5 \)$, and $\( \sigma^2 = 0.9 \)$.


![image](https://github.com/MykytaAvsitidiiskyi/Fractal-time-series-noise-recognition/assets/134547942/ed51c15c-37d0-4a0b-b99a-7883541b0e6b)

Fractal realisation with $H = 0.5$ and $\( \sigma^2 = 0 \)$

![image](https://github.com/MykytaAvsitidiiskyi/Fractal-time-series-noise-recognition/assets/134547942/21a16bca-2103-416c-8bde-1e69114ccfe2)

*Fractal realisation with $H = 0.5$ and $\( \sigma^2 = 0.2 \)$*

![image](https://github.com/MykytaAvsitidiiskyi/Fractal-time-series-noise-recognition/assets/134547942/816aad3a-151e-401f-a017-afe2e32ceaa8)

*Fractal realisation with $H = 0.5$ and $\( \sigma^2 = 0.7 \)$*

![image](https://github.com/MykytaAvsitidiiskyi/Fractal-time-series-noise-recognition/assets/134547942/99c961e1-2e59-4f4f-8a02-e77ec6cf3e97)

*Fractal realisation with $H = 0.5$ and $\( \sigma^2 = 0.9 \)$*


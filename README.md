# Stochastic Volatility Barndorff-Nielsen-Shephard Model and Its Uses in Option Market

In this long code structure, you will find the following applications with real-world data set,

1. Valuation of European Options, 

2. Option Pricing Using Fourier Methods,

3. Semi-Analytical Solution for European Call Options,
   
4. Simulation of the Ornstein–Uhlenbeck (OU) Process and Asset Price Dynamics,
   
5. Application of the BNS Model to Real-World Market Data

Calibration : 

The calibration of option prices can be stated as a least squares minimization problem. Hence, in this subsection we describe data set, optimization method, and objective function which are used to generate parameter vector which allows us to generate market prices via the semi-analytical formula and monte carlo simulation.

Optimization Method :

The calibration is done via the SLSQP optimization algorithm which is available in Python-scipy package. SLSQP is primarily designed for nonlinear constrained optimization. As stated in Joshy and Hwang (2024) ‘’it solves the general nonlinear programming problem:

I tried bunch of other optimization method to abate the pain for deep out of the money options. I particularly observed some improvements in L2 regularization method, but I was so tight on time to dig deeper. 

Note: More will follow from the thesis.

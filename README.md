# Barndorff-Nielsen-Shephard Model and Its Uses in Option Market

In this long code structure, you will find the following applications with real-world data set,

1. Option Pricing Using Fourier Methods,

2. Semi-Analytical Solution for European Call Options,
   
3. Simulation of the Ornstein–Uhlenbeck (OU) Process and Asset Price Dynamics (BDLP is a gamma),

4. Application of the BNS Model to Real-World Market Data

Calibration : 

The calibration of option prices can be stated as a least squares minimization problem. Hence, in this subsection we describe data set, optimization method, and objective function which are used to generate parameter vector which allows us to generate market prices via the semi-analytical formula and monte carlo simulation.

Optimization Method :

The calibration is done via the SLSQP optimization algorithm which is available in Python-scipy package. SLSQP is primarily designed for nonlinear constrained optimization. As stated in Joshy and Hwang (2024) ‘’it solves the general nonlinear programming problem:

I tried bunch of other optimization method to abate the pain for deep out of the money options. I particularly observed some improvements in L2 regularization method, but I was so tight on time to dig deeper. 

Notes :

In this code, well-known Ornstein-Uhlenbeck type stochastic volatility model is implemented, namely BNS Model, and its uses in option valuation. 

First, I simulated the background driving Lévy process (BDLP), the OU Process through BDLP, and the asset price with synthetic model parameters. This allowed me to demonstrate one of the important properties of BNS model which is the leverage effect.

Second, European call option prices were generated with real market data. To gauge the performance of the BNS model, two different pricing approaches were used. The first approach is the semi-analytical pricing formula and the second approach is Monte Carlo simulation. This enabled us to compare two methods directly.

Two important results have been observed in the option pricing with real market data. First result I get is the very low error rate in semi-analytical formula. Here model prices are very close to market prices. This result highlights robustness of semi-analytical solution to price European option. Second result is obtained via Monte Carlo simulation. It is shown to generate realistic valuation. BNS model average error rate is seen to be 1.9%. Please observe that error rate is high in simulation results compared to semi-analytical formula. One reason is discritization errors. Another reason may be the data quality. Master data for this analysis is retrieved from yahoo finance webpage.

Finally, BNS model is shown to generate the obesrved market prices with low error rates. However, improvements are needed  about computational methods.

Note: More will follow soon from the thesis.

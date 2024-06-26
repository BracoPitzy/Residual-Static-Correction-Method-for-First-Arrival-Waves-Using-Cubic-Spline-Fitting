# Residual-Static-Correction-Method-for-First-Arrival-Waves-Using-Cubic-Spline-Fitting

## Abstract
This article aims to explore the method of using spline curves to fit the first arrival times of seismic waves and separate disturbances. Firstly, based on the Karush-Kuhn-Tucker (KKT) conditions, this paper concludes that the optimal solution satisfying the smoothness requirement of the fitting curve is a cubic spline curve, and provides the derivative conditions that the spline curve should satisfy. Subsequently, based on these conditions, this paper establishes a system of linear equations using the three-moment method. By utilizing the KKT conditions, it is obtained that the Lagrange multiplier $\lambda$ should lie on the boundary of the constraint, and then the approximate range of $\lambda$ is obtained through bisection method, and it is discretized to calculate the first arrival time curves on different lines corresponding to different firing points, determining the total disturbance at each receiving point. In the third part, this paper further establishes a linear model to separate the disturbances at each firing point from those at each receiving point. Finally, this paper plots a three-dimensional graph of the random disturbances at all firing and receiving points based on coordinates.

**Keywords**: KKT conditions, cubic spline, three-moment method, static correction

## Background Introduction
In oil and gas exploration, artificial seismic wave generators are often used to detonate explosives at firing points and receivers are placed at surface detection points to collect waveform amplitudes and other information. Each receiver records waveform data for a period of time, forming a seismic trace. Due to environmental factors and the influence of data processing techniques, the first arrival times obtained from the traces often contain random disturbances. Therefore, it is necessary to fit the first arrival waves and separate the disturbances from firing points and detection points.

## Core Issue
The core issue is to solve the following optimization problem:

$$\min \int_{x_0}^{x_n}[FT_{ij}(x)]^2 \mathrm{d}x$$

$$\mathrm{s.t.} \quad \sum_{i=0}^{n}\left ( \frac{FT_{ij}(x_k)-FT_{ij}(x_{ijk})}{\sigma_{jk}} \right )^2 \le S$$

where $FT_{ij}(x)$ represents the first arrival time for the $j$ th line of the $i$ th firing point, which is globally twice continuously differentiable and piecewise four times continuously differentiable; $S$ is a constant satisfying $(n+1)−2\sqrt{n+1} \le S \le (n+1)+2\sqrt{n+1}$

## Results
![FT](https://github.com/BracoPitzy/Residual-Static-Correction-Method-for-First-Arrival-Waves-Using-Cubic-Spline-Fitting/blob/main/Figures/Fire%20Point%2050010001%20Line%201001%20First%20Arrival%20Time.png)
<p align="center">
  Figure 1: Fire Point 50010001 Line 1001 First Arrival Time $FT_{ij}$ and Original $FT \quad (OFT_{ij})$
</p>

![r3D](https://github.com/BracoPitzy/Residual-Static-Correction-Method-for-First-Arrival-Waves-Using-Cubic-Spline-Fitting/blob/main/Figures/3D%20Heat%20Map%20of%20Receiver%20Point%20Perturbations.png)
<p align="center">
  Figure 2: 3D Heat Map of Receiver Point Perturbations
</p>

![fp3D](https://github.com/BracoPitzy/Residual-Static-Correction-Method-for-First-Arrival-Waves-Using-Cubic-Spline-Fitting/blob/main/Figures/3D%20Heat%20Map%20of%20Fire%20Point%20Perturbations.png)
<p align="center">
  Figure 3: 3D Heat Map of Fire Point Perturbations
</p>



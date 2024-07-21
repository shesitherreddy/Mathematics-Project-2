# Replicating Model for treatment of Influneza A virus

APA Citation for the referenced paper:

Catherine A.A. Beauchemin , James J. McSharry , George L. Drusano, Jack T. Nguyen,
Gregory T. Went, Ruy M. Ribeiro, Alan S. Perelson.https://www.sciencedirect.com/science/article/pii/S0022519308002798#!

This project aimed to replicate, and maybe improve, the model described in the preceding paper. I picked the eclipse model since it fits better than the delay and simple models. This paper focuses on the dynamics of influenza virus strains and their behavior with varying drug concentrations inside the body. The drug that is typically used to treat this virus is adamantane, which has an efficiency of 80 to 90% when used within 48 hours of the onset of symptoms. In this paper, they examined how vivo and vitro models behave with the V variable, which is our main interest (infectious viral titer) in pfu/mL.

The Author used variations of the ordinary differential equation (ODE) models proposed by Baccam et al.(2006).below are the mentioned differential equations for eclipse model. Below are my model equations and my model fit which was done in python.

<p align="center">
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/Coupled%20ODE%20equations.png" width="350"><br>
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/fit_0.png" width="350"><br>
</p>


## Optimization of the parameters

I used the cruve_fit function to fit the parameters for the experimental data provided by the author, and the resulting graph showed a better fit than the author's model, but I am not confident in the optimized parameter results because some of the parameters are outside the range of 95% CI mentioned by the author. I chose to leave the optimized parameters to conduct further research and continued with the parameters mentioned in the paper.The values I obtained after optimization are shown below, as well as a graph created using the optimized parameters.


<p align="center">
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/optimized%20parameters.png"  width="350"><br>
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/optimized.png"  width="350"><br>
</p>

## Bifurcation Analysis

I performed a bifurcation study by changing the parameter p, which is the generation rate of infectious virions by productively infected cells, for the specified CI. I observed multiple steady states and then performed a bifurcation analysis for the same parameter by changing another parameter epsilon, which is drug efficacy, and discovered that the whole system reacted differently for different epsilon values. This is because epsilon is a direct function of D, which is drug concentration, and this made more sense when I performed local parametric sensitivity, as shown in sentivity analysis.The following graph depicts the analysis for two distinct medication concentrations.

<p align="center">
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/bifurication_1.png"  width="350"><br>
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/bifurication_2.png"  width="350"><br>
</p>

## Sensitivity Analysis

I performed a local sensitivity analysis by perturbing my parameters by 1% and discovered that epsilon is my sensitive parameter. To confirm this, I performed another sensitivity analysis known as the local initial condition sensitivity analysis, which revealed that epsilon has the greatest impact on our models, followed by p.

<p align="center">
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/local%20sensitivity_1.png" width="350"><br>
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/local%20sensitivity_2.png" width="350"><br>
</p>


I now considered checking my global sensitivity analysis for a larger perturbation of 20% and visualizing my parameter's effect on the model when repeated 1000 times.


<p align="center">
  <img src="https://github.com/shesitherreddy/Mathematics-Project-2/blob/main/global%20sensitivity_1.png" width="350"><br>
</p>








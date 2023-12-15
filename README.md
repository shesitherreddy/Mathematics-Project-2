# Replicating Model for treatment of Influneza A virus

APA Citation for the referenced paper:

Catherine A.A. Beauchemin , James J. McSharry , George L. Drusano, Jack T. Nguyen,
Gregory T. Went, Ruy M. Ribeiro, Alan S. Perelson.https://www.sciencedirect.com/science/article/pii/S0022519308002798#!

This project aimed to replicate, and perhaps improve, the model which is mentioned in the above paper. I used eclipse model since it has better fit when compared to delay and simple models this paper is focused on the dynamics of influenza virus strains and its behaviour with varying drug concenterations inside the body the drug which usually used to treat this virus is adamantane and it has an efficiency of 80 to 90% when used before 48 hours of the on set of symptoms in this paper they examined how vivo and vitro models are behaving with the V variable which is our main interest (infectious viral titer) in pfu/mL.

The Author used variations of the ordinary differential equation (ODE) models proposed by Baccam et al.(2006).below are the mentioned differential equations for eclipse model.

## Optimization of the parameters

I used cruve_fit function to fit the parameters for experimental data given by the author and the resulting graph showed better fit than the model given by the author but I am not confident with the optimized parameter results since some of the parameters are outside the range of CI mentioned by the Author I chose to leave the optimized parameters to conduct any further study and continued with the parameters mentioned in the paper.

## Bifurcation Analysis

I conducted bifurcation analysis by chnaging the parameter p which is the production rate of infectious virions by productively infected cells by varying this value for the given CI I observed multiple steady states and the conducted the bifurcation analysis for the same parameter by chnaging now another parameter epsilon which is drug efficacy and got to know that the whole system reacted differently for different epsilon values this is because epsilon is a direct function of D which is drug concenteration and this made more sense when I performed local parametric sensitivity which can be seen under sentivity analysis.

## Sensitivity Analysis

I conducted my local sensitivity analysis by perturbating my parameters by 1% and observed that the epsilon is my sensitive parameter to confirm this I conducted another sensitivity analysis which is called local initial condition sensitivity analysis which indicated that epsilon effects our models the most followed by p.

I now considered to check my global sensitivity analysis for bigger perturbation of 20% and visualized my paramerter effect on the model out but when is repeated for 1000 times.







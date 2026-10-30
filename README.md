# econ3916-lab10-causal-logic

# Correlation & Causality: Confounders, Colliders and the Limits of Controls

## Objective

In this lab, I explored why correlation does not always mean causation and how choosing different control variables can affect the accuracy of regression results.

## Methodology

- Simulated three datasets showing causation, confounding, and selection.
- Calculated correlations and created scatterplots to compare the three situations.
- Used networkx to create directed graphs showing confounders, colliders, and mediators.
- Ran regressions with and without control variables to observe changes in estimated effects.
- Tested how controlling for a collider can create a false relationship between independent variables.
- Created a function called `coef_on_d()` to calculate the coefficient on D with different controls.
- Compared experimental and observational estimates using the LaLonde job-training dataset.

## Key Findings

The three simulated worlds had correlations of 0.654, 0.664, and 0.632, even though only the first world had a true causal effect.

Controlling for a confounder improved the estimate from 2.476 to 1.500, matching the true effect of 1.5.

Controlling for a collider created a false estimate of -0.592, even though the true effect was zero.

In the M-bias simulation, controlling for W produced an estimate of -0.191. Adding u1 as another control brought the estimate back to approximately 0.006, much closer to the true effect of zero.

In the LaLonde analysis, the experimental estimate was $1,794, while the observational estimate without controls was -$8,498. Adding eight control variables increased the observational estimate to $699, closing approximately 89% of the gap.

## Conclusion

This lab taught me that a strong correlation does not necessarily mean one variable causes another. I also learned that adding more controls does not always improve a regression because some controls can introduce bias. Understanding the relationships between variables is important when deciding which controls to include.

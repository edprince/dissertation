\pagebreak

# Conclusion

Throughout the experiments put forward in this dissertation, several points can be
identified. Firstly, the choice of bundler and framework do impact the performance
of a web page - however, depending on the size of the app, the performance benefits
may be negligible. As researched by Lawson, the choice of bundler becomes more integral upon scaling the
usage of modules (Lawson 2016). When comparing each of the bundlers over multiple throttling thresholds,
it was seen that Rollup was in fact demonstrating its marginal benefits - utilising the
shared function scope bundling tactic.

As seen from Figure \ref{framework_chart}, the optimal solution when developing
for users on lower-power smartphones is the combination of Hyperapp and Rollup.
This combination sees the lowest overall score across multiple throttling
thresholds. This validates the prediction made in section \ref{prediction}.

This leads to an answer to the original question - How Can Web Developers
Optimise for Lower-Power Smartphones in the developing world?

They can choose their bundler carefully - based on the structure of their
application - with very modular applications seeing large
performance benefits from Rollup, and if further optimisation is desired, creating the 
project using Hyperapp will yield the greatest performance across
all four of the tested frameworks.

Hopefully this is just one brick in the foundations of more research
within this domain to create faster and better user experiences for
global users - not just with the latest smartphones.


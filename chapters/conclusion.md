\pagebreak

# Conclusion

Throughout the experiments put forward in this dissertation, several points can be
identified. Firstly, the choice of bundler and framework do impact the performance
of a web page - however, depending on the size of the app, the performance benefits
may be negligible. 

As researched by Lawson, the choice of bundler becomes more integral upon scaling the
usage of modules (Lawson 2016). When comparing each of the bundlers over multiple throttling thresholds,
it was seen that Rollup was in fact demonstrating its marginal benefits - utilising the
shared function scope bundling tactic.

As seen from the full comparison table, the optimal solution when developing
for users on lower-power smartphones is the combination of Hyperapp and Rollup.
This combination sees the lowest overall score across multiple throttling
thresholds. This validates the prediction made in section \ref{prediction}.

\pagebreak

# Evaluation and Results

To find an overall score for each combination, the 20 results collected
were averaged to create a sinlge score, before the average at each throttle
threshold were accumulated to give a final overall score. This represents the
overall time the CPU is processing. These final scores can then be compared
to the other combinations.

## Case Study 1: Bundlers

### Results of Webpack Bundling
| React Webpack(ms) | Preact Webpack(ms) | Inferno Webpack(ms) | Hyperapp Webpack(ms) |
|---|---|---|---|
| 0x | 3553.43 | 3207.11 | 3158.77 | 3107.11 |
| 4x | 12461.31	| 12307.86 | 12454.80 |	12184.16 |
| 6x | 18414.10 |	18133.34 | 18261.34 |	17943.42 |
| Total	| 34428.84 | 33648.31	| 33874.905	| 33234.69 |

### Results of Rollup Bundling
| React Rollup (ms) | Preact Rollup (ms) | Inferno Rollup (ms) | Hyperapp Rollup (ms) |
|---|---|---|---|
| 0x | 3099.51 | 3057.97 | 3081.70 | 2951.24 |
| 4x | 12088.92 | 12077.82 | 11947.46 | 12005.86 |
| 6x | 17711.29 | 17624.91 | 17694.07	| 17560.245 |
| Total | 32899.72 | 32760.7 | 32723.23 | 32517.345 |

![Webpack vs Rollup \label{webpack_vs_rollup}](./images/webpack_vs_rollup.png)

Figure \ref{webpack_vs_rollup} demonstrates that rollup performs better than webpack consistently
in these tests, with between one and three seconds faster cumulative times over the three
throttle thresholds.

## Case Study 2: Frameworks

![Frameworks \label{framework_chart}](./images/framework_chart.png)


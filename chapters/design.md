\pagebreak

# Design and Implementation

## Hardware Specifications
The experiment is being carried out on a machine running an AMD FX-8350
with the following specifications:

| Specification | Value |
|---|---|
| Processor Speed | 4GHz |
| Processor Count | 8 |
| Processor Socket | Socket AM3+ |
| Memory Type | DDR3 SDRAM |
| Wattage | 25w |

Table: CPU Specifications \label{cpu_specs}

## Testing Matrix

For the final results, each bundler would be tested with each
framework over three throttling thresholds - 0x, 4x and 6x. This
gives the final testing matrix.

Using this final matrix, the tests were run with the hardware specified
in table \ref{cpu_specs}. Each combination of framework and bundler was
tested 20 times separately in the headless Chrome browser. This eliminates
the possibility of an outlier being used if a single measurement is taken.
 
## Case 1 - Bundling

To test each bundlers performance, the testbed application was bundled
using the configuration files in the appendix (Rollup configuration in Appendix G,
Webpack configuration in Appendix H). One the application has been bundled
and served, the Puppeteer scripts found in Appendix E was used to run the
DevTools profiling.

### Prediction

Upon bundling the app, there are expectations that the loading time 
reduces, along with the total page weight. There is anticipation that 
the rendering and painting times will not fluctuate much if at all - 
as the same content is still being calculated, and exactly the same 
page is still being painted onto the screen. Loading and scripting 
times are expected to be where the fluctuation will be seen. It is
expected there will be a trade-off, and the final score will depend on
the weighting of that trade-off. Whilst the browser must do some extra
work when parsing the bundled version of the scripts, it also sees
the performance benefits as described in section 3.4.1. This also
backs up the prediction that of the two bundlers, Rollup should yield
better performance.

## Case 2 - Framework Analysis

With the application re-written in four different frameworks - React,
Preact, Inferno and Hyperapp, the testing required using each version
along with each bundler, and running the Puppeteer script on the resulting
locally-hosted application.

### Prediction

It is expected that React will be the slowest - with all of the other
frameworks marketing themselves as faster alternatives to React. With
Hyperapp being the smallest of all of them, there is a marginal weighting
to expect Hyperapp to be the best performer.

## Summary \label{prediction}
Before analysing the results, there are two key predictions - that
Rollup should outperform  Webpack - and Hyperapp is expected to be
the best performing framework. This creates a concise summated prediction
statement.

The optimal performance of the testbed application should be seen using
the combination of Hyperapp and Rollup.

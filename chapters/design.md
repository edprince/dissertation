\pagebreak

# Design and Implementation

## Case 1 - Bundling

### Summary

Whilst the browser can process many unminified JavaScript and CSS files, they can be bundled together into a single file with tools like “Webpack”.  This means the browser must only load, parse and execute one large file, rather than lots of separate files. 
“Create React App” uses this by default to optimise applications when they are built for production.

### Prediction

Upon bundling the app, there are expectations that the loading time reduces, along with the total page weight. There is anticipation that the rendering and painting times will not fluctuate much if at all - as the same content is still being calculated, and exactly the same page is still being painted onto the screen. Loading and scripting times are expected to be where the most significant increases are seen.

### Outcome
![Unbundled Chart](./images/unbundled_chart.png)
Figure: Unbundled App Across Throttle Levels \label{unbundled_chart}


## Case 2 - Server Decision Tools

## Summary

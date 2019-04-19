\pagebreak

# Design and Implementation

## Case 1 - Bundling

### Summary

Whilst the browser can process many unminified JavaScript and CSS files, they can be bundled together into a single file with tools like “Webpack”.  This means the browser must only load, parse and execute one large file, rather than lots of separate files. 
“Create React App” uses this by default to optimise applications when they are built for production.

### Prediction

Upon bundling the app, there are expectations that the loading time reduces, along with the total page weight. There is anticipation that the rendering and painting times will not fluctuate much if at all - as the same content is still being calculated, and exactly the same page is still being painted onto the screen. Loading and scripting times are expected to be where the most significant increases are seen.

When measuring the performance of Rollup - it is anticipated that the execution time should
decrease, as its handles modules in a different style to Webpack (Lawson, 2016).
Webpack turns each module into its own isolated function scope, whereas Rollup puts everything into the same function scope, which increases performance. Why is this?

~~~js
function foo(a, b) {
    function bar() {
        return a + b;
    }

    return bar();
}

let result = foo(1, 2);
~~~

When the JavaScript engine reaches this section of code, it creates a new function object
in memory for `foo()`. When the engine reaches the line where `foo()` is called, it executes
the function, which creates a new function: `bar()`. When the function execution finishes, the
`bar()` object in memory is destroyed. This means if `foo()` is called 100 times, the `bar()`
function is created and destroyed 100 times. This costs processing, making it generally
slower than non-nested functions.

### Outcome - Webpack

![Unbundled Chart](./images/unbundled_chart.png)


### Outcome - Rollup

It is evident from profiling the application that has been bundled with
Rollup has significantly reduced scripting times.

![Rollup Chart](./images/rollup_chart.png)

## Case 2 - Framework Analysis

## Summary

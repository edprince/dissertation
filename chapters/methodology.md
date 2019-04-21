\pagebreak

# Methodology

## Introduction

In order to perform in-depth analysis on the largest areas for optimisation, a web app would need to be studied in depth to gain insights. Rather than study an existing application, over which no control would be granted, a better solution would be to create a testbed application using modern technologies. In tandem with this, Devtools provides accurate and reliable data on browser applications, with the ability to throttle the CPU to judge performance on simulated lower-hardware. This would allow comparisons to be drawn across the different CPU throttle amounts, but with no other parameter changes.



## Testbed Application

The testbed application is a realtime chatting application - an application with a genuine use anywhere in the world. The front-end is built with React, making use of the popular Create React App library, and Socket.io to communicate with a Node.js server also running Socket.io. On top of this, the app makes use of several other libraries, such as Bootstrap, Moment, JQuery and Faker, giving a partially realistic build to the application.

## Bundlers 

To understand why bundlers are used - it is important to understand the history of JavaScript, and its current state. JavaScript is a programming language, created in 1995 - and
has been standardised with ECMA (European Computer Manufacturer's Association). Whilst the 9th edition of ECMAScript (ES2018) was finalised in June 2018, only modern browsers can
read ES2015 and above, meaning that if developers want their applications to be comprehensively compatible with browsers, the application must be written in ES2015. This raises
the issue that the newer versions of ECMAScript have introduced many features of the language that offer superior development - meaning developers want to write their code in ES2015+.
This is where a compiler like Babel comes in. Babel can take ES2015+ code, and convert it into ES5 code.

To adhere to good programming conventions, developers tend to build applications out of many modules, but this raises more issues. To import a JavaScript file in HTML, you use a tag
like so:

```HTML
<script src="/path/to/file.js"></script>
<script src="/path/to/file2.js"></script>
etc.
```
If the applications is made up of 200 different files, the browser has to separately send a request for each file, taking a long time to fetch the resources before the user can interact
with the full application. This is where bundlers are used. The bundler can take all these files, and bundle them into one JavaScript file - which the browser then requests:

```HTML
<script src="/path/to/bundle.js"></script>
```

Now there is only one file request from the browser, and one file to parse, albeit much larger. Bundlers can do much more than just this however - they can also
use plugins like Babel to convert ES2015 to ES5, making the application fully browser compatible, along with minification, setting up development servers and more.
This leaves us being able to write modular code, in ES2015+, and still run the optimised app on older browsers. For the purpose of this project, two of the major
bundlers were chosen to analyse: Webpack and Rollup.

### Webpack
Webpack is the bundler used by the tool 'create-react-app', popular amongst developers for quickly getting React Apps
set up. 
Webpack turns each module into its own isolated function scope.
**Case Study 2** will be analysing the performance differences between each of these frameworks.


### Rollup

Rollup puts everything into the same function scope.
When measuring the performance of Rollup - it is anticipated that the execution time should
decrease, as its handles modules in a different style to Webpack (Lawson, 2016).

```javascript
function foo(a, b) {
    function bar() {
        return a + b;
    }

    return bar();
}

let result = foo(1, 2);
```

When the JavaScript engine reaches this section of code, it creates a new function object
in memory for `foo()`. When the engine reaches the line where `foo()` is called, it executes
the function, which creates a new function: `bar()`. When the function execution finishes, the
`bar()` object in memory is destroyed. This means if `foo()` is called 100 times, the `bar()`
function is created and destroyed 100 times. This costs processing, making it generally
slower than non-nested functions.

**Case Study 1** will be analysing the performance differences between each of these bundlers.

| Framework | Size | Usage (Downloads in past year) |
|---|---|---|
| React | 106.6Kb | 1,786,699	|
| Preact | 3Kb | 29,385 |
| Inferno | 48K| 7744 |
| Hyperappp | 1Kb | |

Table: Framework Comparison \label{framework_comparison}

## Frameworks
**Case Study 2** will be analysing the performance differences between each of these frameworks. React has been chosen as
the benchmark framework - as the current leader in industry, and will be compared to three other frameworks, designed
as faster alternatives.

### React
"React is a declarative, efficient, and flexible JavaScript library for building user interfaces" (Reactjs.org)
It was designed for component-based web development - making it easier for developers to create reusable components
for the applications. It uses JSX, which allows usage of HTML tag syntax within components. At the time of writing,
React is in use across 735,040 websites (https://www.similartech.com/technologies/react-js). As of January 28th, 2018,
React had 1,786,699 downloads, a 152.2% increase from the previous year (https://jsreport.io/javascript-frameworks-by-the-numbers-winter-2018/).
https://books.google.co.uk/books?hl=en&lr=&id=NZCKCgAAQBAJ&oi=fnd&pg=PR6&dq=React+js&ots=KAwuYmAw-d&sig=GSstOX8Ag0OYJNGM8hT5nNDSlKU#v=onepage&q=React%20js&f=false

### Preact
As of 28th January 2018, Preact had 29,385 downloads, a 254.3% increase from the previous year.

### Inferno
As of 28th January 2018, Inferno had 29,385 downloads, a 276.5% increase from the previous year.

### Hyperapp


## Performance Profiling

To collect accurate metrics about the performance of the chat web app, the Google Chrome Development Tools were used. These tools allow for performance profiling, detailed audits for progressive web apps, and information about load times and page weight. Additionally, they have the capability for CPU throttling, which allows visualising the scale of performance difference between unthrottled and throttled CPU with the same application.




Initially, the unbundled version of the application was analysed, with an unthrottled CPU. This gives the initial set of metrics that can be calculated against. These are: 


| Metric | Description |
|---|---|
| Load time | Total load time for page resources to be rendered |
| TTI | Time to interactive (e.g When the user can interact with page) |
| Page Weight | Accumulated total file size |
| Loading | Parsing, sending/receiving requests |
| Scripting | Compiling and evaluating scripts |
| Rendering | Executing page layout |
| Painting | Drawing the render to the screen |
| Other | |
| Idle | Time spent waiting |

Table: Devtools terminology \label{devtools_terminology}


Then a x4 throttle on the CPU was selected, and the again, giving a new set of results. From here, it was possible to calculate the percentage increase from the unthrottled set to the throttled set.

\begin{gather*}
PI\ =\ Percentage\ Increase\\*
T\ =\ Throttled\ CPU\ result\\*
U\ =\ Unthrottled\ CPU\ result\\*  
PI = \frac{T\ -\ U}{U} \times 100  
\end{gather*}

Across the results, this gives the full range of percentage increases between the data with no CPU throttling and the application of the 4x throttle. Then the steps were repeated but with a 6x throttle applied, and once again calculated the percentage increase. Across multiple passes, the metrics with the largest percentage increase upon throttling the CPU was rendering, idling and other. Despite these being the largest percentage increases, it must also be taken into account the total time they are taking. A 10% increase of a task taking 1000ms will see a bigger performance hit than a 50% increase of a task taking 5ms. Given the results varied, more passes of the test under the same conditions will be conducted in order to provide the average metric.

To gain the data, Puppeteer was used to run a headless browser, navigate to the URL where the app was being hosted. At this point, the client emulation configuration was decided upon and sent to the headless browser. It could then apply the correct emulation, and begin a timeline trace. Once finished, the trace data would be written to a JSON file, and saved with a name of the current timestamp (to avoid any duplicate file names). The script would run the tracing 20 times each for non-throttled, 4 times throttling, and six times throttling. This reduced outliers, and an average for each metric was collected, before compiling into charts. 

Webpack supports all ES5-compliant browsers - and if developers wish to support browsers older than this - polyfills can be loaded
to make the application compatible. When using Create React App, webpack's configuration
is kept hidden. This default is what will be used in this project to measure
performance. This is because the programmer must actively "eject" their application
to access customisation of webpack configuration. 

Why I chose case 1, 2 etc. (justify with example - expected result)
Make a comparison table between predicted/actual results with discussion of relevance
Justify reasoning for cases
Requirements flow chart + descriptions

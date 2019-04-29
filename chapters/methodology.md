\pagebreak

# Methodology

## Introduction

In order to perform detailed analysis on potential areas for optimisation, a web app would need to be 
studied and modified to gain insights. Rather than study an existing application, over which no control would 
be granted, a better solution would be to create a testbed application using modern technologies. In 
tandem with this, DevTools provides accurate and reliable analysis on browser applications, with the ability 
to throttle the CPU to judge performance on simulated lower-hardware. This would allow comparisons to be 
drawn across the different CPU throttle thresholds, but with no other parameter changes.

To understand the decision for the case study subjects, first there must be a basic grasp on the history
and current usage of JavaScript and ECMAScript. 

## A Brief History and Analysis of JavaScript and ECMAScript
ECMAScript (European Computer Manufacturer's Association) was 
designed as a way to standardise JavaScript
(a programming language created in 1995) - and was first released in 1997.
Versions have been regularly released, with ES6/ES2015 being the current modern standard.
Initially it was named ES6, but later renamed ES2015. For consistency,
this dissertation will always refer to it as "ES2015". Whilst the 
9th edition of ECMAScript (ES2018) was finalised in June 2018, browsers
are some way behind, with only modern browsers supporting the features
of ES2015 - limiting them to old features, or they can use a compiler
such as Babel to compile their ES2015 code into valid and compatibile ES5 - ensuring cross-browser
compatibility, whilst having use of ES2015 features. 

## Puppeteer

Puppeteer is a Node Library which provides a high-level API to control
headless or non-headless Chrome instances over the DevTools protocol.
This allows programmatic control over the browser, offering automation
capabilities. The DevTools protocol has the ability to set the throttle
speed of the browser when running a performance profile - lending
itself perfectly for the experiment being conducted in the following
chapter. Rather than manually opening the testbed application, selecting
the throttle speed, and running a performance profile, Puppeteer allows
all of this to be automated - with the resulting performance profile
being saved into its own file. This increased the number of experiments
it would be feasible to run - adding credibility to the results collected.


## Testbed Application

### System Requirements
The testbed application had to be:

 * Made with modern JavaScript frameworks
 * Browser compatible with older browsers
 * Built with realistic dependencies
 * Simulate heavy workload
 * Functional

In order to comprehensively test the technologies being analysed,
a testbed application was required. For the purposes of this project,
realtime chatting application was created - an application with 
genuine purpose and functionality - requirements of the application.

Initially, the application was built with React, and later re-written
several times using different front-end frameworks. Using bundlers
meant it could be written in ES2015, but compiled to ES5 to run on older
browsers - another system requirement. The app utilises Socket.io 
to communicate with a Node.js 
server also running Socket.io. On top of this, the app utilises
several other libraries, such as Bootstrap, Moment, JQuery and Faker, 
giving a partially realistic build to the application. To simulate
heavy workload, a factorial function was created, and called upon
initialisation with an input of 1000. This gave the application a
significant amount of work to do.

## Case Study One: Effect of Bundlers on Performance

Case study 1 analyses the performance comparison between two popular bundlers - Webpack and Rollup. 
These bundlers are
being tested using the testbed application with each framework to ensure consistency across all other parameters other
than the bundler itself. 



### Bundlers 

Adhering to modern programming conventions, developers tend to build 
applications out of many modules, but 
from a performance perspective - this has its own issues. 
To import a JavaScript file in HTML, a tag is used like so:

```HTML
<script src="/path/to/file.js"></script>
<script src="/path/to/file2.js"></script>
etc.
```
If the applications is made up of 200 different files, the browser has to separately send a request for 
each file individually - consuming valuable time and resources before the user can interact
with the full application. This is where bundlers are used. The bundler can take all these files, and 
bundle them into one JavaScript file - which the browser then requests:

```HTML
<script src="/path/to/bundle.js"></script>
```

This resolution leaves only one file request from the browser and does not
sacrifice developing standards. Bundlers 
can do much more than just this however - they can also use plugins like Babel to convert ES2015 to ES5, 
making the application fully browser compatible, along with minification, setting up development servers 
and more. This leaves us being able to write modular code, in ES2015+, and still run the optimised app 
on older browsers. For the purpose of this project, two of the major bundlers were chosen to analyse: 
Webpack and Rollup.

#### Webpack
Webpack is the bundler used by the tool `create-react-app`, popular amongst developers for quickly getting React Apps
set up. 
Webpack turns each module into its own isolated function scope.


#### Rollup

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

In each case, the bundler will:

 * Bundle the JS files
 * Bundle the CSS files
 * Compile the JS into ES5
 * Set up a server and serve the project

The configuration file for each bundler is in the Appendix.


## Case Study Two: Effect of Different JavaScript Frameworks on Performance

Case study 2 analyses the performance difference between four different 

### Frameworks
| Framework | Size | Number of GitHub Stars |
|---|---|---|
| React | 106.6KB | 127,752	|
| Preact | 3KB | 22,385 |
| Inferno | 48KB | 13,619 |
| Hyperappp | 1KB | 16,660 |

Table: Framework Comparison \label{framework_comparison}

React has been chosen as
the benchmark framework - as the current leader in industry, and will be compared to three other frameworks, designed
as faster alternatives.

#### React
"React is a declarative, efficient, and flexible JavaScript library for building user interfaces" (Reactjs.org)
It was designed for component-based web development - making it easier for developers to create reusable components
for the applications. It uses JSX, which allows usage of HTML tag syntax within components. At the time of writing,
React is in use across 735,040 websites (https://www.similartech.com/technologies/react-js). As of January 28th, 2018,
React had 1,786,699 downloads, a 152.2% increase from the previous year (https://jsreport.io/javascript-frameworks-by-the-numbers-winter-2018/).
https://books.google.co.uk/books?hl=en&lr=&id=NZCKCgAAQBAJ&oi=fnd&pg=PR6&dq=React+js&ots=KAwuYmAw-d&sig=GSstOX8Ag0OYJNGM8hT5nNDSlKU#v=onepage&q=React%20js&f=false

### Preact
Preact is a fast alternative to React - using the same ES2015 API (Yomi 2017).
The only changes from React are trivial, but most can be accessed by making
use of `preact-compat` - an additional package that re-integrates removed
features.
As of 28th January 2018, Preact had 29,385 downloads, a 254.3% increase from the previous year.

### Inferno
Like Preact, Inferno is a lightweight JavaScript library that resembles
React. It was created to examine analyse whether a UI library could improve
web application experience on mobile devices by addresseing issues around
battery drain, memory consumption and performance (Maida 2016).
As of 28th January 2018, Inferno had 29,385 downloads, a 276.5% increase from the previous year.

### Hyperapp
Hyperapp is a JavaScript framework for building web applications that uses the Elm-inspired approach
to state management. GZipped and compressed, the framework is around 1KB (Bucaran 2018).

## Performance Profiling

To collect accurate metrics about the performance of the testbed application, the DevTools were used. 
These tools allow for performance profiling, detailed audits for progressive web apps, and information about load 
times and page weight. Additionally, they have the capability for CPU throttling, which allows visualising the scale 
of performance difference between unthrottled and throttled CPU with the same application.

Initially, the unbundled version of the application was analysed, with an unthrottled CPU. This gives the initial 
set of metrics that can be measured. These are: 

 * Load time
 * TTI
 * Page Weight
 * Loading
 * Scripting
 * Rendering
 * Painting
 * Other
 * Idle

(These are defined in the section \ref{terminology}

Then a CPU throttling was activated, and the profiling re-run, giving a new set of results. From here, it was possible to 
calculate the percentage increase from the unthrottled set to the throttled set.

\begin{gather*}
PI\ =\ Percentage\ Increase\\*
T\ =\ Throttled\ CPU\ result\\*
U\ =\ Unthrottled\ CPU\ result\\* 
PI = \frac{T\ -\ U}{U} \times 100 
\end{gather*}

Across the results, this gives the full range of percentage increases between the data with no CPU throttling and the 
application of the 4x throttle. Then the steps were repeated but with a 6x throttle applied, and once again calculated 
the percentage increase. Across multiple passes, the metrics with the largest percentage increase upon throttling the 
CPU was rendering, idling and other. Despite these being the largest percentage increases, it must also be taken into 
account the total time they are taking. A 10% increase of a task taking 1000ms will see a bigger performance hit than 
a 50% increase of a task taking 5ms. Given the results varied, more passes of the test under the same conditions will 
be conducted in order to provide the average metric.

To gain the data, Puppeteer was used to run a headless browser, navigate to the URL where the app was being hosted. At 
this point, the client emulation configuration was decided upon and sent to the headless browser. It could then apply 
the correct emulation, and begin a timeline trace. Once finished, the trace data would be written to a JSON file, and 
saved with a name of the current timestamp (to avoid any duplicate file names). The script would run the tracing 20 
times each for non-throttled, 4 times throttling, and six times throttling. This reduced outliers, and an average for 
each metric was collected, before compiling into charts. This technique for data collection has not been used in any of
the relevant academic papers found in Chapter 2. The code for this script is found in Appendix E.

![Experiment Flow Chart \label{flow_chart}](./images/flow_chart.png)

As described in Figure \ref{flow_chart}, each version of the testbed application (e.g React, Hyperapp etc.) would be
used as the input - hosting the app locally. Then the Puppeteer script would be run, loading the app and running a performance
profile. The output of the script would be written to a file (using JavaScript's `date()` function to create unique
file names. Each file could then be loaded into the DevTools and the inbuilt parser would display a summary of key information.
This data was then written to a spreadsheet for further analysis.

Webpack supports all ES5-compliant browsers - and if developers 
wish to support browsers older than this - polyfills 
can be loaded to make the application compatible. When using 
Create React App, webpack's configuration is kept hidden as a 
way to abstract complexity away from the developer. If they want 
to, the developer can still edit the Webpack configuration
files by "ejecting" their application.

For this reason, to avoid any bias, this project will not
use `create-react-app` as the method of testing Webpack. Instead
webpack will be added manually, allowing full control over the
configuration file. This provides a closer and fairer comparison to
Rollup. 

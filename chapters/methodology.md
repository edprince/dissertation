\pagebreak

# Methodology

## Introduction

In order to perform in-depth analysis on the largest areas for optimisation, a web app would need to be studied in depth to gain insights. Rather than study an existing application, over which no control would be granted, a better solution would be to create a testbed application using modern technologies. In tandem with this, Devtools provides accurate and reliable data on browser applications, with the ability to throttle the CPU to judge performance on simulated lower-hardware. This would allow comparisons to be drawn across the different CPU throttle amounts, but with no other parameter changes.



## Testbed Application


The testbed application is a realtime chatting application - an application with a genuine use anywhere in the world. The front-end is built with React, making use of the popular Create React App library, and Socket.io to communicate with a Node.js server also running Socket.io. On top of this, the app makes use of several other libraries, such as Bootstrap, Moment, JQuery and Faker, giving a partially realistic build to the application.

## Performance Profiling

To collect accurate metrics about the performance of the chat web app, the Google Chrome Development Tools were used. These tools allow for performance profiling, detailed audits for progressive web apps, and information about load times and page weight. Additionally, they have the capability for CPU throttling, which allows visualising the scale of performance difference between unthrottled and throttled CPU with the same application.

## Bundling
Bundling is a modern standard of web development for several reasons.
It means developers can seperate files into smaller, more manageable
components, making further development easier than all the code being
in one file - the principle being similar to the separation of concerns.
If the programmer were to split up their code without using a bundler,
they would have to tell the browser to fetch each JavaScript file using
`<script>` tags. This would cause the browser to fetch each file, one
by one - not very efficient. Bundling allows the developers to work
on separate files, keeping their separation of concerns, but upon building
the project, the files are all compiled into a single, bundled JavaScipt file.
This file is then called by the HTML file - meaning only one script is
being fetched using `<script>` tags. It also allows programmers to make
use of ES6 standards, but the compiler can use Babel to compile the code
into valid ES5 code - making the code compatible across all major browsers.



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










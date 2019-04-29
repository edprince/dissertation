# Introduction  
Developers take advantage of the outstanding capabilities
present in modern smartphones. With a popular comparison being
a current smartphone versus the Apollo-mission-era computers,
the iPhone 6 processor clock speed is 32,600 times faster than the
Apollo-era processors (Puiu 2019). Whilst not quite the same scale
of gulf - there exists a distinct difference between the quality
of smartphone in popular usage across developed countries versus
smartphones in popular usage across developing countries (Hiscott 2016). Additionally,
there is a distinct lack of research into optimising web applications
for lower power smartphones - contextualising the importance of
this subject topic.

With Google, Mozilla, Microsoft and Huawei all
releasing cheap smartphones for developing countries, it is likely the developing world's
mobile device population will follow a trend of being considerably less powerful than the mobile device
population of developed 
countries (Hiscott 2016). With over 98% mobile phone adoption in developing countries (Sharwood, 2017)
this offers a large market of potential users for web applications.

A future high speed networks and lower-powered CPU's (more detail in chapter 2),
may indicate a trend of developing for lower-powered CPU's. In anticipation of such a trend, this research is focused around
performing an analysis of two major components to modern web applications:
bundlers and JavaScript user interface frameworks. 

Older devices also means a lack of compatibility with the newest browsers, meaning that for global
usage, developers must make their applications work on older versions of browsers. To mitigate a
loss of quality of the application, the tests should be performed on an application built with
modern front-end frameworks, as a realistic benchmark. Then metrics can be gathered
by measuring performance of applications even when converted into older versions of JavaScript that
are compatible with older browsers - and making sure the application runs on those versions.

In summary - the applications must be browser compatible for older browsers, and should be made
with modern JavaScript frameworks and techniques, as not to hinder potential developers. 

These objectives will be tested by using the Google Chrome DevTools to monitor the CPU-throttled
performance, and different technology implementations that allow comprehensive browser compatibility.
There is an expectation that the lighter front-end frameworks perform best.

## Dissertation Structure

The Literature Review explores a selection of the relevant existing literature surrounding and 
encapsulating the topic, establishing its context. Due to the subject being in its infancy in relation to most 
areas of Computer Science - there is a distinct lack of relevant literature. 
Network-based optimisations are a popular article subject - but as it bears little need 
in developed countries - optimisations for low-powered CPU's is not a thriving research topic. 

The Methodology chapter lays the ground work for the experiments to be conducted. It shows the
techniques used to gain data, explains how they work, and justifies their selection for this project.
The experiments are split up into component sections, each identifying a different area for potential optimisation. Each section has a brief summary, 
a prediction of the expected results upon modification and re-profiling, and the actual results, 
how the compare, and why they might differ to the predictions. 

The Design and Implementation chapter describes exactly how the experiments were conducted, along with
the results. The experiments are split into two case studies, analysing bundler performance, and
analysing front-end JavaScript framework performance.

The Discussion chapter begins to weave the results into an argument which responds to the initial
research question, along with providing assessment on the quality and validity of this research.
It also highlights further areas for study regarding this research.

The Project Management chapter provides clarity and reflection on the process of
creating this project, and the methodologies employed to ensure completion within the timeframe
given.

The Conclusion highlights the extent to which the findings provide a suitable answer to the initial research
question. 


## Terminology \label{terminology}

| Term | Definition |
|---|---|
| **Developing Countries** | As defined by the United Nations (UN 2014:146) | 
| **0x** | No CPU throttling being applied |
| **4x** | Four times CPU throttling being applied |
| **6x** | Six times CPU throttling being applied |
| **Chrome** | Google Chrome Browser |
| **DevTools** | Google's suite of developer tools built directly into Chrome |
| **CDN**  | Content Delivery Network |
| **ES5** | ECMAScript 5 |
| **ES2015** | ECMAScript 2015, the version after ES5 |
| **Babel** | JavaScript compiler, often used for converting ES2015+ to ES5 |
| **Polyfill** | Browser feature implementation that isn't naturally supported |
| **Node** | Nodejs, a JavaScript runtime built on Chrome's V8 engine |
| **JSX** | Preprocessing step to add XML syntax to JavaScript |

### DevTools-Specific Terminology

| Metric | Description |
|---|---|
| **Load time** | Total load time for page resources to be rendered |
| **TTI** | Time to interactive (e.g When the user can interact with page) |
| **Page Weight** | Accumulated total file size |
| **Loading** | Parsing, sending/receiving requests |
| **Scripting** | Compiling and evaluating scripts |
| **Rendering** | Executing page layout |
| **Painting** | Drawing the render to the screen |
| **Idle** | Time spent waiting |

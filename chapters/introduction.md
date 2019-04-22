# Introduction  
When developing for mobile phones, the devices used to optimise for, are the current standard
of modern mobile phones - proving useful for a target audience of users able to buy this
standard of device - but less so for the many people who are unable to be accessing web apps
on new smarthones. Much of the developing world uses mobile phones several generations behind
what is in popular usage across developed countries. These smartphones are not as powerful
as the current devices, and yet web applications can still be optimised to give a low-powered
smartphone a high standard of user experience.

With the anticipation of a high speed network and low-power CPU future (more detail in chapter 2),
it is important that applications are designed to run on lower-powered CPU's. To test this,
this research will include analysis of performance changes when the CPU power is being throttled.
Older devices also means a lack of compatibility with the newest browsers, meaning that for global
usage, developers must make their applications work on older versions of browsers. To mitigate a
loss of quality of the application, the tests should be performed on an application built with
modern front-end frameworks, as a realistic benchmark. Then metrics can be gathered
by measuring performance of applications even when converted into older versions of JavaScript that
are compatible with older browsers - and making sure the application runs on those versions.

These objectives will be met by using the Google Chrome Devtools to monitor the CPU-throttled
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

The Design and Implementation chapter describes exactly how the experiments were conducted, along with
the results. The experiments are split into two case studies, analysing bundler performance, and
analysing front-end JavaScript framework performance.

The Discussion chapter begins to weave the results into an argument which responds to the initial
research question, along with providing assessment on the quality and validity of this research.

The Project Management chapter.

The Conclusion is where the extent to which the findings provide a suitable answer to the initial research
question. It also highlights further areas for study regarding this research.

## A Brief History of JavaScript
ECMAScript was designed as a way to standardise JavaScript - and was first released in 1997.
Versions have been regularly released, with ES6/ES2015 being the current modern standard. For
this dissertation, it will be referred to as ES6 for consistency. The issue with ES6 is that 
not all versions of browsers support ES6, many still only support up to ES5. This means developers
are either stuck developing purely in ES5, limiting them to old features, or they can use the
Babel compiler to compile their ES6 code into valid and compatibile ES5 - ensuring cross-browser
compatibility, whilst having use of ES6 features. 

A section on why ES Modules are relevant but not used.

The methodology chapter presents the formation and execution of the experiments, and details 
on how results could be replicated. The experiments are split up into component sections, 
each identifying a different area for potential optimisation. Each section has a brief summary, 
a prediction of the expected results upo modification and re-profiling, and the actual results, 
how the compare, and why they might differ to the predictions. The chapter is concluded with a 
summary of all of the results, and how they relate to optimisations for low-powered smartphones.

## Terminology

**Devtools** Google Chrome Development Tools  
**CDN** Content Delivery Network  
**ES5** ECMAScript 5  
**ES2015**  
**Polyfill** The implementation of a feature for a browser that does not support the feature  
**Create React App**  


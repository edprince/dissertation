# Introduction  
The Literature Review explores a selection of the relevant existing literature surrounding and 
encapsulating the topic. Due to the subject being in its infancy in relation to most 
areas of Computer Science - there is a distinct lack of relevant literature. 
Network-based optimisations are a popular article subject - but as it bears little need 
in developed countries - less powerful CPU based optimisations are not a hot topic for 
academic research. Whilst the usefulness is definitely questionable in developing 
countries - many developing country populations still use older smartphones, and could 
benefit from more research in this area - ultimately providing better user experiences 
for global user bases. Additionally - if an application can reduce the required usage of 
the CPU - it can also reduce the CPU power consumption and required cooling - ultimately 
increasing battery life, a feature useful anywhere in the world.

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
**Polyfill** The implementation of a feature for a browser that does not support the feature  
**Create React App**

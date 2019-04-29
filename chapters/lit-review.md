\pagebreak

# Literature Review

## Introduction \ref{lit-intro}
As of 2018, there were 3.7 billion mobile devices connecting to the internet (Stevens, 2018) 
showing global usage and coverage, and according to Poushter and the
research undertaken by PewResearchCentre - in 12 developing countries that
were surveyed in 2014 and 2015, there were "significant" increases in
adult mobile phone users. This gives credibility to the claim that
there is a likely upwards trend in smartphone users in the developing world.

Where there are users, there is also likely to be dissatisfaction,
and Google estimate that a 400ms delay can see a drop off of 0.44% (Brutlag 2009).
It has also been found that 90% of users stop using an app due to poor performance, and 86% will uninstall 
the app altogether (AppDynamics and University of London 2014), there is the possibility for 
unoptimised web apps to lose huge numbers of potential users due to the app performance not meeting 
modern web application performance. This research reinforces the statement
that poor performing applications negatively impacts the number of users - 
making the topic of optimising applications to avoid this a valid and
useful area for research.

Nejati and Balasubramanian discuss the difficulty in isolating the effects of the mobile browser in 
determining the root of poor performance (Nejati, Balasubramanian 2016). This project will differ 
from that research by making use of the DevTools mobile simulator - taking many of 
the factors out of consideration, allowing isolation on only changes to the CPU performance. They 
also identify the issue of mobile browsers being much slower than desktop, as agreed with in other 
research on mobile optimisations in the cloud era (Wang et al. 2013), a problem given the dramatic 
increase in mobile devices globally.

## CPU

It is suggested that network round-trip time is a major problem. Whilst this may have been true at the 
time, due to the increase in network capacity, and the trends shown so far, it could be assumed that 
time-based network problems become increasingly less relevant, with the hardware-based issues becoming 
more prominent. Particularly in developed countries, modern smartphones with the latest hardware are 
readily available, which is why this project focuses on mobile phones in usage in the developing world.
This evidence is collected through a well-thought out series of experiments resulting
in consistent, communicated correctly with no evident omissions. This gives
credibility to these results.

Over the last 20 years, Moore’s Law has begun to plateau (Simonite 2016), demonstrated by Figure \ref{moore} 
and hardware capability increases along with it. 

![Moore's Law Plateau \label{moore}](./images/moore.png)

Networks on the other hand are continuing to get faster and offer better coverage.  Taking Kenya (a developing 
country) as an example, Figure \ref{kenya} shows that network speeds are continuing to increase over time.

Together, Figures \ref{moore} and \ref{kenya} allude to the likely outcome of a fast-network, slow CPU future.


![Kenyan Network Speeds \label{kenya}](./images/kenya_network.png)

“Of all ITU [International Telecommunication Union] regions, the strongest 
growth was reported in Africa, where the percentage of people using the 
Internet increased from just 2.1% in 2005 to 24.4% in 2018” (ITWeb, 2018). 
Containing a large number of developing countries, by looking at Africa as 
a whole, and Kenya as a microcosm - we can see there is a likelihood of a 
fast network future. With the plateau in Moore’s Law, a likelihood of 
stagnation in CPU performance increases. 

A fast network future may lead to an emergence in prioritisation of CPU-based 
optimisation. There has also been extensive 
research on optimization over networks already - reducing content, using 
CDN’s, compressing content, utilising browser caching techniques (Iliev 2014), 
and front end optimisations for modern devices. This research will avoid 
liminality by relying on the research already conducted on networks, and 
instead fill the gap left for optimising web applications to perform highly 
for low-end smartphones. With mobile web browsers being intensive programs for
CPU's (Meyerovich and Bodík 2010), there is evidence that opimisations are
justified in this field.

Nejati and Balasubramanian provide research around locating mobile browser bottlenecks. 
They concludes that computational activities are the main bottlenecks, highlighting 
the need for research on optimising for lower-powered CPU devices, where the 
effects of computational bottlenecks will be be exceedingly more relevant.

It also states that this is not the case for desktops, where network activity 
is the dominant bottleneck - also emphasizing the importance of optimising 
CPU-intensive applications for mobile devices. Wang et al. suggest that 
the most costly area for TTI is resource loading - which, as the sources are 
credible, makes sense - however no speculation is offered about the state of 
the future of processors and networks, making the research presently relevant, 
but perhaps not in years to come. These conclusions are the result of
an experiment conducted by the authors, and backed up consistently
by relevant academic papers.

In summary - the browser is an intensive program, and heavy computational
activities are the main bottlenecks.

## Mobile Web Browser

There are also many comparisons made between the mobile browser and 
desktop browser, over the same network speed - finding that the mobile
version can take up to nine times as long to load (Wang et al. 2013). As they are on the 
same network - we know that this is therefore down to the hardware and
mobile browser - not server-to-client issues. Suggestions have been 
made that more effort should be put into making mobile browser 
optimisations - with which future developers could utilise to make web
applications more globally usable. Whilst this research is not founded
on data collected first-hand, it is rigorously supported by multiple
credible academic sources.

## Development Issues

Thiagarajan et Al. show that reducing JavaScript and utilising HTML functionality leads to 
a less power-hungry application. JavaScript being the most power-hungry 
part of the traditional web application. It also shows the importance of 
optimising CSS rules, with a reduction to only necessary rules, along with 
the migration of multiple CSS files into one file for a given page seeing 
a drop of 5 Joules from the power supply.

It also looks at the benefits of web page prefetching by predicting which 
links the user will click, and prefetching/loading the relevant data to render 
the page should the link be clicked more quickly. Does low CPU capability make 
this a relevant point or not? 

The other large aspect they discuss, is the usage of cloud-based architecture. 
This might increase network latency, and there are other potential security issues, 
but focusing purely on optimisation, this style of architecture allows processing 
to be partially taken away from client devices, reducing the workload of the client 
CPU’s. This could be introduced into the chat web app by analysing the impact of 
moving some intensive functionality from the client to the server.

To keep this research focused into a more specific topic area - architecture optimisations
will not be analysed. The topics will be strictly front-end focused.

In summary - whilst prefetching and cloud-based architecture are useful
avenues for exploration with regards to mobile optimisation, this research
will focus on JavaScript reduction to help lower the load on the CPU.


## Summary

Optimisation over networks is a popular topic, with an array of literature covering
the subject. This helps guide this research in starting to fill the gap in front-end optimisations.
Following on from the research conducted by Thiagarajan et al,
this project will look at ways to reduce JavaScript by using and comparing two
different bundlers - Webpack and Rollup.

There is a distinct lack of literature based around front-end JavaScript frameworks,
which, along with the bundlers creates the foundation of this research. The following
chapter will outline how an experiment is created to test the performance of a testbed
web application whilst using different technologies.

The experiments conducted in this dissertation shall be run using
the Google Chrome browser. Not only does this browser give acces to
the use of the comprehensive DevTools suite and Puppeteer, but it
is also the most popular browser, with 62.63% of global traffic using
it, ahead of Safari at 15.56% (GlobalStats 2019).

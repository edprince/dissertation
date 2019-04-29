\pagebreak
\pagebreak

# Discussion and Future Research

Whilst useful data has been recorded in this project, the data could be
substantially backed up with more experiments. Critically, testing the
application across real mobile phones would further the claim that the
conclusions were valid in specific relation to the original research question.
Building on this - the experiment could also be carried out on specifically
the most common devices being used in developing countries, with direct
comparisons to performance on new smartphones. It may also positively
impact the performance of Inferno, being specifically built for
addressing battery drain, memory consumption and performance issues (Maida 2016).

Given more time, the author would have performed the same experiment
again, using mobile devices running Android 8.0 and higher. This would
allow the use of Chrome's remote debugging feature. Once setup on the
device, it allows inspection and debugging of live content on an android
device as well as screencasting content from the device onto a DevTools
instance (Basques 2019). Alongside this, doing the same tests across
multiple versions of Chrome to verify that the application is still
fully compatible - as at this stage, its compatibility is rooted
in theory, and has not been tested for verification. Whilst this
data would be useful - it would have also been time-consuming to
collect, with other browsers development tools not being the same
as Chrome, meaning at the very least, the Puppeteer script would need
to be rewritten to ensure compatibility, and at worst an entirely new
method for collecting the data needed.

In addition to this, if a way was found to automate getting the summary
data from the performance profile result, the experiment could be
entirely automated, and therefore collect substantially more results
to further the evidence for the discovered outcome.

Another useful avenue for testing could be to utilise a more substantial
open source application, for example the Hacker News clone on GitHub at
https://github.com/vuejs/vue-hackernews-2.0. This would also reinforce
the conclusions being made in this dissertation, with no uncertainty based
on the validity of the testbed application as a source of potential outlying
results. 

In summary, the project could be improved or extended by looking
into any of the following methods:
 
 * Testing on real mobile devices
 * Testing across more browsers and browser versions
 * Automate all data collection
 * Use more substantial testbed applications

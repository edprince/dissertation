---
title:  'How Can Web Developers Optimise for Lower-Power Smartphones in the Developing World?'
header-includes: |
  \usepackage{authblk}
  \author{Edward George Prince}
  \affil{6151713}
  \affil{Supervised by Dr Norlaily Yaacob}
  \affil{Computer Science, Department of Computing}
  \affil{Coventry University}
  \lstset{
    basicstyle=\ttfamily,
    breaklines=true,
    frame=single
   }
  \usepackage{fancyhdr}
  \pagestyle{fancy}
date: 29th April 2019
numbersections: true
chapters: true
listings: true
subparagraph: yes
---

\maketitle
![Certificate of Ethics](./certificate.jpg)
\thispagestyle{empty}
\clearpage
![Certificate of Ethics](./statement.png)
\thispagestyle{empty}
\clearpage
\begin{abstract}
  This paper looks at methods for optimising modern web applications for users with
  low-powered smartphones. The research focuses on front-end optimisations,
  in particular bundlers, and JavaScript user interface frameworks. 
  By analysing a testbed realtime chatting applications, built with
  different frameworks, socket.io and Node.js, it is discovered that
  performance optimisations can be made without sacraficing user or developer 
  experience. This was found using the Google Development Tools to analyse the
  testbed application being created with different frameworks, bundlers and running
  at different simulated CPU speeds.
\linebreak
\linebreak
  Keywords: Mobile, Optimisation, Web, JavaScript, Bundling, Framework
\end{abstract}
\renewcommand{\abstractname}{Acknowledgements}
\begin{abstract}
A special thanks to Dr Norlaily Yaacob for supervision throughout this
project - and to Dan Prince for his unwavering encouragement and support.
\end{abstract}
\pagebreak
\tableofcontents
\pagebreak

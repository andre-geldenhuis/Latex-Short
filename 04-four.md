---
layout: page
title: LaTeX
subtitle: Images, Figures and Cross Referencing
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Images
> * Figures
> * Cross Referencing

If you have done the previous lessons your document should look something
like the following

~~~ {.latex}
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{Latex Intro}
\author{Andre Geldenhuis }
\date{April 2015}

\begin{document}

\maketitle
\tableofcontents

\section{Introduction}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce risus 
urna, finibus at augue luctus, mattis mollis tellus. Aliquam consequat 
accumsan magna sit amet vestibulum. Cum sociis natoque penatibus et 
magnis dis parturient montes, nascetur ridiculus mus. Maecenas ut 
pellentesque mauris. Nulla ac dolor at leo hendrerit interdum. Etiam 
vulputate posuere nisi in tincidunt. Sed non scelerisque purus. Phasellus 
efficitur faucibus nisl, eget posuere urna. Phasellus tincidunt dui 
lacus, in semper nulla volutpat eget. Pellentesque habitant morbi 
tristique senectus et netus et malesuada fames ac turpis egestas. 
Suspendisse nibh massa, rhoncus aliquam mattis in, ultrices eu urna. 
Vivamus in accumsan erat. 


\section{Thesis}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eu nisl nisi. 
Curabitur sagittis sodales laoreet. Fusce efficitur dictum orci, sed 
viverra ex ullamcorper a. Morbi sem libero, placerat eu augue nec, 
hendrerit eleifend tortor. Curabitur auctor magna eget hendrerit accumsan. 
Aenean faucibus magna sed enim ullamcorper vulputate. Aliquam non eros 
ac quam sollicitudin cursus eu ac est. Donec consectetur eget nibh id 
mollis. Quisque euismod diam velit, quis pretium justo accumsan id. 

\subsection{Abstract}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris facilisis, 
diam pretium pretium lobortis, metus dolor fermentum augue, ultrices 
consequat dolor tortor nec risus. Aenean sagittis hendrerit turpis, a 
porta eros facilisis in. In efficitur posuere risus, eu ullamcorper 
arcu. Morbi fermentum auctor arcu, non interdum ligula placerat 
maximus. Morbi nec metus et urna gravida rhoncus. Donec interdum, nisi 
vitae volutpat vehicula, odio eros pulvinar mauris, ac mollis elit enim 
sit amet diam. Ut blandit hendrerit luctus. Duis eget augue sed mi 
pellentesque mattis non finibus libero. Aliquam rhoncus, orci tempus 
consectetur mattis, enim turpis dignissim eros, sit amet sollicitudin 
justo turpis a justo. 

\section{Math Mode}

$ \alpha \rightarrow \Rightarrow \exists \forall $
$ \acute{e} $

$ \hat{a} , \acute{a} , \bar{a} , \dot{a} , \breve{a} ,
\check{a} , \grave{a} , \vec{a} , \ddot{a} , \tilde{a} $

$hello^2$ $hello_2$ $hello_{world}$ 

$\frac{topline}{bottomline}$

$$
\int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}
$$

$$\underbrace{a+\overbrace{b+\cdots}^{{}=t}+z}
_{\mathrm{total}} ~~
a+{\overbrace{b+\cdots}}^{126}+z
$$

\end{document}
~~~

To include images in LaTeX we need to include a new package 
```\usepackage{graphicx}```.  We do this in the preamble section 
above ```\begin{document}```.  We also need to
set a location for the images (it is tidier to have images in their own
folder or directory), this is done via ```\graphicspath{ {images/} }```

To add an image we use the command ```include{imagename}```.

> ## Upload an image to ShareLatex so we can use it  {.challenge}
> 
> Make a new folder in your sharelatex document (upper left, above main.tex)
> Call the new folder images.  Download [this image](https://github.com/andre-geldenhuis/Latex-Short/blob/gh-pages/fig/space_rocket.pdf) and then
> upload it to the images folder in sharelatex (upload button next to the 
> new folder button).  If the file ends up in the wrong location you can
> just drag and drop it to the images folder. 




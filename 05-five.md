---
layout: page
title: LaTeX
subtitle: Where The Magic Happens -- Preamble and Macros
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Preamble
> * Macros
> * References

If you have been following along you should have roughly the following
document in ShareLatex.  You should also havea  folder called images
with the following two files in it.  [space_rocket.pdf](https://github.com/Andre Geldenhuis and Sarah Hoyte/Latex-Short/blob/gh-pages/fig/space_rocket.pdf)
 and [polarplot.eps](https://github.com/Andre Geldenhuis and Sarah Hoyte/Latex-Short/blob/gh-pages/fig/polarplot.eps).


~~~ {.latex}
\documentclass{article}
\usepackage[utf8]{inputenc}

\usepackage{graphicx}
\graphicspath{ {images/} }

\title{Latex Intro}
\author{Andre Geldenhuis and Sarah Hoyte }
\date{April 2015}

\begin{document}

\maketitle
\tableofcontents
\listoffigures

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
Vivamus in accumsan erat. See equation \ref{eq:TooComplex} on page \pageref{eq:TooComplex}.


\section{Thesis}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. In eu nisl nisi. Curabitur sagittis sodales laoreet. Fusce efficitur dictum orci, sed viverra ex ullamcorper a. Morbi sem libero, placerat eu augue nec, hendrerit eleifend tortor. Curabitur auctor magna eget hendrerit accumsan. Aenean faucibus magna sed enim ullamcorper vulputate. Aliquam non eros ac quam sollicitudin cursus eu ac est. Donec consectetur eget nibh id mollis. Quisque euismod diam velit, quis pretium justo accumsan id. Figure \ref{fig:CoolRocket} on page \pageref{fig:CoolRocket}

\subsection{Abstract}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris facilisis, diam pretium pretium lobortis, metus dolor fermentum augue, ultrices consequat dolor tortor nec risus. Aenean sagittis hendrerit turpis, a porta eros facilisis in. In efficitur posuere risus, eu ullamcorper arcu. Morbi fermentum auctor arcu, non interdum ligula placerat maximus. Morbi nec metus et urna gravida rhoncus. Donec interdum, nisi vitae volutpat vehicula, odio eros pulvinar mauris, ac mollis elit enim sit amet diam. Ut blandit hendrerit luctus. Duis eget augue sed mi pellentesque mattis non finibus libero. Aliquam rhoncus, orci tempus consectetur mattis, enim turpis dignissim eros, sit amet sollicitudin justo turpis a justo. See Figure \ref{fig:CoolRocket}

\section{Math Mode}

$ \alpha \rightarrow \Rightarrow \exists \forall $
$ \acute{e} $

$ \hat{a} , \acute{a} , \bar{a} , \dot{a} , \breve{a} ,
\check{a} , \grave{a} , \vec{a} , \ddot{a} , \tilde{a} $

$hello^2$ $hello_2$ $hello_{world}$ 

$\frac{topline}{bottomline}$

\begin{equation}
\int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}
\end{equation}

\begin{equation}
\underbrace{a+\overbrace{b+\cdots}^{{}=t}+z}
_{\mathrm{total}} ~~
a+{\overbrace{b+\cdots}}^{126}+z
\label{eq:TooComplex}
\end{equation}

\section{Images}

\begin{figure}[h]
    \caption{Cool Polar plot\label{fig:CoolPolarPlot}}
    \centering
    \includegraphics[width=0.2\paperwidth]{polarplot}
\end{figure}

\begin{figure}[h]
    \caption{The Rocket Equation $\Delta V = \nu_e \ln\frac{m_0}{m_1}$\label{fig:CoolRocket}}
    \centering
    \includegraphics[width=0.2\paperwidth]{space_rocket}
\end{figure}

\end{document}
~~~

Now that we have a more substantive document, we can experiment with changing
the preamble to automatically make large changes to our document.   In 
first lesson we noticed that LaTeX makes a document with large margins in 
order to manage to words per line.  One elegant way to make better use of
space is to use a two column layout.  This is done by adding an argument
to the ```\documentclass{article}``` on the first line.

> ## Add a figure frame  {.challenge}
> Add ```[twocolumn]``` to your document class.  

> ## More reasonable margins {.callout}
>
> LaTeX has automatically reduced the size of the margins in order to as
> it needs a bit more room for the correct words per line in two column
> layouts.  Note you can manually set the margin size by using commands
> in the preamble.

Some changes made in the preamble can be more subtle.

> ## Microtype {.challenge}
> Add the package microtype in your preamble ```\usepackage{microtype}```

These changes are subtle modifications on the inter word spacing and 
kerning.  It tends to make your document look just a little bit 
better. [Tips on Writing a Thesis in LaTeX](http://www.khirevich.com/latex/microtype/) provides
a good overview of what it does.

If you want to add coloured fonts to your document, you will need to 
include the package ```\usepackage{color}```.  You can then add colour
to text by using a textcolor environment. ```\textcolor{red}{some text I want red}```
 
> ## Colour some text {.challenge}
> Add some colour to your document.  Remember you will be using the 
> American spelling of colour!

> ## More colours {.callout}
>
> You may notice that there an't many colours you can directly use
> with the simple ```\usepackage{color}```.  If you need more colours
> you can either use the xcolor argument ```\usepackage[usenames,dvipsnames]{xcolor}```
> which gives you 68 more named colours or you can predefine your own
> colours in your preamble.  Google has good resources on this.

Suppose that in the process of writing your document you need to add red 
text quite regularly, typing ```\textcolor{red}{some text I want red}``` 
every time might get a bit tiresome. This is where macros come in, they
are one of LaTeX most powerful features.  Macros allow you to create new,
custom commands for LaTeX.  In fact LaTeX is just TeX with many macros that
make things easier.  


> ## Make a macro {.challenge}
>
> Lets make a new command called ```\colourtxt``` we do this by adding the
> following commands into the preamble 
> ```\newcommand{\colourtxt} [1] {  \textcolor{red}{#1}  }```.  To make 
> some text red in your document, use ```\colourtxt{The Text I want red}```.
> Note that LaTeX ignores spaces in commands, so I have spaced this line
> out more than you usually would to try to clarify it a bit.

> ## Macro Syntax {.callout}
>
> The syntax can seem a bit confusing at first, it helps to break it 
> down. ```\newcommand{\colourtxt}``` creates our new command.  ```[1]```
> specifies that we have one argument for our new command.  ```{  \textcolor{red}{#1}  }```
> is the set of commands that run whenever we call ```\colourtxt```.  In 
> fact we could have put as many commands into this ```{   }``` pair as 
> we liked to do arbitrarily complicated things.  However in this case
> the only command we are running is ```\textcolor{red}{#1}``` the ```{#1}```
> gets replaced by whatever we put inside the ```\colourtxt{sometext}``` brackets.




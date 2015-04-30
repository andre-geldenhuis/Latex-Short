---
layout: page
title: LaTeX
subtitle: Where The Magic Happens
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Preamble
> * Macros

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

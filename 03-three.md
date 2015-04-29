---
layout: page
title: LaTeX
subtitle: Formatting, symbols and math
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Simple text formatting
> * Symbols
> * Math mode

If you have done the previous lessons your document should look something
like the following

~~~ {.latex}
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{Latex Intro}
\author{andre.geldenhuis }
\date{April 2015}

\begin{document}

\maketitle

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
Aenean faucibus magna sed enim ullamcorper vulputate. Aliquam non eros ac 
quam sollicitudin cursus eu ac est. Donec consectetur eget nibh id mollis. 
Quisque euismod diam velit, quis pretium justo accumsan id. 

\subsection{Abstract}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Mauris facilisis, diam pretium pretium lobortis, metus dolor fermentum 
augue, ultrices consequat dolor tortor nec risus. Aenean sagittis 
hendrerit turpis, a porta eros facilisis in. In efficitur posuere risus, 
eu ullamcorper arcu. Morbi fermentum auctor arcu, non interdum ligula 
placerat maximus. Morbi nec metus et urna gravida rhoncus. Donec interdum, 
nisi vitae volutpat vehicula, odio eros pulvinar mauris, ac mollis elit 
enim sit amet diam. Ut blandit hendrerit luctus. Duis eget augue sed mi 
pellentesque mattis non finibus libero. Aliquam rhoncus, orci tempus 
consectetur mattis, enim turpis dignissim eros, sit amet sollicitudin 
justo turpis a justo. 

\end{document}
~~~

In LaTeX everything is done with commands, including basic formatting.
`\textbf{text}` will boldface the text in the brackets.  `\textbf` is the
command and `{ }` contains the argument to that command.  Note that you 
can apply this command to an as much of your document as you like.

> ## Apply some formatting {.challenge}
>
> Bold face your entire introduction paragraph.  Italicise several *separate*
> words in your second paragraph.  Remember to google for commands you
> don't know.

> ## Three ways to add italics to text {.callout}
>
> There are actually three ways to italicise text in LaTeX, can your
> work out what the differences are?


Math mode is used to generate mathematical equations and symbols.  It is
also used to generate many non math symbols.  





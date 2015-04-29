---
layout: page
title: LaTeX
subtitle: Sections, subsections and the table of contents
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Use of Sections and subsections
> *  **T**able **o**f **C**ontents (TOC)
> * Searching for help

> * Simple use of Math Mode
> * Basic formatting in LaTeX
> * Images and Floats



In this lesson we will cover day to day tasks in LaTeX, how to format 
your document, how to add symbols and equations, adding images and figures
and lastly sections and subsections.

If you are using ShareLatex you will already have a section in your document.
Otherwise, you can copy the following commands into your LaTeX editor.

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
Vivamus in accumsan erat. -- generated with http://www.lipsum.com/

\end{document}
~~~

It is quite common when writing LaTeX documents that you will forget how
to do something.  The easiest way to remember is to look back at older 
parts of your current document or documents you wrote in the past.

> ## Add a new section {.challenge}
>
> Add a new section below the paragraph making up your introduction. Look
> to the commands already in your document to determine how best to do it.
> One you have a new section, check that your document compiles, then
> add some text to your new section.

Sometimes (often) when writing you will want to do something that you
don't have an example of in your previous writing and commands.  
Thankfully there is a huge community of helpful LaTeX users!  Googling 
for what you want to do will usually turn up something helpful.  You can
add terms to your search to bring up particularly helpful communities, 
such as [stackoverflow](http://stackoverflow.com/) if your first search 
is not fruitful. 

> ## Add a subsection {.challenge}
>
> Google for how to add a subsection to your document. 

> ## Googling for help {.callout}
>
> Never be afraid to google for a solution to your LaTeX problem,
> even experts google for solutions all the time.  Even when you can 
> figure out a way of doing something complicated yourself, often someone
> else has figured out a more elegant solution.

One of the reasons people use LaTeX is to avoid unnecessary work.  Now 
that we have some sections and subsections, lets automatically 
create a table of contents.

> ## Add a Table of Contents {.challenge}
>
> Insert ```\tableofcontents``` in the location you would like the TOC
> to appear.  Once your document compiles, try moving 
> ```\tableofcontents``` somewhere else.  What happens if you move it
> before ```\begin{document}```? Have a look at the error message.
> What kif you moved it about after ```end{document}``` ?  Return
> the TOC to a sensible lcaotion when done and make sure your document
> compiles without errors 













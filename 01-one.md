---
layout: page
title: LaTeX
subtitle: Document Structure and Basics
minutes: 10
---
> ## Learning Objectives {.objectives}
>
> * Basic LaTeX document structure
> * How commands work

Unlike a word document, LaTeX documents need a little structure before
we can get started writing.  Thankfully many editors automatically create 
this for you when you make a new document.

If you are using sharelatex, create a new document with the big red 
New Project button on the top left.  Lets call it Latex Intro.
In your new project you will see your commands on the left pane and the 
output on the right pane.

In the left pane you should see the LaTeX document with the minimal amount
of required structure.



--- possibly including [key word 1](reference.html#key-word-1) ---



~~~ {.latex}
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{Latex Intro}
\author{andre.geldenhuis }
\date{April 2015}

\begin{document}

\maketitle

\section{Introduction}

\end{document}
~~~

> ## If you are not using ShareLatex {.callout}
>
> You might not have the same minimal document, if so just copy the commands
> above and paste them into your editor.  Note you might want to change
> the author to you!

On the right hand panel we see the output we get when we compile the LaTeX
commands.  You will immediately notice the output is very different from the
input commands.  This is the key difference between **W**hat **Y**ou 
**S**ee **i**s **W**hat **Y**ou **G**et  (WYSIWYG - Pronounced "wiz-ee-wig")
and LaTeX which separates presentation from content.  Initially this can 
be frustrating to users who are familiar with word but it offers some big
advantages once you are used to it, such as focusing on writing content rather
than constantly tweaking formatting.

Every time we use \something in LaTeX, it is interpreted as a command. 
Some commands have arguments, they are contained inside the curly brackets {}
```latex
\title{Latex Intro}
```  
In this case we are using the command to tell LaTeX to create a title, 
and setting the title to *Latex Intro*

> ## Remove a command and see what happens {.challenge}
>
> Try remove a command and then recompile to see what happens
> I suggest removing `\maketitle`  
> what happens?  Replace `\maketitle` afterwards

LaTeX documents have some required commands, we need to have a 
`\documentclass` a `\begin{document}` and an `\end{document}`

> ## Remove a required command {.challenge}
>
> Try removing one of the required commands and recompiling the document
> 
> Depending on which command you removed you will get different errors,
> you can see the errors by clicking on the *logs and output files* icon
> next to the recompile button.  Have a look at the errors and try to
> get a feel for what they mean.  Afterward, replace the required command
> you removed and make sure your document compiles correctly.

> ## LaTeX tries to compile with errors {.callout}
>
> Note that LaTeX tries to compile your document, even with errors.  Sometimes
> it even succeeds.  If you had removed `\begin{document}` you would still
> get a reasonable output as LaTeX guesses what you are missing and tries
> to compile anyway.  However, it is never a good idea to just keep going
> with compile errors as they **will** cause problems down the road.
> Always check what the compile errors are and try to fix them.

LaTeX Documents also have a minimal amount of structure, the preamble and the
document text.  All the commands above `\begin{document}` are known as the preamble. In 
the preamble you setup which packages to use, make board overarching
changes to your document, such as selecting fonts or configuring layouts.   

Everything from `\begin{document}` to `\end{document}` is 
the document text.  This is where you write your document.

> ## Add some content {.challenge}
>
> Write a paragraph or two below the `\section{Introduction}` and compile
> it.

> ## Huge Margins {.callout}
>
> Something you will likely have noticed by now is the large margins on your
> document.  This is because LaTeX is trying to manage your words per line
> for optimal readability.  We will cover ways to make better use of the
> page in the third lesson.





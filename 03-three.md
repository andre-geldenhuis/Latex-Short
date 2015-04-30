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

LaTeX lets you add a huge variety of symbols to your document. The easiest
way to add these symbols to your document is to use Math Mode.  There are
several ways to use math mode but for now we we use inline math mode.  We
do this by placing our symbol command inside a pair of ```$```. To create
the greek character alpha we enter ```$ \alpha $```

> ## Apply some symbols your document {.challenge}
>
> Add the symbols ```\alpha```, ```\rightarrow``` and ```\Rightarrow```.
> How would we add the logic symbol for all or exists?  You can also put
> multiple symbols inside the pair of ```$  $```.

The space between the ```$  $``` symbols is known as an environment, in this
case, the maths environment.  We also use this math mode environment to
create accented characters. This is done via an accent command with the
character as the argument.  For instance we can create and acute e by 
entering ```$ \acute{e} $```

> ## Add accented characters to your document. {.challenge}
>
> The accenting commands are 
>  ```\hat{a}``` , ```\acute{a}``` , ```\bar{a}``` ,  ```\dot{a}``` , ```\breve{a}``` ,  
>  ```\check{a}``` , ```\grave{a}``` , ```\vec{a}``` , ```\ddot{a}``` , ```\tilde{a}``` 
> Try put some accented characters into your document.

> ## LaTeX handles all formatting {.callout}
>
> If you are anything like me, you might have just copy pasted the 
> the accent commands directly into the environment between a pair of 
> ```$  $```.  What happens to the spaces?  What about a return breaking
> the line? 

Math mode is also useful for superscript and subscript.  ```^``` is used 
for super script and ```_``` is used for subscript.

> ## Use superscript and subscript in your document. {.challenge}
>
> Try out subscripts and superscripts.  How would you apply a superscript
> to more than one character?  Remember to use math mode!

Lastly math mode can obviously be used for math!  
```\frac{topline}{bottomline}``` creates a fraction.  Note that this is 
the first time we have come across a command with multiple arguments.

> ## Make a simple fraction. {.challenge}
>
> Try out a simple fraction in math mode.

If we have a more complicated mathematical equation, it should be placed
on its own, rather than being inline.  Here we use ```$$ $$``` to set the
display math environment.  Equations are one of LaTeX strong points, it
allows you to quickly enter equations that would be very hard to create
in word.  It can look complicated at first, but once you are used to it,
it is a fast and reliable way to render equations

> ## A more complex equation {.callout}
> 
> Enter the following into a *display math* enviroment
> ```{.latex}
> \int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}
> ```
> or
> ```{.latex}
> \underbrace{a+\overbrace{b+\cdots}^{{}=t}+z}
>_{\mathrm{total}} ~~
> a+{\overbrace{b+\cdots}}^{126}+z
> ```












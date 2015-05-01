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
\author{Andre Geldenhuis and Sarah Hoyte }
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

\begin{equation}
\int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}
\end{equation}

\begin{equation}
\underbrace{a+\overbrace{b+\cdots}^{{}=t}+z}
_{\mathrm{total}} ~~
a+{\overbrace{b+\cdots}}^{126}+z
\end{equation}

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

> ## Add the image to your document  {.challenge}
> 
> Now add the image to your document. You will need the graphicx package
> in your preamble and you will also need to set your graphicspath to ```images/```.
> Create a new section and add your image to it.  

When adding images into documents like a thesis or a publication it is
a good idea to add the image in a figure frame.  This is done by creating 
a figure environment with ```\begin{figure} ... \end{figure}```.

> ## Add a figure frame  {.challenge}
> Modify the image you included previously to be a figure.  Wrap the
> original ```\includegraphics``` with the figure environment. Note that
> you can put everything on one line but it is tidier to put the environment
> begin and end on separate lines.

> ## LaTeX handles formatting {.callout}
>
> When you recompile your document, did you notice the image (now a figure)
> moved ?  This is because LaTeX is trying to put the figure in the best
> place to optimise the look of the page.  Sometimes you might not want
> LaTeX to do this, you can suggest the LaTeX should place the figure
> where it is in the source document by adding ```[h]``` (for **h**ere) after 
> begin figure environment like this ```\begin{figure}[h]```.  Note that 
> this is only a suggestion, if you want to force LaTeX to place the 
> figure **H**ere, use a capital ```H```

Initially the image might be quite small, you can set the size of the image
by adding the argument ```[width=150pt]``` to ```\includegraphics```.  
In this case it would be ```\includegraphics[width=150pt]{space_rocket}```.
However, it might be more convenient to set the width to a ratio of 
something else on the page.  LaTeX has many macros which return useful
values from the current document such as ```\textwidth``` and 
```\paperwidth```.

> ## Change the size of the image {.challenge}
> Set the size of the image, but use a reference to the text width or 
> the paper width.  Try both.

> ## Warning messages {.callout}
>
> Note that when you set the image to ```\textwidth``` you get a *warning*.
> This is shown as a yellow number next to the compile button. Have a look
> at the log by clicking the button.  What does this warning mean?  When
> you set the width to ```\paperwidth``` you get even more warnings.  Have
> a look at them too.  Warnings don't stop your document from compiling
> but they do mean it might not look as good as it could.  It is a good
> idea to compile your document often and try to fix errors and warnings 
> when they come up.  Note that sometimes you won't be able to remove
> all the warnings, particularly warnings about LaTeX not being able
> to place objects where it would like.

In this case, to remove the warnings you need to reduce the image size.  
We can do this by setting the image to be a ratio of either ```\paperwidth```
or ```\textwidth```.  You do this my multiplying ```\textwidth``` by a 
fraction.  

> ## Adjust the image width {.challenge}
>
> Try ```0.2\textwidth```. Experiment with other values too.

Now that we have a more reasonable image size, lets add a caption to the 
image.  This is done with the ```\caption{ }``` command. 

> ## Add a caption {.challenge}
>
> Try adding a simple caption.  Once that has compiled, we can try a more
> complex caption, we can include an inline math enviroment. Try adding 
> ```\Delta V = \nu_e \ln\frac{m_0}{m_1}``` to your caption.  Remember
> that you will need to put it inside the inline math environment.

> ## Center the image {.challenge}
>
> The image might look better centred.  Google for how to do this.

Now that we have a nice figure with a cool caption, lets refer to this figure
elsewhere in our document.  We do this by adding a label to our figure
and then cross-referencing it elsewhere in the document.  We give the
figure a label by adding ```\label{fig:CoolRocket}``` to the figure
environment.  The Best practice is to add the label *inside* the caption.
So ```\caption{Some Neat Caption\label{fig:CoolRocket}}``` We refer to 
it in the document text by ```\ref{fig:CoolRocket}```
or ```\pageref{fig:CoolRocket}```.  Note that labeling and cross-referencing
is **case sensitive**.

> ## Label and Cross-Reference your figure {.challenge}
>
> Add the label to the figure environment and then refer to it in an 
> earlier paragraph.  Try both ways of cross-referencing your figure.

> ## Labelling Equations {.callout}
>
> You have seen how to label the figure environment, can you do the same
> for equations?  This works best with non-inline equations defined by
> ```\begin{equation}``` and the like.

> ## Add another figure {.challenge}
>
> Upload the image [polarplot.eps](https://github.com/andre-geldenhuis/Latex-Short/blob/gh-pages/fig/polarplot.eps)
> to your images folder on ShareLatex.  Above the figure you already have, 
> add the new image in its own figure environment. Give it its own caption 
> and label.

> ## LaTeX handles laborious tasks for you {.callout}
>
> Note that previously your ```\ref{CoolRocket``` returned 1 for the first
> figure?  What did it change to when you added a new figure above the 
> old one?

Now that we have several figures, it might be nice to have a list of figures.

> ## List of figures {.challenge}
>
> Add a list of figures to your document in a sensible location.  ```\listoffigures```









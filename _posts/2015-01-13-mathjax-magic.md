---
title: "The magic of LaTeX"
layout: post
photo_url: "http://mpe.berklee.edu/academics/resources/math.jpg" 
tags: LaTeX, jekyll
category: website
comments: no
---


One of the nicest things I found about Jekyll is that it's able to support the
best typesetting language of them all, `\( \LaTeX \)`, on the net, right here in
your browser! 

I've followed [this useful guide](http://cwoebker.com/posts/latex-math-magic).

It's super easy to set up. Using a default Jekyll setup with
rdiscount as your Markdown parser, the only thing you'll need to do is drop a 
couple of lines of JavaScript in your default.html layouts file.
I've added it to my _includes folder and linked it.

This is the code in question:

    <!-- MathJax Section -->                                                       
    <script type="text/javascript"    
        src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
    </script>
    <script>    
    MathJax.Hub.Config({    
        tex2jax: {    
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre']    
        }    
    });    
    MathJax.Hub.Queue(function() {    
        var all = MathJax.Hub.getAllJax(), i;    
        for(i=0; i < all.length; i += 1) {    
            all[i].SourceElement().parentNode.className += ' has-jax';    
        }    
    });    
    </script>

What we're doing here is calling the MathJax JavaScript code to render 
our LaTeX and essentially telling our markdown parser not to crush all that
lovely LaTeX code into smithereens.

We get the ability to render something like Maxwell's equations in
full glory.

`\[
\begin{aligned}
\nabla \times \vec{\mathbf{B}} -\, \frac1c\,
\frac{\partial\vec{\mathbf{E}}}{\partial t} & = \frac{4\pi}{c}\vec{\mathbf{j}}
\\   \nabla \cdot \vec{\mathbf{E}} & = 4 \pi \rho \\
\nabla \times \vec{\mathbf{E}}\, +\, \frac1c\,
\frac{\partial\vec{\mathbf{B}}}{\partial t} & = \vec{\mathbf{0}} \\
\nabla \cdot \vec{\mathbf{B}} & = 0 \end{aligned}
\]`

A cross product formula perhaps?

`\[
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix}
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0
\end{vmatrix}
\]`


It's a neat addition and one I can see myself using in the future.
As soon as I find something good to math about.


<p align="center">
<a href="http://kieranhealy.org/blog/archives/2011/02/23/choice-of-language-and-its-consequences/">
<img src="/images/ltx_paper.png" style="float: middle"></a>
</p>

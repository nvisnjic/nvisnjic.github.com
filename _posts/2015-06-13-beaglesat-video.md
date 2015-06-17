---
title: "VIDEO IS UP!"
photo_url: "/images/beagleshot_small.png"
layout: post
tags: beaglebone, gsoc2015, video, youtube
category: BeagleSat
comments: no
---



After much back and forth with the good YouTube service and my VPN, I've
finally managed to upload the intro video for the BeagleSat project.

Without further ado, here it is!


<iframe width="560" height="315" 
src="https://www.youtube.com/embed/ojDqtxv9oGY" frameborder="0"
allowfullscreen></iframe>



It took a bit longer to put together, but the overall workflow looked something like this: 


<pre><code class="html">
    Impress.js presentation        voice-over in Ardour4 
            ||                               ||
            ||                               ||
           \||/                             \||/
            \/                               \/ 
   simplescreenrecorder           sync video & audio mix
            ||                               ||
            ||                               ||
           \||/                             \||/
            \/                               \/
        video_file                       audio_file
            ||                               ||
            ||                               ||
            ||         Edit in ShotCut       ||
             ===============|+|===============
                            | |
                           \| |/
                            \ /
                             V 
                         Final Cut => YouTube
</pre></code>


I'll make a blog post at some point on how to do this and
[Impress.js](http://bartaz.github.io/impress.js), while
being a brilliant tool for presentations, needs a blog post of its own.

Thanks for watching!



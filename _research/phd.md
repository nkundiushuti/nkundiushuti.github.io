---
layout: page
#
# Content
#
subheadline: "Source separation for orchestral mixtures"
sidebar: right
title: "PhD Thesis"
teaser: "isolate instrument tracks, recreate experiences"
permalink: "/research/phd/"
categories:
  -
tags:
  - phd, source separation, thesis
header:
   image_fullwidth: "header_orchestra.jpg"
---


My PhD topic was source separation of classical musical instruments from orchestral pieces. It was a part of the european project [PHENICX][1], which aimed at transforming the way classical music is enjoyed. Being able to separate the audio corresponding to the instruments, allowed for interesting applications such as focusing on a particular sections in the orchestra or the re-creating the experience of the concert in virtual reality.

I was supervised by [Jordi Janer][5] and [Emilia Gomez][6].


Below you can watch a demo from the official [app][2] which uses the separated tracks.

<div class="flex-video">
        <iframe width="1280" height="720" src="https://www.youtube.com/embed/7kxS8nblDYk" frameborder="0" allowfullscreen></iframe>
</div>

Although I mainly worked on orchestral music, in this [github repository][7] I have code for pop music source separation using deep learning.


Traditionally, music source separation is done through a popular convex optimization technique, namely non-negative matrix factorization or, more recently, through deep learning. These approaches improve if we have the multi-microphone recordings of the piece, if we know which instruments are present in the piece, and if we have the score e.g. the notes played by each instrument. In fact, the more information we have about a music piece, the more we can restrict our model, and the better the resulting separation. For orchestral music the instruments are known, so we train timbre models for each instrument. Because any orchestral piece is accompanied by a score, we use the score information to further improve the separation.



If a dataset comprising isolated tracks for all instruments exists, then one can evaluate source separation objectively. Otherwise, the only solution is a more costly and difficult to replicate experimental evaluation. Thus, we proposed a [dataset][3] which not only that allowed us to evaluate our system, but it can be useful for future research on this topic. More info about these experiments in the following journal paper:

{% include alert text='M. Miron, J. Carabias-Orti, J. J. Bosch, E. Gómez and J. Janer, "Score-informed source separation for multi-channel orchestral recordings", Journal of Electrical and Computer Engineering (2016))"' %}


We basically wanted to simulate a real recording and to have control on the important factors such as reverberation, position of microphones in the room, number of instruments in a section. Thus, we can have a robust evaluation by considering the influence of each of the factors on the quality of separation. To our knowledge, it is the first time that such a dataset is proposed for this scenario: orchestral music.

Source separation makes possible a range of creative applications such as virtual reality concerts:
![Virtual Reality Concert]({{ site.url }}/images/vr.jpg)

You can have a go with the [orchestra focus demo][4] where you can listen specific instruments from an orchestra.

 [1]: http://phenicx.upf.edu/
 [2]: http://phenicx.com/
 [3]: http://mtg.upf.edu/download/datasets/phenicx-anechoic
 [4]: https://repovizz.upf.edu/phenicx/
 [5]: http://www.dtic.upf.edu/~jjaner/
 [6]: https://emiliagomez.com/people/
 [7]: https://github.com/MTG/DeepConvSep
 [8]: #
 [9]: #
 [10]: #

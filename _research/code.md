---
layout: page
sidebar: right
title: "Code & data"
teaser: ""
permalink: "/research/code/"
header:
    image_fullwidth: "mediaplayer_js-home.jpg"
categories: 
  - research
tags:
  - music information retrieval, code, python, c++, c, matlab
---
Code is made available through github, either at my [repository][1] or at the research groups I have been with, [MTG][2] and [SMC-INESC][3]. 

Except parts of code which I couldn't publish because of non-disclosure agreements, the research presented in [papers][4] is documented in the repositories referenced in the papers, along with links to the datasets and instructions on how to replicate those experiments. 

### DeepConvSep
![deepconvsep]({{ site.url }}/images/widget_deepconvsep.png)

Deep Convolutional Neural Networks for Musical Source Separation

This repository contains classes for data generation and preprocessing, useful in training neural networks with large datasets that do not fit into memory. Additionally, you can find classes to query samples of instrument sounds from [RWC instrument sound dataset][5]. In the 'examples' folder you can find use cases for the classes above for the case of music source separation.

### beatStation
![beatstation]({{ site.url }}/images/widget_beat-station2.png)

an openFrameworks tapping recorder

beatStation was designed as a game with a purpose application in which users can compete between each other in tapping various songs. It can be used by researchers to annotate audio, conduct experiments, or as an inspiration for future apps.

### Live drum transcription
<div class="flex-video">
        <iframe width="1280" height="720" src="https://www.youtube.com/embed/RB-1nWavrmg" frameborder="0" allowfullscreen></iframe>
</div>

This is audio drum transcription algorithm in pure data, MaxMSP and Max4Live which can transcribe kick, snare, and hi-hat from live drum performances. The software takes live audio or files as input and triggers events for each drum type as output.

### PHENICX anechoic dataset 
[![phenicx]({{ site.url }}/images/Logo_Phenicx-04.gif)][7]

This [dataset][7] includes audio and annotations useful for tasks as score-informed source separation, score following, multi-pitch estimation, transcription or instrument detection, in the context of symphonic music.The [dataset][7] was presented and used in the evaluation of:

{% include alert text='M. Miron, J. Carabias-Orti, J. J. Bosch, E. Gómez and J. Janer, "Score-informed source separation for multi-channel orchestral recordings", Journal of Electrical and Computer Engineering (2016))"' %}

 [1]: https://github.com/nkundiushuti
 [2]: https://github.com/MTG
 [3]: https://github.com/SMC-INESC
 [4]: http://mariusmiron.com/research/publications/
 [5]: https://staff.aist.go.jp/m.goto/RWC-MDB/
 [6]: https://github.com/SMC-INESC/beatStation
 [7]: http://mtg.upf.edu/download/datasets/phenicx-anechoic
 [8]: #
 [9]: #
 [10]: #

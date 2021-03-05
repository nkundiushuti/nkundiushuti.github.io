---
layout: page
sidebar: right
subheadline: ""
title: "Deep learning source separation for hip hop and classical music"
teaser: "Source separation papers at ISMIR conference and MML workshop..."
header:
    image_fullwidth: "mediaplayer_js-home.jpg"
categories:
  - blog
tags:
  - hiphop, classical music, deep learning, source separation
---
During October I have attended the [Music and Machine Learning Workshop][7] in Barcelona and the [ISMIR][8] conference in Suzhou, China presenting papers on source separation for hiphop and Western classical music. You can check the PhD section on this website if you are new to source separation and you want to understand what I have been doing during the past 4 years.

So what do hiphop and classical music have in common? :) Rather than having an universal model which separates any music piece, we were targeting context-specific approaches which deal with  problems which one encounters in particular music genres. For instance, in hiphop the vocal part is not sung and there is wide variety of timbres and production styles. On the other hand, in classical music, the complexity arrises from the multitude of harmonic instruments of similar timbre (depending on the piece). In this case, there are also opportunities which are given by the scores: the Western classical music pieces depart from symbolic representations.

How can the deep learning or data-driven approaches take advantage of these characteristics? According to [Ian Goodfellow][1] a way to increase generalization is through data augmentation. So, hip hop and classical music source separation can improve using data augmentation or generation. This is the main idea behind the two papers.

The MML paper, [Data augmentation for deep learning source separation of HipHop songs][4] is based on work done by Hector Martel during his [undergrad thesis][3] at UPF. He is also a hiphop producer so he proposed a [hiphop dataset][5]. You can check out the [demo][6] he did for his thesis' presentation. I uploaded the presentation on [slideshare][10]. Here's a video of the demo:

<div class="flex-video">
        <iframe width="1280" height="720" src="https://www.youtube.com/watch?v=h8v0_3qKLHo" frameborder="0" allowfullscreen></iframe>
</div>

The ISMIR paper, [Monaural score-informed source separation for classical music using convolutional neural networks][11] is a part of my PhD thesis on orchestral music source separation. It's one of the first papers trying to improve deep learning source separation methods with score information. Similarly to the other deep learning papers, the code is made available through the [github repository][2], and the separated tracks and computed evaluation metrics are on [zenodo][14].

Demos:

<div class="flex-video">
        <iframe width="1280" height="720" src="https://www.youtube.com/watch?v=c0xJIJrp5w8" frameborder="0" allowfullscreen></iframe>
</div>


<div class="flex-video">
        <iframe width="1280" height="720" src="https://www.youtube.com/watch?v=9vSxRVh1YZU" frameborder="0" allowfullscreen></iframe>
</div>

 [1]: http://www.deeplearningbook.org
 [2]: https://github.com/MTG/DeepConvSep
 [3]: https://repositori.upf.edu/bitstream/handle/10230/32919/Martel_2017.pdf?sequence=1&isAllowed=y
 [4]: http://mtg.upf.edu/node/3825
 [5]: https://doi.org/10.5281/zenodo.823037
 [6]: https://hiphopss.github.io
 [7]: https://musml.weebly.com
 [8]: https://ismir2017.smcnus.org
 [9]: https://www.slideshare.net/MariusMiron2/presentation-ismir
 [10]: https://www.slideshare.net/MariusMiron2/presentation-mml
 [11]: http://mtg.upf.edu/node/3806
 [12]: https://www.youtube.com/watch?v=c0xJIJrp5w8
 [13]: https://www.youtube.com/watch?v=9vSxRVh1YZU
 [14]: https://doi.org/10.5281/zenodo.1009136






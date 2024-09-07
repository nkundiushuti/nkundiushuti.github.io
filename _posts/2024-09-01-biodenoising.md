---
layout: page
subheadline: "Unsupervised animal vocalization denoising"
sidebar: right
title: "Biodenoising"
teaser: "how to denoise without clean data?"
mediaplayer: true
header:
    image_fullwidth: "whale.png"
categories:
  - blog
tags:
  - bioacoustics, denoising
---

We published the arxiv preprint of our paper on denoising animal vocalizations without clean data. 

{% include alert text='Marius Miron, Sara Keen, Jen-Yu Liu, Benjamin Hoffman, Masato Hagiwara, Olivier Pietquin, Felix Effenberger, Maddie Cusimano, "Biodenoising: animal vocalization denoising without access to clean data"' %}

Along with it we release a Python library, ***biodenoising***, which can be used to denoise audio recordings of animal vocalizations. We provide three benchmark datasets: one comprising a variety of species and noises, a zebra finch dataset, and a carrion crow dataset. The training data can be downloaded and processed using another library ***biodenoising-datasets***.

Speech enhancement e.g. denoising speech signals, currently requires large amounts of isolated speech. This is not the case for animal vocalizations. Data recorded in the wild is often noisy, and even biologgers capture self-generated and wind noise. In the lab, self-noise or fan noise are often present. 

How can we denoise animal vocalizations without clean data? The current research relies on estimating the noisy targets in noisier mixture i.e. creating mixtures by adding more noise on top of these targets. However, speech enhancement models already know a lot about patterns in audio time series. So why not use these models to obtain pseudo-clean targets instead of using the noisy targets.

One important thing, in our experiments we discovered that time scaling e.g. slowing down or speeding up the vocalization can help. Why does this transformation makes sense? We know that with some exceptions the pitch of a vocalization is correlated with the size of the its body. Check out the video below to see how this works for whales and birds.

<video width="640" height="360" id="player1" preload="none">
  <source type="video/youtube" src="http://www.youtube.com/watch?v=M5OCCuCIMbA" />
</video>

If we can bring up the pitch within the human speech range, we could re-use speech enhancement models. Speech enhancement models learn signal priors such as sparsity, structure of vowels and phonemes that may be useful when denoising animal vocalizations.




 [1]: #
 [2]: #


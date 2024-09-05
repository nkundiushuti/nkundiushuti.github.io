---
layout: page
subheadline: "Unsupervised animal vocalization denoising"
sidebar: right
title: "Biodenoising"
teaser: "how to denoise without clean data?"
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

So how can we denoise animal vocalizations without clean data? In our experiments we discovered that time scaling e.g. slowing down or speeding up the vocalization can help. Why does this transformation makes sense? We know that with some exceptions the pitch of a vocalization is correlated with the size of the its body. Check out the video below to see how this works for whales and birds.


<div class="flex-video">
        <iframe width="1280" height="720" src="https://www.youtube.com/watch?v=M5OCCuCIMbA" frameborder="0" allowfullscreen></iframe>
</div>

So in theory if we can bring up the pitch within the human speech range, we could re-use speech enhancement models. We rely on the fact that the enhancement models learn signal priors such as sparsity, structure of vowels and phonemes that may be useful when denoising animal vocalizations.




 [1]: #
 [2]: #


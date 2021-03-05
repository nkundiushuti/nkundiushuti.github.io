---
layout: page
#
# Content
#
subheadline: "Source Separation Methods for Orchestral Music. Timbre-informed and score-informed strategies"
sidebar: right
title: "PhD Thesis Companion Page"
teaser: "pdf, datasets, code, applications"
permalink: "/research/thesis/"
categories:
  -
tags:
  - phd, source separation, thesis
header:
   image_fullwidth: "header_orchestra.jpg"
---


This is the companion page of my PhD thesis. You can read a description of the topic [here][1]. The purpose of this page is to provide the resources mentioned in the thesis: pdf, datasets, code, applications.

The PDF of the thesis is hosted on this [website][2].

{% include alert text='Abstract:

Humans are able to distinguish between various sound sources in their environment and  selectively attend to specific ones. However, it is a difficult task to teach a computer to automatically separate the acoustic scene into sources and solely focus on specific elements. This signal processing task is commonly known as audio source separation and involves recovering the sources which are mixed together in a combined signal.

This thesis is concerned with source separation of Western classical music mixtures, namely orchestral music. Being able to separate the audio corresponding to the instruments allows for interesting applications such as focusing on a particular section in the orchestra or re-creating the experience of a concert in virtual reality. Additionally, the separated instrument tracks can be further analyzed by other music information research algorithms which perform better on these signals than on the audio signal of the mixture.

Music source separation improves if we know which instruments are present in the piece, and if we have the score e.g. the notes played by each instrument. In fact, the more information we have about a music piece, %the more we can restrict our model, and
the better the resulting separation. For orchestral music the instruments are known, and we train timbre models for each instrument, a case commonly known as timbre-informed source separation. In addition, since scores are commonly available for orchestral pieces, we leverage this  information to further improve the separation. This scenario is known in literature as score-informed source separation.

Towards an objective evaluation, in the second part of the thesis we propose an orchestral music dataset accompanied by score annotations and an evaluation methodology which assesses the influence of difference parts of the separation framework.
In the third part of the thesis, our contributions are towards fixing context-specific problems encountered  in score-informed source separation, like the errors in the alignment between a score and the associated renditions. Furthermore, while we work towards improve existing separation frameworks, in the fourth part of the thesis we propose a low latency framework relying on deep learning. With respect to that, we aim at overcoming data scarcity in the case of supervised source separation approaches by taking advantage of the traits of this music tradition to generate better data to train neural networks. In addition, in the fifth part, we introduce a cloud-based source separation software architecture and the associated applications.

Most of this work follows the research reproducibility principles, inasmuch the datasets, code, software prototypes, published papers, and project reports are made available along with the necessary instructions.'%}

A video recording of the PhD defense has been uploaded on youtube
<div class="flex-video">
        <iframe width="1280" height="720" src="//www.youtube.com/embed/FDrFTTVOtr0" frameborder="0" allowfullscreen></iframe>
</div>

## Datasets

We propose the [PHENICX-Anechoic][5] dataset which relies on the Aalto orchestral anechoic recordings. We denoised the original recordings and annotated each of the tracks corresponding to the instrument groups.

The Bach10 recordings synthesized with Sibelius can be found on the [zenodo repository][11].

## Code

The note refinement code in part three of the thesis is on [github][6]. We do not have the rights to distribute the NMF framework and to some extent note refinement is integrated with this framework. However, multi-channel score-informed source separation can be computed using the [Repovizz][4] website. You need to create a datapack with [datapack designer][7], upload it and select the checkbox which computes the source separation. The uploaded datapack will comprise the separated tracks.

Code and detailed instructions on how to reproduce experiments in part four (source separation using deep learning) can be found on the associated [github repository][8]. The separation results and the computed metrics with BSS Eval can be found on the [zenodo page][9]. Similarly, for the score-informed version, check the [zenodo page][10].


 [1]: http://mariusmiron.com/research/phd/
 [2]: http://mariusmiron.com/phd_thesis/MariusMiron_thesis.pdf
 [3]: http://mtg.upf.edu/download/datasets/phenicx-anechoic
 [4]: https://repovizz.upf.edu/phenicx/
 [5]: https://zenodo.org/record/840025
 [6]: https://github.com/nkundiushuti/Note-refinement-
 [7]: https://repovizz.upf.edu/designer/
 [8]: https://github.com/MTG/DeepConvSep
 [9]: https://zenodo.org/record/344499
 [10]: https://zenodo.org/record/1009136
 [11]: https://zenodo.org/record/321361
 [12]: #
 [13]: #
 [14]: #

---
layout: page
sidebar: right
subheadline: "High frequency magnitude spectrogram reconstruction for music mixtures using convolutional autoencoders"
title: "Music Bandwidth Expansion"
teaser: "autoencoders in frequency domain yet again ..."
header:
    image_fullwidth: "mediaplayer_js-home.jpg"
categories:
  - blog
tags:
  - research, news, deep learning, machine learning, music bandwidth expansion, convolutional autoencoders
---


Shortly after finishing writing my PhD thesis I collaborated with [Matthew Davies][1] from INESC TEC, Porto on music bandwidth expansion - basically recovering the high frequency part of the spectrum. This has big implications in encoding and transmitting music and audio in general through bandwidth-limited media. You might recall how the voice is compressed before transmitting it through telephone lines, and then reconstructed. And how you waited and listened to a crappy sounding Mozart tune while waiting to talk with the support department. Well, if your phone had a system to better reconstruct that music piece, then it would have sounded better.

[![bandwidth-expansion](https://telecom.inesctec.pt/~mdavies/dafx18/sounds/overviewfig.png)][2]

You can check the [companion page][2] for music examples and more details on the method.
{% include alert text='Abstract:
We present a new approach for audio bandwidth extension for music signals using convolutional neural networks (CNNs). Inspired by the concept of inpainting from the field of image processing, we seek to reconstruct the high-frequency region (i.e., above a cutoff frequency) of a time-frequency representation given the observation of a band-limited version. We then invert this reconstructed time-frequency representation using the phase information from the band-limited input to provide an enhanced musical output. We contrast the performance of two musically adapted CNN architectures which are trained separately using the STFT and the invertible CQT. Through our evaluation, we demonstrate that the CQT, with its logarithmic frequency spacing, provides better reconstruction performance as measured by the signal to distortion ratio.
'%}

The [paper][3] was presented in the Digital Audio Effects 2018 conference in Portugal.

 [1]: https://telecom.inesctec.pt/~mdavies
 [2]: https://telecom.inesctec.pt/~mdavies/dafx18/
 [3]: https://telecom.inesctec.pt/~mdavies/pdfs/MironDavies18-dafx.pdf

---
layout: page
sidebar: right
subheadline: ""
title: "Sound and Music Computing conference"
teaser: "Paper on generating training data for deep learning source separation methods..."
header:
    image_fullwidth: "mediaplayer_js-home.jpg"
categories:
  - blog
tags:
  - coding, deep learning, source separation
---
During July 5th and 9th I have attended the [Sound and Music Computing Conference][1] in Helsinki, Finland. I presented a [paper][5] on [generating training data][4] for deep learning source separation method, particularly in classical music, where you have the score but no multi-track data. The slides can be found [online][3] and the code is on the source separation github repository [DeepConvSep][2].

I had the opportunity to visit the acoustics lab at Aalto University and attend a few demos. I've been in the anechoic rooms where they recorded the orchestra dataset which I have annotated and used in my paper on [score-informed orchestral separation][6]. Interestingly, in one of the demos, Jukka Patynen convolved close-microphone recordings with impulse responses taken from famous concert venues, to demonstrate how different the same recording can sound in varius halls.


There were quite a few interesting posters, from which I mention:

* Interesting app which doesn't see the learning process as a game but rather as a collaborative process, [Burns et al. : Learning to Play the Guitar at the Age of Interactive and Collaborative Web][8]
* Source separation for voice removal and then DTW for the automatic accompaniment, [Wada et al. : An Adaptive Karaoke System that Plays Accompaniment Parts of Music Audio Signals Synchronously with Users' Singing Voices][9]
* [Kirkbride: Troop: A Collaborative Tool for Live Coding][10]

From the presented papers, I was mostly interested in the MIR ones using deep learning, but there were also some other interesting ones:

* Emotion recognition using many features and MFCCs with two CNN branches for each emotion, [Malik et al.: Stacked Convolutional and Recurrent Neural Networks for Music Emotion][11]
* In contrast to other architectures which use large filters, they use small filters, [Lee et al.: Sample-Level Deep Convolutional Neural Networks for Music Auto-Tagging Using Raw Waveforms][12]
* Basically in-ear filtering and mixing for hearing protection, [Albrecht et al.: Electronic Hearing Protection for Musicians][13]
* Meter detection in symbolic files, [Mcleod et al. : Meter Detection in Symbolic Music Using a Lexicalized PCFG][14]
* Transcription with RNNs and alignment with DTW for piano recordings, [Kwon et al.: Audio-to-Score Alignment of Piano Music Using RNN-Based Automatic Music ][15]
* Orchestration using a RBM with a binarized version of the piano roll as input, [Crestel et al.: Live Orchestral Piano, a System for Real-Time Orchestral Music Generation][16]
* Active listening; they change onsets and pitches of the voice, [Ojima et al.: A Singing Instrument for Real-Time Vocal-Part Arrangement of Music and Audio Signals][17]

The proceedings can be found [online][7].

I really liked the keynote from Anssi Klapuri. A few years ago he moved from academia to Yousician, a company that develops apps for music learning. He presented the app and the architecture of their audio engine (they use Unity for graphics but for audio they use their own audio engine). Interestingly, most of the audio part is minimally processed and the audio is rooted as soon as possible to the output. The cross-cancelling seemed quite robust. Also, I really liked the testing techniques: they record the impulse responses of different phones and instruments so they can use this data afterwards for testing.


 [1]: https://smc2017.aalto.fi
 [2]: https://github.com/MTG/DeepConvSep
 [3]: https://drive.google.com/file/d/0Bxgc1jYXBwD6cngwSWRLU2FEbVU/view?usp=sharing
 [4]: https://www.upf.edu/web/mtg/news/-/asset_publisher/WM181VyAQipW/content/id/16769628/maximized#.WV99oPy6yRs
 [5]: https://mtg.upf.edu/node/3765
 [6]: https://www.hindawi.com/journals/jece/2016/8363507/
 [7]: https://smc2017.aalto.fi/proceedings.html
 [8]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p77.pdf
 [9]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p110.pdf
 [10]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p104.pdf
 [11]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p208.pdf
 [12]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p220.pdf
 [13]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p306.pdf
 [14]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p373.pdf
 [15]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p380.pdf
 [16]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p434.pdf
 [17]: https://smc2017.aalto.fi/media/materials/proceedings/SMC17_p443.pdf





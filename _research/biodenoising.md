---
layout: page
#
# Content
#
subheadline: "Unsupervised animal vocalization denoising"
sidebar: right
title: "Biodenoising"
teaser: "how to denoise without clean data?"
permalink: "/research/biodenoising/"
categories:
  -
tags:
  - bioacoustics, denoising
header:
   image_fullwidth: "whale.png"
mediaplayer: true

---

## Introduction 

{% include alert text='Marius Miron, Sara Keen, Jen-Yu Liu, Benjamin Hoffman, Masato Hagiwara, Olivier Pietquin, Felix Effenberger, Maddie Cusimano, "Biodenoising: animal vocalization denoising without access to clean data"' %}

#### Abstract
{% include alert text='
Animal vocalization denoising is a task similar to human speech enhancement, a well-studied field of research. In contrast to the latter, it is applied to a higher diversity of sound production mechanisms and recording environments, and this higher diversity is a challenge for existing models. Adding to the challenge and in contrast to speech, we lack large and diverse datasets comprising clean vocalizations. As a solution we use as training data pseudo-clean targets, i.e. pre-denoised vocalizations, and segments of background noise without a vocalization. We propose a train set derived from bioacoustics datasets and repositories representing diverse species, acoustic environments, geographic regions. Additionally, we introduce a non-overlapping benchmark set comprising clean vocalizations from different taxa and noise samples. We show that that denoising models (demucs, CleanUNet) trained on pseudo-clean targets obtained with speech enhancement models achieve competitive results on the benchmarking set. We publish data, code, libraries, and demos https://mariusmiron.com/research/biodenoising.'%}

## Audio demos

<audio src="http://archive.org/download/music_from_all_around_the_world/02._music_from_all_around_the_world_-_the_black_atlantic_-_dandelion.mp3" type="audio/mp3" controls="controls"></audio>


## Training dataset description 

| Noisy datasets              | Hours  | Medium     | Private | Direct | Link       | Type        |
|-----------------------------|--------|------------|---------|--------|------------|-------------|
| Dolphin signature whistles  | 0.23   | underwater |   yes   |  no    | [link][1]  | dolphins    |
| Hanaian Gibbons             | 1.11   | terrestrial|   no    |  yes   | [link][2]  | gibbons     |
| Geladas                     | 2.23   | terrestrial|   yes   |  no    | [link][3]  | geladas     |
| Orcasound Aldev             | 0.25   | underwater |   no    |  yes   | [link][4]  |  orcas      |
| Thyolo                      | 0.61   | terrestrial|   no    |  yes   | [link][1]  |  birds      |
| Anuran                      | 1.13   | terrestrial|   no    |  no    | [link][5]  |  frogs      |
| South-Alaska humpback whale | 14.13  | underwater |   yes   |  no    | [link][6]  |  cetaceans  |
| Orcasound SKRW              | 2.41   | underwater |   no    |  yes   | [link][4]  |  orcas      |
| Black and white ruffed lemur| 1.06   | terrestrial|   no    |  yes   | [link][7]  |  lemurs     |
| Orcasound humpback whale    | 0.8    | underwater |   no    |  yes   | [link][4]  |  orcas      |
| Orchive                     | 0.03   | underwater |   no    |  yes   | [link][13] |  orcas      |
| Whydah                      | 0.57   | terrestrial|   no    |  yes   | [link][8]  |  birds      |
| Sabiod NIPS4B               | 0.55   | underwater |   no    |  yes   | [link][9]  |  cetaceans  |
| Xeno canto labeled subset   | 6.82   | terrestrial|   no    |  yes   | [link][26] |  birds      |
| ASA Berlin                  | 4.69   | terrestrial|   no    |  no    | [link][10] |  various    |
| Watkins                     | 5.33   | underwater |   no    |  yes   | [link][11] |  various    |
| Macaques coo calls          | 0.7    | terrestrial|   no    |  yes   | [link][15] |  macaques   |

| Noise datasets              | Hours  | Medium     | Private | Direct | Link       | Type        |
|-----------------------------|--------|------------|---------|--------|------------|-------------|
| FSD50k subset               | 26.34  | terrestrial|   no    |  yes   | [link][19] |  various    |
| IDMT Traffic                | 9.72   | terrestrial|   no    |  yes   | [link][20] |  streets    |
| ShipsEar                    | 3.55   | underwater |   yes   |  no    | [link][21] |  ships      |
| DeepShip subset             | 1.78   | underwater |   no    |  yes   | [link][22] |  ships      |
| Orcasound ship noise        | 7.23   | underwater |   no    |  yes   | [link][4]  |  ships      |
| TUT 2016 subset             | 0.33   | terrestrial|   no    |  yes   | [link][23] |  home       |


| Extracted noise             | Hours  | Medium     | Private | Direct | Link       | Type        |
|-----------------------------|--------|------------|---------|--------|------------|-------------|
| MARS MBARI                  | 0.5    | underwater |   no    |  yes   | [link][24] |  various    |
| NOAA Sanctsound             | 47.48  | underwater |   no    |  yes   | [link][25] |  various    |
| Orcasound best os           | 1.6    | underwater |   no    |  yes   | [link][4]  |  various    |
| South-Alaska humpback whale | 114.85 | underwater |   yes   |  no    | [link][6]  |  various    |

 
## Benchmarking sets



 [1]: https://www.sciencedirect.com/science/article/abs/pii/S0003347207002722#:~:text=In%201965%2C%20Melba%20and%20David,et%20al.%2C%201990
 [2]: https://zenodo.org/record/7997739
 [3]: https://link.springer.com/article/10.1007/s00265-018-2612-5
 [4]: https://github.com/awslabs/open-data-registry/blob/main/datasets/orcasound.yaml
 [5]: https://www.kaggle.com/datasets/mehmetbayin/anuran-sound-frogs-or-toads-dataset
 [6]: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6071617/
 [7]: https://zenodo.org/record/6331594/
 [8]: https://zenodo.org/record/6330711
 [9]: https://sabiod.univ-tln.fr/nips4b
 [10]: https://www.museumfuernaturkunde.berlin/en/science/animal-sound-archive
 [11]: https://whoicf2.whoi.edu/science/B/whalesounds/about.cfm
 [12]: "http://download.magenta.tensorflow.org/datasets/nsynth
 [13]: https://github.com/earthspecies/library/tree/main/orcas
 [14]: https://zenodo.org/record/1442513
 [15]: https://archive.org/download/macaque_coo_calls
 [16]: https://archive.org/download/giant_otters
 [17]: https://archive.org/download/egyptian_fruit_bats_10k
 [18]: https://zenodo.org/record/1206938/
 [19]: https://zenodo.org/record/4060432/
 [20]: https://zenodo.org/record/7551553
 [21]: https://www.sciencedirect.com/science/article/abs/pii/S0003682X16301566
 [22]: https://github.com/irfankamboh/DeepShip
 [23]: https://zenodo.org/record/996424
 [24]: https://www.mbari.org/project/open-acoustic-data/ 
 [25]: https://sanctuaries.noaa.gov/news/feb21/sanctsound-overview.html
 [26]: https://doi.org/10.5281/zenodo.7828148
 [27]: #
 [28]: #
 [29]: #
 [30]: #
 [31]: #
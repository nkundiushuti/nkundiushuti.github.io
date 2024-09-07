---
layout: page
sidebar: right
subheadline: "Review of interpretability in machine learning"
title: "Interpretability"
teaser: "Inside the black box ..."
header:
    image_fullwidth: "mediaplayer_js-home.jpg"
categories:
  - blog
tags:
  - research, news, deep learning, machine learning, interpretability, fatml
mediaplayer: true
---

Interpretability is a requisite of machine learning systems which allows for an explanation of their decisions or functionality. The machine learning literature does not have a consensus on a definition of interpretability and state of the arts methods evaluate it through proxy characteristics. Fortunately, this topic benefits from two position papers [Doshi-Velez and Kim (2017), Lipton (2016)] which try to formalize it. I will present the main points of these papers. Then, I will discuss interpretability in medicine as a strictly-regulated field, and the potential for confirmation bias in personalized explanations.

## Position papers


There are two main position papers on the topic of interpretability:


Doshi-Velez, F., & Kim, B. (2017). Towards A Rigorous Science of Interpretable Machine Learning, (Ml), 1–13. [pdf][1]


<video width="640" height="360" id="player1" preload="none">
  <source type="video/youtube" src="https://www.youtube.com/embed/bQfYRcXc9F0" />
</video>


Lipton, Z. C. (2016). The Mythos of Model Interpretability, (Whi). [pdf][2]



Because the literature on interpretability comes with different definitions and ways of evaluating it, both of these position papers underline the need to formalize this term.



## Why do we need interpretability:

* Scientific understanding -> We need to gain knowledge about a topic. Often we are not solely interested in a method’s accuracy, but also in its informativeness.
* Safety -> We want to make sure that an AI system is robust to domain mismatch (e.g. a medical AI which works in a different hospital than where it was design which has a different prevalence of a disease), adversarial attacks (through AI generated examples from which a given AI system can learn erroneous decision boundaries, or which can manipulate the decision boundaries of the AI system), errors in training data (we want to detect potential biases in training data)
* Ethics -> We want to ensure that the algorithms are fair and do not discriminate
* Mismatch objectives -> ML models usually learn by minimizing a loss function. In many cases it is difficult to translate interpretability in such a function, resulting in an opaque model.


Often, interpretability comes as a proxy to various characteristics we seek in a machine learning models. These are the auxiliary or complementary characteristics, which might compete with each other are:

* Fairness, un-biasness - we do not want our algorithm to discriminate. For evaluating fairness we have formal criteria; [pdf][3]
* Privacy - we want our algorithm to protect the privacy of the data it learns from. This has formal evaluation criteria. [pdf][4]
* Reliability - do we trust our algorithm to be robust in any real-life test scenario? Does it generalize well? Is it vulnerable to adversarial attacks (e.g. AI generated examples which manipulate the decision of another AI)
* Causality - the associations learned reflect true causes rather than spurious correlations.
* Trust - algorithms which are right for the right reasons. We can correctly predict the decision boundaries of the system and check where it will go wrong.

Unfortunately, reliability, causality and trust do not have a formal criteria, can’t be enforced explicitly through a mathematical equation or included within a cost function.

## Evaluation taxonomy:

* Application-grounded evaluation: in this scenario we have real humans, real tasks e.g. medical imaging -> We are interested in asking questions on the quality of explanation: does it better identify errors, new facts, discrimination
* Human-grounded evaluation: real humans, simplified tasks -> We are interested in studying what kinds of explanations are better
* Functionally-grounded evaluation: no humans, proxy tasks -> We can only do these experiments after human-grounded of application grounded evaluation, once we have a model of that
Doshi-Velez and Kim (2017) recommend human produced explanations as a baseline. I am not sure whether this results in confirmation bias. Check the last section of this document.

## Interpretability hypotheses:

* Global vs local: what are the most relevant features for a particular class vs why has this particular example/data point been classified as an instance of this particular class
* Area, severity of incompleteness: what part of the problem is incomplete and to what extent? E.g. safety in self-driving cars vs sensors that cause the car to drive off the road by 10cm
* Time constraints/user cost: how long can the user afford to spend to understand the explanation? What is the cost of an explanation? A personal credit system should be more interpretable than musical recommendation system?
* Nature of the user expertise: sets the level of sophistication of the explanation: decision makers, researchers, expert users, users, safety engineers, data scientists


## Properties of interpretable models:

* Simulatabilty: the model can be contemplated at once e.g. small linear models
* Decomposability: each parameter and input feature can be interpreted Algorithmic transparency: linear model vs deep learning
* Post-hoc interpretability: text, image, local explanations, explanation by example

## Existing methods/frameworks
### (Post-hoc) Interpretability frameworks


[LIME][5] -  local+global explanations, evaluating trust, proxy to detect bias, robustness, can evaluate a multitude of models


Ribeiro, M. T., Singh, S., & Guestrin, C. (2016). “Why Should I Trust You?”: Explaining the Predictions of Any Classifier. [pdf][6]


<video width="640" height="360" id="player1" preload="none">
  <source type="video/youtube" src="https://www.youtube.com/embed/KP7-JtFMLo4" />
</video>

[GRADCAM][7] - local explanations, evaluating reliability/trust, can evaluate convolutional neural networks


Selvaraju, R. R., Cogswell, M., Das, A., Vedantam, R., Parikh, D., & Batra, D. (2017). Grad-CAM: Visual Explanations from Deep Networks via Gradient-Based Localization. Proceedings of the IEEE International Conference on Computer Vision, 2017–Octob, 618–626. [pdf][8]



[LRP][9] - local explanations, evaluating relevant features, can evaluate neural networks


Montavon, G., Samek, W., & Müller, K. R. (2018). Methods for interpreting and understanding deep neural networks. Digital Signal Processing: A Review Journal, 73, 1–15. [pdf][10]



[DeepLIFT][11] - local explanations, counterfactual,  can evaluate neural networks



Shrikumar, A., Greenside, P., & Kundaje, A. (2017). Learning Important Features Through Propagating Activation Differences. [pdf][12]


<video width="640" height="360" id="player1" preload="none">
  <source type="video/youtube" src="https://www.youtube.com/embed/v8cxYjNZAXc" />
</video>


[Network Dissection][13] - local explanations, model interpretability, interpretability = alignment with semantic concepts, can evaluate convolutional neural networks



Bau, D., Zhou, B., Khosla, A., Oliva, A., & Torralba, A. (2017). Network Dissection: Quantifying Interpretability of Deep Visual Representations. [pdf][14]


[Influence functions][15] - local explanations, counterfactual, can evaluate a multitude of models



Koh, P. W., & Liang, P. (2017). Understanding Black-box Predictions via Influence Functions. [pdf][16]

<video width="640" height="360" id="player1" preload="none">
  <source type="video/youtube" src="https://www.youtube.com/embed/0w9fLX_T6tY" />
</video>
s

[RRR][17] - local and global explanation, can evaluate gradient-based methods - neural networks


Ross, A. S., Hughes, M. C., & Doshi-Velez, F. (2017). Right for the right reasons: Training differentiable models by constraining their explanations. IJCAI International Joint Conference on Artificial Intelligence, 2662–2670. [pdf][18]

<video width="640" height="360" id="player1" preload="none">
  <source type="video/youtube" src="https://www.youtube.com/embed/MMxZlr_L6YE" />
</video>


### Collections of methods:

* [DeepExplain][19]

* [Themis][20]

* [IMLP][21]



## Strictly-regulated fields: medical AI


Interpretation is highly valued in strictly-regulated fields such as medicine. Rather than aiming at an end-to-end solution where the machine learning algorithm gives a diagnostic, ideally replacing the doctor, the medicine AI target sub-tasks which can assist doctors in making a more informed decision or help them become more efficient by filtering some true-positives or false negatives. By targeting sub-tasks the medical AI works at a lower semantical level which makes them more interpretable.



Due to complex interactions within data which might yield biases or spurious correlations, doctors favour a more interpretable machine learning method as linear regression, although its performance is not as high as the deep learning methods. One example here:



Caruana, R., Lou, Y., Gehrke, J., Koch, P., Sturm, M., & Elhadad, N. (2015). Intelligible Models for HealthCare. Proceedings of the 21th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining - KDD ’15, 1721–1730. [pdf][22]

Some medical AI research suffer has the same issues present in the whole AI field: exaggerated claims (e.g. claiming to solve a task but solving solely a proxy sub-task), small datasets, evaluation issues. Particularly in medicine where the diseases are rare, taking into account prevalence helps assessing the robustness of a [system][23].



However, in 2017 we had a few breakthroughs in medical AI:



* Gulshan, V., Peng, L., Coram, M., Stumpe, M. C., Wu, D., Narayanaswamy, A., … Webster, D. R. (2016). Development and validation of a deep learning algorithm for detection of diabetic retinopathy in retinal fundus photographs. JAMA - Journal of the American Medical Association, 316(22), 2402–2410. [pdf][24]

* Salehinejad, H., Valaee, S., Mnatzakanian, A., Dowdell, T., Barfett, J., & Colak, E. (2017). Interpretation of Mammogram and Chest X-Ray Reports Using Deep Neural Networks - Preliminary Results. [pdf][25]

* Merkow, J., Lufkin, R., Nguyen, K., Soatto, S., Tu, Z., & Vedaldi, A. (2017). DeepRadiologyNet: Radiologist Level Pathology Detection in CT Head Images, 1–22. [pdf][26]



These papers propose large datasets and a solid evaluation which assumes a ROC sensitivity/specificity and a comparison with doctors. In contrast to other AI (e.g. self driving cars, recommendation systems), none of these medical AI has been implemented in hospitals as medical solutions.



## Potential for confirmation bias in personalized explanations


People express greater confidence in a hypothesis, although false, when asked to generate explanations for it.



Koehler, D. J. (1991). Explanation, imagination, and confidence in judgment. Psychological Bulletin, 110(3), 499–519. [pdf][27]



Explanations:
* Constrain inference by excluding possibilities inconsistent with current beliefs
* Guide generalization


Explanations override:
* Similarity
* Diversity


Lombrozo, T. (2006). The structure and function of explanations. Trends in Cognitive Sciences, 10(10), 464–470. [pdf][28]



Explanations can be used to manipulate people’s decisions or to facilitate learning:


Baumeister, R. F., & Newman, L. S. (1994). Self-Regulation of Cognitive Inference and Decision Processes. Personality and Social Psychology Bulletin, 20(1), 3–19. [pdf][29]



Interpretability in machine learning advocates for human-centric explanations of black-box models. In simple tasks, the explanation is straightforward, for instance emphasizing the pixels corresponding to a detected object in an image. For other tasks which require slow judgements, a personalized explanation might enforce one’s confirmation biases, e.g. in topic detection a personalized interpretation underlines the words might point to one’s vocabulary. Therefore, in certain slow judgement tasks human-centric explanations as evaluation baselines for interpretability can be biased towards certain individuals.


 [1]: https://arxiv.org/abs/1702.08608
 [2]: https://arxiv.org/abs/1606.03490
 [3]: https://arxiv.org/abs/1610.02413
 [4]: https://arxiv.org/abs/0907.3754
 [5]: https://github.com/marcotcr/lime
 [6]: https://doi.org/10.1145/1235
 [7]: https://github.com/ramprs/grad-cam
 [8]: https://doi.org/10.1109/ICCV.2017.74
 [9]: https://www.heatmapping.org/
 [10]: https://doi.org/10.1016/j.dsp.2017.10.011
 [11]: https://github.com/kundajelab/deeplift
 [12]: https://arxiv.org/abs/1704.02685
 [13]: https://github.com/CSAILVision/NetDissect
 [14]: https://doi.org/10.1109/CVPR.2017.354
 [15]: https://github.com/kohpangwei/influence-release
 [16]: https://arxiv.org/abs/1703.04730
 [17]: https://github.com/dtak/rrr
 [18]: https://doi.org/10.24963/ijcai.2017/371
 [19]: https://github.com/marcoancona/DeepExplain
 [20]: https://github.com/LASER-UMASS/Themis
 [21]: https://github.com/jphall663/interpretable_machine_learning_with_python
 [22]: https://doi.org/10.1145/2783258.2788613
 [23]: https://spectrumnews.org/opinion/viewpoint/quest-autism-biomarkers-faces-steep-statistical-challenges/
 [24]: https://doi.org/10.1001/jama.2016.17216
 [25]: https://arxiv.org/abs/1708.09254
 [26]: https://arxiv.org/abs/1711.09313
 [27]: https://doi.org/10.1037//0033-2909.110.3.499
 [28]: https://doi.org/10.1016/j.tics.2006.08.004
 [29]: https://doi.org/10.1177/0146167294201001

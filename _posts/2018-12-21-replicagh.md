---
layout: post
title: "Continuous Vector Representations for Source Code"
author: "Achyudh Ram"
---

Over the last few years, there has been a lot of effort to create a continuous higher dimensional vector space representation of words, sentences, and even documents such that similar entities are closer to each other in that space. Such learned distributed representation of words alleviate the curse of dimensionality, and have consequently accelerated the application of deep learning techniques for natural language processing (NLP) tasks.
Drawing parallels with the recent history of NLP research, developing pre-trained code embeddings would considerably accelerate and ease the research process of solving software problems with deep learning. Some initial work in this direction has already been published. Alon et al. [1] proposed code2vec, a path-attention network that learns how to aggregate context vectors representing a code snippet as bag of contexts, in a weighted manner. However, the paper doesn't extensively evaluate how the embeddings perform on various downstream tasks. They evaluate their embeddings by predicting an unseen method's name from the vector representation of its body, which was how they learnt the code vectors in the first place! This doesn't offer much information on how these embeddings generalize to other downstream tasks such as semantic code clone detection, code captioning and code completion.

![The architecture of the path attention network](/public/path_attention.png)

However, there are a number of other drawbacks with code2vec due to which I feel that further research in this domain is required. Mikolov et al. [2] introduced the now popular word2vec for learning distributed vector representations for natural language. Their method can be used to re-train for languages other than English (provided the language can be tokenized) and for domain specialization, by just replacing the data, without any changes to the model or the methodology. In order to re-train code2vec on a new language, a new parser and an extractor needs to be implemented to extract paths from the abstract syntax tree (AST) specific to that language. Learning vector representations directly from source code would be considerably easier to scale across many languages.

Building multilingual code embeddings, analogous to MUSE from Facebook Research for natural languages [3], would allow researchers to develop models that automatically scale across multiple languages. This would open up further avenues for research, such as developing sequence-to-sequence models for converting code from one programming language into a common higher dimensional concept space and translating the higher dimensional representations to another language of choice.

> _Research on continuous vector representations for code could be a first step towards achieving true semantic code clone detection across multiple languages._

A reflection on the current state of labelled datasets in SE (or the lack thereof) throws light on limited practicality of deep learning models for certain software engineering tasks. While creating larger ground-truth datasets would always be helpful, it might not be possible given the time and budget constraints in academia. The ongoing research on pre-trained code embeddings that don't require a labelled dataset to train is a step in the right direction.


### References
<div class="references"> <p>
[1] Alon, Uri, et al. "code2vec: Learning Distributed Representations of Code." arXiv preprint arXiv:1803.09473(2018).  <br>

[2] Mikolov, Tomas, et al. "Efficient estimation of word representations in vector space." arXiv preprint arXiv:1301.3781 (2013).  <br>

[3] Conneau, Alexis, et al. "Word translation without parallel data." arXiv preprint arXiv:1710.04087 (2017).
</p></div>

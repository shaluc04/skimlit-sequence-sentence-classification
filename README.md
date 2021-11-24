## skimlit-sequence-sentence-classification


### What is Natural Language Processing?

NLP is a subfield of artificial intelligence that helps machines understand natural human language.

There are various applications of NLP ranging from sentiment analysis, machine translation to chatbots and virtual assistants and many more. One such useful application has been discussed in the 2017 paper : [PubMed 200k RCT: a Dataset for Sequenctial Sentence Classification in Medical Abstracts](https://arxiv.org/abs/1710.06071).

The paper presented a new dataset called **PubMed 200k RCT** which consists of ~200,000 labelled Randomized Controlled Trial (RCT) abstracts. *The goal of the dataset was to explore the ability for NLP models to classify sentences which appear in sequential order.* 

In this repo, I try to replicate the deep learning model behind the above paper. This notebook builds an end-to-end multi-class classifier using TensorFlow 2.0 and TensorFlow hub.

#### Problem
> Increasing release of RCT papers with unstructured abstracts has become harder to read and comprehend. It consumes a lot of time and has slowed down researchers moving through the literature.

#### Objective
> Create an NLP model to classify abstract sentences into categories as per thier role (e.g. objective, methods, results, etc) to enable researchers to skim through the literature efficiently.

#### Data
* Dataset has been provided in [PubMed 200k RCT: a Dataset for Sequenctial Sentence Classification in Medical Abstracts](https://arxiv.org/abs/1710.06071).
* It is available on author's github: [PubMed RCT200k from GitHub](https://github.com/Franck-Dernoncourt/pubmed-rct)
* The dataset consists of approximately 200,000 abstracts of randomized controlled trials, totaling 2.3 million sentences. Each sentence of each abstract is labeled with their role in the abstract using one of the following classes: **background, objective, method, result, or conclusion**.
* PubMed 20k is a subset of PubMed 200k. I.e., any abstract present in PubMed 20k is also present in PubMed 200k.
* `PubMed_200k_RCT` is the same as `PubMed_200k_RCT_numbers_replaced_with_at_sign`, except that in the latter all numbers had been replaced by `@`. (same for `PubMed_20k_RCT` vs. `PubMed_20k_RCT_numbers_replaced_with_at_sign`).

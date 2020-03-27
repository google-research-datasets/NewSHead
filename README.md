# NewSHead
This repository contains the raw dataset used in NHNet [[1]](#1) for the task of **News S**tory **Head**line Generation. The code of data processing and training will soon be released under [Tensorflow Models](https://github.com/tensorflow/models/tree/master/official/nlp).

A news story is defined as a list of articles about the same event with a coherent topic. The released dataset contains 369,940 such stories with 932,571 unique URLs. Each news story contains at least three (and up to five) articles. 

The dataset is collected from news stories published between May 2018 and May 2019, where a proprietary clustering algorithm iteratively loads articles published in a time window and groups them based on content similarity<sup id="a1">[1](#f1)</sup>. Up to five representative articles are picked from the cluster for generating the story headline<sup id="a1">[2](#f2)</sup>. Curators from a crowd-sourcing platform are requested to provide a headline of up to 35 characters to describe the major information covered by the story. 

Example Headlines:

* International Space Station flyover
* Drilling for oil in Pakistan
* Review of 'Mr. Local'
* MLB: Pirates vs Padres


## References

<a id="1">[1]</a> Xiaotao Gu, Yuning Mao, Jiawei Han, Jialu Liu, Hongkun Yu, You Wu, Cong
Yu, Daniel Finnie, Jiaqi Zhai and Nicholas Zukoski "Generating
Representative Headlines for News Stories": https://arxiv.org/abs/2001.09386.
World Wide Web Conf. (WWW’2020).

## Footnote
<b id="f1">1</b> Clustering algorithm could contain noise. It is possible if some articles in a story are not relevant to the rest.

<b id="f2">2</b> These articles presented don't necessarily map to articles we would show on Google products such as Search and News App.

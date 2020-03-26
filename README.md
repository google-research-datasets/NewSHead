# NewSHead
This repository contains the raw dataset used in NHNet [[1]](#1) for the task of **News S**tory **Head**line Generation. The code related to data processing and training will soon be released under [Tensorflow Models](https://github.com/tensorflow/models/tree/master/official/nlp).

A news story is a cluster of news articles regarding the same event. The NewSHead dataset contains 369,940 such stories with 932,571 unique URLs. Each news story contains three to five relevant articles, and curators from a crowd-sourcing platform are requested to provide a headline of up to 35 characters to describe the major information covered by the story. 

This dataset is collected from news stories published between May 2018 and May 2019, where a proprietary clustering algorithm iteratively loads articles published in a time window and groups them based on content similarity <sup id="a1">[1](#f1)</sup>. Up to five representative articles are picked from the cluster for generating the story headline <sup id="a1">[2](#f2)</sup>.


## References

<a id="1">[1]</a> Xiaotao Gu, Yuning Mao, Jiawei Han, Jialu Liu, You Wu, Cong
Yu, Daniel Finnie, Hongkun Yu, Jiaqi Zhai and Nicholas Zukoski "Generating
Representative Headlines for News Stories": https://arxiv.org/abs/2001.09386.
World Wide Web Conf. (WWW’2020).

## Footnote
<b id="f1">1</b> Clustering algorithm could contain noise. It is possible if some articles in a story are not relevant to the rest.

<b id="f2">2</b> These articles presented don't necessarily map to articles we would show on Google products such as Search and News App.

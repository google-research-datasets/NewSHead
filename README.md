# NewSHead
This repository contains the raw dataset used in NHNet [[1]](#1) for the task of **News S**tory **Head**line Generation. The code of data processing and training is available under [Tensorflow Models - NHNet](https://github.com/tensorflow/models/tree/master/official/projects/nhnet).

A news story is defined as a list of articles about the same event with a coherent topic. The released dataset contains 369,940 *English* stories with 932,571 unique URLs, among which we have 359,940 stories for training, 5,000 for validation, and 5,000 for testing, respectively. Each news story contains at least three (and up to five) articles.

The dataset is collected from news stories published between May 2018 and May 2019, where a proprietary clustering algorithm iteratively loads articles published in a time window and groups them based on content similarity<sup id="a1">[1](#f1)</sup>. Up to five representative articles are picked from the cluster for generating the story headline<sup id="a1">[2](#f2)</sup>. Curators from a crowd-sourcing platform are requested to provide a headline of up to 35 characters to describe the major information covered by the story. 

Example Headlines:

* International Space Station flyover
* Drilling for oil in Pakistan
* Review of 'Mr. Local'
* MLB: Pirates vs Padres
* Braves re-sign Jerry Blevins

**[Download Link](https://github.com/google-research-datasets/NewSHead/releases/tag/v1.0)**

**[Tools to Process](https://github.com/tensorflow/models/tree/master/official/projects/nhnet#dataset)**

# Citation
If you use or discuss this dataset in your work, please cite our [paper](https://arxiv.org/abs/2001.09386):
```
@InProceedings{headline2020,
  title = {{Generating Representative Headlines for News Stories}},
  author = {Gu, Xiaotao and Mao, Yuning and Han, Jiawei and Liu, Jialu and Yu, Hongkun and Wu, You and Yu, Cong
and Finnie, Daniel and Zhai, Jiaqi and Zukoski, Nicholas},
  booktitle = {Proc. of the the Web Conf. 2020},
  year = {2020}
}
```

# Analysis
We did broad topic analysis for the 932,571 articles in our dataset. A histogram is attached as below.
<p align="center">
<img src="/images/article_topic_distribution.png" width="450">
</p>

Among all the 369,940 stories, each headline is required to be between 10 and 35 characters.
<p align="center">
<img src="/images/story_headline_length.png" width="400">
</p>

Such lengths of curated story headlines are much shorter than traditional summaries, and even shorter than
article titles in our dataset depicted below
<p align="center">
<img src="/images/article_title_length.png" width="400">
</p>

## References

<a id="1">[1]</a> Xiaotao Gu, Yuning Mao, Jiawei Han, Jialu Liu, Hongkun Yu, You Wu, Cong
Yu, Daniel Finnie, Jiaqi Zhai and Nicholas Zukoski "Generating
Representative Headlines for News Stories": https://arxiv.org/abs/2001.09386.
World Wide Web Conf. (WWW’2020).

## Footnote
<b id="f1">1</b> Clustering algorithm could contain noise. It is possible if some articles in a story are not relevant to the rest.

<b id="f2">2</b> These articles presented don't necessarily map to articles we would show on Google products such as Search and News App.

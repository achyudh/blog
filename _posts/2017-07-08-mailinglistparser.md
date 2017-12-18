---
layout: post
title: "Bringing Network Analysis to Software Engineering"
author: "Achyudh Ram"
---

An undergraduate student's first research project would always have a special place in his or her mind. I was super excited to work on a 'real' project, and had no idea of the amount of trial and error would ensue. A year back, right after completing a semester of courses in Computer Science, I approached [Prasad Talasila](http://prasad.talasila.in/about/) from the Networks Group at BITS Pilani, to work on the [Mailing List Network Analyzer](https://github.com/achyudhk/Mailing-List-Network-Analyzer) project. It was a part of a larger study on an analysis framework for decoding online developer communities. One of the objectives was to guide contributors to open-source projects towards core members best suited to answering a specic query or reviewing a patch, by labelling communities and identifying topic experts using the latent structures in mailing lists. This project draws its inspiration from various fields such as data mining, graph theory, information retrieval and inferential modelling in order to form predictive models that help in understanding certain intricate characteristics of a social network.

The field of social network analysis, one of the major paradigms in contemporary sociology, involves analyzing the observed entities, dynamics and patterns in a social structure. By modelling the social structure of the social actors (such as authors, groups or organizations) in online developer communities, and their interactions between these actors, we can derive the local and global communication patterns between users on different threads. 

![Infomap Vertex Clustering](https://raw.githubusercontent.com/prasadtalasila/MailingListParser/master/data/lkml/graphs/vertex_clustering_infomap.png)

I frequently ran out of computational resources due to the time and space complexities of certain graph algorithms, especially motif detection. I had to resort to hacks such as caching intermediate results on the hard disk, or segmenting the problem into multiple chunks for individual execution (the astute reader might notice that this may not always lead to optimal results). The fun part was writing algorithms to merge them later. Consequently, I developed an interest in learning how to build scalable distributed systems and this led to a collaboration with IBM Research, which I'll talk about in another post. Not only did working on this project enable me to view software engineering from a social networks standpoint, it started a chain reaction that allowed me to work on a number of fields in Computer Science.

Even though I will be leaving for TU Delft to work on my thesis in August, I will remain the sole maintainer of the Mailing-List-Network-Analyzer code base. I am currently helping with the on-boarding of sophomore and junior students to this project. I believe that the future of this project lies in the hands of these students and I might have to provide them with a sense of direction in which to proceed. I will make it a priority to review each contribution made to this project and provide constructive feedback. 

Since I have no idea how to conclude, here is a cool set of outdated graphs I generated a long time ago for a publication draft of this study.

![Infomap Vertex Clustering](https://raw.githubusercontent.com/achyudhk/Mailing-List-Network-Analyzer/development/data/sakai-devel/plots/conversation_chars.png)



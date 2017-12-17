---
layout: post
title: "Why study the reviewability of code changes?"
author: "Achyudh Ram"
---

_Peer code review_ is a practice adopted widely in the industry to reduce defects in code and to improve the quality of software. Peer code review has been verified to contribute to a significant reduction in the occurrence of defects, at a lower cost compared to testing. _Pull-based development_, a model of distributed software development, allows the distribution of the development of code artifacts from their integration into the code repository. A popular implementation of this model is GitHub's [pull request](https://help.github.com/articles/about-pull-requests/). By combining various aspects of pull-based development and modern code review, GitHub has made it easier to receive and review contributions. 

In the [Software Engineering Research Group](http://swerl.tudelft.nl/bin/view/Main/WebHome>") at TU Delft, I set out to find out what contributes to the “reviewability” of pull requests submitted to open source projects. Reviewability can broadly be defined as the ease with which a code change can be reviewed, conditional to the assumption that there are no technical effects in the code. In this post, I wanted to explain why there is a need for research in this field and how you can contribute to our study

Existing work on code review focuses only on factors pertaining to the merge decision of a patch or time taken for its evaluation, and not on the effectiveness and ease of the code review process. Even though a set of factors exist that affect either the merge decision or the evaluation time due to an effect on the reviewability of the code change, 

Various studies have shown that reviewers prefer to review code changes that are simple, readable and easy to comprehend. Further, managing time is the greatest challenge for integrators when working with the pull-based development model due to the open nature of submitting contributions [4]. The amount of time reviewers spend on reviewing contributions and understanding code changes could be improved with a framework that can guide contributors to write reviewable patches. By helping both reviewers and contributors save time in the code review process, this study can reduce effort in both open-source and industrial projects. There is also less uncertainty when merging simple changes that are less complicated and smaller in scope [5].

## How can you help?
Determining what makes a reviewable pull request has direct implications for contributors and maintainers of OSS projects as it could help in improving the overall reviewability of contributions and therefore reduce the time spent by reviewers. In addition, a study with a purely academic setting may not accurately capture the viewpoint of the developers, and involving practitioners from the industry into the study would enable us to paint a more accurate picture. 

I developed **Propr** to enable reviewers to provide feedback on pull requests reviewability to contributors, and for contributors to gain insights from this feedback using a reports dashboard. You can check it out [here](http://propr.tudelft.nl). To learn more, head on over to [this blog post](http://blog.achyudh.xyz/2017-10-20/propr) where I explain how Propr works and what you get out of it. We don’t store any personal information and all feedback is collected anonymously.

In a study by Gousios et al., more than 15% of the participants mentioned that getting feedback for their pull requests, something that they deem important, is hard and they might get a delayed or no feedback at all [1]. The authors also observe a magnification of this problem due to project size and the lack of guidelines or documentation. The evaluation lifecycle of a submitted patch can take days before a merge decision is made due to the evaluation - revision cycle [2]. Moreover, unreadable patches are more likely to be rejected, requiring further revisions from the author [3]. This study can help contributors by providing guidelines to write reviewable patches, and an automated reviewability evaluation framework, **Improv**, to provide preliminary feedback on their pull requests. 

To assess the validity and the impact of the reviewability themes identified, Improv needs to be deployed in the industry. The feedback that reviewers provide via Propr would help in improving this framework. The development of Improv is still at an early stage and an open-source beta release can be expected in Q1 2018. Watch this space for any updates! 


### References
<div class="references"> <p>
[1] Gousios, Georgios, Margaret-Anne Storey, and Alberto Bacchelli. "Work practices and challenges in pull-based development: The contributor's perspective." Software Engineering (ICSE), 2016 IEEE/ACM 38th International Conference on. IEEE, 2016. <br>

[2] Baysal, Olga, et al. "The secret life of patches: A firefox case study." Reverse Engineering (WCRE), 2012 19th Working Conference on. IEEE, 2012. <br>

[3] Tao, Yida, DongGyun Han, and Sunghun Kim. "Writing acceptable patches: An empirical study of open source project patches." Software Maintenance and Evolution (ICSME), 2014 IEEE International Conference on. IEEE, 2014. <br>

[4] Gousios, Georgios, et al. "Work practices and challenges in pull-based development: the integrator's perspective." Proceedings of the 37th International Conference on Software Engineering-Volume 1. IEEE Press, 2015. <br>

[5] Marlow, Jennifer, Laura Dabbish, and Jim Herbsleb. "Impression formation in online peer production: activity traces and personal profiles in github." Proceedings of the 2013 conference on Computer supported cooperative work. ACM, 2013.
</p></div>

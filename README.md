# Community Detection Survey 

## Introduction
The repository collects and refactors some overlapping Community detection algorithms. Major content is survey, algorithms' implementations, 
graph input benchmarks, submodules, scripts.

Recommend ide are from jetbrains, namely clion, pycharm and intellij for c++, python and java.

Some Non-Overlapping Community Detections Algorithms could be found in [NonOverlappingCodes](NonOverlappingCodes).

A community-detection survey in [Survey](Survey), you can have a look, if interested. 

## Graph Benchmarks

### Synthetic Tool

Content | Detail | Status
--- | --- | ---
[2009-LFR-Benchmark](Benchmark/2009-LFR-Benchmark) | LFR Benchmark to generate five types of graphs | build success, some files unused

### Real-World DataSets(Edge List)

Detailed information is in [Datasets](Datasets).

Newly occurring useful links(Websites for downloading)

* http://networkrepository.com/soc.php
* http://konect.uni-koblenz.de/
* http://law.di.unimi.it/datasets.php

Old links

* http://vlado.fmf.uni-lj.si/pub/networks/data/
* https://snap.stanford.edu/data/

## Quality-Evaluation Metrics
### Without-Ground-Truth

Evaluation Metric Name | Implementation | Heuristic
--- | --- | ---
Link-Belonging-Based Modularity | [link_belong_modularity.py](Metrics/metrics/link_belong_modularity.py) | compare to random graph

### With-Ground-Truth

Evaluation Metric Name | Implementation | Heuristic
--- | --- | ---
Overlap-NMI | [overlap_nmi.py](Metrics/metrics/overlap_nmi.py) | info-theory entropy-measure
Omega-Idx | [omega_idx.py](Metrics/metrics/omega_idx.py) | unadjusted compared to expected

## Algorithms

In each algorithm, there is a `ReadMe.md`, which gives brief introduction of corresponding information of the algorithm and 
current refactoring status. Category information are extracted, 
based on Xie's 2013 Survey paper [Overlapping Community Detection in Networks: The State-of-the-Art
and Comparative Study](http://dl.acm.org/citation.cfm?id=2501657).

All c++ projects are built with `cmake`, java projects are built with `maven`, python projects 
are not specified how to build. 

Algorithm | Category | Language | Dependency | Status
--- | --- | --- | --- | ---
[2008-CPM](Algorithms/2008-CliquePercolation) | clique percolation | c++, python | [lcelib](https://github.com/CxAalto/lcelib) | build success
[2009-CIS](Algorithms/2009-Connected-Iterative-Scan) | seed expansion | c++ |  | build success
[2009-EAGLE](Algorithms/2009-EAGLE) | seed expansion | c++ | [igraph](https://github.com/igraph/igraph), boost | build success
[2010-LinkComm](Algorithms/2010-LinkCommunity) | link partition | python| optparse | python okay
[2010-iLCD](Algorithms/2010-iLCD) | seed expansion | java | args4j, trove4j | build success
[2010-CONGA](Algorithms/2010-CONGA) | dynamics | java | | build success
[2010-TopGC](Algorithms/2010-TopGC) | statistical inference | java | | build success
[2011-GCE](Algorithms/2011-GCE) | seed expansion | c++ | boost | build success
[2011-OSLOM](Algorithms/2011-OSLOM-v2) | seed expansion | c++ |  |
[2011-MOSES](Algorithms/2011-MOSES) | fuzzy detection | c++ | boost | build success
[2011-SLPA](Algorithms/2011-SLPA) | dynamics | c++, java, python | networkx, numpy | build success for java
[2012-FastCPM](Algorithms/2012-Fast-Clique-Percolation) | clique percolation | python, c++ | networkx | build success
[2012-ParCPM](Algorithms/2012-CPMOnSteroids) | clique percolation | c | [igraph](https://github.com/igraph/igraph) | build success
[2012-DEMON](Algorithms/2012-DEMON) | seed expansion | python | networkx | python okay
[2013-SVINET](Algorithms/2013-SVINET) | statistical inference | c++ | gsl, pthread | build success
[2013-SeedExpansion](Algorithms/2013-Seed-Set-Expansion) | page-rank | c++, matlab | [graclus](https://github.com/GraphProcessor/Graclus), [matlab-bgl](https://github.com/dgleich/matlab-bgl) | 
[2014-HRGrow](Algorithms/2014-Heat-Kernel) | matrix-exponential | c++, matlab, python | pylibbvg | python okay
[2015/2018-LEMON](Algorithms/2015-LEMON) | seed expansion | python | pulp | python okay
[2017-multicom](Algorithm/2017-multicom) | seed expansion | python | pandas | 
[2018/2019-loglike](Algorithm/2018-loglike) |[statistical inference](https://github.com/altsoph/community_loglike)| python | | 
[2018-LARC](Algorithm/2018-LARC)|[tensor-based method](http://www.cs.albany.edu/~petko/lab/code.html)| Matlab | | 
[2019-ncd](Algorithm/2019-ncd) | [Graph Neural Networks](https://github.com/shchur/overlapping-community-detection) | python | pytorch | 
2019-locd | [seed expansion](https://dl.acm.org/doi/pdf/10.1145/3361739) | do not open source| | 
[2019-CommunityGAN](Algorithm/2019-CommunityGAN) |[Generative Adversarial Nets](https://github.com/SamJia/CommunityGAN)|python||
2020-medof |[fuzzy detection](https://dl.acm.org/doi/pdf/10.1145/3313374)| do not open source| | 
2020-Fox |[dynamics](https://dl.acm.org/doi/pdf/10.1145/3404970)| do not open source||
[2020-RWM](Algorithm/2020-RWM)|[random walk](https://github.com/flyingdoog/RWM/)| c++ | | 






## Presentation Files

[survey-presentation-slides-yche.pdf](Prensentation/survey-presentation-slides-yche.pdf) is available.

Some files for my survey presentation is in [Presentation](Prensentation), including algorithm visualization scripts, 
graph serialization related scripts and social network visualization scripts and corresponding figures. 

## Submodules(Dependencies)

Detailed information is in [SubModules](SubModules).

Submodule | Implementation Language | Detail
--- | --- | ---
[igraph](https://github.com/igraph/igraph) | c | also provide python wrapper, graph utilities 
[matlab-bgl](https://github.com/dgleich/matlab-bgl) | c++, matlab | [matlab implementation with bgl dependency](http://dgleich.github.io/matlab-bgl/)
[graclus](https://github.com/GraphProcessor/Graclus) | c++ | graph partition algorithm
[lcelib](https://github.com/CxAalto/lcelib) | c++ | graph utilities by [CxAalto](http://complex.cs.aalto.fi/)

## Scripts

Some file processing utility python scripts are put in [Scripts](Scripts).

## Attention
These codes are all research codes, which I found through the internet. Please do not use them in production environment.

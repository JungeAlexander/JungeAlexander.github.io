---
layout: page
title: projects
description: Website created by Alexander Junge with GitHub Pages
---

- [Current projects](#curr)
- [Previous projects](#prev)
- [Pet projects](#pet)

# <a name="curr">Current projects</a>

# <a name="prev">Previous projects</a>

## Active transitivity clustering

In my Master's thesis project, I worked on an active clustering approach to
[transitivity clustering](http://transclust.compbio.sdu.dk/main_page/index.php).
Clustering of large data sets is hampered by a) storing the quadratic pairwise
similarity matrix in main memory, and b) evaluating a potentially costly
similarity function for each pair of objects.
Active transitivity clustering circumvents both problems by *actively* deciding
which pairwise similarities to compute and
updating the clustering on the fly as new information becomes available.
This saves both runtime and memory.
The key workflow in active clustering is illustrated in the following flowchart:

![active_clustering]({{BASE_PATH}}/assets/projects/active_clustering.png)

I worked on this project in the [research group](http://www.baumbachlab.net/)
of Jan Baumbach at the [University of Southern Denmark](http://imada.sdu.dk/)
and formerly the
[Max-Planck Institute for Informatics](https://www.mpi-inf.mpg.de/home/).
My thesis advisor was
[Richard Röttger](http://www.imada.sdu.dk/~roettger/main_page/index.php).

## KeyPathwayMiner

KeyPathwayMiner is a tool to identify parts of a given biological network
that are dysregulated in a disease or condition of interest.
We employ heuristic (ant colony optimization) and exact approaches to solve the
underlying combinatorial optimization problem.

I contributed to the development of the
KeyPathwayMiner 4.0 [Cytoscape](http://cytoscape.org/) App with a focus on
designing the graphical user interface.
The publication is [here](dx.doi.org/10.1186/s12918-014-0099-x).
A sample of the KeyPathwayMiner 4.0 user interface is displayed below:

![kpm_user_interface]({{BASE_PATH}}/assets/projects/kpm.png)

For more information about the project, please visit the KeyPathwayMiner
website here:
[http://tomcat.compbio.sdu.dk/keypathwayminer/](http://tomcat.compbio.sdu.dk/keypathwayminer/)

## Integrative clustering of cancer data

In my Bachelor's thesis project, I identified tumor subtypes in data from
[The Cancer Genome Atlas](https://tcga-data.nci.nih.gov/tcga/) based on
genomic, epigenomic, and transcriptomic features using an integrative K-medoids
clustering approach. Sample counts for each data type and their overlap is
depicted in the following Venn diagram.

![tcga_venn]({{BASE_PATH}}/assets/projects/tcga_venn.png)

The project covered a total of seven cancer types.
The four resulting clusters/subtypes of breast invasive carcinoma
displayed differential promoter DNA methylation and gene expression levels of
the BRCA2 tumor-suppressor gene. Two of the Glioblastoma multiforme
(an aggressive form of brain cancer) subtypes included an enriched number of
tumor samples harboring TP53 mutations.

I worked on this project in the [research group](http://www.baumbachlab.net/)
of Thomas Lengauer at the
[Max-Planck Institute for Informatics](https://www.mpi-inf.mpg.de/home/).
My thesis advisors were
[Yassen Assenov](https://bioinf.mpi-inf.mpg.de/homepage/index.php?&account=yassen)
and
[Fabian Müller](https://bioinf.mpi-inf.mpg.de/homepage/index.php?&account=fmueller).

# <a name="pet">Pet projects</a>

## Quantified self

Since early 2016, I am tracking my activity (step count, heart rate, sleep
duration, and more).
I wrote two blog posts,
[1]({{BASE_PATH}}/2016/03/19/fitbit-data-01)
and
[2]({{BASE_PATH}}/2016/03/28/fitbit-data-02/),
about downloading, cleaning and visualizing these data.
For instance, the following graph depicts the rolling mean of my daily step
count over time.

![steps data]({{BASE_PATH}}/assets/posts/2016-03-28/steps.png)

Inspired by [Bastian Greshake's work](http://ruleofthirds.de/quantifiedself/),
I plan to integrate my activity data with Google Maps location data to see,
for instance, how the weather at my location influences my activity.

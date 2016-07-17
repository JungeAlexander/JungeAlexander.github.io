---
layout: page
title: projects
description: Website created by Alexander Junge with GitHub Pages
---

- [Current projects](#curr)
- [Previous projects](#prev)
- [Pet projects](#pet)

# <a name="curr">Current projects</a>

As part of my PhD at the
[Center for non-coding RNA in Technology and Health (RTH)](http://rth.dk/), University of Copenhagen, Denmark, I work on the
following projects. My thesis supervisor is
[Jan Gorodkin](http://rth.dk/~gorodkin/).

## Integrating RNA and protein interactions

In this project we are developing a database called
[RAIN](http://rth.dk/resources/rain/) (RNA–protein Association and Interaction Networks).
The project goal is to collect RNA--RNA and RNA--protein interactions from a
diverse range of sources: we
a) search interactions by text mining abstracts of millions of
scientific papers,
b) collect experimentally validated interactions of non-coding RNAs from various
databases,
c) predict miRNA--targets using state of the art prediction algorithms,
and d) collect curated knowledge from biological textbooks.
We then integrate these sources of evidence and assign an easily interpretable
confidence score to each interaction.
This integrative scoring allows users to decide whether to trust a given
interaction or not.

The integration of RAIN with the popular [STRING](http://string-db.org/)
database enables us to visualize both RNA and protein interaction networks in a
single, easily accessible user interface.
This project is a collaboration between four research institutes in Denmark
and one in Switzerland.

## Clustering of RNA secondary structures

Besides being translated into proteins, RNA molecules fulfill many biological
functions ranging from the regulation of gene expression to genomic defense
mechanisms.
The secondary structure of RNA molecules is often crucial to their function.
We are developing an approach o identify similar RNA structures in large-scale
data sets thus shedding light on potential functional relationships between
RNAs.
Our approach tries to take RNA secondary structure conserved across species
into account in order to improve the clustering.

This project is a collaboration with the
[Bioinformatics Group](http://www.bioinf.uni-freiburg.de/?en) at the University
of Freiburg, Germany. The project website is available
[here](http://www.bioinf.uni-freiburg.de/Software/RNAscClust/).
Furthermore, a short video (~1 min.) where I talk about our project is available
([link to blog post]({{BASE_PATH}}/2016/07/17/video)). 

## Competitive endogenous RNAs in leukemia

Competitive endogenous RNAs (ceRNAs), also known as miRNA sponges, are
RNA molecules that bind microRNAs thus titrating those microRNAs away from their
normal targets.
This phenomenon leads to a dysregulation of the fine-tuned gene expression
levels in the cell.
ceRNAs have been linked to breast or skin cancer development.
We are researching into the role of miRNA sponges in leukemia.

This project is a collaboration with the The Granulocyte Research Laboratory at
[Rigshospitalet](https://www.rigshospitalet.dk/english/Pages/default.aspx),
the Danish State Hospital.
This close collaboration between experimental and computational biology makes
this project especially interesting to me.

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

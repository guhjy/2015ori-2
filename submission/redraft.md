---
title: 'Understanding data fabrication: Qualitative Comparative Analysis (QCA) of
fabrication strategies'
author: "CHJ Hartgerink"
date: '`r format(Sys.time(), "%d %B, %Y")`'
output:
  word_document: default
  pdf_document:
    toc: yes
  html_document:
    toc: yes
    toc_depth: 2
csl: ../bibliography/apa.csl
bibliography: ../bibliography/library.bib
---

```{r, echo = FALSE}
library(QCA)
```

# Introduction 

Cases of data fabrication in research often peak the interest of people in research and beyond, where it speaks to the imagination to understand why, what, or how data were fabricated. 
For reasons why researchers fabricate data, some look at systemic origins (i.e., the bad barrel argument), such as the highly competitive research system [@10.1172/JCI36371;10.1038/521259a], whereas others look to personality traits that might be predictive of likelihood to commit misconduct [i.e., the bad-apple argument; @10.1038/534173a]. 
What was fabricated (i.e., which results) is often a question that drives scientific integrity committees established to investigate the case in order to correct the scientific record.

How data are fabricated remains puzzling because of incomplete knowledge of cases and lack of first-hand information on data fabrication. 
We have incomplete knowledge about data fabrication strategies because those that are effective at avoiding detection are not available for self-evident reasons (i.e., discovery bias). 
Vice versa, the cases we do know about can teach us what strategies are unsuccessful, but not the range of strategies that potentially are applied.
However, those cases that are discovered often do not result in confessions with explicit descriptions of how they fabricated the data. 
For example, Diederik Stapel confessed to fabricating data and wrote a book about his recollections and interpretations [@stapel2012ontsporing]. 
This is an exceptional case because of the confessive approach he takes. 
However, even in this exceptional case little specific information is available as to how he fabricated data to be of value for research on data fabrication strategies. 
The following excerpt includes a general description of how he fabricated data over the years [@stapel2012ontsporing;@apsstapel]:

>I preferred to do it at home, late in the evening, when everyone was asleep. I made myself some tea, put my computer on the table, took my notes from my bag, and used my fountain pen to write down a neat list of research projects and effects I had to produce ... Subsequently I began to enter my own data, row for row, column for column ... 3, 4, 6, 7, 8, 4, 5, 3, 5, 6, 7, 8, 5, 4, 3, 3, 2. When I was finished, I would do the first analyses. Often, these would not immediately produce the right results. Back to the matrix and alter data. 4, 6, 7, 5, 4, 7, 8, 2, 4, 4, 6, 5, 6, 7, 8, 5, 4. Just as long until all analyses worked out as planned. (p. 167)

Moreover, when scientific integrity committees investigate for data fabrication, rarely will they be able to conclusively state how data were fabricated. 
Some data fabrication strategies might be obvious if the raw data are available (e.g., copy-pasting responses), whereas others will be less obvious (e.g., multivariate modeling of the observed variables for the desired outcomes). 
Moreover, many fabricated results have underdetermined data fabrication strategies (i.e., multiplicity). 
That is, many different fabrication strategies can result in the observed data set, such that differentiating which one actually occurred based on the data is non-trivial [see also @10.12688/f1000research.12584.1].
Additionally, given that odds of data availability decrease each year after publication [@10.1016/j.cub.2013.11.014], methods to learn about how data were fabricated retrospectively by looking at the dataset are increasingly unfeasible even if underdetermination was not a problem. 
Data availability is especially problematic in cases where it takes longer to uncover problems in the first place, such that data are more likely to be unavailable for investigation in cases that go undetected longer.
Second-hand information about data fabrication offers relatively little indication on how data are actually fabricated by researchers due to this underdetermination and increasing lack of data availability.

Hence, first-hand knowledge from controlled settings about how researchers fabricate data is useful to further understand and maybe even improve detection of data fabrication in uncontrolled settings. 
There is unknown variability in how researchers fabricate data, which could result in foregone detection mechanisms if we focus on the limited and preselected knowledge that is available. 
However, we currently do not even know what methods are used and therefore only operate from hunches and inferences from psychology theory [e.g., @Haldane1948-nm] and how often they occur.
As far as we know, only one such study asked participants to fabricate data, but did not investigate how they did so [@10.1136/bmj.331.7511.267].
Qualitative information would provide a first-hand insight into how data are fabricated and could provide fruitful avenues for the development of new statistical tools to detect data fabrication. 

<!-- Er mist nog 1 superbelangrijke alinea, nl over waarom het zo belangrijk is te weten hoe men data fabriceert.  -->
<!-- Ik zou dit in aparte alinea zetten en oppompen (pompen pompen!) – belang van weten HOE moet duidelijk zijn. Geef ook een voorbeeld of voorbeelden hoe dat dan kan helpen.
Ontwikkelen verschillende technieken te detecteren
 Proces van ontdekken, waarbij deze technieken kunnen worden toegepast; bijv, eerst kijken of er ruwe data is, dan naar of er stimulus materiaal voor handen is, dan naar of er missings zijn (zo niet, dan zegt dat wellicht iets over gebruik pc), dan iets over grootte effect size, etc.
Dit is verrekte lastig, mag ook op het eind gedaan worden! Ik bedoel, in discussie -->

In this report, we qualitatively assess the data fabrication strategies that practicing researchers used to fabricate data in one of our controlled studies [@2015ori-1]. 
Based on the transcripts of the interviews about how participants fabricated data [@10.5281/zenodo.832490], we apply qualitative methods to learn more about characteristics of the observed data fabrication strategies. 
Moreover, we combine the observed data fabrication strategies with results from various statistical tools to detect data fabrication [see also @], in order to assess whether certain data fabrication characteristics cause better or worse detection.

# Methods

We used transcripts of 28 interviews with researchers who we previously asked to fabricate data in a controlled setting [available at @10.5281/zenodo.832490]. 
In these interviews, we asked participating researchers to answer questions separated into five sections. 
Section 1 pertained to general information about the researcher (e.g., frequent programs used). 
Section 2 inquired about the time and days spent on fabricating data (e.g., how many hours spent). 
Section 3 asked the researcher about their general framework with which they fabricated the data (e.g., what makes data look weird according to them).
Section 4 focused on the specific steps taken to fabricate data (e.g., did they use a (pseudo-)random number generator).
Section 5 was about the motivations of the researcher to participate in this study and their general assessment of their performance. All participating researchers consented to the public sharing of their transcripts.

To recapitulate, we previously asked these 28 researchers to fabricate raw data for a Stroop experiment [see Figure 1; @stroop1935]. 
In short, a Stroop experiment is typically a within-subjects experiment with two conditions measuring response times: (1) congruent (e.g., the word 'red' is presented in red) and (2) incongruent (e.g., the word 'red' is presented in green). 
We asked the participating researchers to fabricate response times for 25 participants, such that there was a statistically significant effect between conditions (i.e., a Stroop effect). 
Using these fabricated data ([](https://osf.io/xxxxx), we tested whether statistical methods could help separate fabricated data sets from (assumably) genuine datasets from Many Labs 3 [[https://osf.io/n8xa7/](https://osf.io/n8xa7/); @10.1016/j.jesp.2015.10.012].

![Example of a filled in template spreadsheet used in the fabrication process. Respondents fabricated data in the yellow cells and green cells, which were used to compute the results of the hypothesis test of the condition effect. If the fabricated data confirm the hypotheses, a checkmark appeared. This template is available at [https://osf.io/2qrbs/](https://osf.io/2qrbs/).](../figures/spreadsheet2.png)

In this paper, we take a two-pronged approach to evaluating the transcripts of these interviews. First, we provide qualitative summaries and reflections on each transcript. We include a description of the researcher (e.g., career stage, statistics knowledge) and how they fabricated the data according to the transcript. We also add what we considered noteworthy anecdotes from the interview. Secondly, we systematically compare what characteristics   researchers applied to fabricate the data using Qualitative Comparative Analysis [QCA; @rihoux2008]. The first approach provides us with a more detailed but also less systematic picture of data fabrication, whereas the second approach provides us with a more general and more systematic picture of data fabrication.

## Qualitative Comparative Analysis

In Qualitative Comparative Analysis [QCA; @rihoux2008], qualitative information is deconstructed into characteristics and related to an outcome measure. 
In crisp set QCA, which we apply here, these characteristics are binary [e.g., present v absent;@rihoux2008]. 
Each unique combination of characteristics is regarded as a pattern and is used to assess necessary and sufficient conditions for the binary outcome measure to be present or absent. 
Using the coded characteristics for each unit of analysis (e.g., participants, group), we compile truth tables. 
Table xxxxx depicts a fictitious example of a truth table. 
For each unique combination of characteristics, the range of outcomes is inspected. 
The pattern `0-0-0` (first row) is observed $\geq1$ times and, in this sample, always leads to the absence of the outcome (vice versa for the last row).
The pattern `0-0-1` (second row) is observed $>1$ times and has conflicting (`C`) outcomes; both presence and absence occur with this pattern.
The pattern `0-1-0` (third row) is not observed and therefore has no information about the outcome (i.e., a logical remainder; `?`).
A truth table can subsequently be minimized to determine necessary and sufficient conditions for the outcome to be present or absent.

```{r, echo = FALSE}
data(LC)
LC <- LC[, -(1:2)]
names(LC) <- c(sprintf('char%s', 1:3), 'outcome')
ttLC <- truthTable(LC, "outcome")
ttLC$tt$OUT[2] <- 'C'
df <- ttLC$tt[,1:4]

knitr::kable(df, caption="Example of a truth table as used in crisp set Qualitative Comparative Analysis (csQCA). The outcome measure is the dependent variable, where the various patterns of the characteristics are used to determine under what conditions the outcome is observed. A `?` indicates that pattern was not observed and therefore the outcome is unknown; a `C` indicates that this pattern was observed >1, but that both outcomes occurred, creating a conflict in csQCA.")
```

Based on the interview protocol ([osf.io/xxxx](https://osf.io/xxxx)), we identified five general data fabrication characteristics for our QCA. 
Each unique combination of data fabrication characteristics makes up a data fabrication strategy. 
We limited ourselves to five characteristics, considering that 2^*n* strategies would be possible. 
In other words, we balanced the number of transcripts (i.e., 28) to the number of unique data fabrication strategies possible (i.e., $2^4=16$; $2^5=32$; $2^6=64$). 
We coded whether 
(1) the participant prepared for the data fabrication (e.g., by reading literature on detecting data fabrication); 
(2) the participant used a (pseudo-)Random Number Generator (RNG) in fabricating the data; 
(3) the participant used assumably genuine Stroop data; 
(4) the participant duplicated or transformed data; 
(5) the participant checked the fabricated data for detectibility. 
The first author coded each of these five data fabrication characteristics for all of the 28 transcripts. 
Additionally, we coded ten participant characteristics (e.g., PhD attained, self-reported statistical knowledge; further described at [osf.io/xxxx](https://osf.io/xxxx) and available at [osf.io/xxxx](https://osf.io/xxxx)). 
We note that these data fabrication characteristics are inherently multiplicitous, hence, we do not know how much we will learn from the QCA. 

As outcome measures, we included whether the researcher's fabricated data was detected as such, by taking the results from the three best statistical methods to detect data fabrication [@REF]. 
In our original project, we included XX tests to detect data fabrication and included only the top three here, based on their Area Under the Curve value. 
We could assess these AUCs based on (assumably) genuine data from the Many Labs 3 initiative [@10.1016/j.jesp.2015.10.012]. 
As a result, we included as outcome measures the results of the detection methods based on 
(1) ?
(2) ?
(3) ?
We did not include the other methods, which consisted of (amongst others) X, X, and X. 
<!-- how did we determine this -->
<!-- which methods are this -->
<!-- which methods didn't make it -->

We conducted three separate csQCA analyses combining the coded data fabrication characteristics with the outcomes of these statistical detection methods. 
In csQCA, unique combinations with conflicting outcomes are either omitted (similar to listwise deletion) or additional characteristics are inductively added to resolve the conflicting outcomes [@rihoux2008]. 
Here, we omit conflicting outcomes for analysis and try to qualitatively assess potentially relevant characteristics. 
We do not run new QCAs because adding additional characteristics quickly increases the state space of unique patterns to 128 (by just adding two) or beyond (512 by adding four). 
If we would add two characteristics it  would result in maximum coverage of `r round((28/128) * 100, 0)`%; maximum coverage would be `r round((28/512) * 100, 0)`% if we add four characteristics. 

We used the R package `QCA` [@;@] to conduct these csQCAs. 
For each of the three statistical methods to detect data fabrication, we assessed both sufficient and necessary conditions for detection as well as going undetected. 
We minimized the truth tables using the enhanced Quine-McCluskey algorithm [@]. 
Data are available at [osf.io/xxxxx](https://osf.io/xxxxx); analysis code is available at [osf.io/xxxxx](https://osf.io/xxxxx). 

<!-- As such, we minimized the truth tables with the outcome measuresfor both detecting data as fabricated and for fabricated data going undetected. 
As such, we initially conduct ten QCA's, with at most ten more in the case of conflicting outcomes in for all methods. -->
<!-- https://raw.githubusercontent.com/chartgerink/2015ori-2/c706d77e4d85daa285624028d379d7b9b00bd1d0/submission/manuscript.Rmd -->
<!-- 
# Results

## Qualitative summaries

## Qualitative Comparative Analysis

# Discussion -->

# Author's note

All materials used in this project are available at [https://github.com/chartgerink/2015ori-2](https://github.com/chartgerink/2015ori-2) and are preserved at Zenodo. This project was funded by the Office of Research Integrity (ORI-).

# References

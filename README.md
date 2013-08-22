# Nurse Family Partnership Impact Evaluation
 
This is a [Data Science for Social Good Fellowship](http://dssg.io) project to help the Nurse Family Partnership evaluate its effectiveness at promoting healthy child developmental outcomes and stable families.


![NFP](http://dssg.io/img/partners/nfp.jpg)
 
## The Problem
 
The Nurse-Family Partnership (NFP) is a home-visitation program that pairs a nurse with an at-risk first-time mother for the duration of her pregnancy and the first two years of her child's life. The Affordable Care Act of 2010 made new money available to home visitation programs such as NFP, but also required increased accountability for evidence-based demonstrations of effectiveness. NFP was founded on the basis of multiple randomized controlled trials (which are on-going, in follow-up), and the organization continues to study program outcomes. However, while NFP's formidable information tracking system affords them a large-scale, systematic perspective for reviewing participants' outcomes, they face two principle challenges to performing a large-scale evaluation:

1) They do not have data on child and mother outcomes for a comparison population (i.e. which they do not serve);

2) NFP's program participants differ from the general population on a range of characteristics, including some, like income or educational attainment, that probably impact the outcomes in question.  As a result, a simple comparison of means between the outcomes of NFP participants and the outcomes of the general population does not capture the full story.

[More information about the challenges that shaped our project are available in our wiki.](https://github.com/dssg/nfp/wiki/Problem)


## The Solution

To assist NFP, we are using matching techniques to identify women in public national datasets who are similar on all observable characteristics (such as demographics) to the women in NFP's administrative data.  We can plausibly estimate NFP's impact as the difference in outcomes between these two groups.  [Our wiki contains more details about our methodology.](https://github.com/dssg/nfp/wiki/Methodology)

Our project has two goals:

1) To provide a rough evaluation of NFP's impact at a national level. Although this study will not have validity equivalent to a randomized controlled trial, it represents a significant improvement over the evidence basis that would otherwise be available to current decision processes.

2) To develop a methodology for basic impact evaluation of nonprofit programs where resource limitations and program size make traditional experimental evaluations impractical or impossible.


## The Project and The Data 

NFP ultimately hopes to assess outcomes across a range of areas, including child development and health, mother's life course, and child welfare/intimate partner violence.  For this project, we focused on two specific outcomes: immunization and breastfeeding rates.  We created our comparison groups from the National Immunization Survey and the National Survey of Children's Health respectively.  We also did some significant exploration in the Current Population Survey as a potential dataset for assessing mother's life outcomes like employment and educational attainment.

The *data_preparation* directory includes all of the scripts we used to clean and reshape our data.  Ultimately, we needed to develop uniform datasets from both the NFP data and the comparison data files, so that we could combine these datasets for analysis.  The code in this directory demonstrates the details of that process.

The *data_analysis* directory contains the scripts used for our actual analysis, including data exploration and matching.  This directory also includes a few sample/simulation scripts we developed while we explored the details of our methodology.

[More information about each of the datasets we used, as well as additional datasets we reviewed and considered is available in our Data wiki.](https://github.com/dssg/nfp/wiki/Data)


## Contributing to the Project

Because our project involved working with proprietary health information, much of our data is not accessible for public use.  However, we are making our methodology transparent in hopes that it may be useful for other projects.  We would love to hear from other individuals using parts of our code or just doing the same kind of work.  We can be reached at dssg-nfp@googlegroups.com.


## Using R

All of our data analysis, impact estimation, and exhibit generation code is written in R, as an openly available and widely used statistics software. We made this choice to ensure accessibility of our work to the broad non-profit and research community that might be interested in this work. While R is widely--and increasingly--being used, we recognize that many potential users of this code may not have any, or at least, comfortable acquaintance with programming in R. Several references and tutorials that we highly recommend are:

* [Code School's free, interactive tutorial in R](http://www.codeschool.com/courses/try-r)
* Books tailored to one's programming background, such as [R for SAS and SPSS Users](http://www.amazon.com/SAS-SPSS-Users-Statistics-Computing/dp/1461406846/ref=sr_1_1?s=books&ie=UTF8&qid=1376955179&sr=1-1) by Robert Muenchen or  [R for Stata Users](http://www.amazon.com/R-Stata-Users-Statistics-Computing/dp/1461425964/ref=sr_1_2?s=books&ie=UTF8&qid=1376955179&sr=1-2) by Robert Muenchen and Joseph Hilbe
 * Note that these books have excellent, and freely available, code samples for many common operations in R, with comparisons to the equivalent commands in SAS, SPSS and Stata.
* [R in a Nutshell](http://web.udl.es/Biomath/Bioestadistica/R/Manuals/r_in_a_nutshell.pdf) by Joseph Adler, published by O'Reilly
* A number of freely available "quick reference" sheets such as ones by [Tom Short](http://cran.r-project.org/doc/contrib/Short-refcard.pdf), and staff at the [University of Auckland](https://www.stat.auckland.ac.nz/~stat380/downloads/QuickReference.pdf).
* Researchers interested in using R specifically to work with complex national surveys may be interested in [Anthony D'Amico's usgsd repo](https://github.com/ajdamico/usgsd), which includes sample import and analysis scripts for many popular surveys.
 
Searching the internet is also an excellent way to understand the commands that we used or to search for methods of interest to you, due to the large and active community of R users.


## License

Copyright (C) 2013 Data Science for Social Good Fellowship at the University of Chicago

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

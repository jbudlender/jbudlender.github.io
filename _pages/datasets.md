---
layout: page
permalink: /datasets/
title: Datasets
description: Datasets produced by myself and coauthors, or which are otherwise not easily publicly accessible.
nav: false
---
<!---
* * *

##### "Updated 2021" NIDS and LCS datasets
Data and code from [Social Distress and (Some) Relief: Estimating the impact of pandemic job loss on poverty in South Africa](*) with Ihsaan Bassier and Maya Goldman.
The data come with significant health warnings and it is essential to read our paper prior to use. If you use the data, please cite the paper.  
[[Code](*) | [Datasets](*)]

* * *
-->
<br/>

* * *

##### South African industry codes and concordance tables
Tables from [Industry classification in the South African tax microdata](https://sa-tied.wider.unu.edu/sites/default/files/pdf/SA-TIED-WP-134.pdf) with Amina Ebrahim.
Concordance tables come from a combination of official sources and our own hand-matching; please see the paper. 
If you use these tables, please cite the paper.  
[Industry codes: [Stats SA SIC 7](https://github.com/jbudlender/IndustryClassification/blob/main/sic7codes_wide.dta) | [Stats SA SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/sic5codes_wide.dta) | [SARS Activity Codes](https://github.com/jbudlender/IndustryClassification/blob/main/actcodes_wide.dta) | [SARS Profit Codes](https://github.com/jbudlender/IndustryClassification/blob/main/profcode_wide.dta)]  
[Concordance tables: [SIC 5 to SIC 7](https://github.com/jbudlender/IndustryClassification/blob/main/SIC%20edition_5%20and%20SIC%20edition_7%20correspondence%20table%20V1.00.xls) | [SIC 7 to SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/concordv2__sic7_sic5.dta) | [Activity Codes to SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/concordv2__act_sic5.dta) | [Profit Codes to SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/concordv2__prof_sic5.dta)]  
[[Github repo with CSV versions & additional resources](https://github.com/jbudlender/IndustryClassification)]

* * *

<br/>

* * *

##### Machine-readable CPI

Statistics South Africa's [Historic CPI series](http://www.statssa.gov.za/publications/P0141/CPIHistory.pdf?)
is very useful but is trapped inside a pdf. I wrote a small script to extract and reshape the data into long `.csv` and `.dta` files.  
[[Code and data](https://github.com/jbudlender/HistoricSA_CPI)]

* * *

<br/>

* * *

##### 2011 census shapefiles

The published Stats SA 2011 census Small Area Layer (SAL) shapefiles (available from e.g. [DataFirst](https://doi.org/10.25828/6n0m-7m52)) do not include polygons for areas where a Small Area (SA) contains 10 or fewer individuals.
This can be frustrating to work with. Helene Verhoef kindly provided me with the following Stats SA shapefiles which include (empty) polygons for these sparsely populated SAs.
Please acknowledge Stats SA if you use them.  
[[Shapefiles](https://www.dropbox.com/s/urp5t8onym43k1s/SA_nogaps_2013.zip?dl=0)]

* * *



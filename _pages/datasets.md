---
layout: page
permalink: /datasets/
title: Datasets
description: Links to various public data sources, and datasets created by myself and coauthors.
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

* * *
##### South African microdata
The single best source for South African microdata for academic use, particularly for household surveys, is the [DataFirst Data Portal](https://datafirst.uct.ac.za/dataportal/index.php/catalog/central).  Their catalogue also includes data from a variety of other African countries.

* * *
##### Statistics South Africa
The national statistical office, [Statistics South Africa](https://www.statssa.gov.za/), collects and produces an invaluable array of South African data, but their website is difficult to navigate. A few particularly useful pages:
* [Historic CPI series](http://www.statssa.gov.za/publications/P0141/CPIHistory.pdf?), [CPI archive](https://www.statssa.gov.za/?page_id=1866&PPN=P0141&SCH=73033), [PPI archive](https://www.statssa.gov.za/?page_id=1866&PPN=P0142.1&SCH=73035)  
  * The historic headline CPI data is trapped inside a PDF: I wrote a small script to extract and reshape the data into long `.csv` and `.dta` files, available at my [Github repo](https://github.com/jbudlender/HistoricSA_CPI).  
  * [Aidan Horn](https://www.aidanhorn.co.za/home) scrapes and [publishes](https://www.aidanhorn.co.za/inflation/app) this and more disaggregated non-historic data.
* ['Interactive data' webpage](https://www.statssa.gov.za/?page_id=1417), which links to the Nesstar interface for downloading microdata, and to economic time series in machine-readable formats.
* [QLFS](https://www.statssa.gov.za/?page_id=1866&PPN=P0211&SCH=73289), [QES](https://www.statssa.gov.za/?page_id=1854&PPN=P0277&SCH=72995) and [GDP](https://www.statssa.gov.za/?page_id=1866&PPN=P0441&SCH=72934) archives
* Archives of various monthly series, mainly production and sales data: 
  [Mining](https://www.statssa.gov.za/?page_id=1866&PPN=P2041&SCH=73088), [Manufacturing](https://www.statssa.gov.za/?page_id=1866&PPN=P3041.2&SCH=73089), [Electricity](https://www.statssa.gov.za/?page_id=1866&PPN=P4141&SCH=73090), 
  [Retail trade](https://www.statssa.gov.za/?page_id=1866&PPN=P6242.1&SCH=72671), [Wholesale trade](https://www.statssa.gov.za/?page_id=1866&PPN=P6141.2&SCH=72672),
  [Food and beverages](https://www.statssa.gov.za/?page_id=1866&PPN=P6420&SCH=73109), [Motor trade](https://www.statssa.gov.za/?page_id=1866&PPN=P6343.2&SCH=73105), 
  [Tourist accomodation](https://www.statssa.gov.za/?page_id=1866&PPN=P6410&SCH=72889), [Tourism and Migration](https://www.statssa.gov.za/?page_id=1866&PPN=P0351&SCH=73296), [Import/Export Unit Value Indices](https://www.statssa.gov.za/?page_id=1866&PPN=P0142.7&SCH=73049)
* [Input-output](https://www.statssa.gov.za/?page_id=1866&PPN=Report-04-04-02&SCH=7002) (see also [here](https://www.statssa.gov.za/?page_id=1854&PPN=D0404.1) and [here](https://www.statssa.gov.za/?page_id=1854&PPN=D0404)) and [Supply and use](https://www.statssa.gov.za/?page_id=1866&PPN=Report-04-04-03&SCH=73278) (see [here](https://www.statssa.gov.za/?page_id=1866&PPN=Report-04-04-01&SCH=4764) for 1998-2005) tables
* [Mid-year population estimates](https://www.statssa.gov.za/?page_id=1866&PPN=P0302&SCH=73305)

* * *
##### Matched employer-employee tax administrative data
Can be accessed in-person at the [National Treasury Secure Data Facility (NT-SDF)](https://sa-tied.wider.unu.edu/data) in Pretoria. Access to the data and output retrieval is strictly controlled to ensure anonymity is preserved and to comply with relevant legislation: see the [SA-TIED](https://sa-tied.wider.unu.edu/) website for details.
* The datasets are very large, the underlying tax data is not collected with researchers in mind, and the data documentation is incomplete. This data is incredibly rich, but is not easy to work with. You must be very comfortable with Stata, R or Python to conduct productive research with this data; the NT-SDF is not a place to learn these languages as you go.
* I have provided some [tips on working with large data in Stata](/largedatastata), based on my experiences at the NT-SDF.
* The NT-SDF administrators may be able to direct you to research assistants based in Pretoria who can run analysis for you, but keep in mind that the data is complex to work with and it is probably a good idea to retain fairly close oversight and run many checks on the data as you go.
* Carefully reviewing the [available documentation](https://sa-tied.wider.unu.edu/article/guide-cit-irp5-panel-version-40) before you start is highly beneficial. More detailed documentation and discussion is available for sub-components of the data, which may be more disaggregated than the firm-level (e.g. worker-level employment data). See references in the combined panel guide.
* Data updates are available [here](https://sa-tied.wider.unu.edu/data/data-updates); more detail is provided [here](https://onlineunu-my.sharepoint.com/personal/abena_larbiodam_wider_unu_edu/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fabena%5Flarbiodam%5Fwider%5Funu%5Fedu%2FDocuments%2FNational%20Treasury%20Secure%20Data%20Facility%20%28NT%2DSDF%29%5FUpdates%2Epdf&parent=%2Fpersonal%2Fabena%5Flarbiodam%5Fwider%5Funu%5Fedu%2FDocuments&ga=1).  

* * *
##### South African industry codes and cross-walks
Tables from my report with Amina Ebrahim, [Industry classification in the South African tax microdata](https://sa-tied.wider.unu.edu/sites/default/files/pdf/SA-TIED-WP-134.pdf), are available below and at the NT-SDF. If you use these tables, please cite the paper.
* Industry codes: [Stats SA SIC 7](https://github.com/jbudlender/IndustryClassification/blob/main/sic7codes_wide.dta) \| [Stats SA SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/sic5codes_wide.dta) \| [SARS Activity Codes](https://github.com/jbudlender/IndustryClassification/blob/main/actcodes_wide.dta) \| [SARS Profit Codes](https://github.com/jbudlender/IndustryClassification/blob/main/profcode_wide.dta)  
* Concordance tables: [SIC 5 to SIC 7](https://github.com/jbudlender/IndustryClassification/blob/main/SIC%20edition_5%20and%20SIC%20edition_7%20correspondence%20table%20V1.00.xls) \| [SIC 7 to SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/concordv2__sic7_sic5.dta) \| [Activity Codes to SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/concordv2__act_sic5.dta) \| [Profit Codes to SIC 5](https://github.com/jbudlender/IndustryClassification/blob/main/concordv2__prof_sic5.dta)  
* [Github repo with CSV versions & additional resources](https://github.com/jbudlender/IndustryClassification)

* * *
##### South African COVID-19 data
* [Machine-readable South African COVID-19 data](https://github.com/dsfsi/covid19za), from the [Data Science for Social Impact](https://dsfsi.github.io/) group at the University of Pretoria.
* The [NICD](https://www.nicd.ac.za/) is the definitive source for SA COVID-19 data, but last I checked most of their data were trapped inside PDFs.
* [Weekly deaths and estimated excess deaths data](https://www.samrc.ac.za/research-reports/report-weekly-deaths-south-africa) from the [SAMRC](https://www.samrc.ac.za/).

* * *

##### Electricity supply/generation and load shedding (rolling blackouts)
* [National load shedding implementation data](https://docs.google.com/spreadsheets/d/1ZpX_twP8sFBOAU6t--Vvh1pWMYSvs60UXINuD5n-K08/edit#gid=863218371) from [EskomSePush](https://sepush.co.za/).
* The [Eskom Data Portal](https://www.eskom.co.za/dataportal/) provides a wide array of detailed time series data. Use the (automated) "Data request form". Longer time series are available via [PAIA request](https://www.eskom.co.za/paia-popia/).
* The [City of Cape Town Open Data Portal](https://odp-cctegis.opendata.arcgis.com/) provides [detailed load shedding implementation data](https://odp-cctegis.opendata.arcgis.com/documents/42551ffb9c494932ac16c4e9cd7dc28e) for city-supplied regions. 
* [Detailed Eskom monthly plant-level energy availability factors (EAF)](https://amabhungane.org/stories/220928-the-collapse-of-old-king-coal/) (see the "Evidence docket" link) provided by [amaBhungane](https://amabhungane.org/).


* * *
##### Geospatial data
* The 2011 South African Census data and shapefiles are available from [DataFirst](https://doi.org/10.25828/6n0m-7m52). 
   * The lowest Small Area Layer (SAL) shapefiles do not include polygons for areas where a Small Area (SA) contains 10 or fewer individuals. Helene Verhoef kindly provided me with [additional Stats SA shapefiles](https://www.dropbox.com/s/urp5t8onym43k1s/SA_nogaps_2013.zip?dl=0) which include these (empty) polygons. Please acknowledge Stats SA if you use them.  
  * [Adrian Frith's](https://adrian.frith.dev/) census mapping [website](https://census2011.adrianfrith.com/) is very useful if working with this data.  
  * Adrian Frith also provided a [small dataset](https://pastebin.com/E1P618CG) linking 2001 to 2011 municipality geographies, which one can use to construct a cross-walk ([context](https://twitter.com/adrianfrith/status/1725255307189006600)).
* The SALDRU [YouthExplorer](https://www.youthexplorer.org.za/) is also a very useful source for geolocated South African data. Apart from youth-focused socio-economic statistics, it also provides downloadable point data for the coordinates of "service points" such as schools, police stations, post offices, healthcare facilities, SASSA offices, and a variety of other facilities.  
* South African police station coordinates with their boundaries are available from [SAPS](https://www.saps.gov.za/services/boundary.php).
* The [Copernicus Climate Data Store](https://cds.climate.copernicus.eu/cdsapp#!/home) is a definitive source of weather data.
* [The Gridded Population of the World (GPW)](https://sedac.ciesin.columbia.edu/data/collection/gpw-v4) data from [SEDAC](https://sedac.ciesin.columbia.edu/) is very useful if you need the spatial distribution of human population across a continuous raster surface, rather than one defined by administrative boundaries.  

* * *
##### Other
* [Catalogue of public data sources](https://docs.google.com/spreadsheets/d/1asrQMHp_aJrD-LqkmW9n5yLT6Cm-K1geBEn9nLfYb3E/edit#gid=388540894) courtesy of [Open Data South Africa](https://opendataza.gitbook.io/toolkit/).
Their website, with data organised by theme, is easier to navigate than the (overwhelming) catalogue.

* * *
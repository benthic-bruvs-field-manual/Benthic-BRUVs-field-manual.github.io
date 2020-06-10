---
layout: home
permalink: /image-annotations
title: "Image annotations"
excerpt: "<br>"
image:
  feature: /banners/04_banner.jpg
---
{% include toc.html class="toc-left" h_min=2 h_max=2 %}

## Software

Software specifically designed to annotate and measure fish from stereo-video will substantially increase the cost-efficiency and consistency of image annotation (Gomes-Pereira _et al._ 2016). For stereo-video the challenge is not the annotation by the calibration of imagery to provide accurate length and range measurement. Annotation software and packages with measurement capabilities include Vision Measurement System (Harman, Harvey & Kendrick 2003), NIH Image (Dunbrack 12/2006), SEBASTES package in Python (Boldt _et al._ 2018), StereoMorph package in R (Olsen & Westneat 2015), and EventMeasure from SeaGIS ([seagis.com.au](seagis.com.au)). We recommend EventMeasure due to its established workflow, ability to create 3-D stereo-calibrations, and active development, which enables cost-effective and consistent point and stereo annotation of video imagery. Manual image annotation and measurement can be time consuming, but the emerging field of automated image annotation provides promise of increased cost efficiency and collection of novel metrics (Marini _et al._ 2018).


## Annotation metadata

Field metadata (Supp. 4) should be used to populate a unique sample code for each sample and annotation set. Time on the seabed should be annotated to provide a start time for the stereo-BRUV deployment period. It is important that the link between annotations and imagery are maintained.


## Abundance estimates

We recommend all fish be identified to the lowest taxonomic level possible. The standard metric of abundance is MaxN, the maximum number of individuals of a given species present in a single video frame (Priede _et al._ 1994). MaxN is widely used for BRUVs (Whitmarsh _et al._ 2017) conservative, and ensures that no individual is counted more than once (Schobernd, Bacheler & Conn 2013) It has frequently been suggested that MaxN underestimates both small and large-bodied individuals, whereas the only study so far to evaluate this has found MaxN provides a representative sample of size-distributions (Coghlan _et al._ 2017). Syncronise left and right cameras to allow the analyst to determine the range of fish in the field of view and ensure they are within a predefined distance from the cameras. Typically, fish are counted within a maximum distance of 8 m, beyond which length estimates are likely to be inaccurate unless specialist calibrations have been conducted. Annotations of the current MaxN may be updated when individual fish are more clearly visible, and therefore easier to measure, by taking photogrammetric measurements of individual body length at the last MaxN annotated.


## Body-size measurements

Synchronised and calibrated stereo-video streams are used to accurately measure body size. All individuals of each species should be measured at their MaxN. We recommend measuring fork length rather than total length, as it is more easily definable across a range of species. Biomass estimates typically rely on total length, but fork length to total length conversions can be used to complete these calculations (Froese & Pauly 2019). For species where total length can be unreliable or there is no definable fork, body size is estimated using other measures (e.g. disk length for rays). Photogrammetric length measurements are typically made with some degree of error, which can be minimised by measuring individuals when they are as close to cameras as possible with both the nose and the tail-fork clearly visible, still or slowly moving, at an angle less than 45° perpendicular to the cameras. Defining cut-offs for measurement error across projects will help to maintain accurate and precise body-size estimates, we provide recommended stereo-measurement length rules for EventMeasure in the table below. If fish cannot be measured within these parameters, a ‘3D point’ may be used for annotation, which records the 3D location of the fish to ensure it is within the sampling area (Harvey _et al._ 2004). To create a relative abundance metric standardised to a consistent sample area, abundance should be summed from the lengths and 3D points at the MaxN for each species. For biomass estimates, 3D points provide a basis for extrapolating a median length value to fish that could not be measured (Wilson _et al._ 2018). When large tightly packed schools are encountered, fish that cannot be measured should have 3D points. When lengths or 3D points are not possible for every fish, multiple individuals can be assigned to a single length or 3D point, but care should be taken to represent the range of body sizes within a school.


Recommended stereo-measurement length rules for EventMeasure.

<table>
  <tr>
   <td><strong>Name</strong>
   </td>
   <td><strong>Data</strong>
   </td>
   <td><strong>Units</strong>
   </td>
  </tr>
  <tr>
   <td>Use lengths rules
   </td>
   <td>True
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Apply range rule
   </td>
   <td>True
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Minimum range
   </td>
   <td>0.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Maximum range
   </td>
   <td>8000.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Apply RMS rules
   </td>
   <td>True
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Maximum RMS
   </td>
   <td>20.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Apply precision to length ratio rules
   </td>
   <td>True
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Maximum precision to length ratio
   </td>
   <td>10.0000
   </td>
   <td>%
   </td>
  </tr>
  <tr>
   <td>Apply precision rule
   </td>
   <td>False
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Maximum precision
   </td>
   <td>10.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Apply direction rule
   </td>
   <td>False
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Maximum direction
   </td>
   <td>45.0000
   </td>
   <td>Degrees
   </td>
  </tr>
  <tr>
   <td>Apply horizontal direction rule
   </td>
   <td>False
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Maximum horizontal direction
   </td>
   <td>45.0000
   </td>
   <td>Degrees
   </td>
  </tr>
  <tr>
   <td>Apply vertical direction rule
   </td>
   <td>False
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Maximum vertical direction
   </td>
   <td>45.0000
   </td>
   <td>Degrees
   </td>
  </tr>
  <tr>
   <td>Apply x coordinate range rule
   </td>
   <td>False
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Minimum x coordinate
   </td>
   <td>-2500.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Maximum x coordinate
   </td>
   <td>2500.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Apply y coordinate range rule
   </td>
   <td>False
   </td>
   <td>Boolean
   </td>
  </tr>
  <tr>
   <td>Minimum y coordinate
   </td>
   <td>-2500.0000
   </td>
   <td>mm
   </td>
  </tr>
  <tr>
   <td>Maximum y coordinate
   </td>
   <td>2500.0000
   </td>
   <td>mm
   </td>
  </tr>
</table>


 


## Behaviour

A range of behavioural observations, including time of first arrival, time to first feed, and minimum approach distance may also be calculated (Goetze _et al._ 2017; Coghlan _et al._ 2017).


## Interoperable and reproducible annotations

Video imagery enables annotators to work collaboratively to ensure identifications are consistent. A library of reference images, such as that supported by EventMeasure, will assist with identification and training. It is acknowledged that some genera cannot be consistently identified to species level from imagery, so individuals are recorded at genus‐family levels (e.g. flathead: _Platycephalus _spp). For unidentified individuals, a common convention is that fish that are potentially identifiable at a later date are annotated to _Genus_ sp1–10, this permits a batch‐rename at a later stage if the species is successfully identified. Individuals that are clearly unidentifiable to species are annotated as _Genus_ sp. 


## Habitat classification 

Information on relief, habitat types, and benthic composition (e.g. percent cover of benthos types) should be recorded from each deployment (Bennett _et al._ 2016; Collins _et al._ 2017), to facilitate investigation of fish-habitat relationships and to enable the sampling field of view to be standardised or controlled for in subsequent data analysis (McLean _et al._ 2016). It is important that these data are annotated consistently and it is recommended that they are mapped to the CATAMI classification scheme (Althaus _et al._ 2015) and a 0-5 estimate of benthic relief  (Polunin & Roberts 1993; Wilson, Graham & Polunin 2007). An example of habitat composition and relief annotation schema are provided in a GitHub repository  (Langlois 2017). Forward facing imagery can be annotated in a range of software, including TransectMeasure from SeaGIS ([seagis.com.au](https://www.seagis.com.au)), BenthoBox ([https://benthobox.com](https://benthobox.com)), CoralNet ([https://coralnet.ucsd.edu/](https://coralnet.ucsd.edu/)), and Squidle+ ([https://squidle.org](https://squidle.org)). 


## Quality control and data curation

Quality control and data curation are vital to ensure FAIR data workflows (Wilkinson _et al._ 2016). All corrections should be made within the original annotation files to ensure data consistency over time. We recommend the following approaches to ensure quality control:



*   Annotators should complete “training” videos where species IDs and MaxN are known and can be used to assess competency.
*   A different annotator should complete the MaxN and length measurement annotations to provide an independent check of the species identifications.
*   Quality assurance should be carried out by a senior video analyst or researcher and involve a random review of 10% of annotated videos and data within a project. If accuracy is below 95 % for all identifications and estimates of MaxN, reannotation should be undertaken.
*   Unique identifiers of annotators and dates of when imagery was annotated should be maintained to provide a data checking trail (see Supp. 4).

R workflows and function packages are provided in a GitHub repository (Langlois 2020) to enable validation with regional species lists and likely minimum and maximum sizes for each species.


## Data storage, discoverability and release

We encourage open data policies and recommend archiving and sharing stereo-BRUV annotations on global biodiversity data repositories, such as OBIS (Ocean Biogeographic Information System), GBIF (Global Biodiversity Information Facility) and the recently developed GlobalArchive ([globalarchive.org](about:blank)). GlobalArchive is a centralised repository that allows open access and private sharing of fish image annotation data from stereo-BRUVs or similar imagery-based sampling techniques. GlobalArchive allows users to store data in a standardised and secure manner and makes meta-data discoverable, thus encouraging collaboration and synthesis of datasets within the community of practice. We recommend all quality controlled annotation data and any associated calibration, taxa and habitat data should be uploaded to GlobalArchive and we encourage that all data should be made publicly available via the public data option. As an example, the Australian standards for data management, discoverability and release are provided in Supp. 6.

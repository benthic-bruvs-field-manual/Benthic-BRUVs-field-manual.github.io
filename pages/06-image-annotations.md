---
layout: home
permalink: /image-annotations
title: "Image Annotations"
excerpt: "<br>"
image:
  feature: /banners/04_banner.jpg
---
{% include toc.html class="toc-left" h_min=2 h_max=2 %}

## Software

Software specifically designed to annotate and measure fish from stereo-video will substantially increase the cost-efficiency and consistency of image annotation (Gomes-Pereira et al. 2016). For stereo-video the challenge is not the annotation but the calibration of imagery to provide accurate length and range measurement. Annotation software and packages with measurement capabilities include Vision Measurement System (Harman, Harvey & Kendrick 2003), NIH Image (Dunbrack 12/2006), SEBASTES package in Python (Boldt et al. 2018), StereoMorph package in R (Olsen & Westneat 2015), and EventMeasure from SeaGIS ([seagis.com.au](seagis.com.au)). We recommend EventMeasure due to its established workflow, ability to create 3-D stereo-calibrations, and active development, which enables cost-effective and consistent point and stereo annotation of video imagery. Manual image annotation and measurement can be time consuming, but the emerging field of automated image annotation provides promise of increased cost efficiency and collection of novel metrics (Marini et al. 2018).


## Annotation metadata

Field metadata (Table 2) should be used to populate a unique sample code for each sample and annotation set. Time on the seabed should be annotated to provide a start time for the stereo-BRUV deployment period. It is important that the link between annotations and imagery are maintained.


## Abundance estimates

We recommend all fish be identified to the lowest taxonomic level possible. The standard metric of abundance is MaxN, the maximum number of individuals of a given species present in a single video frame (Priede et al. 1994). MaxN is widely used for BRUVs (Whitmarsh et al. 2017) conservative, and ensures that no individual is counted more than once (Schobernd, Bacheler & Conn 2013) It has frequently been suggested that MaxN underestimates both small and large-bodied individuals, whereas the only study so far to evaluate this has found MaxN provides a representative sample of size-distributions (Coghlan et al. 2017). Synchronise left and right cameras to allow the analyst to determine the range of fish in the field of view and ensure they are within a predefined distance from the cameras. Typically, fish are counted within a maximum distance of 8 m, beyond which length estimates are likely to be inaccurate unless specialist calibrations have been conducted. Annotations of the current MaxN may be updated when individual fish are more clearly visible, and therefore easier to measure, by taking photogrammetric measurements of individual body length at the last MaxN annotated. Please see the [Annotation guides on the CheckEM website](https://globalarchivemanual.github.io/CheckEM/articles/manuals/EventMeasure_annotation_guide.html) for a step by step guide.


## Body-size measurements

Synchronised and calibrated stereo-video streams are used to accurately measure body size. All individuals of each species should be measured at their MaxN. We recommend measuring fork length rather than total length, as it is more easily definable across a range of species. Biomass estimates typically rely on total length, but fork length to total length conversions can be used to complete these calculations (Froese & Pauly 2019). For species where total length can be unreliable or there is no definable fork, body size is estimated using other measures (e.g. disk length for rays). Photogrammetric length measurements are typically made with some degree of error, which can be minimised by measuring individuals when they are as close to cameras as possible with both the nose and the tail-fork clearly visible, still or slowly moving, at an angle less than 45° perpendicular to the cameras. Defining cut-offs for measurement error across projects will help to maintain accurate and precise body-size estimates, we provide recommended stereo-measurement length rules for EventMeasure in Table 4. If fish cannot be measured within these parameters, a ‘3D point’ may be used for annotation, which records the 3D location of the fish to ensure it is within the sampling area (Harvey et al. 2004). To create a relative abundance metric standardised to a consistent sample area, abundance should be summed from the lengths and 3D points at the MaxN for each species. For biomass estimates, 3D points provide a basis for extrapolating a median length value to fish that could not be measured (Wilson et al. 2018). When large tightly packed schools are encountered, fish that cannot be measured should have 3D points. When lengths or 3D points are not possible for every fish, multiple individuals can be assigned to a single length or 3D point, but care should be taken to represent the range of body sizes within a school. Please see the [Annotation guides on the CheckEM website](https://globalarchivemanual.github.io/CheckEM/articles/manuals/EventMeasure_annotation_guide.html) for a step by step guide.


## Table 4. Recommended stereo-measurement length rules for EventMeasure.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-aoc0{background-color:#629ACD;color:#FFF;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-5jfb{background-color:#CFE2F3;text-align:left;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 785px"><colgroup>
<col style="width: 297.88889px">
<col style="width: 231.88889px">
<col style="width: 254.88889px">
</colgroup>
<thead>
  <tr>
    <th class="tg-aoc0"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#FFF;background-color:transparent">Name</span></th>
    <th class="tg-aoc0"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#FFF;background-color:transparent">Data</span></th>
    <th class="tg-aoc0"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#FFF;background-color:transparent">Units</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Use lengths rules</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">True</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply range rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">True</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Minimum range</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">0.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum range</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">8000.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply RMS rules</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">True</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum RMS</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">20.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply precision to length ratio rules</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">True</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum precision to length ratio</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">10.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">%</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply precision rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">False</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum precision</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">10.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply direction rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">False</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum direction</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">45.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Degrees</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply horizontal direction rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">False</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum horizontal direction</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">45.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Degrees</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply vertical direction rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">False</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum vertical direction</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">45.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Degrees</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply x coordinate range rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">False</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Minimum x coordinate</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">-2500.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum x coordinate</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">2500.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Apply y coordinate range rule</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">False</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Boolean</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Minimum y coordinate</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">-2500.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Maximum y coordinate</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">2500.0000</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">mm</span></td>
  </tr>
</tbody></table>


## Behaviour

A range of behavioural observations, including time of first arrival, time to first feed, and minimum approach distance may also be calculated (Goetze et al. 2017; Coghlan et al. 2017).


## Interoperable and reproducible annotations

Video imagery enables annotators to work collaboratively to ensure identifications are consistent. A library of reference images, such as that supported by EventMeasure, will assist with identification and training. It is acknowledged that some genera cannot be consistently identified to species level from imagery, so individuals are recorded at genus‐family levels (e.g. flathead: _Platycephalus spp_). For unidentified individuals, a common convention is that fish that are potentially identifiable at a later date are annotated to Genus sp1–10, this permits a batch‐rename at a later stage if the species is successfully identified. Individuals that are clearly unidentifiable to species are annotated as _Genus sp_. 


## Habitat classification 

Information on relief, habitat types, and benthic composition (e.g. percent cover of benthos types) should be recorded from each deployment (Bennett et al. 2016; Collins et al. 2017), to facilitate investigation of fish-habitat relationships and to enable the sampling field of view to be standardised or controlled for in subsequent data analysis (McLean et al. 2016). It is important that these data are annotated consistently and it is recommended that they are mapped to the CATAMI classification scheme (Althaus et al. 2015) and a 0-5 estimate of benthic relief  (Polunin & Roberts 1993; Wilson, Graham & Polunin 2007). Forward facing imagery can be annotated in a range of software, including TransectMeasure from SeaGIS ([seagis.com.au](https://www.seagis.com.au)), BenthoBox ([https://benthobox.com](https://benthobox.com)), CoralNet ([https://coralnet.ucsd.edu/](https://coralnet.ucsd.edu/)), and Squidle+ ([https://squidle.org](https://squidle.org)). Please see the CheckEM website for the [standard operating procedures](https://globalarchivemanual.github.io/CheckEM/articles/manuals/TransectMeasure_annotation_guide.html) and [QAQC scripts](https://globalarchivemanual.github.io/CheckEM/articles/r-workflows/check-habitat.html). An example of habitat composition and relief annotation schema are also provided.


## Quality control and data curation

Quality control and data curation are vital to ensure FAIR data workflows (Wilkinson et al. 2016). All corrections should be made within the original annotation files to ensure data consistency over time. We recommend the following approaches to ensure quality control:



* Annotators should complete “training” videos where species IDs and MaxN are known and can be used to assess competency.
* A different annotator should complete the MaxN and length measurement annotations to provide an independent check of the species identifications.
* Quality assurance should be carried out by a senior video analyst or researcher and involve a random review of 10% of annotated videos and data within a project. If accuracy is below 95 % for all identifications and estimates of MaxN, reannotation should be undertaken.
* Unique identifiers of annotators and dates of when imagery was annotated should be maintained to provide a data checking trail (see Table 2 and Table 3).

R workflows and functions are provided on the CheckEM website available at  ([globalarchivemanual.github.io/CheckEM/](https://globalarchivemanual.github.io/CheckEM/)) to enable validation with regional species lists and likely minimum and maximum sizes for each species. A web based application is also available at ([marine-ecology.shinyapps.io/CheckEM/](https://marine-ecology.shinyapps.io/CheckEM/)) for those who are not familiar with R.


## Data storage, discoverability and release

We encourage open data policies and recommend archiving and sharing stereo-BRUV annotations on global biodiversity data repositories, such as OBIS (Ocean Biogeographic Information System), GBIF (Global Biodiversity Information Facility) and the recently developed GlobalArchive ([globalarchive.org](about:blank)). GlobalArchive is a centralised repository that allows open access and private sharing of fish image annotation data from stereo-BRUVs or similar imagery-based sampling techniques. GlobalArchive allows users to store data in a standardised and secure manner and makes meta-data discoverable, thus encouraging collaboration and synthesis of datasets within the community of practice. We recommend all quality controlled annotation data and any associated calibration, taxa and habitat data should be uploaded to GlobalArchive and we encourage that all data should be made publicly available via the public data option. As an example, the Australian standards for data management, discoverability and release are provided below.


## Australian Standards for Data Management, Release, and Discoverability of Stereo-BRUV Data


### Quality control and data curation

Quality control and data curation are vital, but are potentially time consuming. These time considerations (and associated costs) should be considered during the survey planning stages.

All data corrections should be made within the original annotation files (i.e. within EventMeasure) to ensure data consistency over time. Four complementary approaches for QAQC of data are recommended:



* Analysts should first be adequately trained by completing deployments for which a species composition and density are known to which they can be compared.
* Once the first annotation for a deployment is completed, a different analyst should view each MaxN annotation to double check the species ID and abundance estimates.
* Footage from any previously unrecorded (i.e. range or depth extensions) or unidentifiable species should be sent to the project taxonomist for formal ID. It is important to send footage clip rather than still images.
* R workflows are provided on the [CheckEM website](https://globalarchivemanual.github.io/CheckEM/index.html) to enable comparison with regional species lists and likely minimum and maximum sizes for each species).

It cannot be stressed enough that any corrections should be made to the annotation files before data is exported to GlobalArchive or other repositories (i.e. only QA/QC and validation annotations should be publicly released).

A national stereo-BRUV steering group has been set up to oversee a nationally coordinated BRUV monitoring program (Table 5). Any new stereo-BRUV deployments should be discussed with this steering group to ensure that, where possible, they can be integrated within the national program.

#### Table 5. Australian National BRUV Working Group, as of May 2020.

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-aoc0{background-color:#629ACD;color:#FFF;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-5jfb{background-color:#CFE2F3;text-align:left;vertical-align:top}
</style>
<table class="tg" style="undefined;table-layout: fixed; width: 677px"><colgroup>
<col style="width: 257.88889px">
<col style="width: 247.88889px">
<col style="width: 170.88889px">
</colgroup>
<thead>
  <tr>
    <th class="tg-aoc0"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#FFF;background-color:transparent">Name</span></th>
    <th class="tg-aoc0"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#FFF;background-color:transparent">State</span></th>
    <th class="tg-aoc0"><span style="font-weight:700;font-style:normal;text-decoration:none;color:#FFF;background-color:transparent">Organisation</span></th>
  </tr></thead>
<tbody>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Euan Harvey*</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Western Australia</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Curtin</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Tim Langlois</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Western Australia</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">UWA</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Neville Barrett</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Tasmania</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">IMAS</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Jacquomo Monk</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Tasmania/Victoria</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">IMAS</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Nathan Knott</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">New South Wales</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">NSW DPI</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Hamish Malcolm</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">New South Wales</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">NSW DPI</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Daniel Ierodiaconou</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Victoria</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Deakin</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Charlie Huveneers</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">South Australia</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Flinders University</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Daniel Brock</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">South Australia</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">SA DEWNR</span></td>
  </tr>
  <tr>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Leanne Currey</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">Queensland</span></td>
    <td class="tg-5jfb"><span style="font-weight:400;font-style:normal;text-decoration:none;color:#000;background-color:transparent">AIMS</span></td>
  </tr>
</tbody></table>


<p>
* Chair
</p>


### Data release

GlobalArchive (www.globalarchive.org) is a centralised repository for stereo- and single-camera image annotation of mobile fauna, in particular from Baited Remote Underwater stereo-Video (stereo-BRUVs) and Diver Operated stereo-Video (stereo-DOVs). A user manual for GlobalArchive is available in an open-access[ GitHub repository](https://globalarchivemanual.github.io/). Metadata should be made publicly available via[ GlobalArchive](http://globalarchive.org/) as soon as possible after survey completion and data QA/QC and validation. This should include positional data, as well as the purpose of the sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. Annotations can also be uploaded once complete. Spatial metadata from GlobalArchive data will in the future be harvested by the Australian Ocean Data Network, and the metadata will accordingly be available on their national portal. Until this is done, metadata should be published on both GlobalArchive and AODN to ensure data discoverability.

There is currently no national repository for BRUV imagery so we recommend following agency-specific protocols to ensure public release. A national marine imagery repository (including for BRUV imagery) will be scoped in 2020 and updates provided in this field manual.

If desired by the researcher or requested by the funding agency all quality controlled annotation data and any associated calibration, taxa and habitat data should be uploaded to GlobalArchive ([www.globalarchive.org](http://www.globalarchive.org)) and made publicly available via the public data option. Other funding agency requirements may apply.

Immediate post-trip reporting should be completed by creating metadata records. This can be done far in advance of annotation (scoring) of raw video which is time-consuming and often does not occur for some time following completion of sampling. 

ISO 19115 records should be generated at both the Project¹ and Campaign(s)¹ level. For Project records, the ScopeCode element should be set to “fieldSession”.  Accompanying Campaign metadata record(s) should use the ScopeCode element “dataset” and be linked to the Project record by adding the Project record identifier (the UUID) into the parentIdentifier element of the Campaign record. An example of a Project record with linked Data records (equivalent to Campaign records) in AODN is [here](https://catalogue.aodn.org.au/geonetwork/srv/eng/main.home?uuid=6fc86902-d98d-4ae4-b7f2-00e5b831bb88). This approach improves discoverability, provides context to datasets, and aligns with the schema used by services like [Research Data Australia](https://researchdata.ands.org.au/nesp-mb-project-continental-shelf/686654/).

The Project metadata record should document the project name, purpose, description, location, dates/times, and relevant contacts. The Campaign metadata record(s) should document the purpose of the BRUV sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered.  

¹ See Global Archive definitions [here](https://globalarchivemanual.github.io/definitions).


### Data discoverability

Following the steps listed below will ensure the timely release of video and associated annotation data in a standardised, highly discoverable format.

1. Immediate post-trip reporting should be completed by creating a metadata record documenting the purpose of the BRUV sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. This can be done far in advance of annotation (scoring) of raw video which is time-consuming and often does not occur for some time following completion of sampling.
2. Publish metadata record to the[ Australian Ocean Data Network (AODN) catalogue](http://catalogue.aodn.org.au/geonetwork/srv/eng/main.home) as soon as possible after metadata has been QA/QC. This can be done in one of two ways:
    * If metadata from your agency is regularly harvested by the AODN, follow agency-specific protocols for metadata and data release.
    * Otherwise, metadata records can be created and submitted via the[ AODN Data Submission Tool](https://metadataentry.aodn.org.au/submit). Note that user registration is required, but this is free and immediate.

Lodging metadata with AODN in advance of annotation data being available is an important step in documenting the BRUV campaign and enhancing future discoverability of the data.

1. Annotate video (fish counts and length) using EventMeasure or similar software.
2. Upload annotation data and any associated calibration, taxa and habitat data to GlobalArchive.
3. Upload raw video data to a secure, publicly accessible online repository (contact AODN if you require assistance in locating a suitable repository for large video collections).
4. Add links to GlobalArchive campaign and raw video storage location to previously published metadata record. You may also wish to attach or link a copy of the annotation data directly to the published metadata record.
5. Produce a technical or post-survey report documenting the purpose of the survey, sampling design, sampling locations, sampling equipment specifications, annotation schema, and any challenges or limitations encountered. Provide links to this report in all associated metadata.

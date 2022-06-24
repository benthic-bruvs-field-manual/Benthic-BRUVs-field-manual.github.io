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

Software specifically designed to annotate and measure fish from stereo-video will substantially increase the cost-efficiency and consistency of image annotation (Gomes-Pereira _et al._ 2016). For stereo-video the challenge is not the annotation by the calibration of imagery to provide accurate length and range measurement. Annotation software and packages with measurement capabilities include Vision Measurement System (Harman, Harvey & Kendrick 2003), NIH Image (Dunbrack 12/2006), SEBASTES package in Python (Boldt _et al._ 2018), StereoMorph package in R (Olsen & Westneat 2015), and EventMeasure from SeaGIS ([seagis.com.au](seagis.com.au)). We recommend EventMeasure due to its established workflow, ability to create 3-D stereo-calibrations, and active development, which enables cost-effective and consistent point and stereo annotation of video imagery. Manual image annotation and measurement can be time consuming, but the emerging field of automated image annotation provides promise of increased cost efficiency and collection of novel metrics (Marini _et al._ 2018).


## Annotation metadata

Field metadata ([Supp. 4](https://benthic-bruvs-field-manual.github.io/files/Supp. 4_ Example-Field-and-Labsheet.xlsx)) should be used to populate a unique sample code for each sample and annotation set. Time on the seabed should be annotated to provide a start time for the stereo-BRUV deployment period. It is important that the link between annotations and imagery are maintained.


## Abundance estimates

We recommend all fish be identified to the lowest taxonomic level possible. The standard metric of abundance is MaxN, the maximum number of individuals of a given species present in a single video frame (Priede _et al._ 1994). MaxN is widely used for BRUVs (Whitmarsh _et al._ 2017) conservative, and ensures that no individual is counted more than once (Schobernd, Bacheler & Conn 2013) It has frequently been suggested that MaxN underestimates both small and large-bodied individuals, whereas the only study so far to evaluate this has found MaxN provides a representative sample of size-distributions (Coghlan _et al._ 2017). Syncronise left and right cameras to allow the analyst to determine the range of fish in the field of view and ensure they are within a predefined distance from the cameras. Typically, fish are counted within a maximum distance of 8 m, beyond which length estimates are likely to be inaccurate unless specialist calibrations have been conducted. Annotations of the current MaxN may be updated when individual fish are more clearly visible, and therefore easier to measure, by taking photogrammetric measurements of individual body length at the last MaxN annotated.


## Body-size measurements

Synchronised and calibrated stereo-video streams are used to accurately measure body size. All individuals of each species should be measured at their MaxN. We recommend measuring fork length rather than total length, as it is more easily definable across a range of species. Biomass estimates typically rely on total length, but fork length to total length conversions can be used to complete these calculations (Froese & Pauly 2019). For species where total length can be unreliable or there is no definable fork, body size is estimated using other measures (e.g. disk length for rays). Photogrammetric length measurements are typically made with some degree of error, which can be minimised by measuring individuals when they are as close to cameras as possible with both the nose and the tail-fork clearly visible, still or slowly moving, at an angle less than 45° perpendicular to the cameras. Defining cut-offs for measurement error across projects will help to maintain accurate and precise body-size estimates, we provide recommended stereo-measurement length rules for EventMeasure in [Supp. 5](https://benthic-bruvs-field-manual.github.io/image-annotations#supp-5-recommended-stereo-measurement-length-rules-for-eventmeasure) below. If fish cannot be measured within these parameters, a ‘3D point’ may be used for annotation, which records the 3D location of the fish to ensure it is within the sampling area (Harvey _et al._ 2004). To create a relative abundance metric standardised to a consistent sample area, abundance should be summed from the lengths and 3D points at the MaxN for each species. For biomass estimates, 3D points provide a basis for extrapolating a median length value to fish that could not be measured (Wilson _et al._ 2018). When large tightly packed schools are encountered, fish that cannot be measured should have 3D points. When lengths or 3D points are not possible for every fish, multiple individuals can be assigned to a single length or 3D point, but care should be taken to represent the range of body sizes within a school.


## *Supp 5. Recommended stereo-measurement length rules for EventMeasure.*

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

Information on relief, habitat types, and benthic composition (e.g. percent cover of benthos types) should be recorded from each deployment (Bennett _et al._ 2016; Collins _et al._ 2017), to facilitate investigation of fish-habitat relationships and to enable the sampling field of view to be standardised or controlled for in subsequent data analysis (McLean _et al._ 2016). It is important that these data are annotated consistently and it is recommended that they are mapped to the CATAMI classification scheme (Althaus _et al._ 2015) and a 0-5 estimate of benthic relief  (Polunin & Roberts 1993; Wilson, Graham & Polunin 2007). Forward facing imagery can be annotated in a range of software, including TransectMeasure from SeaGIS ([seagis.com.au](https://www.seagis.com.au)), BenthoBox ([https://benthobox.com](https://benthobox.com)), CoralNet ([https://coralnet.ucsd.edu/](https://coralnet.ucsd.edu/)), and Squidle+ ([https://squidle.org](https://squidle.org)). Please see this [GitHub repository](www.github.com/UWA-Marine-Ecology-Group-projects/forward-facing-benthic-composition-annotation) for the standard operating procedures and QAQC scripts. An example of habitat composition and relief annotation schema are also provided.


## Quality control and data curation

Quality control and data curation are vital to ensure FAIR data workflows (Wilkinson _et al._ 2016). All corrections should be made within the original annotation files to ensure data consistency over time. We recommend the following approaches to ensure quality control:



*   Annotators should complete “training” videos where species IDs and MaxN are known and can be used to assess competency.
*   A different annotator should complete the MaxN and length measurement annotations to provide an independent check of the species identifications.
*   Quality assurance should be carried out by a senior video analyst or researcher and involve a random review of 10% of annotated videos and data within a project. If accuracy is below 95 % for all identifications and estimates of MaxN, reannotation should be undertaken.
*   Unique identifiers of annotators and dates of when imagery was annotated should be maintained to provide a data checking trail (see [Supp. 4](https://benthic-bruvs-field-manual.github.io/files/Supp. 4_ Example-Field-and-Labsheet.xlsx)).

R workflows and function packages are provided in a GitHub repository (Langlois 2020) to enable validation with regional species lists and likely minimum and maximum sizes for each species.


## Data storage, discoverability and release

We encourage open data policies and recommend archiving and sharing stereo-BRUV annotations on global biodiversity data repositories, such as OBIS (Ocean Biogeographic Information System), GBIF (Global Biodiversity Information Facility) and the recently developed GlobalArchive ([globalarchive.org](about:blank)). GlobalArchive is a centralised repository that allows open access and private sharing of fish image annotation data from stereo-BRUVs or similar imagery-based sampling techniques. GlobalArchive allows users to store data in a standardised and secure manner and makes meta-data discoverable, thus encouraging collaboration and synthesis of datasets within the community of practice. We recommend all quality controlled annotation data and any associated calibration, taxa and habitat data should be uploaded to GlobalArchive and we encourage that all data should be made publicly available via the public data option. As an example, the Australian standards for data management, discoverability and release are provided in [Supp. 6](https://benthic-bruvs-field-manual.github.io/image-annotations#supp-6-australian-standards-for-data-management-release-and-discoverability-of-stereo-bruv-data).

## *Supp 6: Australian standards for data management, release, and discoverability of stereo-BRUV data*
## Quality control and data curation

Quality control and data curation are vital, but are potentially time consuming. These time considerations (and associated costs) should be considered during the survey planning stages.

All data corrections should be made within the original annotation files (i.e. within EventMeasure) to ensure data consistency over time. Four complementary approaches for QAQC of data are recommended:



*   Analysts should first be adequately trained by completing deployments for which a species composition and density are known to which they can be compared.
*   Once the first annotation for a deployment is completed, a different analyst should view each MaxN annotation to double check the species ID and abundance estimates.
*   Footage from any previously unrecorded (i.e. range or depth extensions) or unidentifiable species should be sent to the project taxonomist for formal ID. It is important to send footage clip rather than still images.
*   R workflows are provided in a[ GitHub repository](https://github.com/TimLanglois/Stereo-or-mono-video-annotation-workflows) to enable comparison with regional species lists and likely minimum and maximum sizes for each species[ (Langlois et al. 2017)](https://paperpile.com/c/cxZoCG/dSL3).

It cannot be stressed enough that any corrections should be made to the annotation files before data is exported to GlobalArchive or other repositories (i.e. only QA/QC and validation annotations should be publicly released).

A national stereo-BRUV steering group has been set up to oversee a nationally coordinated BRUV monitoring program (Supp. 7). Any new stereo-BRUV deployments should be discussed with this steering group to ensure that, where possible, they can be integrated within the national program.


## Data release

GlobalArchive (www.globalarchive.org) is a centralised repository for stereo- and single-camera image annotation of mobile fauna, in particular from Baited Remote Underwater stereo-Video (stereo-BRUVs) and Diver Operated stereo-Video (stereo-DOVs). A user manual for GlobalArchive is available in an open-access[ GitHub repository](https://globalarchivemanual.github.io/). Metadata should be made publicly available via[ GlobalArchive](http://globalarchive.org/) as soon as possible after survey completion and data QA/QC and validation. This should include positional data, as well as the purpose of the sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. Annotations can also be uploaded once complete. Spatial metadata from GlobalArchive data will in the future be harvested by the Australian Ocean Data Network, and the metadata will accordingly be available on their national portal. Until this is done, metadata should be published on both GlobalArchive and AODN to ensure data discoverability.

There is currently no national repository for BRUV imagery so we recommend following agency-specific protocols to ensure public release. A national marine imagery repository (including for BRUV imagery) will be scoped in 2020 and updates provided in this field manual.

If desired by the researcher or requested by the funding agency all quality controlled annotation data and any associated calibration, taxa and habitat data should be uploaded to GlobalArchive ([www.globalarchive.org](www.globalarchive.org)) and made publicly available via the public data option. Other funding agency requirements may apply.

 

Immediate post-trip reporting should be completed by creating metadata records. This can be done far in advance of annotation (scoring) of raw video which is time-consuming and often does not occur for some time following completion of sampling. 

 

ISO 19115 records should be generated at both the Project¹ and Campaign(s)¹ level. For Project records, the ScopeCode element should be set to “fieldSession”.  Accompanying Campaign metadata record(s) should use the ScopeCode element “dataset” and be linked to the Project record by adding the Project record identifier (the UUID) into the parentIdentifier element of the Campaign record. An example of a Project record with linked Data records (equivalent to Campaign records) in AODN is [here](https://catalogue.aodn.org.au/geonetwork/srv/eng/main.home?uuid=6fc86902-d98d-4ae4-b7f2-00e5b831bb88). This approach improves discoverability, provides context to datasets, and aligns with the schema used by services like [Research Data Australia](https://researchdata.ands.org.au/nesp-mb-project-continental-shelf/686654/).

 

The Project metadata record should document the project name, purpose, description, location, dates/times, and relevant contacts. The Campaign metadata record(s) should document the purpose of the BRUV sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered.  

 

¹ See Global Archive definitions [here](https://globalarchivemanual.github.io/definitions).




## Data discoverability

Following the steps listed below will ensure the timely release of video and associated annotation data in a standardised, highly discoverable format.



1. Immediate post-trip reporting should be completed by creating a metadata record documenting the purpose of the BRUV sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. This can be done far in advance of annotation (scoring) of raw video which is time-consuming and often does not occur for some time following completion of sampling.
2. Publish metadata record to the[ Australian Ocean Data Network (AODN) catalogue](http://catalogue.aodn.org.au/geonetwork/srv/eng/main.home) as soon as possible after metadata has been QA/QC. This can be done in one of two ways:
    *   If metadata from your agency is regularly harvested by the AODN, follow agency-specific protocols for metadata and data release.
    *   Otherwise, metadata records can be created and submitted via the[ AODN Data Submission Tool](https://metadataentry.aodn.org.au/submit). Note that user registration is required, but this is free and immediate.

Lodging metadata with AODN in advance of annotation data being available is an important step in documenting the BRUV campaign and enhancing future discoverability of the data.



1. Annotate video (fish counts and length) using EventMeasure or similar software.
2. Upload annotation data and any associated calibration, taxa and habitat data to GlobalArchive.
3. Upload raw video data to a secure, publicly accessible online repository (contact AODN if you require assistance in locating a suitable repository for large video collections).
4. Add links to GlobalArchive campaign and raw video storage location to previously published metadata record. You may also wish to attach or link a copy of the annotation data directly to the published metadata record.
5. Produce a technical or post-survey report documenting the purpose of the survey, sampling design, sampling locations, sampling equipment specifications, annotation schema, and any challenges or limitations encountered. Provide links to this report in all associated metadata.

## *Supp. 7: Australian National BRUV working group, as of May 2020.*

<table>
  <tr>
   <td>Name
   </td>
   <td>State
   </td>
   <td>Organisation
   </td>
  </tr>
  <tr>
   <td>Euan Harvey*
   </td>
   <td>Western Australia
   </td>
   <td>Curtin
   </td>
  </tr>
  <tr>
   <td>Tim Langlois
   </td>
   <td>Western Australia
   </td>
   <td>UWA
   </td>
  </tr>
  <tr>
   <td>Neville Barrett
   </td>
   <td>Tasmania
   </td>
   <td>IMAS
   </td>
  </tr>
  <tr>
   <td>Jacquomo Monk
   </td>
   <td>Tasmania/Victoria
   </td>
   <td>IMAS
   </td>
  </tr>
  <tr>
   <td>Nathan Knott
   </td>
   <td>New South Wales
   </td>
   <td>NSW DPI
   </td>
  </tr>
  <tr>
   <td>Hamish Malcolm
   </td>
   <td>New South Wales
   </td>
   <td>NSW DPI
   </td>
  </tr>
  <tr>
   <td>Daniel Ierodiaconou
   </td>
   <td>Victoria
   </td>
   <td>Deakin
   </td>
  </tr>
  <tr>
   <td>Charlie Huveneers
   </td>
   <td>South Australia
   </td>
   <td>Flinders University
   </td>
  </tr>
  <tr>
   <td>Daniel Brock
   </td>
   <td>South Australia
   </td>
   <td>SA DEWNR
   </td>
  </tr>
  <tr>
   <td>Leanne Currey
   </td>
   <td>Queensland
   </td>
   <td>AIMS
   </td>
  </tr>
</table>


<p>
* Chair
</p>

### *Supp. 8: Habitat annotation of stereo-BRUV imagery*
#### Benthic composition and relief for horizontally facing imagery

We have developed a simple approach to characterise benthic composition and complexity from horizontally facing imagery (including stereo-BRUVs and panoramic drop cameras), adapting existing standardised schema for benthic composition ([CATAMI classification scheme](https://github.com/catami/catami.github.com/blob/master/catami-docs/CATAMI%20class_PDFGuide_V4_20141218.pdf)) and benthic complexity <sup><a href="https://paperpile.com/c/0wnItn/M1vE">1</a></sup>.

The annotation approach is rapid and produces point annotation-level composition and mean and standard deviation estimates of complexity, which enable flexible modelling of habitat occurrence and fish-habitat relationships.

This github repository contains:

* A [TransectMeasure](https://github.com/GlobalArchiveManual/forward-facing-habitat-annotation/blob/master/seagis.com.au) Standard Operating Procedures (below)
* A [script](https://github.com/BrookeGibbons/forward-facing-habitat-annotation/blob/master/01_format-dot-point-measurements.R):
    * to check the exports from TransectMeasure against a metadata *.csv
    * to convert the raw TransectMeasure annotations into a tidy dataset.
* Example [broad ](https://github.com/BrookeGibbons/forward-facing-habitat-annotation/blob/master/TM%20schema_BROAD%20ONLY.txt)schema file with only broad attributes
* Example standard schema file with broad, morphology and type attributes
* Example [detailed schema](https://github.com/BrookeGibbons/forward-facing-habitat-annotation/blob/master/TM%20schema_BROAD.MORPH.TYPE.txt) text file with broad, morphology, type and fine attributes


#### Standard Operating Procedure

#### 1. Load images and attribute file

* Open the program TransectMeasure and you will be welcomed with a blank screen (Figure 1).
* To start an analysis for a new set of images: “Measurement” > “New measurement file” (Figure 2). Select “Read from file ...”.
* Locate the folder where your images have been stored: “Picture” > “Set picture directory ...” (Figure 3).
* Load the first image to be analysed: “Picture” > “Load picture ...” (Figure 3).
    * Retake images if they are unfocused and blurry or when visibility is low.
    * For stereo-BRUV imagery, left images are annotated, and for panoramic drop camera imagery, top images are annotated.
* To load the attribute file containing all of the CATAMI habitat classification codes: “Measurements” > “Load attribute file ...” > The attribute file is a text file containing the information necessary for populating the drop down tabs when classifying your image (Figure 4).

![alt_text](images/figures/hab1.jpg "image_tooltip")

##### Figure 1: TransectMeasure initial opening screen. 

![alt_text](images/figures/hab2.jpg "image_tooltip")

##### Figure 2: Creating a new measurement file in TransectMeasure.

![alt_text](images/figures/hab3.jpg "image_tooltip")

##### Figure 3: Setting the picture directory and loading the image in TransectMeasure.

![alt_text](images/figures/hab4.png "image_tooltip")

##### Figure 4: Loading the attribute file in TransectMeasure.


#### 2. Setting and overlaying the grid

* To set up the area of interest: Hold shift and left click on the four corners of the rectangle that forms the lower 50% of the image > Right click > “Add new area of interest” (Figure 5). 
* To set up the points: “Measurements” > “Dot configuration ...”. Set accordingly: Random dots, ‘Number of dots’ = 20 and uncheck the “Overlay rectangles” box (Figure 6). This will allow you to classify the benthic composition according to 20 randomly generated points over the lower 50% of the screen. You should only need to change these settings the first time you use the program on your computer.
* To overlay the points: Right click on an image and select “Overlay dots” (Figure 7). The name of the image will then appear in the table to the left of the image. For all subsequent images, you will need to first right click and select “Use last area of interest” before adding dots to ensure that random points are only added to the lower 50% of the image (Figure 8). 

NOTE: To annotate composite imagery, multiple areas of interest will need to be added corresponding to the images contained in the composite image, with points added to imagery after specifying areas of interest using “cntrl+ right click” > “Add dots” > “Add to the existing points” (Figure 9).

![alt_text](images/figures/hab5.png "image_tooltip")

##### Figure 5: Adding a new area of interest in TransectMeasure.

![alt_text](images/figures/hab6.png "image_tooltip")

##### Figure 6: Setting the dot configuration in TransectMeasure.

![alt_text](images/figures/hab7.png "image_tooltip")

##### Figure 7: Adding dots in TransectMeasure.

![alt_text](images/figures/hab8.png "image_tooltip")

##### Figure 8: Example of a stereo-BRUV image with random points added to the lower 50% of the image ready for annotation. 

![alt_text](images/figures/hab9.png "image_tooltip")

##### Figure 9: Example of a fully annotated panoramic drop camera composite image. The red box in the bottom right image denotes the custom area of interest used to overlay the annotation points in TransectMeasure.

#### 3. Classifying the benthic composition in an image

* Left click on a point to display the “Attribute editor” (Figure 10)
* Select the biota that lies directly underneath the point from the “BROAD” dropdown (includes benthos, un/consolidated substrate, open water and unknown). 

Note: Zoom into an image to analyse the benthic composition more closely by adjusting the "Zoom" value at the top left of the window before holding down the ctrl key and hovering your cursor over the area that you would like to zoom to.

* Continue to populate each dropdown (where possible) after “BROAD” (i.e. “MORPHOLOGY” > “TYPE” ). The “MORPHOLOGY” and “TYPE” drop down options will change depending on which “BROAD” option is chosen . Select “Clear” to reset the dropdowns for all of the categories (Figure 10).
* The dropdown for “Code” is automatically filled by an eight digit code once all possible categories have been selected for that 'rectangle'. Codes are sourced from the CATAMI classification scheme and are dependent on the combination of the first three options selected (i.e. “BROAD”, “MORPHOLOGY” and “TYPE”).
* The dropdown for “FieldOfView” indicates how the camera is positioned when it lands on the substrate. This dropdown includes options for; 
    * Facing Down (No open water visible and the system is facing the benthos/substrate).
    * Facing Up (No substrate visible and the system is facing towards the surface).
    * Limited (Camera system has landed on its side, upside down or the field of view is badly obstructed by benthos or substrate within ~1m of the camera).
    * Open (Camera system has landed upright and level on the substrate with an adequate amount of benthos/substrate available for classification). 
* Relief should not be annotated at this stage, with details on how to annotate relief outlined in the following section (_“4. Classifying the relief of an image”_).

![alt_text](images/figures/hab10.jpg "image_tooltip")

##### Figure 10: The ‘attribute editor’ window within TransectMeasure.


#### 4. Classifying the relief of an image

Annotation of relief will need to be annotated in a separate TransectMeasure file (.TMObs), which can be set up by following the same steps defined in ‘1. Load images and attribute file’. 

* To set up the grid: “Measurements” > “Dot configuration ...”. Set accordingly: Grided dots, ‘Dots across image’ = 5, ’Dots down image’ = 4 and check the “Overlay rectangles” box (Figure 11). This will allow you to classify the relief according to 20 gridded points. You should only need to change these settings the first time you use the program on your computer.
* To overlay the grid: Right click on an image and select “Overlay dots” (Figure 12). The name of the image will then appear in the table to the left of the image. 

NOTE: For composite imagery that consists of multiple images, gridded dot configuration can be changed to reflect multiple images. For panoramic drop camera imagery containing four images, we overlay 10 dots across the image and 8 dots down the image (Figure 14). 

* Left click on a point to display the “Attribute editor” (Figure 15)
* Select the relevant field of view and relief score for the whole rectangle from the “FieldOfView” and “Relief” dropdowns. 
* The dropdown for “FieldOfView” indicates how the camera is positioned when it lands on the substrate. This dropdown includes options for; 
    * Facing Down (No open water visible and the system is facing the benthos).
    * Facing Up (No substrate visible and the system is facing towards the surface).
    * Limited (Camera system has landed on its side, upside down or the field of view is badly obstructed by benthos or substrate within ~1m of the camera).
    * Open (Camera system has landed upright and level on the substrate with an adequate amount of habitat available for classification). 
* The dropdown for “Relief” indicates the structural complexity of the substrate and associated benthos. This dropdown includes six distinct categories adapted from Wilson et al. (2006), which are;
    * **0. **Flat substrate, sandy, rubble with few features. ~0 substrate slope
    * **1. ** Some relief features amongst mostly flat substrate/sand/rubble. &lt;45 degree substrate slope
    * **2. **Mostly relief features amongst some flat substrate or rubble. ~45 substrate slope
    * **3. **Good relief structure with some overhangs. >45 substrate slope
    * **4. **High structural complexity, fissures and caves. Vertical wall. ~90 substrate slope.
    * **5. **Exceptional structural complexity, numerous large holes and caves. Vertical wall. ~90 substrate slope.

NOTE: Any ‘rectangle’ that has some form of benthos/substrate visible should be classified for _Relief _(even if open water makes up the majority of the grid).

![alt_text](images/figures/hab11.png "image_tooltip")

##### Figure 11: Setting the dot configuration in TransectMeasure.

![alt_text](images/figures/hab12.png "image_tooltip")

##### Figure 12: Adding dots to an image in TransectMeasure.

![alt_text](images/figures/hab13.png "image_tooltip")

##### Figure 13: Example of a stereo-BRUV image annotated for relief, showing measurements labels for field of view.

![alt_text](images/figures/hab14.png "image_tooltip")

##### Figure 14: Example of a panoramic drop camera composite image annotated for relief, showing annotation labels for field of view.

![alt_text](images/figures/hab15.jpg "image_tooltip")

##### Figure 15: The ‘attribute editor’ window within TransectMeasure.


#### 5. Saving and exporting from TransectMeasure

* To save your work: “Measurements” > “Write to file ...” (Figure 16). This creates a *.TMObs file where your benthic classifications will be saved.
* To export TMObs file: “Program” > “Batch text file output ...” (Figure 17)
* The following box should appear: Double click to the right of the ✓ (under “Data”) in the “Input file directory” row, then locate the folder where your *.TMObs file has been saved, do the same for the “output file directory” to specify the folder location for saving your text file (Figure 18). Now select “Process”. This will generate an output text file that can be processed using the scripts included in the GitHub repository (see ‘Annotation summary and quality control’). 

![alt_text](images/figures/hab16.jpg "image_tooltip")

##### Figure 16: Writing to file in TransectMeasure in order to save image observations.

![alt_text](images/figures/hab17.jpg "image_tooltip")

##### Figure 17: The ‘batch text file output’ option in TransectMeasure.

![alt_text](images/figures/hab18.jpg "image_tooltip")

##### Figure 18: Input and output file directory options for batch text file outputs in TransectMeasure.

### Recommended approaches

For standard (rapid) assessment of _Benthic Composition_, _FieldOfView_ and _Relief _we recommend using ONLY the: “BROAD” classification within the _Benthic Composition_ and _FieldOfView_ and _Relief_. An experienced analyst would be able to annotate this schema to over 200 images a day.

**OR**

For detailed assessment of _Benthic Composition_ (where coral bleaching or macroalgae composition was of interest), _FieldOfView_ and _Relief_ we recommend using all the classes in _Benthic Composition_ (“BROAD” > “MORPHOLOGY” > “TYPE” and _FieldOfView_ and _Relief_. An experienced analyst would be able to annotate this schema to over 120 images a day.

Forward facing imagery can be annotated in a range of software, including TransectMeasure from SeaGIS ([seagis.com.au](https://www.seagis.com.au/)), ReefCloud ([reefcloud.ai](http://reefcloud.ai)), CoralNet ([coralnet.ucsd.edu](https://coralnet.ucsd.edu/)), and Squidle+ ([squidle.org](https://squidle.org/)). 


#### Annotation summary and quality control

All corrections should be made within the original annotation files to ensure data consistency over time. We recommend the following approaches to ensure quality control:


* Check that _FieldOfView_, _Relief_ and _Benthic Composition_ have been entered for every successful deployment (see R scripts included in the GitHub repository- ‘[forward-facing-benthic-composition-annotation](https://github.com/UWA-Marine-Ecology-Group-projects/forward-facing-benthic-composition-annotation)’).
* Check that the image names match the metadata sample names.
* Check all successful deployments have benthic composition data.

#### Examples of publications that have used this or earlier versions of this SOP

1.	Wilson, S. K., Graham, N. A. J., Pratchett, M. S., Jones, G. P. & Polunin, N. V. C. Multiple disturbances and the global degradation of coral reefs: are reef fishes at risk or resilient? Glob. Chang. Biol. 12, 2220–2234 (2006).
2.	McLean, D. L. et al. Distribution, abundance, diversity and habitat associations of fishes across a bioregion experiencing rapid coastal development. Estuarine, Coastal and Shelf Science 178, 36–47 (2016).
3.	McLean, D. L. et al. Using industry ROV videos to assess fish associations with subsea pipelines. Cont. Shelf Res. 141, 76–97 (2017).
4.	Bond, T., Partridge, J. C., Taylor, M. D., Cooper, T. F. & McLean, D. L. The influence of depth and a subsea pipeline on fish assemblages and commercially fished species. PLoS One 13, e0207703 (2018).
5.	Bond, T. et al. Fish associated with a subsea pipeline and adjacent seafloor of the North West Shelf of Western Australia. Mar. Environ. Res. (2018) doi:10.1016/j.marenvres.2018.08.003.
6.	Bond, T. et al. Diel shifts and habitat associations of fish assemblages on a subsea pipeline. Fish. Res. 206, 220–234 (2018).
7.	Lester, E. et al. Drivers of variation in occurrence, abundance, and behaviour of sharks on coral reefs. Sci. Rep. 12, 728 (2022).
8.	Lester, E. K. et al. Relative influence of predators, competitors and seascape heterogeneity on behaviour and abundance of coral reef mesopredators. Oikos 130, 2239–2249 (2021).
9.	Rolim, F. A. et al. Network of small no-take marine reserves reveals greater abundance and body size of fisheries target species. PLoS One 14, e0204970 (2019).
10.	Rolim, F. A., Rodrigues, P. F. C. & Gadig, O. B. F. Baited videos to assess semi-aquatic mammals: occurrence of the neotropical otter Lontra longicaudis (Carnivora: Mustelidae) in a marine coastal island in São Paulo, Southeast Brazil. Mar. Biodivers. (2018) doi:10.1007/s12526-018-0868-7.
11.	Haberstroh, A. J., McLean, D., Holmes, T. H. & Langlois, T. Baited video, but not diver video, detects a greater contrast in the abundance of two legal-size target species between no-take and fished zones. Mar. Biol. 169, (2022).
12.	Piggott, C. V. H., Depczynski, M., Gagliano, M. & Langlois, T. J. Remote video methods for studying juvenile fish populations in challenging environments. J. Exp. Mar. Bio. Ecol. 532, 151454 (2020).
13.	MacNeil, M. A. et al. Global status and conservation potential of reef sharks. Nature 583, 801–806 (2020).
14.	Goetze, J. S. et al. Drivers of reef shark abundance and biomass in the Solomon Islands. PLoS One 13, e0200960 (2018).

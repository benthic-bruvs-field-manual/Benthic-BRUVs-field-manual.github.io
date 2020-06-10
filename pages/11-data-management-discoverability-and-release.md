---
layout: home
permalink: /standards
title: "Australian standards for data management, release, and discoverability of stereo-BRUV data"
excerpt: ""
image:
  feature: /banners/04_banner.jpg
---
{% include toc.html class="toc-left" h_min=2 h_max=2 %}

<h2><strong>Quality control and data curation</strong></h2>


<p>
Quality control and data curation are vital, but are potentially time consuming. These time considerations (and associated costs) should be considered during the survey planning stages.
</p>
<p>
All data corrections should be made within the original annotation files (i.e. within EventMeasure) to ensure data consistency over time. Four complementary approaches for QAQC of data are recommended:
</p>
<ul>

<li>Analysts should first be adequately trained by completing deployments for which a species composition and density are known to which they can be compared.

<li>Once the first annotation for a deployment is completed, a different analyst should view each MaxN annotation to double check the species ID and abundance estimates.

<li>Footage from any previously unrecorded (i.e. range or depth extensions) or unidentifiable species should be sent to the project taxonomist for formal ID. It is important to send footage clip rather than still images.

<li>R workflows are provided in a<a href="https://github.com/TimLanglois/Stereo-or-mono-video-annotation-workflows"> GitHub repository</a> to enable comparison with regional species lists and likely minimum and maximum sizes for each species<a href="https://paperpile.com/c/cxZoCG/dSL3"> (Langlois et al. 2017)</a>.
</li>
</ul>
<p>
It cannot be stressed enough that any corrections should be made to the annotation files before data is exported to GlobalArchive or other repositories (i.e. only QA/QC and validation annotations should be publicly released).
</p>
<p>
A national stereo-BRUV steering group has been set up to oversee a nationally coordinated BRUV monitoring program (Supp. 7). Any new stereo-BRUV deployments should be discussed with this steering group to ensure that, where possible, they can be integrated within the national program.
</p>
<h2><strong>Data release</strong></h2>


<p>
GlobalArchive (www.globalarchive.org) is a centralised repository for stereo- and single-camera image annotation of mobile fauna, in particular from Baited Remote Underwater stereo-Video (stereo-BRUVs) and Diver Operated stereo-Video (stereo-DOVs). A user manual for GlobalArchive is available in an open-access<a href="https://globalarchivemanual.github.io/"> GitHub repository</a>. Metadata should be made publicly available via<a href="http://globalarchive.org/"> GlobalArchive</a> as soon as possible after survey completion and data QA/QC and validation. This should include positional data, as well as the purpose of the sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. Annotations can also be uploaded once complete. Spatial metadata from GlobalArchive data will in the future be harvested by the Australian Ocean Data Network, and the metadata will accordingly be available on their national portal. Until this is done, metadata should be published on both GlobalArchive and AODN to ensure data discoverability.
</p>
<p>
There is currently no national repository for BRUV imagery so we recommend following agency-specific protocols to ensure public release. A national marine imagery repository (including for BRUV imagery) will be scoped in 2020 and updates provided in this field manual.
</p>
<p>
If desired by the researcher or requested by the funding agency all quality controlled annotation data and any associated calibration, taxa and habitat data should be uploaded to GlobalArchive (<a href="http://www.globalarchive.org">www.globalarchive.org</a>) and made publicly available via the public data option.
</p>
<h2><strong>Data discoverability</strong></h2>


<p>
Following the steps listed below will ensure the timely release of video and associated annotation data in a standardised, highly discoverable format.
</p>
<ol>

<li>Immediate post-trip reporting should be completed by creating a metadata record documenting the purpose of the BRUV sampling campaign, the survey design, all sampling locations, equipment specifications, and any challenges or limitations encountered. This can be done far in advance of annotation (scoring) of raw video which is time-consuming and often does not occur for some time following completion of sampling.

<li>Publish metadata record to the<a href="http://catalogue.aodn.org.au/geonetwork/srv/eng/main.home"> Australian Ocean Data Network (AODN) catalogue</a> as soon as possible after metadata has been QA/QC. This can be done in one of two ways: 
<ul>
 
<li>If metadata from your agency is regularly harvested by the AODN, follow agency-specific protocols for metadata and data release.
 
<li>Otherwise, metadata records can be created and submitted via the<a href="https://metadataentry.aodn.org.au/submit"> AODN Data Submission Tool</a>. Note that user registration is required, but this is free and immediate.
</li> 
</ul>
</li> 
</ol>
<p>
Lodging metadata with AODN in advance of annotation data being available is an important step in documenting the BRUV campaign and enhancing future discoverability of the data.
</p>
<ol>

<li>Annotate video (fish counts and length) using EventMeasure or similar software.

<li>Upload annotation data and any associated calibration, taxa and habitat data to GlobalArchive.

<li>Upload raw video data to a secure, publicly accessible online repository (contact AODN if you require assistance in locating a suitable repository for large video collections).

<li>Add links to GlobalArchive campaign and raw video storage location to previously published metadata record. You may also wish to attach or link a copy of the annotation data directly to the published metadata record.

<li>Produce a technical or post-survey report documenting the purpose of the survey, sampling design, sampling locations, sampling equipment specifications, annotation schema, and any challenges or limitations encountered. Provide links to this report in all associated metadata.
</li>
</ol>
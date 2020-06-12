---
permalink: /sampling-design
title: "Sampling Design"
excerpt: "<br>"
image:
  feature: /banners/04_banner.jpg
layout: home

---
{% include toc.html class="toc-left" h_min=2 h_max=2 %}


Sampling strategies should be designed to ensure valid inferences and interpretations of resulting data (Smith, Anderson & Pawley 2017). We recommend spatially balanced statistical routines, such as R package MBHdesign (Foster _et al._ 2019), which can incorporate environmental information and legacy sites to create sampling designs with known inclusion probabilities (Foster _et al._ 2017, 2018). Due to the need to revisit each site to retrieve stereo-BRUVs after deployment, spatially balanced designs may be inefficient for sampling large regions (>10 minutes transit time between samples), and clustered sampling designs may be preferred (Hill _et al._ 2018).

Individual stereo-BRUV samples should be separated to reduce the likelihood of non-independence due to individuals being concurrently sampled by adjacent stereo-BRUVs. Separation distance will depend on the mobility of the species and the habitat being studied, for typical demersal fish assemblages a minimum of 400 m for one-hour deployments is recommended (Bond _et al._ 2018b) or 250 m for 30 minute deployments (Cappo, Speare & Wassenberg 2001).
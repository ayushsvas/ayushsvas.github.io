---
layout: page
title: Machine Learning
description: Sandstone Classification Problem
img: 
importance: 3
category: work
---

Sandstones originate from different geological epochs and have different formation histories. Does the geometry of the pore volume (yellow in the images below) inside a matrix of sintered sand grains (blue) capture enough of these difference such that one can predict the type of sandstone from the image of a two-dimensional slice of a sandstone?

This dataset of this competition consists of 4 different types of sandstone: Bentheim (B49), Berea (Br46), Fontainebleau (F57), and Gildehausen (G44). The raw data was captured as three-dimensional volumes with Computed X-ray Tomography. Subsequently two-dimensional slices of a size of 150 by 150 pixels were cut out of these volumes. The images below give an idea of the four different specimen (at a resolution of 400 by 400 pixels).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/B49.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Br46.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/F57.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/G44.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">

</div>

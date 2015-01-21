---
layout: post
title: polycrunch
sketchpath: sketches/01_20_2015_polycrunch
imagenames: 
- polycrunch.png
blendnames: 
- polycrunch.blend
---

{% comment %} 
Explanation of liquid code. 
- Loop through the array of imagenames in the front matter. 
  - Build an image path from the front matter variables. 
  - Load that image path and make it a link, so that clicking takes you to a full resolution image. 
{% endcomment %}

{% for imagename in page.imagenames %}
{% capture imagepath %}{{ site.baseurl }}/{{ page.sketchpath }}/{{ imagename }}{% endcapture %}
[![{{ imagename }}]({{ imagepath }})]({{ imagepath}})
{% endfor %}

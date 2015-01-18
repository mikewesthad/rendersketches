---
layout: post
title: finfinity
sketchpath: sketches/06_22_2014_finfinity
imagenames: 
- finfinity.png
blendnames: 
- finfinity.blend
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

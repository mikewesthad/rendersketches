---
layout: post
title: softbodies
sketchpath: sketches/10_15_2014_softbodies
imagenames: 
- softbodies_34.png
- softbodies_35.png
- softbodies_36.png
- softbodies_37.png
blendnames: 
- softbodies_longer_higherquality.blend
coverimagename: softbodies_37.png
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

<div class="flex-video widescreen" style="margin: 0 auto;text-align:center;">
<iframe src="//player.vimeo.com/video/109319201" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>
</div>
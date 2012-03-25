---
layout: page
title: SimpleCV - GSoC
tagline: Google Summer of Code Home Page
---
{% include JB/setup %}

<p>
SimpleCV is happy to announce its participation in the 2012 <a href="http://code.google.com/soc/">Google Summer of Code</a>. We are looking for up to three talented students who want to become experts in computer vision and Python and work with a top-notch team on professional open-source development.
</p>

<hr>
<p>
  <b>
    You must submit your application through the Google Summer of Code website (NOTE THAT APPLICATIONS WILL NOT BE ACCEPTED BY GOOGLE UNTIL 3/26/2012).
    We cannot take applications directly.
  </b>
  Make sure to read the <a href="apply.html">How to apply</a> section before trying to contact anyone.
</p>
<hr>

<p>
Recent Posts
</p>
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>




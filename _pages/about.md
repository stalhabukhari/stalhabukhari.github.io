---
permalink: /
author_profile: true
---

<p align="justify">
Hi!
I'm <b>Talha</b> (طلحہ).
I'm a PhD student in Computer Science and Fulbright Scholar at <a href="https://www.purdue.edu" style="font-weight:bold">Purdue</a>.
My current research focus is on Learning Generative Models and Implicit Neural Representations for Robot Motion Planning tasks.
</p>

<p align="justify">
Previously, I was a ML Software Engineer at <a href="https://pointivo.com" style="font-weight:bold">Pointivo</a> where I developed and deployed ML pipelines to derive insights for 3D asset inspection.
Before that, I studied Mechatronics & Control Engineering at <a href="https://www.uet.edu.pk" style="font-weight:bold">UET Lahore</a>, and Signal Processing and Machine Learning at <a href="https://sbasse.lums.edu.pk" style="font-weight:bold">LUMS</a>.
</p>

<h2> Research Interests
</h2>
Machine Learning, Motion Planning, Scene Understanding

<h2> Selected Publications
</h2>

<!-- Publications list -->
{% include base_path %}

<table>
<tbody>

{% for post in site.publications reversed %}

{% if post.header.teaser %}
    {% capture teaser %}{{ post.header.teaser }}{% endcapture %}
{% else %}
    {% assign teaser = site.teaser %}
{% endif %}

<!-- {% if post.id %}
    {% assign title = post.title | markdownify | remove: "<p>" | remove: "</p>" %}
{% else %}
    {% assign title = post.title %}
{% endif %} -->
{% assign title = post.title %}

<tr class="list__item" itemscope itemtype="http://schema.org/CreativeWork">
  <td>
    {% if teaser %}
      <img src="{{ teaser | prepend: "/images/" | prepend: base_path }}" alt=""
      width="200">
    {% endif %}
  </td>

  <td>
    <!-- Title -->
    <b>{{ title }}</b>
    <br>
    <!-- Authors -->
    {{ post.authors }}. <i>{{ post.venue }}</i>. {{ post.year }}
    <br>
    <!-- paper -->
    {% if post.paper %}
      <a href="{{ post.paper }}">
      <i class="fa-solid fa-file-pdf fa-lg"></i>
      </a>
    {% endif %}
    <!-- Code -->
    {% if post.code %}
      <a href="{{ post.code }}">
      <i class="fa-brands fa-github fa-lg" style="margin-left:2px"></i>
      </a>
    {% endif %}
    <!-- Website -->
    {% if post.website %}
      <a href="{{ post.website }}">
      <i class="fa-solid fa-globe fa-lg"></i>
      </a>
    {% endif %}
    <!-- Data -->
    {% if post.data %}
      <a href="{{ post.data }}">
      <i class="fa-solid fa-database fa-lg" style="margin-left:2px"></i>
      </a>
    {% endif %}
  </td>
</tr>

{% endfor %}

</tbody>
</table>

<!-- Embedded Twitter Timeline -->
<!-- <a class="twitter-timeline" data-height="450" data-dnt="true" data-theme="light" href="https://twitter.com/stalhabukhari?ref_src=twsrc%5Etfw">Tweets by stalhabukhari</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> -->

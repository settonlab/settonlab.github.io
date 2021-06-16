---
permalink: /members/
title: "Members"
layout: single

header:
  overlay_filter: "0.0"
  overlay_image: /assets/images/group.jpg

classes:
  - solid-header-formatting

---
# Principal Investigator

[![image-left]({{ site.url }}{{ site.baseurl }}/assets/images/Setton.jpg)](https://engineering.wustl.edu/faculty/Lori-Setton.html){: .align-left}{: height="100"}
### [**Lori Setton**](https://www.danforthcenter.org/our-work/principal-investigators/r-keith-slotkin/)  
Department Chair, [Biomedical Engineering](https://bme.wustl.edu/index.html)  
Lucy & Stanley Lopata Distinguished Professor of Biomedical Engineering

<a href="https://scholar.google.com/citations?user=HUxQ1TAAAAAJ&hl=en&oi=ao" itemprop="sameAs" rel="nofollow noopener noreferrer">
  <i class="fab fa-google" aria-hidden="true"></i></a>
<a href="https://orcid.org/0000-0001-5992-4206" itemprop="sameAs" rel="nofollow noopener noreferrer">
  <i class="fas fa-info-circle" aria-hidden="true" style="color:#ABC953"></i></a>
<a title='Email' href="mailto:setton@wustl.edu">
  <i class="fas fa-envelope fa-fw" style="color:#000000"></i></a>
<a title="Twitter" href="https://twitter.com/setton_lab">
  <i class="fab fa-fw fa-twitter" style="color:#00acee"></i></a>

<div class="section">
  <h2><a id="members">Members</a></h2>
</div>

<div class="grid__wrapper">
  {% for author in site.data.authors %}
      <div class="grid__item">
        <div style="max-height: 240px" class="archive__item-teaser">
            <a href="{{author.uri}}">
              <img src=
                {% if author.avatar contains "://" %}
                  "{{ author.avatar }}"
                {% else %}
                  "{{ author.avatar | absolute_url }}"
                {% endif %}
                 alt="{{ author.name }}">
            </a>
        </div>
          <h2 class="archive__item-title" itemprop="headline">
            {% if author.name %}
              <a href="{{ author.uri }}">{{ author.name }}</a> <a href="{{ author.uri | absolute_url }}" rel="permalink" target="_blank"><i class="fa fa-link" aria-hidden="true" title="permalink"></i><span class="sr-only">Permalink</span></a>
            {% else %}
              <a href="{{ author.uri | absolute_url }}" rel="permalink" target="_blank">{{ author.name }}</a>
            {% endif %}
          </h2>
          {% if author.bio %}<p class="archive__item-excerpt" itemprop="description">{{ author.bio | markdownify | strip_html | truncate: 160 }}</p>{% endif %}
    </div>
  {% endfor %}

</div>

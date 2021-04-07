---
layout: gridlay
title: Publications
subtitle: Upadhyaya Lab Publications
---

# **Featured publications**
#### For a complete list of publications see <a href="https://scholar.google.com/citations?user=FxHzupAAAAAJ&hl=en&oi=ao">Google Scholar</a> or <a href="https://pubmed.ncbi.nlm.nih.gov/?term=%28Upadhyaya+Arpita%5BAuthor%5D%29&sort=date">PubMed</a> or [here](/pages/Publications_full).

{% for pub in site.data.publications %}
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{pub.short}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-3">
    	<img src="{{pub.image}}" alt="{{pub.title}}"><br>
    </div>
    <div class="col-sm-8" style="text-align: justify">
    	<strong>{{pub.title}}</strong> <br>
    	<strong>{{pub.journal}} {{pub.year}}</strong> <br>
    	{{pub.authors | markdownify}}
        {{pub.description | markdownify}}
        {% if pub.pubmed %}
          <a href= "{{pub.pubmed}}">[pubmed]</a>
        {% endif %}
        {% if pub.pdf %}
          <a href= "{{pub.pdf}}">[pdf]</a>
        {% endif %}
        {% if pub.journalLink %}
          <a href= "{{pub.journalLink}}">[{{pub.journalShort}}]</a>
        {% endif %}
    </div>
</div>
{% endfor %}

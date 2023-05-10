---
layout: gridlay
title: Publications
subtitle: Upadhyaya Lab Publications
---

# **Publications**
#### <strong>[2023] (#2023)[2022](#2022) [2021](#2021) [2020](#2020) [2019](#2019) [2018](#2018) [2017](#2017) [2016](#2016) [2014](#2014) [2013](#2013) [2012](#2012) [2011](#2011) [pre-2010](#pre-2010)</strong><br>
<hr>
{%assign my_array = "2023|2022|2021|2020|2019|2018|2017|2016|2014|2013|2012|2011" | split: "|" %}
{% for years in my_array %}
{% assign items_grouped = site.data.Publications_full | where:"year",years %}
#### <strong id = "{{years}}">{{years}}</strong><br>
<hr>
{% for group in items_grouped %}
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{group.short}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-8" style="text-align: justify">
    	<strong>{{group.title}}</strong> <br>
    	<strong>{{group.journal}} {{group.year}}</strong> <br>
    	{{group.authors | markdownify}}
        {% if pub.pubmed %}
          <a href= "{{group.pubmed}}">[pubmed]</a>
        {% endif %}
        {% if group.pdf %}
          <a href= "{{group.pdf}}">[pdf]</a>
        {% endif %}
        {% if group.journalLink %}
          <a href= "{{group.journalLink}}">[{{group.journalShort}}]</a>
        {% endif %}
    </div>
</div>
<br>
{% endfor %}
<hr>
{% endfor %}

{% assign items_grouped = site.data.Publications_full | where_exp:"item", "item.year < 2011" %}
### <strong id="pre-2010">pre-2010</strong> <br>
<hr>
{% for group in items_grouped %}
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{group.short}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-8" style="text-align: justify">
    	<strong>{{group.title}}</strong> <br>
    	<strong>{{group.journal}} {{group.year}}</strong> <br>
    	{{group.authors | markdownify}}
        {% if pub.pubmed %}
          <a href= "{{group.pubmed}}">[pubmed]</a>
        {% endif %}
        {% if group.pdf %}
          <a href= "{{group.pdf}}">[pdf]</a>
        {% endif %}
        {% if group.journalLink %}
          <a href= "{{group.journalLink}}">[{{group.journalShort}}]</a>
        {% endif %}
    </div>
</div>
<br>
{% endfor %}

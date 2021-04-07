---
layout: gridlay
title: Research
subtitle: Upadhyaya Lab Research
---
<div align="center">
	<h1>
		<strong>Research in the Upadhyaya Lab</strong>
	</h1>
</div>
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div class="container">
  <div class="jumbotron jumbotron-correct">
      <p style="font-size:120%;">
        The research in our lab broadly pursues two themes: (1) How the physical properties of the cell and its environment influence biochemical signaling, cellular force generation and force response (with particular emphasis on the immune cells), and (2) How these biochemical and mechanical signals are relayed to the nucleus to regulate gene expression. In order to answer these questions, we use state of the art imaging for the visualization of internal protein dynamics at high spatial and temporal resolution, measurements of cellular forces simultaneously with signaling, single molecule and high-throughput genomics to measure gene expression, and genetic and physical tools to perturb the system.
      </p>
  </div>
</div>

{% for project in site.data.Projects %}
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->
<div id = "{{project.name}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-4">
        <img class="img-responsive" src="{{project.image}}" {% if project.altimage %} onmouseover="this.src='{{project.altimage}}';" onmouseout="this.src='{{project.image}}';" {% endif %} alt="{{project.name}}"><br>
        <strong>{{project.person}}</strong> <br>
        Funding: {{project.funding}} <br>
    </div>
    <div class="col-sm-8" style="text-align: justify">
        <h5>{{project.name}}</h5>
        {{project.description| markdownify}}
    </div>
</div>
{% endfor %}

---
layout: gridlay
title: Image gallery
subtitle: Images
---

# **Assorted images**


{% for item in site.data.images %}
<div class="lightbox" id="lightbox{{ forloop.index }}">
  <div class="table">
    <div class="table-cell">
      <img class="close" src="/img/close.svg" />
      <img class="next" src="/img/next.svg" />
      <img class="prev" src="/img/prev.svg" />
      <div class="item" style="background: url('{{ item.image }}') center center no-repeat; background-size: cover;">
      </div>
    </div>
  </div>
</div>
{% endfor %}
<script type="text/javascript" src="/js/lightbox.js"></script>
<link rel="stylesheet" href="/css/lightbox.css">

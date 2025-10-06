---
layout: single
title: "Siva Cluster"
permalink: /
classes: wide
header:
  overlay_color: "#fdf6e3"
  overlay_filter: 0.0
  caption: ""
---
<div class="split-landing">
  <section class="split-col" aria-label="Work: ML, AI, Blockchain">
    <h2>Lost in the Forest — ML, AI, Blockchain</h2>
    <p>Research notes, experiments, and write‑ups. Click tags to jump to the related repo or filter posts.</p>

    `<div class="tag-list">`
      `<a href="https://github.com/sivacluster?tab=repositories&q=ml" target="_blank" rel="noopener">`ml`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=ai" target="_blank" rel="noopener">`ai`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=llm" target="_blank" rel="noopener">`llm`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=rl" target="_blank" rel="noopener">`rl`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=vision" target="_blank" rel="noopener">`vision`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=blockchain" target="_blank" rel="noopener">`blockchain`</a>`
      `<a href="/year-archive/">`all posts`</a>`
    `</div>`

    `<hr>`

    `<h3>`Recent posts`</h3>`
    {% assign posts_left = site.posts | where_exp: "p", "p.categories contains 'blog'" | slice: 0, 8 %}
    `<ul>`
      {% for post in posts_left %}
      `<li>`
        `<a href="{{ post.url | relative_url }}">`{{ post.title }}`</a>`
        `<small>` — {{ post.date | date: "%b %d, %Y" }}`</small>`
      `</li>`
      {% endfor %}
    `</ul>`

    `<div class="footer-note">`
      `<span>`© {{ site.time | date: "%Y" }} Siva Cluster.
      `<span>` · 
      `<a href="https://www.linkedin.com/in/" target="_blank" rel="noopener">`LinkedIn`</a>`
      `<span>` · 
      `<a href="https://www.reddit.com/user/" target="_blank" rel="noopener">`Reddit`</a>`
      `<span>` · 
      `<a href="https://discord.com/" target="_blank" rel="noopener">`Discord`</a>`
    `</div>`

</section>

<section class="split-col" aria-label="Markets: Stocks and Crypto">
    <h2>Being an Analyst — Stocks & Crypto</h2>
    <p>Market theses, dashboards, and trade reviews. Long‑form notes are posted here; data and code live in linked repos.</p>

    `<div class="tag-list">`
      `<a href="https://github.com/sivacluster?tab=repositories&q=stocks" target="_blank" rel="noopener">`stocks`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=crypto" target="_blank" rel="noopener">`crypto`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=backtest" target="_blank" rel="noopener">`backtest`</a>`
      `<a href="https://github.com/sivacluster?tab=repositories&q=notebook" target="_blank" rel="noopener">`notebooks`</a>`
    `</div>`

    `<hr>`

    `<h3>`Latest analyst notes`</h3>`
    {% assign posts_right = site.posts | where_exp: "p", "p.categories contains 'markets'" | slice: 0, 8 %}
    `<ul>`
      {% for post in posts_right %}
      `<li>`
        `<a href="{{ post.url | relative_url }}">`{{ post.title }}`</a>`
        `<small>` — {{ post.date | date: "%b %d, %Y" }}`</small>`
      `</li>`
      {% endfor %}
    `</ul>`

</section>
</div>

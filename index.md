---
title: Home
layout: base
date: 2026-01-01
summary: An online-only museum of historical objects and the essays written about them.

hero:
  image: /objects/bowl-with-dragons/images/cropped-theme-essay-header.jpg
  alt: Detail of a glazed bowl with coiled dragon iconography
  kicker: An online-only museum
  title: Your Museum Name Goes Here
  text: Historical objects, closely looked at, and the essays that follow them. Everything on this page is a placeholder until your class replaces it.
  buttons:
    - label: Explore the collection
      url: /objects
    - label: Read the essays
      url: /essays

featured:
  - slug: buddha-head
    label: Sculpture
  - slug: bowl-with-dragons
    label: Ceramics
  - slug: cosmetic-jar
    label: Glass
---

{% include layout/home-hero.html hero=page.hero %}

<section class="m-section" markdown="1">
<div class="m-wrap" markdown="1">

<p class="m-statement">This museum has no building. It exists only here, where every object is a <em>question</em> and every essay is an attempt to answer it.</p>

</div>
</section>

<section class="m-section m-section--tint" markdown="1">
<div class="m-wrap" markdown="1">
<div class="m-section-title">
  <h2>From the collection</h2>
  <a href="{{ site.baseurl }}/objects">All objects &rarr;</a>
</div>
{% include layout/picks.html
  items=page.featured
  collection="objects"
  variant="strip"
  columns=3
%}
</div>
</section>

<section class="m-section" markdown="1">
<div class="m-wrap" markdown="1">
<div class="m-section-title">
  <h2>Essays</h2>
  <a href="{{ site.baseurl }}/essays">All essays &rarr;</a>
</div>
{% assign essays = site.pages
   | where_exp: "p", "p.path contains 'essays/'"
   | where_exp: "p", "p.path != 'essays/index.md'" %}
{% include museum/essay-grid.html items=essays limit=3 %}
</div>
</section>

<section class="m-section m-section--dark">
<div class="m-wrap" markdown="1">

<p class="m-kicker" style="color: var(--museum-accent-light)">Visit</p>

<p class="m-statement">Wander by object, by essay, or by place.</p>

<p style="margin-top: 2rem">
<a class="m-button" href="{{ site.baseurl }}/gallery" style="background: var(--museum-paper); color: var(--museum-ink); border-color: var(--museum-paper)">Gallery</a>
&nbsp;
<a class="m-button m-button--ghost" href="{{ site.baseurl }}/map" style="color: var(--museum-paper); border-color: rgba(248,246,243,.5)">Map</a>
&nbsp;
<a class="m-button m-button--ghost" href="{{ site.baseurl }}/about" style="color: var(--museum-paper); border-color: rgba(248,246,243,.5)">About</a>
</p>

</div>
</section>

---
title: Home
layout: base
date: 2026-01-01
summary: An online-only museum of historical objects and the essays written about them.

# The object featured in the opening spotlight. Use an object's folder name.
spotlight: planispheric-astrolabe
spotlight-note: A brass model of the sky that could tell the time, find north and point toward Mecca.

hero:
  kicker: An online-only museum
  title: Your Museum Name Goes Here
  text: Objects from across four thousand years, gathered into rooms and read in essays. Everything on this page is placeholder until your class replaces it.
---

{% include helpers/find-item.html collection="objects" slug=page.spotlight %}
{% assign spot = xanthan_item %}
{% assign all_objects = site.pages | where_exp: "p", "p.path contains 'objects/'" | where_exp: "p", "p.path != 'objects.md'" %}
{% assign all_rooms = site.pages | where_exp: "p", "p.path contains 'exhibitions/'" | where_exp: "p", "p.path != 'exhibitions/index.md'" %}
{% assign all_essays = site.pages | where_exp: "p", "p.path contains 'essays/'" | where_exp: "p", "p.path != 'essays/index.md'" %}
{% assign dated = all_objects | where_exp: "p", "p.year" | sort: "year" %}
{% assign oldest = dated | first %}
{% assign newest = dated | last %}
{% assign span_years = newest.year | minus: oldest.year %}

{% if spot %}
{% capture spot_url %}{% include helpers/link-path.html link=spot.url %}{% endcapture %}
{% capture spot_img %}{% include helpers/image-path.html image-path=spot.thumbnail page-dir=spot.dir %}{% endcapture %}
<section class="home-open">
<div class="home-open-inner">
<div class="home-open-text">
<span class="m-kicker">{{ page.hero.kicker }}</span>
<h1>{{ page.hero.title }}</h1>
<p class="home-open-lede">{{ page.hero.text }}</p>
<p class="home-open-actions">
<a class="m-button m-button--light" href="{{ site.baseurl }}/exhibitions">Enter the rooms</a>
<a class="m-button m-button--outline" href="{{ site.baseurl }}/visit">Plan your visit</a>
</p>
</div>
<a class="home-spotlight" href="{{ spot_url | strip }}">
<span class="home-spotlight-label">Object of the week</span>
<img src="{{ spot_img | strip }}" alt="{{ spot.image-alt | default: spot.title | escape }}">
<span class="home-spotlight-caption">
<strong>{{ spot.title }}</strong>
<span>{{ spot.object-date }}{% if spot.placename %} · {{ spot.placename }}{% endif %}</span>
<em>{{ page.spotlight-note | default: spot.summary }}</em>
</span>
</a>
</div>
</section>
{% endif %}

<section class="home-stats">
<dl>
<div><dt>Objects</dt><dd>{{ all_objects.size }}</dd></div>
<div><dt>Exhibitions</dt><dd>{{ all_rooms.size }}</dd></div>
<div><dt>Essays</dt><dd>{{ all_essays.size }}</dd></div>
<div><dt>Years covered</dt><dd>{{ span_years | default: 0 }}</dd></div>
</dl>
</section>

<section class="m-section" markdown="1">
<div class="m-wrap" markdown="1">

<p class="m-statement">This museum has no building. It exists only here, where every object is a <em>question</em> and every room is an attempt to answer it.</p>

</div>
</section>

<section class="m-section m-section--tint" markdown="1">
<div class="m-wrap" markdown="1">
<div class="m-section-title">
  <h2>The rooms</h2>
  <a href="{{ site.baseurl }}/exhibitions">All exhibitions &rarr;</a>
</div>
{% include museum/exhibition-grid.html items=all_rooms limit=3 %}
</div>
</section>

<section class="m-section" markdown="1">
<div class="m-wrap" markdown="1">
<div class="m-section-title">
  <h2>Travel through time</h2>
  <a href="{{ site.baseurl }}/timeline">Full timeline &rarr;</a>
</div>
{% include museum/ribbon.html items=all_objects %}
</div>
</section>

<section class="m-section m-section--tint" markdown="1">
<div class="m-wrap" markdown="1">
<div class="m-section-title">
  <h2>Essays</h2>
  <a href="{{ site.baseurl }}/essays">All essays &rarr;</a>
</div>
{% include museum/essay-grid.html items=all_essays limit=3 %}
</div>
</section>

<section class="m-section m-section--dark" markdown="1">
<div class="m-wrap" markdown="1">

<p class="m-kicker" style="color: var(--museum-accent-light)">Not sure where to start?</p>

<p class="m-statement">Take a guided route, fifteen minutes or an afternoon.</p>

<p style="margin-top: 2rem">
<a class="m-button m-button--light" href="{{ site.baseurl }}/visit">Plan your visit</a>
&nbsp;
<a class="m-button m-button--outline" href="{{ site.baseurl }}/objects">Browse all objects</a>
&nbsp;
<a class="m-button m-button--outline" href="{{ site.baseurl }}/map">See the map</a>
</p>

</div>
</section>

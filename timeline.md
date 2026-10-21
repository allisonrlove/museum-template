---
title: Timeline
layout: default
date: 2026-01-01
summary: The whole collection in date order, from the oldest object to the most recent.
---

<div class="m-wide-wrap" style="margin-bottom:0" markdown="1">

<span class="m-kicker">Across time</span>

# Timeline

{: .lede}
Four thousand years in one scroll. Objects are placed by the `year:` line in their front matter, so a new object finds its own place in the sequence.

</div>

{% assign objects = site.pages
   | where_exp: "p", "p.path contains 'objects/'"
   | where_exp: "p", "p.path != 'objects.md'" %}

{% include museum/timeline.html items=objects %}

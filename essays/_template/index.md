---
title: Your Essay Title
layout: essay
author: Your Name
date: 2026-01-01
published: false
position: 10
kicker: A short label, like Trade or Belief
thumbnail: /objects/bowl-with-dragons/images/bowl-with-dragons.jpg
lead-image: /objects/bowl-with-dragons/images/bowl-with-dragons.jpg
lead-image-alt: A short description of the big picture at the top
lead-image-caption: "What the picture shows, and where it came from."
summary: One sentence that makes your argument. It appears under your title and on your card.
tags:
  - one-theme

objects:
  - slug: bowl-with-dragons
    label: Place, date
---

<!--
  HOW THIS PAGE WORKS
  Everything between the two lines of dashes above is the "front page" of your
  essay: headline, one-sentence summary, big picture, and author line.
  Fill in each line after the colon.

  `thumbnail` and `lead-image` can use a picture from an object in the
  collection (like the examples above) or one from your own `images` folder
  (like images/my-picture.jpg).

  `objects:` lists the objects your essay is about. Use the folder name from
  objects/ for `slug`. A row of those objects appears at the end of your essay.

  `published: false` hides the essay until your instructor says it is ready.
-->

{: .lede .dropcap}
Open with two or three sentences that tell the reader what this essay is about and why it matters. This paragraph is shown larger than the rest. (Aim for 60–100 words.)

## First section heading

Write your first section here. Link to an object in the collection like this: [Bowl with Dragons]({{ site.baseurl }}/objects/bowl-with-dragons).

{% include essay/figure.html
  image="/objects/bowl-with-dragons/images/bowl-with-dragons.jpg"
  alt="A short description of the picture"
  caption="What the picture shows, and where it came from."
  size="wide"
%}

## Second section heading

Make your argument here.

{% include typography/pullquote.html
  text="Pick one sentence from your essay that you want readers to remember."
%}

{% include essay/object.html slug="bowl-with-dragons" note="One sentence on why this object matters to your point." %}

{% include essay/look-closer.html
  title="Look closer: a detail or a definition"
  text="A short explanation readers can open if they want more."
%}

## Closing section heading

Finish by saying what your reader now understands that they did not before.

## Sources

- Author. *Title*. Publisher, Year.

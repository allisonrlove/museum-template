# Online Museum Template

A website template for an **online-only museum of historical objects and essays**, built on the [Xanthan](https://github.com/xanthan-web/xanthan) framework and hosted on GitHub Pages. Designed for classes where instructors and students have little or no coding experience.

## What you get

- A modern museum look: dark gallery rooms, warm paper tones, a vermilion accent, Newsreader and Manrope type.
- **Exhibitions**: themed rooms that walk visitors through chosen objects and essays.
- **Objects**: a "wall label" page for each object, a grid filtered by region and period, a **timeline**, a gallery and a map.
- **Object of the week** on the home page, and **Plan your visit** guided routes.
- **Essays**: magazine-style long reads with a lead image, reading progress, pull quotes, captioned pictures that zoom, and "look closer" boxes.
- **Copy-and-fill templates** so students never start from a blank page.
- A built-in **Student Guide** (`/instructions`) and **Instructor Guide** (`/instructors`).

## Quick start (instructors)

1. Click **Use this template** on GitHub and create a public repository.
2. In `_config.yml`, set `title`, `baseurl` (`/your-repo-name`) and the `museum:` footer lines.
3. Turn on GitHub Pages in **Settings, Pages**.
4. Invite students as collaborators and send them the Student Guide page.

Full details are in `instructors.md`.

## Structure

```
objects/
  _template/        ← students copy this to add an object
  bowl-with-dragons/
    index.md        ← front matter facts + writing
    images/
essays/
  _template/        ← students copy this to add an essay
  borrowed-forms/
exhibitions/
  _template/        ← copy this to add a room
_data/routes.yml    ← guided routes
timeline.md, visit.md
index.md            ← home page
objects.md          ← object grid (built automatically)
essays/index.md     ← essay grid (built automatically)
gallery.md, map.md, about.md
instructions.md     ← Student Guide
instructors.md      ← Instructor Guide
assets/css/themes/museum.css   ← palette and fonts live at the top
_layouts/object.html, essay.html
_includes/museum/, _includes/essay/
```

Adding a folder adds it to the grids. Deleting one removes it. Folders starting with `_` are never published.

## Customise

Edit the **THE PALETTE** and **THE FONTS** blocks at the top of `assets/css/themes/museum.css`. Edit the menu in `_data/nav-top.yml` and the home page in `index.md`.

## Samples

Ten sample objects, five sample essays and three sample exhibitions are included as stand-ins. Their images come from [The Metropolitan Museum of Art](https://www.metmuseum.org/) open-access collection (via Wikimedia Commons); the text is placeholder. Delete them when you are ready.

More about Xanthan: [documentation](https://xanthan-web.github.io/xanthan/docs/).

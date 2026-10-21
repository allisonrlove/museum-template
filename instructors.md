---
title: Instructor Guide
layout: default
date: 2026-01-01
summary: How to set up, customise, and manage the museum with a class.
---

<span class="m-kicker">Guide for instructors</span>

# Running the museum

{: .lede}
Everything you need to set up the site, make it yours, and prepare students.

## 1. Set up

1. On GitHub, click **Use this template**, then **Create a new repository**. Make it public.
2. Go to **Settings, Pages** and set the source to **GitHub Actions** (or the branch your Xanthan docs recommend). The site appears at `https://USERNAME.github.io/REPOSITORY`.
3. Add your students under **Settings, Collaborators**.
4. Open `_config.yml` and change:
   - `title` and `tagline`: the museum's name.
   - `baseurl`: set to `/REPOSITORY` (your repository name).
   - `museum.credit` and `museum.course`: shown in the footer.

Press **`.`** on the repository page to edit in the browser.

## 2. Make it yours

| To change | Edit |
|---|---|
| Colours | `assets/css/themes/museum.css`, the **THE PALETTE** block at the top |
| Fonts | The same file, **THE FONTS** block. Change the Google Fonts link and the two names. |
| Menu | `_data/nav-top.yml` |
| Home page | `index.md`. Set `spotlight:` to an object's folder name to change the **Object of the week**. |
| Exhibitions (rooms) | Copy `exhibitions/_template`, rename it, and list objects and essays by folder name. Set `position` for the order. |
| Guided routes | `_data/routes.yml`: each route has a title, minutes, description and a list of object folder names. |
| Timeline and filters | Automatic. They use each object's `year` and `region`. Eras: before 500 BCE, 500 BCE to 500 CE, 500 to 1500 CE, after 1500 CE. |
| About page | `about.md` |
| Footer | `_includes/layout/footer.html` |

Palette changes apply everywhere. Keep text and background contrast high so pages stay readable.

### Adding a guided route

Routes appear on the **Plan Your Visit** page. To add one:

1. Open `_data/routes.yml`.
2. Copy a whole block (from `- title:` to the last stop) and paste it below the others.
3. Change the words after each colon:

```yaml
- title: Small and powerful
  minutes: 20
  description: One sentence telling visitors what this walk is about.
  stops:
    - mitanni-cylinder-seal
    - tsuba-sword-guard
    - scarab-of-queen-tiye
```

4. Each line under `stops` is an **object folder name** (the folder inside `objects/`), in the order visitors should see them. Keep the dashes and the two-space indents exactly as shown.
5. Save. The new route appears on the Visit page. If a stop does not show, check the folder name for typos.

To remove a route, delete its whole block.

### Adding an exhibition (room)

An exhibition is a themed room built from objects students have already added. Do this after the objects exist.

1. In the `exhibitions` folder, copy the `_template` folder and rename the copy (lowercase, dashes, like `trade-and-travel`).
2. Open the `index.md` inside it and change `title`, `curator`, `summary` and `position` (the order on the Exhibitions page; lower numbers come first).
3. Set `thumbnail` to the path of any object's picture, like `/objects/bowl-with-dragons/images/bowl-with-dragons.jpg`.
4. Under `objects:`, list each stop with `slug` (the object's folder name) and `note` (one sentence on why it belongs). Copy the two-line pair for more stops. Order matters.
5. Under `essays:`, list essay folder names to recommend, or delete those lines.
6. Write a short introduction below the dashes.
7. Delete the `published: false` line when it is ready.

The room's stops, object count and each object's "Seen in" section fill in automatically.

### Choosing the Object of the Week

Open `index.md`. Change `spotlight:` to an object's folder name and `spotlight-note:` to one sentence about why it is featured. Update it weekly if you like.

### Timeline, regions and eras

These are automatic. Each object needs `year` (a number, negative for BCE) and `region` (Africa, Asia, Americas, Europe or Middle East). An object missing `year` will not appear on the timeline, and one missing `region` will not match the region filter. Check these first if an object seems to be missing.

## 3. Clear the samples

Delete the folders inside `objects`, `essays` and `exhibitions` that do not start with `_`, clear `_data/routes.yml`, and set `spotlight:` on `index.md` to one of your own objects. Keep `_template` folders. Students copy them. Plan rooms after students have added their objects: a room is a curated path through them.

## 4. Prepare students

- Share the [Student Guide]({{ site.baseurl }}/instructions) before the first lab.
- Run a 20-minute demo: copy the template, change the title, commit.
- Have each student make a practice edit with `published: false`.
- Give shared tags in advance (for example, `trade`, `belief`, `daily-life`) so filters stay tidy.
- Tell students where images may come from. Museum open-access collections are a good source.

## 5. Suggested timeline

| Week | Activity |
|---|---|
| 1 | Accounts, invitation, practice edit |
| 2 | Choose objects, collect images and facts |
| 3 | Draft object pages |
| 4 | Review and publish objects |
| 5 to 7 | Draft essays |
| 8 | Review and publish essays |

## 6. Review work

Students work on their own branch. In GitHub, open their **Pull request**, read the **Files changed** tab, leave comments, and click **Merge** when ready. The site rebuilds in about two minutes.

Checklist before merging:

- Folder name is lowercase with hyphens.
- `published: false` is removed.
- Every image has alt text and a credit.
- Facts are cited in Sources.
- Images are under 1 MB each.
- Essay length is within the guide.

## 7. Accessibility and rights

- Require alt text on every image.
- Only use images you may reuse, and credit them.
- Check that links open and make sense when read alone.

## 8. Troubleshooting

| Problem | Try this |
|---|---|
| Build failed | Open the **Actions** tab, then the failed run. The message names the file and line. Usually a missing quotation mark or `---`. |
| Styles missing | `baseurl` in `_config.yml` must match your repository name. |
| Essay not on the Essays page | The file must be `essays/NAME/index.md` and have no `published: false`. |
| Map is empty | Objects need a `geo` field. See `map.md` and the Xanthan docs. |

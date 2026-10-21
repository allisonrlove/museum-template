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
| Home page | `index.md` |
| About page | `about.md` |
| Footer | `_includes/layout/footer.html` |

Palette changes apply everywhere. Keep text and background contrast high so pages stay readable.

## 3. Clear the samples

Delete the folders inside `objects` and `essays` that do not start with `_`, and update the featured items on `index.md`. Keep `_template` folders. Students copy them.

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

---
title: Student Guide
layout: default
date: 2026-01-01
summary: Step-by-step instructions for adding your object and essay to the museum.
---

<span class="m-kicker">Guide for students</span>

# How to add your work

{: .lede}
You do not need to know how to code. You will copy a template, fill in the blanks, and save. This page walks you through it.

## Before you start

You need:

1. A free [GitHub](https://github.com) account.
2. An invitation to this project from your instructor. Accept it by email.
3. Your pictures, saved as `.jpg` files under 1 MB each, with names in lowercase and hyphens (`grandmothers-suitcase.jpg`).

## Step 1. Open the editor

1. Go to the project page on GitHub (your instructor will give you the link).
2. Press the **`.`** (full stop) key on your keyboard. A code editor opens in your browser.

You will see a list of folders on the left. The two you care about are **`objects`** and **`essays`**.

## Step 2. Copy the template

**To add an object**

1. Open the `objects` folder.
2. Right-click the **`_template`** folder and choose **Copy**, then right-click `objects` and choose **Paste**.
3. Right-click the new copy and choose **Rename**. Give it a short name in lowercase with hyphens, like `grandmothers-suitcase`. This name becomes part of the web address.

**To add an essay**, do the same thing in the `essays` folder.

## Step 3. Fill in the blanks

1. Open `index.md` inside your new folder.
2. At the top, between the two lines of `---`, are the "front matter" lines. Change the words after each colon.
3. Below that is the writing. Replace the sample text with your own.
4. Grey text inside `<!-- -->` is a note to you. You can delete it.

### Object fields

| Field | What to write | Required |
|---|---|---|
| `title` | The name of the object | Yes |
| `author` | Your name | Yes |
| `thumbnail` | The picture file, like `images/suitcase.jpg` | Yes |
| `summary` | One or two sentences about the object | Yes |
| `image-alt` | A description of the picture for people who cannot see it | Yes |
| `image-credit` | Where the picture came from | Yes |
| `maker`, `object-date`, `placename`, `medium`, `dimensions`, `collection`, `accession` | Facts for the label. Delete a line if you do not know it. | No |
| `year` | One number that places your object on the timeline. Use a minus sign for BCE (`-500`). | Yes |
| `region` | Africa, Asia, Americas, Europe or Middle East. Used by the filters. | Yes |
| `tags` | One to three themes. Reuse tags other students have used so the filters work. | No |
| `published` | `false` hides your page. Delete the line when you are done. | No |

### Essay fields

| Field | What to write | Required |
|---|---|---|
| `title` | Your headline | Yes |
| `author` | Your name | Yes |
| `kicker` | A short label above the title | No |
| `summary` | One sentence that makes your argument | Yes |
| `lead-image`, `lead-image-alt`, `lead-image-caption` | The big picture at the top | Yes |
| `thumbnail` | The picture for your card | Yes |
| `objects` | The objects your essay is about (use the folder name as `slug`) | No |
| `position` | Order on the Essays page. Leave it, your instructor will set it. | No |

## Step 4. Add pictures

1. In the editor, open your folder's **`images`** folder.
2. Drag your picture files from your computer into it.
3. Use the file name in the blanks: `images/suitcase.jpg`.

Always write alt text and a credit. If you did not take the picture, say who did and link to the source.

## Step 5. Use the special blocks

You can copy these blocks into your writing. Change only the words inside the quotation marks.

**A picture with caption**

```
{% raw %}{% include essay/figure.html
  image="images/suitcase.jpg"
  alt="Describe the picture"
  caption="What it shows and where it came from."
  size="wide"
%}{% endraw %}
```

`size` can be `small`, `normal`, `wide`, or `full`.

**A feature card for an object**

```
{% raw %}{% include essay/object.html slug="bowl-with-dragons" note="Why it matters." %}{% endraw %}
```

**A "look closer" box readers can open**

```
{% raw %}{% include essay/look-closer.html title="Look closer: a detail" text="Explain it." %}{% endraw %}
```

**A pull quote**

```
{% raw %}{% include typography/pullquote.html text="One memorable sentence." %}{% endraw %}
```

## Writing tips

| Part | Length |
|---|---|
| Object description | 150 to 300 words |
| Essay | 800 to 1,500 words |
| Essay opening paragraph | 60 to 100 words |
| Essay sections | 2 to 4, each with a short heading |

Use `## Heading` for a section heading and `*word*` for italics. Leave a blank line between paragraphs.

## Step 6. Save and send

1. Click the **Source Control** icon on the left (a branch symbol).
2. Type a short message, like "Add suitcase object".
3. Click **Commit & Push**. Choose **Create a new branch** if asked, then name it after yourself.
4. Tell your instructor. They will review and publish your work.

The site updates a couple of minutes after your instructor approves it.

## Troubleshooting

| Problem | Try this |
|---|---|
| My page does not appear | Check that `published: false` has been removed and that the folder name has no spaces or capital letters. |
| My picture is missing | Check the file name matches exactly, including `.jpg`. Check it is in your `images` folder. |
| The page is blank or broken | Check the `---` lines are at the top and after the front matter, and that every quotation mark has a partner. |
| A colon in my title breaks things | Put the title in quotation marks: `title: "Trade: A Story"`. |
| My block shows as text | Check it starts with `{% raw %}{% include{% endraw %}` and ends with `%}`. |

Still stuck? Ask your instructor and share the page name.

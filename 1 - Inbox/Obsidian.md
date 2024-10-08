---
modified: 2024-09-03T16:25:45+02:00
---

## Usage

How to decide how to structure stuff in Obsidian [[Links vs Tags vs Folders]]

[[fromSergio's Obsidian playlist]]

## Plugins

### Obsidian File Diff
Creates diffs from notes and find all [[Syncthing]] merge conflicts and eases the work with them.

[[1 - Inbox/Templater]]
[[Canvas]]

## Adding dynamic dates to properties (for Templates)

Using the properties, we need a workaround to use the template syntax in properties, otherwise we just cannot insert something like `{{date:YYYY-MM-DD}}` to the date property, as the template string is not of the *right type*.

We can work around it, by setting the Option to display properties (temporarily) as source code.  `Settings > Editor > Display > Properties in Document > [Source]` .

Then we can work with properties as we did with **yaml frontmatter** before:

```yaml
---
date: {{date:YYYY-MM-DD}}
---
```
## Creating nice code documentation (for) Obsidian

To create some examples of how to format stuff in Obsidian, showing the syntax, sometimes it's convenient to show the literal syntax stopping Obsidian from showing the result. Escaping only works for some things, but not for **code blocks**.

We use a a nested `<pre></pre>` tag.

> [!NOTE] List in Dataview
> 
<pre>
```dataview
LIST
```
</pre>

[[fromSergio's Obsidian playlist]]
[[1 - Inbox/Using Dataview to create maps for content types]]

## Zotero - Obsidian Workflow

Inspired by this [thread](https://forum.obsidian.md/t/my-zotero-annotation-template-that-works/51662/12) I found nocona's github [repo](https://github.com/nocona71/obsidian-literature-note) presenting a set of styles and [[Templates]] for [[1 - Inbox/Obsidian]] and [[Zotero]] .



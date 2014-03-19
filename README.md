# Pattern library plugin

It helps you to generate a pattern library from UI components you develop for
your jekyll website.

## Install

1. Download the project zip file.
2. Copy/paste files (or directories if they don't exist yet).

## Front-matter variables

Here is a list of special variables recognised by the plugin.

### Pattern variable

**As for posts, add any other variables in the Front-matter and use them in
your layout.**

Generated variables :

- `id`: The pattern filename without the `.html` extension.
- `markup`: The pattern HTML markup.
- `markup_escaped`: The HTML escaped version of the markup. Its usefull for
                  `<code>` blocks.

The following variables are recognised but not required.

`section`: This variable points out a section which the pattern belongs to,
           and add the pattern to the page sections list.

### Page variables

Generated variables :

- `page.patterns`: The list of patterns
- `page.sections`: The list of patterns ordered by sections. Work as native
                   posts categories.
- `page.title`: The page title specified in the LibraryPage constructor use.

## To do

- [ ] Review the Pattern.destination method.
- [ ] Add a better layout
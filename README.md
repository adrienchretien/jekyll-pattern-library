# Pattern library plugin

It helps you to generate a pattern library from UI components you develop for
your website running with jekyll.

## Install

1. Download the project zip file.
2. Copy/paste files from _layouts, _plugins and css directories to respectively
   the same directories in your jekyll project. Create the _plugins directory
   if doesn't exist yet.
3. Create a _patterns directory at the project root and add patterns into
   separate HTML files. You can add a YAML Front-matter blocks on top of those
   files.

## Configurations

You can change alter the configuration by modifying the `generate` method
inside the _plugins/pattern_library.rb file.

The `patterns = read_content(site, '', '_patterns', Pattern)` list all patterns
inside the `_patterns` directory.

Then, the `site.pages << LibraryPage.new(site, <page_name>, patterns)` lines
register the pages that jekyll will generate. You can change the `<page_name`
part as you want.

## Front-matter variables

### Pattern variable

Generated variables :

- `id`: The pattern filename without the `.html` extension.
- `markup`: The pattern HTML markup.
- `markup_escaped`: The HTML escaped version of the markup. Its usefull for
                  `<code>` blocks.

**The following variables are recognised but not required.**

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
- [ ] Add template pages.

## Colophon

The layout is highly inspired from the A List Appart pattern library page.
Note : I have to ask @maban the right to use it.
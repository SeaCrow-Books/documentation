> [!info]
>  This guide is for the production of epub using Pandoc. It assumes [Pandoc](https://pandoc.org/) has been installed. 
>  
>  **Resources**
> [This guide](https://pandoc.org/epub.html) is very useful and shows a very basic example of creating an epub. 

## File Formatting

Correct file formatting is essential for a successful conversion to epub. 

> [!warning] 
> Files should be number 01, 02, 03 etc, in the order that they will be formatted. 
> e.g. 01-chapter
### Setting the File Type

For epub3 output, you can mark up the heading that corresponds to an EPUB chapter using the epub:type attribute. For example, to set the attribute to the value prologue, use this markdown:

```
# My chapter {epub:type=prologue}
```

Which will result in:

```
<body epub:type="frontmatter">
  <section epub:type="prologue">
    <h1>My chapter</h1>
```

Pandoc will output ```<body epub:type="bodymatter">```, unless you use one of the following values, in which case either frontmatter or backmatter will be output.

**Frontmatter**
- prologue
- abstract
- acknowledgments
- copyright-page
- dedication
- credits
- keywords
- imprint
- contributors
- other-credits
- errata
- revision-history
- titlepage
- halftitlepage
- seriespage
- foreword
- preface
- frontispiece

**Bakcmatter**
- appendix
- colophon
- bibliography
- index
### Chapter Files Formatting

These will be markdown files.

1. **Headings and Subheadings**:
    - Chapters should be in markdown (.md) and named chapter-1, chapter-2 etc.
    - Use `#` for main chapter titles (e.g., `# Chapter 1`).
    - Use `##`, `###`, etc., for subheadings within chapters. This hierarchical structure is crucial for a clear, navigable EPUB.
2. **Consistency**:
    - Maintain consistent formatting across all chapters. For example, if `##` represents a section title in one chapter, it should do the same in all others.
3. **Paragraphs and Line Breaks**:
    - Write paragraphs as plain text. For a new paragraph, leave an empty line between blocks of text.
    - Use two spaces at the end of a line for a line break without starting a new paragraph.
4. **Lists**:
    - For ordered lists, use numbers followed by a period (e.g., `1. Item`).
    - For unordered lists, use dashes or asterisks (e.g., `- Item` or `* Item`).
5. **Emphasis**:
    - Use asterisks or underscores for emphasis (`*italic*` or `**bold**`).
6. **Links** (if applicable):
    - Format links as `[link text](URL)`.
7. **Images** (for the cover and any other images):
    - Use the format `![Alt text](image-path.jpg)`. Make sure to include alt text for accessibility.
8. **Blockquotes** (if used):
    - Use `>` before the text.

### Metadata File
The metadata can be presented either at the top of each markdown chapter file in YAML format or in a separate md file with the metadata in YAML format. The best practice is a seperate file to fit with [[DRY]] mindset.

EPUB metadata may be specified using the [`--epub-metadata`](https://pandoc.org/MANUAL.html#option--epub-metadata) option, but if the source document is Markdown, it is better to use a [YAML metadata block](https://pandoc.org/MANUAL.html#extension-yaml_metadata_block). Here is an example:

```
---
title:
- type: main
  text: My Book
- type: subtitle
  text: An investigation of metadata
creator:
- role: author
  text: John Smith
- role: editor
  text: Sarah Jones
identifier:
- scheme: DOI
  text: doi:10.234234.234/33
publisher:  My Press
rights: © 2007 John Smith, CC BY-NC
ibooks:
  version: 1.3.4
...
```

The following fields are recognized:

`identifier`

Either a string value or an object with fields `text` and `scheme`. Valid values for `scheme` are `ISBN-10`, `GTIN-13`, `UPC`, `ISMN-10`, `DOI`, `LCCN`, `GTIN-14`, `ISBN-13`, `Legal deposit number`, `URN`, `OCLC`, `ISMN-13`, `ISBN-A`, `JP`, `OLCC`.

`title`

Either a string value, or an object with fields `file-as` and `type`, or a list of such objects. Valid values for `type` are `main`, `subtitle`, `short`, `collection`, `edition`, `extended`.

`creator`

Either a string value, or an object with fields `role`, `file-as`, and `text`, or a list of such objects. Valid values for `role` are [MARC relators](https://loc.gov/marc/relators/relaterm.html), but pandoc will attempt to translate the human-readable versions (like “author” and “editor”) to the appropriate marc relators.

`contributor`

Same format as `creator`.

`date`

A string value in `YYYY-MM-DD` format. (Only the year is necessary.) Pandoc will attempt to convert other common date formats.

`lang` (or legacy: `language`)

A string value in [BCP 47](https://tools.ietf.org/html/bcp47) format. Pandoc will default to the local language if nothing is specified.

`subject`

Either a string value, or an object with fields `text`, `authority`, and `term`, or a list of such objects. Valid values for `authority` are either a [reserved authority value](https://idpf.github.io/epub-registries/authorities/) (currently `AAT`, `BIC`, `BISAC`, `CLC`, `DDC`, `CLIL`, `EuroVoc`, `MEDTOP`, `LCSH`, `NDC`, `Thema`, `UDC`, and `WGS`) or an absolute IRI identifying a custom scheme. Valid values for `term` are defined by the scheme.

`description`

A string value.

`type`

A string value.

`format`

A string value.

`relation`

A string value.

`coverage`

A string value.

`rights`

A string value.

`belongs-to-collection`

A string value. Identifies the name of a collection to which the EPUB Publication belongs.

`group-position`

The `group-position` field indicates the numeric position in which the EPUB Publication belongs relative to other works belonging to the same `belongs-to-collection` field.

`cover-image`

A string value (path to cover image).

`css` (or legacy: `stylesheet`)

A string value (path to CSS stylesheet).

`page-progression-direction`

Either `ltr` or `rtl`. Specifies the `page-progression-direction` attribute for the [`spine` element](http://idpf.org/epub/301/spec/epub-publications.html#sec-spine-elem).

`ibooks`

iBooks-specific metadata, with the following fields:

- `version`: (string)
- `specified-fonts`: `true`|`false` (default `false`)
- `ipad-orientation-lock`: `portrait-only`|`landscape-only`
- `iphone-orientation-lock`: `portrait-only`|`landscape-only`
- `binding`: `true`|`false` (default `true`)
- `scroll-axis`: `vertical`|`horizontal`|`default`

### CSS

By default, pandoc will include some basic styling contained in its `epub.css` data file. (To see this, use `pandoc --print-default-data-file epub.css`.) To use a different CSS file, just use the [`--css`](https://pandoc.org/MANUAL.html#option--css) command line option. A few inline styles are defined in addition; these are essential for correct formatting of pandoc’s HTML output.

The `document-css` variable may be set if the more opinionated styling of pandoc’s default HTML templates is desired (and in that case the variables defined in [Variables for HTML](https://pandoc.org/MANUAL.html#variables-for-html) may be used to fine-tune the style).

This is a [sample of boilerplate styling](https://github.com/mattharrison/epub-css-starter-kit/blob/master/README.rst).
### Step by Step Terminal Guide
This is the guide to creating the epub.

> [!warning] 
> ALL files must be in the same directory to avoid issues.

Open the terminal and navigate to the ebook directory. 

Type:

`pandoc -o OUTPUTNAME.epub INPUTNAME.md`

Here OUTPUTNAME is the name that you want the EPUB file to have, and INPUTNAME is the filename of your book.

Another example:

```
pandoc -o progit.epub title.txt \
  01-introduction/01-chapter1.markdown \
  02-git-basics/01-chapter2.markdown \
  03-git-branching/01-chapter3.markdown \
  04-git-server/01-chapter4.markdown \
  05-distributed-git/01-chapter5.markdown \
  06-git-tools/01-chapter6.markdown \
  07-customizing-git/01-chapter7.markdown \
  08-git-and-other-scms/01-chapter8.markdown \
  09-git-internals/01-chapter9.markdown
```

If you would like to generate a table of contents and include a cover image, you can add a few switches, like this:

`pandoc -o OUTPUTNAME.epub INPUTNAME.md --toc --toc-depth=2 --epub-cover-image=COVERIMAGE.png`

Other useful commands include:
#### Input and Output:
- `-o FILE, --output=FILE`: Write output to a specified file.
- If multiple input files are given, Pandoc will concatenate them before parsing.
#### Format Specification:
- `-f FORMAT, --from=FORMAT`: Specify input format (e.g., markdown, html).
- `-t FORMAT, --to=FORMAT`: Specify output format (e.g., epub, epub3).
#### EPUB-Specific Options:
- `--epub-metadata=FILE`: Specify a metadata file.
- `--css=FILE`: Include a CSS file.
- `--epub-cover-image=FILE`: Specify a cover image.
#### General Options:
- `--data-dir=DIRECTORY`: Set the user data directory.
- `--list-input-formats`: List supported input formats.
- `--list-output-formats`: List supported output formats.
#### Reader Options:
- `--shift-heading-level-by=NUMBER`: Shift heading levels by a specified number.
- `--file-scope`: Parse each file individually (useful for multifile documents).
#### Other Useful Flags:
- `-s, --standalone`: Produce a standalone document.
- `--verbose`: Provide verbose debugging output.
- `--quiet`: Suppress warning messages.

> [!success] Current Best Practice
> 
> ```
> pandoc -o OUTPUTNAME.epub INPUTNAME.md --toc --epub-cover-image=COVERIMAGE.png --epub-metadata=metadata.md --css=styling.css
> ```
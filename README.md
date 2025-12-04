# Calibre Acoup recipe

This recipe aims to convert the Acoup (A collection of unmitigated pedantry) blog to epub. To accomplish this a Calibre Recipe is used, as documented here: https://manual.calibre-ebook.com/news.html

## Processing
The website author uses a lot of footnotes, as historians do. These footnotes are rendered as web links that are poorly manager by ebook readers.

So this recipe adds a function that:
* looks for footnotes on an article
* removes the footnote-link
* converts the footnote into an inline-note, in italic between `[...]`

The resulting ebook is much more readable on readers.

## Debug and test
On MacOS, use the command:

```
/Applications/calibre.app/Contents/MacOS/ebook-convert Acoup.recipe output/Acoup.epub --test -vv --debug-pipeline output/debug
```

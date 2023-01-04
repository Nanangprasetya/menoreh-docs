# Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Setting up navigation

A clear and concise navigation structure is an important aspect of good project 
documentation. Material for MkDocs provides a multitude of options to configure
the behavior of navigational elements, including [tabs] and [sections], and one
of its flag-ship feature: [instant loading].

  [tabs]: #navigation-tabs
  [instant loading]: #instant-loading

## Configuration

## Instant loading

[:octicons-tag-24: 5.0.0][Instant loading support] ·
:octicons-unlock-24: Feature flag

When instant loading is enabled, clicks on all internal links will be
intercepted and dispatched via [XHR] without fully reloading the page. Add
the following lines to `mkdocs.yml`:

``` yaml
theme:
  features:
    - navigation.instant
```

The resulting page is parsed and injected and all event handlers and components
are rebound automatically, i.e., __Material for MkDocs now behaves like a Single
Page Application__. Now, the search index survives navigation, which is
especially useful for large documentation sites.

  [Instant loading support]: https://github.com/squidfunk/mkdocs-material/releases/tag/5.2.0
  [XHR]: https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest

### Anchor tracking

[:octicons-tag-24: 8.0.0][Anchor tracking support] ·
:octicons-unlock-24: Feature flag

When anchor tracking is enabled, the URL in the address bar is automatically
updated with the active anchor as highlighted in the table of contents. Add the
following lines to `mkdocs.yml`:

``` yaml
theme:
  features:
    - navigation.tracking
```

  [Anchor tracking support]: https://github.com/squidfunk/mkdocs-material/releases/tag/8.0.0

### Navigation tabs

[:octicons-tag-24: 1.1.0][Navigation tabs support] ·
:octicons-unlock-24: Feature flag

When tabs are enabled, top-level sections are rendered in a menu layer below
the header for viewports above `1220px`, but remain as-is on mobile.[^1] Add
the following lines to `mkdocs.yml`:

  [^1]:
    Prior to :octicons-tag-24: 6.2.0, navigation tabs had a slightly different
    behavior. All top-level pages (i.e. all top-level entries directly
    refefring to a `*.md` file) defined inside the `nav` entry of `mkdocs.yml`
    were grouped under the first tab which received the title of the first page.
    This made it impossible to include a top-level page (or external link) as a
    tab item, as was reported in #1884 and #2072. From :octicons-tag-24: 6.2.0
    on, navigation tabs include all top-level pages and sections.

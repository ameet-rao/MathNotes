# Ameet Rao Math Notes

A static website of math notes and practice problems. No build step, no dependencies.
Open `index.html` directly, or serve the folder with any static host (e.g. GitHub Pages).

## Layout

```
index.html                  Home page (course cards)
style.css                   Shared styles
calculus-3/index.html       Calculus 3 page
linear-algebra/index.html   Linear Algebra page
courses/<course>/notes/     Notes PDFs
courses/<course>/practice/  Practice problem PDFs
images/                     Course images
```

## Adding a PDF

1. Put the PDF in `courses/<course>/notes/` or `courses/<course>/practice/`,
   named after the topic it covers.
2. Add a line to that course's `index.html` under the matching section:

   ```html
   <li><a href="../courses/<course>/notes/<file>.pdf" target="_blank">Title From The PDF <span class="tag">(PDF)</span></a></li>
   ```

   If the section still says "No ... posted yet", replace that line with a `<ul class="pdf-list">` list.

## Adding a course

1. Copy `linear-algebra/` to a new folder (e.g. `differential-equations/`) and change the title.
2. Create `courses/differential-equations/notes/` and `.../practice/`.
3. Add an image to `images/` and copy a course card in the root `index.html`.

## Placeholders

- `images/linear-algebra-placeholder.svg` is a placeholder. Replace it with a real image
  and update the `<img>` in `index.html`.

## Hosting (GitHub Pages)

Published at https://ameet-rao.github.io/MathNotes/ from the repository root of the
default branch (Settings → Pages → Deploy from a branch). `.nojekyll` tells Pages to
serve the files as-is. All links are relative, so the site works under the `/MathNotes/` path.

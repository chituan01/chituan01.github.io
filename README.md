# chituan.github.io

Personal academic website of Anh-Chi Tuan — PhD student in Statistics and Computer
Science, Bocconi University. Live at <https://chituan.github.io>.

Plain HTML and one stylesheet. No build step, no dependencies: GitHub Pages serves the
root of `main` as-is, so a push is live in under a minute.

## Layout

```
index.html         About — bio, interests, contact, news
research.html      Research interests and projects
publications.html  Working papers, theses, talks
teaching.html      Courses
404.html           Not-found page
assets/style.css   The whole design: colours, type, layout, dark mode
assets/photo.jpg   Portrait (add this, then uncomment the <img> in index.html)
files/cv.pdf       CV (add this, then uncomment the CV links)
.nojekyll          Serve files verbatim; skip Jekyll processing
```

## Editing

Every page carries the same header, nav and footer as literal HTML — there are no
includes, so a change to the nav or the footer means editing all five files. That is the
price of having no build step; with five pages it is a find-and-replace.

Placeholders and templates are left in the files as HTML comments (`<!-- ... -->`),
marked `TODO` where a real value is needed. To add a paper, a course or a talk, copy the
commented template in that page, uncomment it and fill it in.

Two things are commented out until their files exist — uncommenting them before that
would leave broken links:

- the CV link in every nav and in the contact row on `index.html`, waiting on `files/cv.pdf`
- the portrait on `index.html`, waiting on `assets/photo.jpg`

## Local preview

Open `index.html` in a browser, or serve the folder so root-relative links behave the way
they do in production:

```
python -m http.server 8000
```

then visit <http://localhost:8000>.

## Deploying

```
git add -A
git commit -m "Update site"
git push
```

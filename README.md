# Document Archive

A minimal GitHub Pages document browser for PDFs, HTML files, and YouTube links.

Built as a single self-contained HTML file with:

* Recursive folder browsing
* Inline preview panel
* Search/filtering
* YouTube thumbnail support
* GitHub API-powered repository navigation
* Automatic GitHub Pages repo detection

---

## Features

### Documents

Supports:

* `.pdf`
* `.html`

Documents can:

* Preview inside the side panel
* Open in a new tab
* Be searched instantly

---

### YouTube Links

Create a file ending in:

```txt
.youtube
```

Example:

```txt
My Video.youtube
```

Inside the file:

```txt
https://youtu.be/dQw4w9WgXcQ
```

The filename becomes the displayed title automatically.

---

## Folder Structure

Example repository:

```txt
docs/
├── index.html
├── Essays/
│   ├── Nietzsche.pdf
│   ├── Notes.html
│   └── Lecture.youtube
├── Philosophy/
│   ├── Plato.pdf
│   └── Aristotle.html
```

---

## Setup

### Option 1 — GitHub Pages (recommended)

1. Create a GitHub repository
2. Upload:

   * `index.html`
   * your folders/files
3. Enable GitHub Pages:

   * Settings → Pages
   * Deploy from `main`
4. Open your Pages URL

The archive auto-detects:

* GitHub username
* repository name

No configuration needed.

---

## Manual Configuration

If auto-detection fails, edit:

```js
const CFG = {
  owner: '',
  repo: '',
  branch: 'main',
}
```

Example:

```js
const CFG = {
  owner: 'johndoe',
  repo: 'archive',
  branch: 'main',
}
```

---

## Supported File Types

| Type          | Supported |
| ------------- | --------- |
| PDF           | Yes       |
| HTML          | Yes       |
| YouTube Links | Yes       |
| DOCX          | No        |
| MP4           | No        |

---

## Adding HTML Files

Simply place `.html` files anywhere in the repository:

```txt
Essay.html
```

They will automatically:

* appear in the archive
* open in the preview panel
* work in search results

---

## Search

The search bar:

* auto-expands folders
* filters documents instantly
* highlights matching text

---

## Preview Panel

The right-side panel uses an iframe to preview:

* PDFs
* HTML documents

Press:

```txt
ESC
```

to close the preview panel.

---

## Ignored Files

The following are hidden automatically:

```txt
index.html
README.md
.gitignore
LICENSE
.nojekyll
CNAME
```

Edit the `ignore` set to customize this behavior.

---

## Notes

### GitHub API Rate Limits

Unauthenticated GitHub API requests are limited.

If browsing stops working temporarily:

* wait a minute
* refresh the page

---

## License

Free to use and modify.

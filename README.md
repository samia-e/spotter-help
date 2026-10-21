# Spotter Help Library

A searchable library of video guides and FAQs. It is a plain website (no build step). All content lives in `library.json`.

## Publish it on GitHub Pages (about 10 minutes)

1. Sign in at github.com and click **New repository**. Name it, for example, `spotter-help`. Choose **Private** if your plan allows private Pages, otherwise Public. Click **Create**.
2. Click **uploading an existing file**. Drag in everything from this folder: `index.html`, `library.json`, `README.md` and the `assets` folder. Click **Commit changes**.
3. Open **Settings > Pages**. Under **Branch**, choose `main` and `/ (root)`, then **Save**.
4. After a minute the page shows your link, for example `https://YOUR-NAME.github.io/spotter-help/`. Open it to check.
5. Optional: under **Pages > Custom domain**, add an address such as `help.yourcompany.com` and follow GitHub's DNS instructions.

Check GitHub's current rules for private Pages and file size limits before you rely on them.

## Add or edit content

1. In the repo, open `library.json` and click the pencil icon.
2. Copy an existing block, change the text, and click **Commit changes**. The site updates in about a minute.
3. Keep the commas and quotes exactly as in the examples. If the site shows "Could not load library.json", there is a typo. Paste the file into jsonlint.com to find it.

### A guide
- `id`: short, unique, no spaces (for example `save-a-template`)
- `product`: one of `tms`, `app`, `fuel`, `sen`, `int`
- `video`: a file in the repo, for example `assets/my-video.mp4`
- `link`: a Loom, YouTube or Vimeo link (plays inside the page). Use either `video` or `link`.
- `verified`: `true` only after an expert has checked it
- `updated`: date as `YYYY-MM-DD`
- `steps` and `faqs`: lists, as in the example

### A standalone FAQ
Add to the `faqs` list: `{"id": "f1", "q": "Question?", "a": "Answer.", "product": "tms"}`

### Add a video file
Open the `assets` folder, click **Add file > Upload files**, and keep files under about 25 MB (compress them first). Larger videos are better hosted on Loom, YouTube or Vimeo.

### Change the blue
In `index.html`, find `--sign:#1558d6;` and replace it with Spotter's exact blue. Also change the dark-mode `--sign` value.

## Notes
- The site only works through a web address (GitHub Pages or a local server), not by double-clicking `index.html`.
- Anyone who can edit the repo can change the content. Use GitHub's branch protection and pull requests if you want approval before changes go live.

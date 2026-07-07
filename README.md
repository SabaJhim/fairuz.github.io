# Fairuz Mubashwera — Academic Website

A single-page academic homepage, built as one self-contained `index.html`
(HTML + CSS, no build step, no dependencies). It is designed to be hosted for
free on **GitHub Pages**.

## Files

| File          | Purpose                                                       |
|---------------|---------------------------------------------------------------|
| `index.html`  | The entire website. Edit this to change any content.          |
| `cv.pdf`      | Your CV. The "Download CV" button links here.                 |
| `README.md`   | This file (not published; just for you).                      |
| `profile.jpg` | *(optional)* Your photo — see "Add a photo" below.            |

---

## Deploy to GitHub Pages (≈5 minutes)

You can use **either** a user site (nice URL) **or** a project site. Instructions for both.

### Option A — User site: `https://<username>.github.io` (recommended)

1. **Create the repository.** On GitHub, click **New repository**. Name it
   **exactly** `<username>.github.io` (e.g. if your username is `fairuz`, name it
   `fairuz.github.io`). Set it to **Public**. Do **not** add a README (you already have one).

2. **Upload the files.** On the new repo page, click **uploading an existing file**
   (or **Add file → Upload files**). Drag in `index.html`, `cv.pdf`, and your
   `profile.jpg` if you have one. Scroll down and click **Commit changes**.

3. **Turn on Pages.** Go to **Settings → Pages**. Under *Build and deployment*,
   set **Source = Deploy from a branch**, **Branch = `main`**, **Folder = `/ (root)`**,
   then **Save**.

4. **Visit your site.** Wait 1–2 minutes, then open
   `https://<username>.github.io`. Done.

### Option B — Project site: `https://<username>.github.io/<repo>`

Same as above, but name the repo anything you like (e.g. `academic-website`).
After enabling Pages (Settings → Pages → Deploy from a branch → `main` → `/root`),
your URL will be `https://<username>.github.io/academic-website/`.

> **Tip (command line alternative to steps 1–2):**
> ```bash
> git init
> git add index.html cv.pdf            # add profile.jpg too if you have one
> git commit -m "Initial academic website"
> git branch -M main
> git remote add origin https://github.com/<username>/<repo>.git
> git push -u origin main
> ```
> Then do steps 3–4 in the GitHub web UI.

---

## Customize the content

Everything lives in `index.html`. Open it in any text editor and edit the text
between the tags — no coding needed for the common changes below.

### Fill in the placeholders
Search the file for `[Name]` and `href="#"` and replace them:

- **Supervisor name** — search for `[Name]` (in the thesis entry).
- **LinkedIn URL** — replace `https://linkedin.com/in/Fairuz` with your real profile.
- **GitHub URL** — replace `https://github.com/Fairuz`.
- **Google Scholar** — the Scholar link is `href="#"`; paste your Scholar URL, or
  delete that whole `<li>…Google Scholar…</li>` line if you don't have one yet.
- **Trajectory annotation website** — two `href="#"` links (in the AV research
  entry and the Projects card); paste the live survey URL.
- **University link** — the "Presidency University" link is `href="#"`; point it
  to the university site if you wish.

### Add a photo (optional but recommended)
1. Put a square image named `profile.jpg` in the same folder.
2. In `index.html`, find this line:
   ```html
   <div class="avatar">FM</div>
   ```
   and replace it with:
   ```html
   <img src="profile.jpg" class="avatar" alt="Fairuz Mubashwera">
   ```
   (The `.avatar` styling already crops it to a rounded square.)

### Update the CV
Just replace `cv.pdf` with a new file of the **same name**. The download button
will serve the new version automatically.

### Change accent color / fonts (optional)
At the top of the `<style>` block, edit the CSS variables in `:root`:
```css
--accent:#1f3d6e;   /* the deep ink-blue used for links, chips, buttons */
--paper:#fbfaf7;    /* page background */
```
Fonts are loaded from Google Fonts (`Newsreader` for headings, `Inter` for body);
swap the `<link>` and the `font-family` rules if you want different typefaces.

---

## Updating the live site later

Any time you change a file: commit and push (or re-upload via **Add file →
Upload files** and overwrite). GitHub Pages rebuilds within a minute or two.
If you don't see changes, do a hard refresh (Ctrl/Cmd + Shift + R) — the browser
may be caching the old version.

---

## Optional: custom domain

If you own a domain (e.g. `fairuz.dev`), add it under **Settings → Pages →
Custom domain**, then create the DNS records GitHub shows you. GitHub will issue
a free HTTPS certificate automatically.

---

## Notes

- The site is **fully static** — no server, database, or build tools. This makes
  it fast, free to host, and essentially maintenance-free.
- It is **responsive** (works on phones), keyboard-accessible, and lightweight
  (one HTML file + one PDF).
- Nothing here uses browser storage or external services beyond Google Fonts,
  so it will keep working indefinitely.

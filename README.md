# Mahesh Kirubanidhi S — Portfolio

A single-page personal portfolio built with plain HTML, CSS and JavaScript (no build step, no frameworks).

## Structure

```
index.html
style.css
script.js
assets/
  images/profile.jpg
  resume/Mahesh_Kirubanidhi_S_Resume.pdf
  certificates/NPTEL_Cloud_Computing.pdf
  certificates/NPTEL_Industry_4.0_and_IIoT.pdf
```

## Run locally

Double-clicking `index.html` works, but opening it directly from disk (`file://`) can block the download links
in some browsers. It's better to serve it over a local server:

```bash
# from inside the project folder
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

(Any static server works — `npx serve`, VS Code's "Live Server" extension, etc.)

## Deploy to GitHub Pages

1. Create a new GitHub repository (e.g. `portfolio`).
2. Push these files to the repository root:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/maheshdev16/portfolio.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**.
4. Under **Source**, choose the `main` branch and `/ (root)` folder, then save.
5. GitHub will publish the site at `https://maheshdev16.github.io/portfolio/` within a minute or two.

## Updating content later

- **Text/content**: edit the relevant section directly in `index.html`.
- **Colors/fonts/spacing**: edit the CSS variables at the top of `style.css` under `:root`.
- **Photo, resume or certificates**: replace the files inside `assets/` with the same file names, or update the
  file paths in `index.html` if you rename them.

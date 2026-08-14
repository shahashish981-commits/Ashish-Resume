# Ashish Shah — Resume Website

Static site. No build command needed — just HTML, CSS, JS.

## Files
- `index.html` — all page content (text, sections)
- `style.css` — all colors, spacing, layout
- `script.js` — mobile menu behavior
- `photo.png` — your photo
- `Ashish_Shah_Resume.pdf` — the file the Download Resume button serves
- `vercel.json` — tells Vercel this is a static site (no build step)

## First-time deploy (GitHub + Vercel)
1. Create a free account at github.com (if you don't have one).
2. Create a new repository, e.g. `ashish-resume-site`. Keep it Public. Don't add a README when creating it (this one will replace it).
3. On the repo page: **Add file → Upload files**, drag in every file from this folder, then **Commit changes**.
4. Go to vercel.com → **Add New → Project → Import Git Repository** → select your repo.
5. Leave all settings as default (Framework Preset: "Other", no build command) → **Deploy**.
6. Vercel gives you a live URL, e.g. `https://ashish-resume-site.vercel.app`.

## Making changes later (no re-upload needed)
Once the repo is connected to Vercel, any change you commit on GitHub automatically redeploys the live site in ~30 seconds.

- **Change text** (job title, summary, experience bullets): open `index.html` on GitHub.com, click the pencil (Edit) icon, edit the text between the tags, then **Commit changes**.
- **Swap your resume PDF**: on GitHub, delete the old `Ashish_Shah_Resume.pdf`, then **Add file → Upload files** with the new one using the exact same filename `Ashish_Shah_Resume.pdf` (so the Download button keeps working). If you use a different filename, also update the two `href="Ashish_Shah_Resume.pdf"` links in `index.html`.
- **Swap your photo**: same idea — replace `photo.png` with the same filename, or update the `src="photo.png"` line in `index.html` if the filename changes.
- **Change colors**: all colors are defined once at the top of `style.css` under `:root` (e.g. `--purple`, `--teal`, `--bg-top`). Change those hex values and the whole site updates.
- **Change phone/email/LinkedIn**: search for them in the Contact section near the bottom of `index.html`.

## Structure of index.html (for quick edits)
- `<section id="home">` — hero / intro
- `<section id="about">` — about text
- `<section id="experience">` — work history timeline
- `<section id="skills">` — skills grid
- `<section id="education">` — education, certifications, languages
- `<section id="contact">` — email / call / WhatsApp / LinkedIn buttons

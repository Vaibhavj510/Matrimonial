# Vaibhav Jadhav — Matrimonial Portfolio

Personal matrimonial portfolio website. Built with plain HTML, CSS, and JavaScript. Bilingual — English and Marathi. Hosted on GitHub Pages.

---

## File Structure

```
├── index.html                     ← main portfolio file
├── images/
│   ├── hero-vietnam.jpg           ← hero photo (Vietnam golden hour)
│   ├── photo-jaisalmer.jpg        ← full-width break after "Who I Am"
│   ├── photo-varanasi.jpg         ← full-width break after "Looking For"
│   ├── photo-camera.jpg           ← gallery photo 1
│   └── photo-jodhpur.jpg          ← gallery photo 2
├── biodata/
│   └── Vaibhav_Jadhav_Biodata.pdf ← downloadable biodata PDF
└── README.md                      ← this file
```

---

## How to Replace a Photo

1. Prepare your new photo — resize to max 1400px wide, JPG format, quality 85% (use [squoosh.app](https://squoosh.app))
2. Name it exactly the same as the photo you are replacing (e.g. `photo-jodhpur.jpg`)
3. Go to your repo → click `images/` folder → **Add file → Upload files**
4. Upload your new photo — GitHub will overwrite the old one automatically
5. Wait 60 seconds → your live site updates

---

## How to Add a New Photo to the Gallery

1. Upload your new photo to the `images/` folder (e.g. `photo-korea.jpg`)
2. Open `index.html` → click the pencil icon to edit
3. Find the comment `<!-- TO ADD A NEW PHOTO -->` in the gallery section
4. Copy one existing gallery tile block and paste it after the last one:

```html
<div class="gallery-tile">
  <img src="images/photo-korea.jpg" alt="Vaibhav in Korea" loading="lazy">
  <div class="gallery-tile-overlay"></div>
  <div class="gallery-tile-caption"
       data-en="South Korea · Seoul"
       data-mr="दक्षिण कोरिया · सोल">South Korea · Seoul</div>
</div>
```

5. Update `src`, `alt`, `data-en`, and `data-mr` with your new photo details
6. Commit changes → site updates in ~60 seconds

---

## How to Update Text Content

Open `index.html` and use **Ctrl+F** to search for the text you want to change.

Every piece of text appears twice — once for English (`data-en`) and once for Marathi (`data-mr`). Always update both.

| Section | Search for |
|---|---|
| Hero tagline | `Western Ghats` |
| Who I Am — paragraph 1 | `monsoons and mango orchards` |
| Who I Am — paragraph 2 | `quiet start to the morning` |
| Family intro | `close-knit, supportive family` |
| Parents card | `heart of our family` |
| Brothers card | `middle of three` |
| What I Am Looking For — para 1 | `mirror image of myself` |
| What I Am Looking For — para 2 | `Germany is where my life is built` |
| Closing quote | `suitcase and a lot of hope` |
| Contact sub-text | `Families are welcome` |

---

## How to Update Contact Details

Search in `index.html` for:

| Detail | Search for |
|---|---|
| Email address | `vaibhavj510@yahoo.in` |
| LinkedIn URL | `linkedin.com/in/vaibhav-jadhav` |
| Instagram URL | `instagram.com/vaibhavj05` |
| Biodata PDF filename | `Vaibhav_Jadhav_Biodata.pdf` |

---

## How to Update the Biodata PDF

1. Prepare your new PDF
2. Name it exactly: `Vaibhav_Jadhav_Biodata.pdf`
3. Go to repo → `biodata/` folder → **Add file → Upload files**
4. Upload — GitHub overwrites the old file automatically

---

## Language Toggle

The site has an **EN / Marathi** toggle in the navbar.

All text in `index.html` uses `data-en` and `data-mr` attributes:

```html
<p data-en="English text here"
   data-mr="मराठी मजकूर येथे">English text here</p>
```

When the user clicks the toggle, JavaScript swaps all visible text simultaneously. The preference is saved in the browser so returning visitors see their last chosen language.

---

## GitHub Pages — Enable or Re-enable

If the site stops working or you need to re-enable Pages:

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source** select **Deploy from a branch**
4. Branch: **main** · Folder: **/ (root)**
5. Click **Save**
6. Wait 60–90 seconds
7. Your live URL: `https://[your-username].github.io/matrimonial/`

---

## Quick Checklist When Something Breaks

| Problem | Fix |
|---|---|
| Photo not loading | Check filename matches exactly — lowercase, `.jpg` not `.jpeg` |
| Site shows README text only | Check `index.html` is in repo root, not inside a folder |
| Save button greyed out in Pages | Make a small edit to `index.html`, commit, then try again |
| Old version showing | Hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac) |
| Marathi text not showing | Check `data-mr` attribute exists on that element |

---

*Built with plain HTML · No frameworks · No build tools · GitHub Pages ready*

# 📄 [Resume Builder](https://mrkkk091.github.io/Resume-Builder/)

A free, modern resume builder that runs entirely in your browser. No backend, no sign-up, nothing uploaded. Everything lives in one static `index.html`, so it works on GitHub Pages as-is.

**Dev: Glmrk**

## Features

- **80 templates** across three layouts: single column, header band and sidebar
- **Template preview**: tap any template to see its layout in an animated popup, then press *Use this template*
- **Live editing**: change any field and the A4 preview updates instantly
- **Photo placement**: upload a photo, drag it anywhere on the page, resize it from the corner, and pick circle, rounded or square
- **Extract photo from a document**: upload a picture of an ID, CV or form, drag the box over your photo and crop it out (face auto-detect works only on browsers that support it)
- **Export**:
  - **PDF** through your browser's print dialog (*Save as PDF*)
  - **PNG / JPG** image of the finished resume
  - **JSON** save and load, so you can edit later
- **Autosave** to your browser's local storage
- **Dark and light mode**, following your device setting and remembered between visits
- Responsive, so it works on phones and desktops
- Repeatable sections for experience, education and projects, plus accent colour and font options

## Pages

| Page | What it does |
|------|--------------|
| Home | Start screen |
| Templates | Browse all 33 templates and preview them |
| Editor | Edit your details and see the live resume |
| Export | Print / PDF, save as image, save or load JSON |

## Deploy on GitHub Pages

1. Create a new public repository (for example `resume-builder`).
2. Upload `index.html` to the root of the repository.
3. Go to **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.
5. After a minute or two, open `https://<your-username>.github.io/<repo-name>/`.

No build step is needed.

## How to use

1. Open **Templates**, tap a design and press **Use this template**.
2. In the **Editor**, fill in your details. Drag the photo on the preview to place it.
3. Open **Export** (or use *Save image* in the editor) to download your resume.

### Exporting a PDF

Press **Print / PDF**, then choose **Save as PDF** as the destination in the print dialog. If colours are missing, turn on *Background graphics* in the print options.

## Requirements and limitations

- **Internet connection needed** for the Google Fonts and for the image-export library (html2canvas, loaded from cdnjs). Without it, fonts fall back to system fonts and image export won't work.
- Your data is stored only in your own browser. Clearing site data removes it, so use **Save JSON** for backups.
- The printed PDF is A4. The Letter option changes the preview only.
- The photo extractor takes images (JPG, PNG). For a PDF document, take a screenshot of the page and upload that.

## Tech

Plain HTML, CSS and JavaScript in a single file.

- [html2canvas](https://html2canvas.hertzen.com/) for PNG/JPG export
- Google Fonts: Inter, Lora and Manrope
- Browser `localStorage` for autosave

## Project structure

```
resume-builder/
├── index.html   # the whole app
└── README.md
```

## License

MIT. Attribution: **Dev: Glmrk**

The "Dev: Glmrk" credit appears in the app header and in the footer of every resume.

# Fawad Mustafa | Full Stack AI Engineer (Portfolio)

Personal portfolio website of **Fawad Mustafa**, a Full Stack AI Engineer from Rahim Yar Khan, Pakistan.
It is a plain static site (HTML, CSS and JavaScript). There is no build step and no framework.

## Features

- Welcome screen, animated hero, light and dark theme (remembers your choice)
- About, Services, Projects (pinned scroll), Experience timeline, Tech stack and Contact sections
- **Portfolio Assistant**: a chat widget that answers questions about Fawad's projects, skills, experience and contact details, in English and Urdu, by typing or by voice
- **Meeting scheduler**: pick a date and time (Pakistan time, Mon to Fri, 10:00 to 18:00), then add it to Google Calendar, download an `.ics` file or email Fawad
- Downloadable resume (PDF)
- Responsive layout for phone, tablet and desktop

## Project structure

```
portfolio/
├── index.html                 # page markup (all sections)
├── css/
│   └── style.css              # all styles, light and dark theme
├── js/
│   ├── main.js                # theme, slider, projects, chat assistant, voice, meeting scheduler
│   ├── counters.js            # animated numbers in experience cards
│   ├── timeline.js            # reveals experience cards on scroll
│   └── welcome.js             # welcome screen and pinned projects scroll
├── assets/
│   ├── Fawad_Mustafa_CV.pdf   # resume (replace this file to update the CV)
│   ├── favicon.svg
│   └── images/
│       ├── portrait.jpg       # profile photo
│       └── leaf-sample.jpg    # plant disease project image
└── README.md
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy on Vercel

1. Put **all of these files and folders** in the root of a GitHub repository. `index.html` must be directly in the root, not inside another folder.
2. In Vercel choose **Add New, Project**, then import the repository.
3. Set **Framework Preset** to **Other**. Leave Build Command and Output Directory empty. Root Directory stays `./`.
4. Click **Deploy**. Every push to GitHub redeploys the site automatically.

Alternative without GitHub: install the Vercel CLI (`npm i -g vercel`), open the project folder in a terminal and run `vercel --prod`.

## Customising

| What | Where |
| --- | --- |
| Text, links, project cards, contact details | `index.html` |
| Colours, fonts, spacing, dark theme | `css/style.css` (theme variables are at the top) |
| Assistant answers (`KB`), assistant instructions (`CTX`), meeting hours, email | `js/main.js` |
| Resume | replace `assets/Fawad_Mustafa_CV.pdf` (keep the same name) |
| Photo | replace `assets/images/portrait.jpg` |

## Good to know

- **Assistant on your own domain:** the live AI answers only work when the page is opened inside Claude. On Vercel the assistant answers from its built-in knowledge (the `KB` list in `js/main.js`), which already covers projects, skills, experience, education and contact. To get live AI answers on your own site you would need a small backend (for example a Vercel serverless function) that calls an AI API with a secret key. Never put an API key in the front-end code.
- **Meeting requests** are not stored on a server. Confirming a meeting opens Google Calendar or the visitor's email app, so Fawad receives the invite from there.
- Fonts are loaded from Google Fonts, so the first load needs internet.

## Contact

- Email: fawadmustafa1731@gmail.com
- LinkedIn: https://www.linkedin.com/in/fawad-mustafa-19983b277
- GitHub: https://github.com/Fawad1731

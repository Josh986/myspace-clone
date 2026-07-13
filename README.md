# 💼 MySpace-Themed Career Profile

A pixel-perfect, single-page **career / resume page disguised as a classic MySpace profile (2005–2008 era)**.
Pure **HTML5 + CSS3 + vanilla JavaScript** — no frameworks, no build step, no dependencies.
Drop it on GitHub Pages and it just works.

Live profile: **Joshua Ly** — Technical Business Analyst on a Product Owner track. Every nostalgic MySpace module has been repurposed to showcase real professional experience. 🖥️

---

## 🎭 The twist — how MySpace maps to a resume

| MySpace element | Career-page purpose |
|-----------------|---------------------|
| Display name + headline | Your name + professional tagline |
| Mood → **Status** | `Open to Work` availability badge (blinking green) |
| Profile photo | Headshot / monogram avatar |
| Contact box | Real links: email, LinkedIn, phone, resume, portfolio |
| MySpace URL | Your LinkedIn vanity URL |
| Blurbs (About Me / Who I'd like to meet) | Professional summary + target roles |
| **Professional Experience** module | Job history timeline (role, company, dates, impact) |
| Friend Space → **Toolbox** | "Top 8 Tools" grid (Jira, Confluence, Miro, …) |
| Interests → **Skills & Expertise** | Categorized skill groups |
| Details table | Title, track, experience, certification, education, location |
| Comments wall → **Career Highlights** | Signature achievements & project wins |

---

## 📁 What's inside

| File | Purpose |
|------|---------|
| `index.html` | The whole page + a **config object at the top** with all your swappable data |
| `style.css`  | All the retro styling (blue gradient headers, tiled bg, tiny Verdana fonts) |
| `README.md`  | This file |

Everything uses **relative paths**, so it's GitHub Pages ready out of the box.

---

## 🚀 Publish it on GitHub Pages

1. **Fork or clone** this repo:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```

2. Push it to your own GitHub repository (if you cloned it fresh):
   ```bash
   git remote set-url origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

3. On GitHub, go to **Settings → Pages**.

4. Under **Build and deployment**:
   - **Source:** `Deploy from a branch`
   - **Branch:** `main` &nbsp;/&nbsp; folder `/ (root)`
   - Click **Save**.

5. Wait ~1 minute, then visit:
   ```
   https://<your-username>.github.io/<your-repo>/
   ```
   Your profile is live. 🎉

---

## 🎨 Customize your profile (no coding required)

All the swappable data lives in **one JavaScript object** at the very top of
`index.html`, inside a `<script>` tag. Open the file, find the block that starts
with `var PROFILE = {`, and edit the values. Save, refresh — done. No build step.

```js
var PROFILE = {
  // ---- Basic identity ----
  name: "Joshua Ly",
  headline: "\"Translating complex business needs into clear technical solutions.\" ★",
  mood: "Open to Work",
  photo: "https://ui-avatars.com/api/?name=Joshua+Ly&size=250&background=33547a&color=ffffff",

  // ---- Details table ----
  title: "Technical Business Analyst",
  track: "Product Owner Track",
  experience: "5+ Years",
  certification: "UT Austin Gold Seal (BA)",
  education: "B.A. — UT Austin",
  location: "Pasadena, TX",

  online: true,              // true = blinking green "Open to Work!" dot
  profileViews: "5,281",     // retro visitor counter

  // ---- Real contact links ----
  email: "joshualy986@gmail.com",
  phone: "(832) 640-1756",
  linkedin: "https://www.linkedin.com/in/joshua-ly/",

  song: { title: "Now Playing: \"Career Anthem\"", src: "song.mp3" },

  aboutMe: "Technical Business Analyst on a Product Owner track...",
  meet:    "Hiring managers with Business Analyst III / PO openings...",

  // ---- Skills & Expertise ----
  interests: {
    business: "Requirements Gathering • User Stories • Gap Analysis...",
    agile:    "Backlog Refinement • Sprint Planning • Agile Ceremonies...",
    systems:  "ERP • MES • SCADA • RFID • SaaS • Azure AD • ManageEngine",
    testing:  "UAT Planning • Test Scripts • Defect Triage • Regression...",
    methods:  "Agile / Scrum • SDLC • BPMN • Data Validation • RCA"
  },

  // ---- Top 8 Tools (grid re-flows automatically) ----
  friends: [
    { name: "Jira",       img: "https://placehold.co/80x80/0052CC/ffffff?text=Jira" },
    { name: "Confluence", img: "https://placehold.co/80x80/172B4D/ffffff?text=Conf" }
    // ...up to 8
  ],
  toolCount: 8,

  // ---- Career highlights (comment-wall style) ----
  highlights: [
    { user: "MES SaaS Deployment", text: "Drove 99% user adoption of a new MES SaaS platform..." }
  ],

  // ---- Experience timeline ----
  experienceList: [
    { role: "IT Business Analyst", company: "The Lab Consulting",
      dates: "Jul 2025 – Oct 2025", blurb: "Standardized requirements, documentation..." }
  ]
};
```

### Common tweaks

- **Change your photo:** set `photo` to any image URL, or drop a file next to
  `index.html` and use a relative path like `"headshot.jpg"`.
- **Wire up the "Download Resume" link:** drop a `resume.pdf` in the folder and
  point the contact link to it (see the `contactRows` array in the injection script).
- **Edit your Top 8 Tools:** add/remove objects in the `friends` array. The grid
  automatically re-flows into rows of 4.
- **Add jobs:** append objects to `experienceList`.
- **Toggle availability:** set `online: false` to swap the blinking green
  "Open to Work!" badge for a grey "Offline" label.
- **Use `&` and `<` in text:** write them as `&amp;` and `&lt;` inside the strings.

---

## 🖌️ Style tweaks (optional)

Open `style.css` and look for the MySpace palette:

- Classic blue: `#6699CC`
- Orange accent: `#FF6600`
- Dark header/border blue: `#33547a`

Section headers use CSS gradients to mimic the original MySpace header bars,
and the background is a pure-CSS tiled pattern (no image files needed).

---

## 🧪 Run it locally

```bash
# either double-click index.html, or:
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## 📜 Notes

- Tool/avatar tiles come from [placehold.co](https://placehold.co) and the
  monogram from [ui-avatars.com](https://ui-avatars.com) — swap in your own anytime.
- A retro career page for fun. Not affiliated with MySpace / Meta.

**MySpace v3.0 | © 2006-style layout · Joshua Ly · Career Profile** *(parody)*

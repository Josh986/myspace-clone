# 💿 MySpace Clone — 2006 Emo/Scene Profile

A pixel-perfect, single-page recreation of a classic **MySpace profile (2005–2008 era)**.
Pure **HTML5 + CSS3 + vanilla JavaScript** — no frameworks, no build step, no dependencies.
Drop it on GitHub Pages and it just works.

Default profile: **`xX_StarlightEmo_Xx`** — black eyeliner, band tees, MCR on the profile song, and a Top 8 that means everything. 🖤

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
   (Or click **Fork** at the top-right of the GitHub page.)

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
  name: "xX_StarlightEmo_Xx",
  headline: "\"the world is ugly, but you're beautiful to me...\" ♥",
  mood: "emo",
  photo: "https://i.pinimg.com/736x/2d/a6/26/2da626c120150dc33e7cc6da7b40eb92.jpg",

  age: 22,
  gender: "Female",
  location: "Los Angeles, CA",
  status: "Single",
  zodiac: "Scorpio",
  lastLogin: "7/13/2026",

  online: true,              // true = blinking green "Online Now!" dot
  profileViews: "14,892",    // retro visitor counter

  song: {
    title: "My Chemical Romance - Welcome to the Black Parade",
    src: "song.mp3"          // drop your own .mp3 next to index.html
  },

  aboutMe: "hey <3 im just a girl living in a black & white world...",
  meet:    "anyone who gets the reference in my headline...",

  interests: {
    general:    "sleeping, mirror pics, Hot Topic, thrifting...",
    music:      "MCR, Fall Out Boy, Paramore, Panic! at the Disco...",
    movies:     "Donnie Darko, The Nightmare Before Christmas...",
    television: "Invader Zim, Daria, MTV, Adult Swim",
    books:      "The Perks of Being a Wallflower, Go Ask Alice...",
    heroes:     "my mom, Gerard Way, Tim Burton"
  },

  // Top 8 — add/remove entries freely (grid re-flows automatically)
  friends: [
    { name: "Tom",            img: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Style_-_Wouldn%27t_It_Be_Nice.png/1280px-Style_-_Wouldn%27t_It_Be_Nice.png" },
    { name: "xXbrokenDollXx", img: "https://image.aiavatarmaker.net/imgs/2026-02-11/linkedin-twitter-avatar-square-circle-crop.webp" }
    // ...up to 8 (or more)
  ],
  friendCount: 337
};
```

### Common tweaks

- **Change your photo:** set `photo` to any image URL, or drop a file next to
  `index.html` and use a relative path like `"me.jpg"`.
- **Add a real profile song:** put an `.mp3` in the project folder and set
  `song.src` to its filename (e.g. `"black-parade.mp3"`).
- **Edit your Top 8:** add/remove objects in the `friends` array. The grid
  automatically re-flows into rows of 4.
- **Go offline:** set `online: false` to swap the blinking green dot for a
  grey "Offline" label.
- **Use `&` and `<` in text:** write them as `&amp;` and `&lt;` inside the
  strings so they render correctly (the defaults already do this).

---

## 🖌️ Style tweaks (optional)

Want to change the colors? Open `style.css` and look for the MySpace palette:

- Classic blue: `#6699CC`
- Orange accent: `#FF6600`
- Dark header/border blue: `#33547a`

Section headers use CSS gradients to mimic the original MySpace header bars,
and the background is a pure-CSS tiled pattern (no image files needed).

---

## 🧪 Run it locally

No server needed — just open the file:

```bash
# either double-click index.html, or:
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## 📜 Notes

- Placeholder images come from [picsum.photos](https://picsum.photos) — swap in
  your own anytime.
- The profile song `src` is a placeholder; add your own `.mp3` to hear it.
- Built for fun and nostalgia. Not affiliated with MySpace / Meta.

**MySpace v3.0 | © 2006 MySpace Inc. All Rights Reserved** *(parody)*

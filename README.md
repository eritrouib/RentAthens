# 🏛️ RentAthens

A personal property rental website for rooms and studios in Athens, Greece.  
Live site: [eritrouib.github.io/RentAthens](https://eritrouib.github.io/RentAthens)

---

## About

RentAthens has been helping tenants find quality accommodation in Athens since 2018.  
All apartments are newly renovated — cosy, spacious, and well-connected to the city.

**Contact:** Eriola Impersimi  
**WhatsApp:** +30 697 434 0718  
**Facebook:** [facebook.com/eriimpersimi](https://www.facebook.com/eriimpersimi/)

---

## Properties

### Elpidos Street — Athens City Centre
Shared apartment of four rooms on the second floor of a classic Athenian building.  
4 min walk from the Green metro line · 3 min walk from AUEB.

### Spartis Street — Kallithea
A private multi-floor building with multiple unit types:

| Tab | Folder | Description |
|-----|--------|-------------|
| Ground Floor A | `images/Kallithea0a/` | Self-contained studio, ground floor |
| Ground Floor B | `images/Kallithea0b/` | Self-contained studio, ground floor |
| 1st Floor – 4 Rooms | `images/Kallithea1/` | Shared apartment, four private rooms |
| Upper Studio A | `images/Kallithea2a/` | Self-contained studio, upper floor |
| Upper Studio B | `images/Kallithea2b/` | Self-contained studio, upper floor |

---

## Adding Photos

Photos must be named `1.jpg`, `2.jpg`, `3.jpg` … and placed in the correct folder.

### Step 1 — Upload your photos to the right folder

```
images/
  Elpidos/         ← Elpidos apartment photos + optional tour.mp4
  Kallithea0a/     ← Ground Floor Studio A photos
  Kallithea0b/     ← Ground Floor Studio B photos
  Kallithea1/      ← 1st Floor 4-room apartment photos
  Kallithea2a/     ← Upper Studio A photos
  Kallithea2b/     ← Upper Studio B photos
```

### Step 2 — Update the photo counts in `index.html`

Open `index.html` and find the config section near the bottom:

```js
const ELPIDOS_CONFIG = {
    folder: 'images/Elpidos',
    count: 8,   // ← change this to how many photos you have
    ...
};

const KALLITHEA_CONFIG = [
    { label: 'Ground Floor A', folder: 'images/Kallithea0a', count: 5,  ... },
    { label: 'Ground Floor B', folder: 'images/Kallithea0b', count: 4,  ... },
    { label: '1st Floor',      folder: 'images/Kallithea1',  count: 6,  ... },
    { label: 'Upper Studio A', folder: 'images/Kallithea2a', count: 4,  ... },
    { label: 'Upper Studio B', folder: 'images/Kallithea2b', count: 4,  ... },
];
```

Change each `count` number to match how many photos you have in that folder. That's it!

### Adding a Video Tour (Elpidos)

Place your video file at `images/Elpidos/tour.mp4`.  
The **▶ Video Tour** button will appear automatically.  
To use a different filename or format, update this line in `index.html`:

```js
const ELPIDOS_VIDEO = 'images/Elpidos/tour.mp4';
```

Set it to `''` (empty string) to hide the button entirely.

---

## How to Create a New Folder on GitHub

GitHub doesn't allow empty folders. To create one:

1. Go to your repo and click **Add file → Create new file**
2. Type the path including a `/` — e.g. `images/Kallithea0a/placeholder.txt`
3. Add any placeholder text and commit
4. Then navigate into the folder and use **Add file → Upload files** to add your photos

---

## Tech Stack

- Plain HTML, CSS, JavaScript — no frameworks or build tools
- Hosted on **GitHub Pages**
- Fonts via Google Fonts (Raleway, Source Serif 4)
- Icons via Font Awesome 6

---

*© Eriola Impersimi · RentAthens · Athens, Greece*

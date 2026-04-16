# 🎓 Academic Hub

A personal academic portal built for managing class schedules, assignments and coursework — hosted on GitHub Pages.

**Live site:** [arnnavv.github.io/Masters_schedule](https://arnnavv.github.io/Academic_hub/)

---

## 📋 Features

- **Academic Portal** — central landing page with links to Class Schedule and Assignment Pipeline
- **Multi-section Calendar** — separate iCal feeds for Section A, Section B and Face to Face (F2F)
- **Live iCloud Sync** — calendar auto-syncs from iCloud every 5 minutes
- **Monthly & Weekly Views** — Google Calendar-style weekly view with pixel-perfect time positioning
- **Specialization Filters** — filter by Core, Finance, Marketing or Supply Chain
- **Event Modals** — click any event to see full details and join online class links
- **Session Management** — remembers your section selection with configurable session expiry
- **Timezone Aware** — all times automatically converted to the viewer's local timezone

---

## 🗂️ Project Structure

```
├── dev.html          # Development version (test changes here first)
├── index.html        # Production version (live on GitHub Pages)
├── css/
│   └── style.css     # All styles and CSS variables
├── js/
│   └── app.js        # All JavaScript logic
├── .gitignore
└── README.md
```

---

## ⚙️ Configuration

All section iCal URLs are stored in `js/app.js` under `SECTION_URLS`:

```javascript
const SECTION_URLS = {
  'A':   'https://your-section-a-ical-url',
  'B':   'https://your-section-b-ical-url',
  'F2F': 'https://your-f2f-ical-url',
};
```

Session duration is also configurable in `js/app.js`:

```javascript
const SESSION_DAYS = 30; // days before session expires and welcome page reappears
```

---

## 📅 Adding Events (iCloud Calendar)

Events are managed directly in iCloud Calendar. To categorise an event by specialization, add this to the event **Notes** field:

```
Specialization: Core
```

Supported values: `Core`, `Finance`, `Marketing`, `Supply Chain`

To add a **Join Online Class** link, paste the Zoom/Teams URL in the event **URL field**.

---

## 🚀 Deployment

This project is deployed via **GitHub Pages** from the `main` branch root directory. Any commit to `main` automatically updates the live site within a few minutes.

To test changes safely, edit `dev.html` first and access it at `/dev.html` before updating `index.html`.

---

## 🛠️ Built With

- Vanilla HTML, CSS and JavaScript — no frameworks or dependencies
- iCal format (`.ics`) for calendar data — compatible with iCloud, Google Calendar and Outlook
- GitHub Pages for free hosting

---

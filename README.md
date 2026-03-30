# 🎓 Faculty Portfolio Website

A complete, modern 8-page faculty portfolio website with dark/light themes, animated cursor, and full responsive design.

---

## 📁 Complete File Structure

```
faculty-portfolio/
│
├── index.html              ← Page 1: Landing Page (Hero, Stats, Social Links)
├── about.html              ← Page 2: About the Faculty
├── skills.html             ← Page 3: Technical & Academic Skills
├── experience.html         ← Page 4: Experience & Education (4 Timeline Tabs)
├── research.html           ← Page 5: Research (Papers, Patents, Copyrights, Projects, FDPs)
├── courses.html            ← Page 6: Courses & Certificates (Envelope Design)
├── gallery.html            ← Page 7: Activity Gallery (12 items, Lightbox)
├── contact.html            ← Page 8: Contact Details & Form
│
├── css/
│   ├── variables.css       ← CSS Variables & Dark/Light Theme tokens
│   ├── global.css          ← Reset, Typography, Cards, Buttons, Animations
│   ├── navbar.css          ← Navbar styles (desktop + mobile)
│   ├── cursor.css          ← Custom animated cursor styles
│   ├── index.css           ← Landing page specific styles
│   ├── pages.css           ← About, Skills, Experience, Research styles
│   └── secondary-pages.css ← Courses, Gallery, Contact styles
│
├── js/
│   ├── theme.js            ← Dark/Light theme toggle (localStorage persistent)
│   ├── cursor.js           ← Animated cursor with lerp smoothing
│   ├── navbar.js           ← Navbar scroll, hamburger, active link
│   ├── animations.js       ← Scroll reveal, counters, parallax, modals
│   ├── experience.js       ← Experience page 4-tab timeline switcher
│   ├── research.js         ← Research data, tab renderer, click modals
│   ├── gallery.js          ← Gallery filter + lightbox with keyboard nav
│   └── courses.js          ← Certificate data, envelope animation, modals
│
└── assets/
    ├── images/
    │   ├── faculty_photo.jpg      ← Add your faculty photo here
    │   └── gallery/
    │       ├── conf_2024.jpg      ← Conference photo 1
    │       ├── award_2023.jpg     ← Award photo
    │       ├── lecture_vit.jpg    ← Lecture photo
    │       ├── workshop_cyber.jpg ← Workshop photo
    │       ├── phd_grad.jpg       ← PhD graduation
    │       ├── conf_sg.jpg        ← International conference
    │       ├── research_award.jpg ← Research award
    │       ├── hackathon.jpg      ← Hackathon mentoring
    │       ├── nptel_course.jpg   ← NPTEL course
    │       ├── industry_visit.jpg ← Industry visit
    │       ├── seminar_iitd.jpg   ← IIT seminar
    │       └── women_tech.jpg     ← Women in tech award
    └── icons/                     ← Optional custom icons
```

---

## 🚀 How to Run

1. **Download / Extract** the folder
2. Open any `.html` file directly in your browser — **no server required**
3. Or run a local server for best experience:
   ```bash
   # Python 3
   cd faculty-portfolio
   python -m http.server 8080
   # Then open: http://localhost:8080
   
   # OR with VS Code: Install "Live Server" extension → Right-click index.html → Open with Live Server
   ```

---

## 🖼️ Adding Your Photos

### Faculty Photo (appears on Landing + About pages):
- Place your photo at: `assets/images/faculty_photo.jpg`
- Recommended size: **400×500px** or larger, portrait orientation
- In `index.html` find the placeholder comment and replace with:
  ```html
  <img src="assets/images/faculty_photo.jpg" alt="Your Name" class="hero-photo-img" />
  ```
- In `about.html` replace the placeholder div similarly.

### Gallery Photos:
- Add 12 photos to `assets/images/gallery/` with the filenames listed above
- In `gallery.html`, replace each `gallery-item-placeholder` div with:
  ```html
  <img src="assets/images/gallery/your_photo.jpg" alt="Description" />
  ```

---

## ✏️ Personalizing Content

### 1. Update Faculty Information
Edit these files to replace placeholder data:

**index.html** — Name, designation, department, university, stats, LinkedIn/Scholar URLs

**about.html** — Bio paragraphs, info grid (qualification, email, location), expertise tags

**skills.html** — All skill cards with names and proficiency levels (data-width="0–100")

**experience.html** — Timeline cards for each of the 4 tabs

**research.html** — Edit `js/research.js` → update `researchData` object with real papers, patents, projects, FDPs

**courses.html** — Edit `js/courses.js` → update `certificatesData` array

**gallery.html** — Update titles, tags, and photo paths for all 12 gallery items

**contact.html** — Email addresses, phone numbers, office address, social profile URLs

---

## 🎨 Theme Customization

All colors are CSS variables in `css/variables.css`:

```css
/* Change the gold accent to any color: */
--accent-gold: #d4af37;      /* Dark theme accent */
--accent-gold: #a07c20;      /* Light theme accent */

/* Change background: */
--bg-primary: #0a0e1a;       /* Main background */
--bg-secondary: #0f1628;     /* Secondary background */
```

---

## ✨ Key Features

| Feature | Details |
|---------|---------|
| **8 Full Pages** | All uniquely designed with shared nav/theme |
| **Dark / Light Theme** | Smooth toggle, persists via localStorage |
| **Animated Cursor** | Custom gold cursor with lerp ring tracking |
| **Scroll Animations** | IntersectionObserver reveal for all sections |
| **Counter Animation** | Stats animate to target numbers on scroll |
| **Timeline Tabs** | 4-tab experience/education switcher |
| **Research Modals** | Click any paper/patent/project for full details |
| **Envelope Certificates** | Click to open envelope, double-click for full modal |
| **Gallery Lightbox** | Filter + lightbox with prev/next keyboard navigation |
| **Parallax Hero** | Orbs follow mouse on landing page |
| **Fully Responsive** | Mobile-first, breakpoints at 480/768/900/1024px |
| **No Dependencies** | Pure HTML/CSS/JS — zero npm, zero build step |

---

## 📱 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile Chrome / Safari (cursor auto-hides on touch devices)

---

## 📝 Notes

- The contact form shows a success message (frontend only) — connect a backend or form service like **Formspree** for real email delivery:
  ```html
  <form action="https://formspree.io/f/YOUR_ID" method="POST">
  ```
- Google Scholar and LinkedIn URLs in `index.html` and `contact.html` need your real profile links
- All social links open in new tabs with `rel="noopener noreferrer"` for security

---

*Built with pure HTML5, CSS3 (custom properties + animations), and Vanilla JavaScript. No frameworks required.*

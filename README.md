
# Student Portal Dashboard (Offline-First)
![Project Status](https://img.shields.io/badge/status-active-success.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

A simple, self-contained, **offline-first** student dashboard designed to organize course materials, assignments, notes, and important links **without needing an internet connection**. The entire app lives inside a single HTML file for maximum portability.

The core idea: a central hub for your **local** study files and folders so you can study without the internet shaped temptation vortex.

> Current UI version: **Beta 1.4** (shown in the header inside `dashboard.html`).

<img width="1081" height="1091" alt="Screenshot 2026-02-08 020314" src="https://github.com/user-attachments/assets/3d4f63d5-9841-4eb3-9032-fb94d53cf846" />


## Features

- **Zero Installation:** Open `dashboard.html` in any modern browser.
- **Fully Offline-Friendly:** Uses a system font stack (no remote font downloads).
- **Local File Linking:** Link each module card to local folders.
- **Search + Keyboard Shortcuts:** Press `/` to focus search, `ESC` to clear (and close the modal).
- **Favorites System:** Star modules to pin them into a dedicated **⭐ Favorite Modules** section.
- **Quick Stats:** Total core modules, semester progress %, favorites count, and pending tasks.
- **Assignments Widget:**
  - Add tasks with optional due date and priority.
  - Auto-highlights **due-soon/urgent** based on due date proximity.
  - “Clean Up” removes completed items.
- **Quick Notes:** Persistent notes saved automatically.
- **Pomodoro Timer:** Built-in 25/5 timer with start/pause/reset.
- **Data Portability (Export / Import):**
  - Export your favorites, tasks, notes, theme, and tip preference into a JSON file.
  - Import the JSON later to restore your setup.
- **Theme Toggle:** Light/Dark mode toggle (saved in your browser).
- **Dismissable Tip:** “Navigation Tip” can be dismissed and won’t return unless you clear storage.

Project Setup & Folder Structure

Recommended structure (flexible, but strongly suggested):

```
/your-main-course-folder/
├── dashboard.html            <-- Main dashboard file (open this)
├── student-photo.jpg         <-- Your profile picture
│
├── prompt/                   <-- Text-based prompt & link reference files
│   ├── moodle.txt
│   ├── student-email.txt
│   ├── library.txt
│   └── ...
│
├── modules/                  <-- Core course modules
│   ├── module-1/
│   ├── module-2/
│   └── ...
│
└── essentials/               <-- General student resources
    ├── study-skills/
    ├── research-skills/
    └── career-skills/
```

Setup notes

1. Put dashboard.html in your main course directory.
2. Create a modules folder and a sub-folder for each module.
3. Create an essentials folder for general resources.
4. Put your profile picture (e.g., student-photo.jpg) next to dashboard.html.

## ⚙️ How to Customize

Open `dashboard.html` in a text editor (VS Code, Notepad++, etc.) and look for comments marked:

`<!-- EDITABLE: ... -->`

### 1) Profile Information

- **Photo:** Update `src="student-photo.jpg"` on the `<img class="profile-photo">`.
- **Name / ID / Email:** Replace placeholders in the profile card.

### 2) Semester Dates (Progress %)

Semester progress uses the **machine-readable** dates on these elements:

- `id="startDateValue"` with `data-date="YYYY-MM-DD"`
- `id="endDateValue"` with `data-date="YYYY-MM-DD"`

Update those values to match your semester.

### 3) Program Name

In the `<header>`, replace `[Your Program Name]`.

### 4) Modules and Links

- **Core Modules**
  - Edit cards inside `#core-modules-grid`
  - Set `href` to a local folder (example: `./modules/your-module-folder/`)
  - Update the title/subtitle text and icon
- **Student Essentials**
  - Edit the cards under the “Student Essentials” section
- **Quick Links**
  - Edit links in `.quick-links-grid`
  - These can be web URLs or local file links (e.g., `file:///C:/path/to/file.pdf`)

## 🤖 AI Customization Prompts

This project includes three AI prompts located in the `/prompts/` folder to help customize the HTML file using an AI agent.

- **PROMPT_STUDENT_INFO.md** – update personal and semester information  
- **PROMPT_QUICK_LINKS.md** – update dashboard shortcuts  
- **PROMPT_FILES.md** – update local module and file links  

Use only one prompt at a time, depending on what you want to change.


## 🚀 How to Use

1. Double-click `dashboard.html` to open it.
2. **All data is stored locally** in your browser’s `localStorage` (nothing is uploaded anywhere).
3. When opening local folders, it’s often best to **right-click → “Open in New Tab”** so you don’t navigate away from the dashboard.
4. Use the footer buttons:
   - **Export Data** → saves a JSON backup (defaults to `student-portal-data.json`)
   - **Import Data** → restores from a previously exported JSON

## 🔐 Local Storage Keys (for the curious)

The dashboard stores data under these keys:

- `portal_favorites`
- `portal_assignments`
- `portal_notes`
- `portal_theme`
- `tipDismissed`

Clearing site data/storage in your browser will reset the dashboard.

## 💻 Technology

Pure, simple web tech—no frameworks, no build step, no dependencies.

<p>
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
</p>

## 📞 Contact

Mohamad Malek Albeik

<p>
<a href="https://linkedin.com/in/mohamad-malek-albeik" target="_blank">
  <img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>
<a href="https://mohamad-albeik.github.io/portfolio-website-main/" target="_blank">
  <img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-333333?style=for-the-badge&logo=github&logoColor=white"/>
</a>
</p>

*Built with passion and continuous learning.*

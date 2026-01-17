# Offline Student Dashboard

A simple, self-contained, and offline-first student dashboard designed to help organize course materials, assignments, and important links without needing an internet connection. The entire application is packed into a single HTML file for maximum portability.

The core idea is to provide a central hub for all your local study files and folders, removing the distraction of the internet while studying.

## Features

*   **Zero Installation:** Just open the `dashboard.html` file in any modern web browser.
*   **Fully Offline:** Designed to work without an internet connection. (Note: Google Fonts are fetched on first load but are typically cached by the browser for future offline use).
*   **Local File Linking:** Easily link to local folders for each course module and resource.
*   **Task Management:** An integrated "Assignments" widget to keep track of your to-do list, with items saved locally in your browser.
*   **Quick Notes:** A persistent "Quick Notes" area for jotting down reminders.
*   **Customizable:** Easily edit student information, course details, and links directly in the HTML file.
*   **Dynamic Stats:** At-a-glance view of total modules, semester progress, and pending tasks.
*   **Favorites System:** Pin your most important modules to a dedicated "Favorites" section.
*   **Keyboard Shortcuts:** Press `/` to search and `ESC` to clear.

## Project Setup & Folder Structure

To get the most out of the dashboard, it's recommended to organize your files using the following structure.

```
/your-main-course-folder/
├── dashboard.html         <-- The main file you open
├── student-photo.jpg        <-- Your profile picture
│
├── modules/                 <-- Folder for your core course modules
│   ├── module-1/
│   ├── module-2/
│   └── ...
│
└── essentials/              <-- Folder for general resources
    ├── study-skills/
    └── research-skills/
```

1.  Place the `dashboard.html` file in your main course directory.
2.  Create a `modules` folder to hold a sub-folder for each course module.
3.  Create an `essentials` folder for other resources.
4.  Place your profile picture (e.g., `student-photo.jpg`) in the same directory as the dashboard.

## How to Customize

This dashboard is designed to be easily customized by editing the HTML file. Open `dashboard.html` in a text editor (like VS Code, Notepad++, or Sublime Text) and look for the comments marked `<!-- EDITABLE: ... -->`.

### 1. Profile Information

*   **Photo:** Find the `<img class="profile-photo">` tag and change `src="student-photo.jpg"` to your image file's name.
*   **Name, ID, Email:** Find the profile card section and replace the `[Student Name]`, `[Student ID]`, and `[student.id]@institution.edu` placeholders.

### 2. Semester Dates

The "Semester Progress" bar is calculated automatically based on two dates in the profile card:
*   **Date Joined:** This is the start date of your semester.
*   **End Date:** This is the end date of your semester.

Update these values (e.g., `2025-09-01`) to match your academic calendar.

### 3. Program Name

In the `<header>` section, change `[Your Program Name]` to your actual course title.

### 4. Modules and Links

*   **Core Modules & Student Essentials:**
    *   Find the `div` with the ID `core-modules-grid`.
    *   Edit the `href` attribute on each `<a>` tag to point to the correct local folder (e.g., `href="./modules/your-module-folder-name/"`).
    *   Change the "Module Name" and "Module Subtitle" text.
    *   You can copy and paste these `<a>` blocks to add or remove modules.
*   **Quick Links:**
    *   Find the `div` with the class `quick-links-grid`.
    *   Update the `href` attribute for each link. These can be web links (like `https://google.com`) or local file links (`file:///C:/path/to/file.pdf`).

## How to Use

1.  Double-click the `dashboard.html` file to open it in your preferred web browser (Chrome, Firefox, Edge, etc.).
2.  All data, such as your assignments and notes, is saved in your browser's `localStorage`. This means it stays on your computer and is not sent anywhere.
3.  When clicking on links to local folders, it's often best to **right-click** and select **"Open in New Tab"** so you don't navigate away from the dashboard.

## Technology

This project is built with:
*   **HTML5**
*   **CSS3**
*   **Vanilla JavaScript (ES6+)**

No frameworks, no libraries, no dependencies. Just pure, simple web technologies.

## 📞 Contact

Mohamad Malek Albeik

- **LinkedIn:** linkedin.com/in/mohamad-malek-albeik
- **Website:** mohamad-albeik.github.io/portfolio-website-main/

---

*This project was built with passion and continuous learning.*
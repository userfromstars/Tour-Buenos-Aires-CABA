# 🗺️ Secret City Map - CABA Edition

[![Project Status](https://img.shields.io/badge/Status-In_Development-yellow)](#)
[![Tech Stack](https://img.shields.io/badge/Tech-HTML5_|_CSS3_|_JS_ES6+-blue)](#)

## 📌 Overview

A static website focused on discovering lesser-known places in the Autonomous City of Buenos Aires (CABA). This project features a modular architecture designed for maintainability, highlighting the implementation of an interactive map (GeoJSON), a dual theme system (Day/Night), and advanced data exploration tools. It was developed as an individual practice project to consolidate web development fundamentals.

---

## ✨ Key Features

*   **🔎 Search & Exploration:** Integrated search engine by place name and neighborhood.
*   **📂 Filters & Sorting:** Dynamic filtering by category, schedule, and price. Alphabetical sorting, or by price, neighborhood, and category.
*   **⭐ Favorites Management:** Data persistence using `localStorage` and a dedicated "My Favorites" view.
*   **🌙 Day / Night Mode:** Persistent toggle that fully adapts the UI and automatically filters place availability based on their schedule.
*   **🗺️ Synchronized Interactive Map:** Marker rendering using `caba.geojson`. Two-way synchronization (clicking on the map highlights the card, clicking the card centers the map).
*   **💡 Reasoned Recommendations:** Detailed reviews justifying the inclusion of each place in the catalog.

---

## 🏗️ Project Architecture

The project follows a directory structure designed to separate logical, visual, and data responsibilities, facilitating scalability:

```text
proyecto/
├── index.html                 # Landing page and presentation
├── pages/
│   ├── lugares.html           # Catalog, search, sorting, and Favorites view
│   └── mapa.html              # Vector interactive map
├── assets/
│   ├── css/
│   │   ├── styles.css         # Global styles, layout, and typography
│   │   └── themes.css         # CSS Variables for Day/Night Mode
│   ├── js/
│   │   ├── main.js            # Global logic: navbar and theme toggle
│   │   ├── mapa.js            # Rendering, GeoJSON logic, and synchronization
│   │   ├── lugares.js         # Search engine, sorting, and list rendering
│   └── data/
│       ├── lugares.json       # Local database (schedules, prices, categories)
│       └── caba.geojson       # Vector data for the map
```

---

## 🛠️ Technologies Used

*   **Structure & Styling:** Semantic HTML5, CSS3 (Variables, Flexbox, Grid, Mobile First).
*   **Logic & Functionality:** JavaScript (ES6+), Fetch API, LocalStorage.
*   **Data & Geometry:** JSON, GeoJSON.
*   **Version Control:** Git, GitHub (Conventional Commits).

---

## ♿ Accessibility (A11y)

To ensure an inclusive experience, the project implements:
*   Descriptive `alt` attributes for images.
*   Use of `aria-label` on buttons and links without visible text.
*   Validated color contrast in both Day and Night modes.
*   Full-keyboard navigation with always-visible `:focus` states.
*   Status indicators (success/error) using icons and text, without relying solely on color.

---

## 🚀 Installation & Local Usage

Due to the use of the `Fetch API` to load the `.json` and `.geojson` files, the project must be run through a local server (`http://` protocol), rather than opening the file directly (`file://`).

1. Clone the repository:
   ```bash
   git clone https://github.com/userfromstars/Tour-Buenos-Aires-CABA.git
   ```
2. Open the project folder in your code editor (e.g., VS Code).
3. Start a local server. If you use the **Live Server** extension in VS Code, right-click on `index.html` and select *Open with Live Server*.

---

## 👨‍💻 Author

*   **Axel Figueredo** - *Individual practice project* - [GitHub Profile](https://github.com/userfromstars)

---

## 📄 Useful Links

*   **🌐 Live Deploy:** *(Coming soon - Link will be updated once deployed)*
*   **🤖 AI Report:** *(Coming soon - Link to the AI report will be added here)*
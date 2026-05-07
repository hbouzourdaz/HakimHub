# Hakim Ecosystem (مكتبة برامج حكيم)

![Hakim Ecosystem](https://img.shields.io/badge/Status-Production_Ready-success) ![License](https://img.shields.io/badge/License-Proprietary-blue) ![Design](https://img.shields.io/badge/UI-Material_Design_3-orange)

**Hakim Ecosystem** is a modern, high-performance, and responsive Single Page Application (SPA) built to showcase a professional suite of educational and administrative software developed by **Hakim BOUZOURDAZ**. 

The interface is heavily inspired by Google's **Material Design 3 (M3)** guidelines, offering a premium "SaaS" aesthetic, smooth micro-animations, and dynamic content rendering without the need for complex frontend frameworks.

---

## ✨ Key Features

- **Google Material Design 3 UI:** Utilizes M3 tonal color palettes, outlined cards with ripple effects, rounded filter chips, dynamic search bars, and the official Google Material Symbols Rounded library.
- **Fully Bilingual (Arabic / English):** Complete localization support with dynamic RTL (Right-to-Left) and LTR (Left-to-Right) switching depending on the selected language.
- **Dynamic Database (`data.js`):** All 16 software programs are injected dynamically from a centralized JSON-like array, making updates, additions, and deletions effortless.
- **Dark / Light Mode:** A fully integrated theme switcher that dynamically adjusts surface colors, container elevations, and typography contrasts to reduce eye strain.
- **Smart Filtering & Live Search:** Instantly filter software by categories (e.g., Middle School, Primary, Administration) or use the live search bar to find programs by name or description.
- **Interactive Detail Views:** Each software has its own dedicated view containing technical specifications, version details, feature lists, file sizes, and direct download links.
- **Fallback Asset Handling:** Intelligently displays colorful, premium-looking placeholder icons featuring M3 symbols and gradients if an app lacks a custom image asset.

---

## 🛠 Technologies Used

- **HTML5:** Semantic HTML structuring the Single Page Application.
- **Vanilla JavaScript (ES6+):** Handling DOM manipulation, state management (views/languages), search algorithms, and category filtering logic. No external JS libraries/frameworks were used.
- **Vanilla CSS3:** Advanced usage of CSS Custom Properties (Variables) for theming, CSS Grid & Flexbox for responsive layouts, and keyframe animations for smooth page transitions.
- **Typography:** The highly legible **Rubik** font family from Google Fonts.
- **Iconography:** Official **Google Material Symbols Rounded**.

---

## 📂 File Structure

```text
Hakim_Ecosystem/
│
├── index.html       # The core SPA interface containing layout, styling, and UI logic.
├── data.js          # The localized data source containing all software metadata.
├── README.md        # This documentation file.
│
└── ../images/       # External directory containing application icons (.png, .ico).
                     # (Ensures assets are shared centrally with other deployment tools).
```

---

## 📝 How to Add or Edit Software

To add a new program or edit an existing one, you only need to modify the `appsData` array inside the `data.js` file. The UI in `index.html` will automatically adapt and render the new content.

**Example `data.js` Object:**

```javascript
{
    id: 17, // Must be a unique number
    name: "New Software App", // English Name
    nameAr: "تطبيق جديد", // Arabic Name
    category: "أدوات", // Arabic Category
    categoryEn: "Tools", // English Category
    icon: "../images/new_app_icon.png", // Path to icon (or "default" for fallback)
    gradient: "linear-gradient(135deg, #3b82f6, #6366f1)", // UI accent background
    color: "#3b82f6", // UI accent shadow color
    version: "1.0.0", // Software version
    size: "50.0 MB", // File size
    fileName: "New_App_Setup.exe", // Exact filename for download link
    description: "وصف البرنامج بالعربية.", // Arabic description
    descriptionEn: "Software description in English.", // English description
    features: ["ميزة 1", "ميزة 2"], // Arabic feature list
    featuresEn: ["Feature 1", "Feature 2"], // English feature list
    downloads: 1500 // Download count
}
```

*Note: If `icon` is set to `"default"`, the system will automatically generate a beautiful gradient placeholder icon.*

---

## 🚀 Running the Project Locally

Because this project is built with static files and uses modern JavaScript modules, you may need a local web server to avoid CORS (Cross-Origin Resource Sharing) issues when loading local files, though standard double-clicking `index.html` works in most modern browsers.

If needed, use Python's built-in HTTP server:
```bash
# Navigate to the project directory
cd "Hakim_Ecosystem"

# Start a local server on port 8000
python -m http.server 8000
```
Then, open `http://localhost:8000` in your web browser.

---

## © Copyright

Developed and Designed for **Hakim BOUZOURDAZ**.
All Rights Reserved.

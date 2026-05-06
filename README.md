# 🛍️ Product Preview Card Component

A responsive product preview card built with **HTML** and **CSS**, featuring adaptive layouts for mobile and desktop screens.

---

## 📌 Overview

This project displays a product (perfume) with its image, description, and pricing. It is designed to switch layouts and images depending on screen size.

* 📱 Mobile-first responsive design
* 💻 Desktop layout with side-by-side content
* 🖼️ Image swapping for different screen sizes
* 🎨 Clean UI using CSS variables

---

## 🚀 Features

* Responsive layout using **media queries**
* Separate images for **mobile and desktop views**
* Styled button with hover effect
* Typography using **Google Fonts (Fraunces & Montserrat)**
* Clean and reusable CSS structure with variables

---

## 🧱 Built With

* HTML5
* CSS3 (Flexbox + Media Queries)
* Google Fonts

---

## 📂 Project Structure

```
/project-folder
│── index.html
│── style.css
│── /assets
│    ├── /images
│    │    ├── image-product-desktop.jpg
│    │    ├── image-product-mobile.jpg
│    │    └── icon-cart.svg
```

---

## 📱 Responsive Behavior

### Mobile (≤ 585px)

* Stacked layout (image on top, text below)
* Mobile image is displayed
* Button expands to full width

### Desktop (≥ 886px)

* Side-by-side layout (image + content)
* Desktop image is displayed
* Centered card using Flexbox

---

## ⚙️ How It Works

### 1. Image Switching

Two images are used:

```html
<img id="desktop">
<img id="mobile">
```

They are toggled using media queries:

```css
#desktop { display: none; }

@media (min-width: 886px){
  #mobile { display: none; }
  #desktop { display: block; }
}
```

---

### 2. Layout System

* The `body` uses Flexbox to center the card:

```css
body {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

* The `.container` adapts between:

  * `column` (mobile)
  * `row` (desktop)

---

### 3. Styling

CSS variables are used for:

* Colors
* Fonts

Example:

```css
--Green-500: hsl(158, 36%, 37%);
--Primary-font: "Montserrat", sans-serif;
```

---

## ⚠️ Known Issues / Improvements

* ❌ Font-weight variables use `px` instead of numeric values
* ❌ Typo: `.line-throught` → `.line-through`
* ❌ `font-weight: semi-bold` is invalid (use `600`)
* 💡 Could improve image handling using `<picture>` instead of two `<img>` tags
* 💡 Reduce repeated CSS across media queries

---

## 💡 Future Improvements

* Use `<picture>` element for cleaner responsive images
* Add accessibility improvements (ARIA labels, better alt text)
* Convert to a reusable component (React / Vue)
* Add animation for hover and transitions

---

## ▶️ Getting Started

1. Clone or download the project
2. Open `index.html` in your browser

```bash
git clone https://github.com/your-username/product-preview-card.git
```

---

## 🙌 Acknowledgements

* Design inspired by Frontend Mentor challenges
* Fonts from Google Fonts

---

## 📄 License

This project is open-source and free to use.

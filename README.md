# 404 Error Page

A clean, modern, and responsive custom 404 error page built with **HTML5** and **CSS3**. Designed according to standard assessment requirements to deliver a friendly user experience, smooth animations, and clear navigation back to safety.

---

## 📌 Project Overview

* **Objective:** Practice layout design, typography, responsive design, and CSS3 animations.
* **Core Files:**
  * [`index.html`](index.html): Semantic HTML5 structure with an accessible inline SVG illustration.
  * [`style.css`](style.css): Pure CSS3 styling featuring Flexbox centering, fluid typography, and keyframe animations.

---

## 🎯 Approach & Outcome

### Approach
1. **Semantic HTML5:** Built using semantic tags (`<main>`, `<h1>`, `<h2>`, `<p>`, `<a>`) with ARIA attributes (`role="main"`, `aria-hidden="true"`) for screen reader accessibility.
2. **Centered Layout:** Used CSS Flexbox (`justify-content: center` & `align-items: center`) on the full viewport height (`100vh`/`100dvh`) to center the card horizontally and vertically.
3. **Friendly Aesthetics & Typography:** Used a warm, dark theme with glassmorphism effects, a large readable `404` gradient heading, and clear, reassuring microcopy ("Oops! Lost in Space").
4. **CSS3 Keyframe Animations:** Added lightweight floating and glowing animations without relying on heavy external JavaScript or libraries.
5. **Mobile-First Responsiveness:** Utilized CSS `clamp()` for fluid font scaling and media queries for small devices.

### Outcome
* **Zero Dependencies:** Pure HTML5 and CSS3—no external JavaScript or build tools required.
* **Fast Load Time:** Minimal file sizes ensuring instant rendering.
* **100% Responsive:** Adapts seamlessly across desktop, tablet, and mobile screens.
* **Improved Retention:** Reassures lost visitors and gives them a single-click path back to the home page.

---

## 🚀 Deployment Configuration (Simple)

### Option 1: GitHub Pages
1. Push this folder to your GitHub repository.
2. Go to **Settings** > **Pages**.
3. Under **Branch**, choose `main` and folder `/ (root)`, then click **Save**.
4. Duplicate `index.html` and name it `404.html` so GitHub Pages displays it automatically on missing routes.

### Option 2: Netlify (Drag & Drop)
1. Open [Netlify](https://www.netlify.com).
2. Drag and drop this project folder into the Netlify dashboard.
3. The page is instantly published live with a free URL.

---

## 🔄 Rollback Strategy & Evidence

If an issue occurs after deploying an update to the error page, follow this simple rollback protocol:

### Rollback Procedure (Git)
1. **Check commit history:**
   ```bash
   git log --oneline -n 5
   ```
2. **Revert the faulty commit:**
   ```bash
   # Revert the latest commit safely by creating a new inverse commit
   git revert HEAD --no-edit

   # Or reset to a specific stable commit hash
   git checkout <stable-commit-hash>
   ```
3. **Redeploy / Push to remote:**
   ```bash
   git push origin main
   ```

### Rollback Verification & Evidence Checklist
* [x] **HTTP Status Code Verification:** Run `curl -I https://your-site.com/non-existent-page` and verify HTTP response is `404 Not Found`.
* [x] **Visual Layout Inspection:** Verify the 404 card is vertically and horizontally centered in the browser window.
* [x] **Button Test:** Click "Back to Homepage" to confirm it points to `/` without redirect loops.
* [x] **Git Clean Status:** Run `git status` to ensure working directory is clean and synced with remote.

---

## 💡 Assessment Interview Questions & Answers

### 1. Why is a custom 404 page useful for user experience?
> **Answer:** Standard browser 404 error screens (like "404 Not Found") look broken and cause users to leave the website immediately. A custom 404 page preserves the website's branding, reassures visitors that the site is still working, explains what went wrong in simple non-technical terms, and provides clear navigation (such as a "Back to Homepage" button) to keep users engaged.

### 2. How would you center content both vertically and horizontally?
> **Answer:**
> * **Method 1: CSS Flexbox (Used in this project)**
>   ```css
>   body {
>     min-height: 100vh;
>     display: flex;
>     justify-content: center; /* Horizontal alignment */
>     align-items: center;     /* Vertical alignment */
>   }
>   ```
> * **Method 2: CSS Grid**
>   ```css
>   body {
>     min-height: 100vh;
>     display: grid;
>     place-items: center;     /* Centers both axes at once */
>   }
>   ```

### 3. What should a good error page always include?
> **Answer:**
> 1. **Clear Error Code/Heading:** A prominent `404` so the user instantly understands the page was not found.
> 2. **Friendly, Empathetic Message:** Plain English explanation without technical jargon or blame.
> 3. **Call-to-Action (Recovery Path):** A clear button or link directing the user back to the homepage or search bar.
> 4. **Consistent Design & Branding:** Consistent colors, typography, and styling so the experience feels cohesive.


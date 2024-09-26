# CS100 Basic Web Development 1 - Lab Sheet 2

## Changing CSS Layout to Have Navigation on the Left

### Objective:
By the end of this lab, students will update an HTML and CSS file for the Grandma’s Recipe page to have a navigation bar on the left side of the page using the float and position properties.

---

### Files Needed:
- ![`recipe_css.html`](recipe_css.html) (provided)
- ![`styles.css`](styles.css) (provided)

---

## Instructions:

### Step 1: Understanding the HTML Structure
- Open the `recipe_css.html` and `styles.css` files in a code editor.
   - The `nav` section in the HTML looks like this:
```html
<nav>
  <ul>
    <li><a href="index.html">Home</a></li>
    <li><a href="#cakes">Cakes</a></li>
    <li><a href="#cookies">Cookies</a></li>
    <li><a href="#savory">Savory</a></li>
    <li><a href="#desserts">Desserts</a></li>
    <li><a href="#drinks">Drinks</a></li>
    <li><a href="#contact">Contact Us</a></li>
  </ul>
</nav>
```

- In the CSS (`styles1.css`), the navigation is styled to be horizontal using inline-block:
```css
nav ul li {
  display: inline-block;
  margin: 0 15px;
}
```

---
### Step 2: Modify the Navigation Layout to a Sidebar
- Modify the CSS `nav ul li` style:
  - Adjust the `display` property so that it displays list items vertically
  - Adjust the margin so that it looks appropriate (more spacing between list items).
```css
nav ul li {
    display: block;
    margin: 20px;
}
```

- Modify the CSS `nav` style:
   - Float the navigation to the left.
   - Set the width of the sidebar to 20%.
   - Make the sidebar extend to the full height of the viewport.
   - Add padding to the top of the navigation content.
```css
nav {
    float: left;
    width: 20%;
    height: 100vh;
    padding-top: 20px;
}
```

---
### Step 3: Adjust the Main Content Width
- Modify the CSS `main` section to ensure the main content takes up the remaining width of the page and floats to the right of the sidebar.
```css
main {
    padding: 20px;
    width: 75%;
    float: right;
}
```

---
### Step 4: Styling the Footer
- Since the `nav` and `main` sections are floated, ensure the footer stays below them by clearing the floats by adding relevant CSS styles to achieve this.
```css
footer {
    clear: both;
}
```

---
### Step 5: Keeping the Navigation Bar Visible
- Add CSS to position the `nav` element so that the navigation stays fixed while scrolling.
```css
nav {
    position: sticky;
    top: 0;
}
```

---
### Step 6: Testing the Layout
1. Open the `recipe_css.html` file in a web browser.
2. Verify that the layout is updated with the navigation on the left and fixed while scrolling like the pictures below.

![img/recipe_page1](img/recipe_page1.png)
![img/recipe_page2](img/recipe_page2.png)


---



# 🎨 Phase 2: CSS Fundamentals

Welcome to CSS Fundamentals at **SYK Studio — Scale Your Knowledge**!

CSS stands for **Cascading Style Sheets**. It controls how webpages look, including colours, typography, spacing, layouts, and responsive behaviour.

In this phase, you will learn CSS step by step and use it to transform your HTML pages into attractive, responsive websites.

**Prerequisites:** Complete [Phase 1 — HTML Fundamentals](01-html-fundamentals.md).

**Estimated time:** 2–3 weeks, depending on your pace.

**Goal:** Style a webpage confidently, build layouts with Flexbox and Grid, and create a responsive website.

---

## 🧭 Learning Path

1. [Step 1 — Connect CSS to HTML](#-step-1--connect-css-to-html)
2. [Step 2 — Selectors and CSS Rules](#-step-2--selectors-and-css-rules)
3. [Step 3 — Colours, Backgrounds, and Typography](#-step-3--colours-backgrounds-and-typography)
4. [Step 4 — The CSS Box Model](#-step-4--the-css-box-model)
5. [Step 5 — Display and Positioning](#-step-5--display-and-positioning)
6. [Step 6 — Flexbox](#-step-6--flexbox)
7. [Step 7 — CSS Grid](#-step-7--css-grid)
8. [Step 8 — Responsive Web Design](#-step-8--responsive-web-design)
9. [Step 9 — Borders, Effects, and Transitions](#-step-9--borders-effects-and-transitions)
10. [Step 10 — CSS Variables and Maintainable Styles](#-step-10--css-variables-and-maintainable-styles)
11. [Step 11 — Build a Responsive Website](#-step-11--build-a-responsive-website)

---

## 📍 Step 1 — Connect CSS to HTML

**Goal:** Understand how CSS applies styles to HTML elements.

### Learn these concepts

- [ ] What CSS is and how it works with HTML
- [ ] CSS rules, properties, and values
- [ ] Inline CSS
- [ ] Internal stylesheets using `<style>`
- [ ] External stylesheets using `<link>`
- [ ] Why external stylesheets are generally preferred for larger projects
- [ ] How to save CSS files and refresh your browser

### 🎥 Video lesson

Start with one beginner CSS lecture that explains CSS syntax and all three ways of adding styles.

[Find: CSS Introduction and How to Add CSS to HTML](https://www.youtube.com/results?search_query=CSS+introduction+external+internal+inline+CSS+beginners)

Choose one clear explanation. You do not need to watch several videos covering the same basics.

### 🧠 Understand the example

Create a file named `style.css`:

```css
body {
    background-color: #f4f7fb;
    font-family: Arial, sans-serif;
}

h1 {
    color: #2457c5;
}
```

Connect it to your HTML document inside the `<head>`:

```html
<link rel="stylesheet" href="style.css">
```

### 🧪 Practice

- [ ] Create a `style.css` file beside your `index.html`.
- [ ] Connect the stylesheet.
- [ ] Change the page background colour.
- [ ] Change the heading colour.
- [ ] Modify the font family and observe the result.

### ✅ Completion check

You can connect an external stylesheet and explain how a CSS rule changes an HTML element's appearance.

---

## 📍 Step 2 — Selectors and CSS Rules

**Goal:** Select the right HTML elements and apply styles to them.

### Learn these concepts

- [ ] Element selectors
- [ ] Class selectors
- [ ] ID selectors
- [ ] Grouping selectors
- [ ] Descendant and child selectors
- [ ] Attribute selectors
- [ ] Pseudo-classes such as `:hover` and `:focus`
- [ ] Pseudo-elements such as `::before` and `::after`
- [ ] The cascade, inheritance, and specificity
- [ ] Why overly complicated selectors are difficult to maintain

### 🎥 Video lesson

[Find: CSS Selectors, Specificity and Cascade Explained](https://www.youtube.com/results?search_query=CSS+selectors+specificity+cascade+inheritance+complete+tutorial)

If your main CSS lecture already explains these concepts with practical examples, continue with it. Add a focused lesson only for concepts that remain unclear.

### 🧪 Practice

- [ ] Style all paragraph elements.
- [ ] Create a reusable `.card` class.
- [ ] Give one element a unique ID.
- [ ] Style links when hovered or focused.
- [ ] Experiment with conflicting CSS rules and observe which rule wins.

### ✅ Completion check

You can select elements using classes and other selectors, and explain why a particular CSS rule takes effect.

---

## 📍 Step 3 — Colours, Backgrounds, and Typography

**Goal:** Make webpages visually clear and readable.

### Learn these concepts

- [ ] Named colours, hexadecimal colours, RGB, and HSL
- [ ] Background colours and images
- [ ] Font families and font stacks
- [ ] Font size, weight, and style
- [ ] Text alignment and line height
- [ ] Letter spacing and text decoration
- [ ] Using web fonts
- [ ] Readable contrast and consistent typography
- [ ] CSS units such as `px`, `%`, `em`, `rem`, `vw`, and `vh`

### 🎥 Video lesson

[Find: CSS Colours, Units, Backgrounds and Typography](https://www.youtube.com/results?search_query=CSS+colors+units+typography+backgrounds+complete+tutorial)

Choose a lesson that combines the basics of styling text and backgrounds. A separate video is unnecessary if the main course covers these topics well.

### 🧪 Practice

- [ ] Create a consistent colour palette.
- [ ] Choose readable fonts for headings and body text.
- [ ] Adjust paragraph line height.
- [ ] Add a background colour to a card.
- [ ] Check that text remains readable against its background.

### ✅ Completion check

Your webpage uses readable typography, consistent colours, and appropriate spacing.

---

## 📍 Step 4 — The CSS Box Model

**Goal:** Understand how element dimensions and spacing work.

### Learn these concepts

- [ ] Content, padding, border, and margin
- [ ] Width and height
- [ ] `box-sizing`
- [ ] `border-box` versus `content-box`
- [ ] Margin collapsing
- [ ] Overflow
- [ ] Minimum and maximum dimensions
- [ ] Why unexpected spacing occurs

### 🎥 Video lesson

[Find: CSS Box Model Explained for Beginners](https://www.youtube.com/results?search_query=CSS+box+model+margin+padding+border+box-sizing+explained)

Choose a lesson that demonstrates the box model visually in browser developer tools.

### 🧪 Practice

- [ ] Create three cards with different padding values.
- [ ] Add borders and margins.
- [ ] Compare their dimensions using both box-sizing models.
- [ ] Inspect their computed styles in developer tools.
- [ ] Fix any unwanted horizontal overflow.

### ✅ Completion check

You can explain how content, padding, borders, and margins affect an element's size and spacing.

---

## 📍 Step 5 — Display and Positioning

**Goal:** Control how elements appear and how they relate to one another.

### Learn these concepts

- [ ] `block`, `inline`, and `inline-block`
- [ ] The `none` value for display
- [ ] Normal document flow
- [ ] Relative and absolute positioning
- [ ] Fixed and sticky positioning
- [ ] The `z-index` property
- [ ] Overflow behaviour
- [ ] Common layout mistakes

### 🎥 Video lesson

[Find: CSS Display and Positioning Complete Tutorial](https://www.youtube.com/results?search_query=CSS+display+block+inline+position+relative+absolute+fixed+sticky+tutorial)

If positioning is not adequately covered in your main CSS lecture, use a focused positioning lesson.

### 🧪 Practice

- [ ] Create a horizontal navigation area.
- [ ] Position a small badge inside a card.
- [ ] Create a sticky header.
- [ ] Test fixed positioning while scrolling.
- [ ] Observe how different display values affect elements.

### ✅ Completion check

You can choose appropriate display and positioning techniques without relying on random spacing hacks.

---

## 📍 Step 6 — Flexbox

**Goal:** Arrange elements in flexible rows and columns.

### Learn these concepts

- [ ] What Flexbox solves
- [ ] Flex containers and flex items
- [ ] `display: flex`
- [ ] Main axis and cross axis
- [ ] `flex-direction`
- [ ] `justify-content`
- [ ] `align-items` and `align-self`
- [ ] `flex-wrap` and `gap`
- [ ] `flex-grow`, `flex-shrink`, and `flex-basis`
- [ ] Common navigation and card layouts

### 🎥 Video lesson

[Find: CSS Flexbox Complete Course](https://www.youtube.com/results?search_query=CSS+Flexbox+complete+course+justify-content+align-items+flex-wrap)

**Preferred approach:** Use one complete Flexbox lecture that covers the required properties. Add a focused lesson only for concepts the main lecture does not explain.

### 🧪 Practice

- [ ] Create a navigation bar with evenly spaced items.
- [ ] Centre a card horizontally and vertically.
- [ ] Build a row of cards with consistent gaps.
- [ ] Make the cards wrap on narrower screens.
- [ ] Explain which axis each alignment property controls.

### ✅ Completion check

You can build flexible one-dimensional layouts and explain the properties used to arrange their elements.

---

## 📍 Step 7 — CSS Grid

**Goal:** Build layouts using rows and columns.

### Learn these concepts

- [ ] What CSS Grid is used for
- [ ] Grid containers and grid items
- [ ] Defining rows and columns
- [ ] Fractional units using `fr`
- [ ] `gap`
- [ ] Grid placement and spanning
- [ ] `repeat()` and `minmax()`
- [ ] `auto-fit` and `auto-fill`
- [ ] Responsive card grids
- [ ] When Grid is preferable to Flexbox

### 🎥 Video lesson

[Find: CSS Grid Complete Course for Beginners](https://www.youtube.com/results?search_query=CSS+Grid+complete+course+fr+minmax+auto-fit+responsive+layout)

Choose a lesson that includes practical layouts and responsive grids, not just property definitions.

### 🧪 Practice

- [ ] Create a two-column layout.
- [ ] Build a responsive grid of cards.
- [ ] Experiment with `repeat()` and `minmax()`.
- [ ] Make a card span multiple columns.
- [ ] Compare the layout with a Flexbox version.

### ✅ Completion check

You can create two-dimensional layouts and choose suitable Grid properties for the design.

---

## 📍 Step 8 — Responsive Web Design

**Goal:** Make webpages work across mobile, tablet, and desktop screens.

### Learn these concepts

- [ ] What responsive design means
- [ ] Mobile-first design
- [ ] The viewport meta tag
- [ ] Media queries
- [ ] Flexible widths and max-width
- [ ] Responsive images
- [ ] Responsive navigation
- [ ] Combining Flexbox and Grid
- [ ] Testing different screen sizes
- [ ] Avoiding horizontal overflow

### 🎥 Video lesson

[Find: Responsive Web Design with CSS](https://www.youtube.com/results?search_query=responsive+web+design+CSS+mobile+first+media+queries+flexbox+grid+complete+course)

Prefer a comprehensive responsive design lesson that uses real layouts. Add a focused lesson only for any important missing topic.

### 🧪 Practice

- [ ] Make your navigation usable on narrow screens.
- [ ] Make cards adapt to available width.
- [ ] Resize images without distorting them.
- [ ] Add a media query for a smaller screen.
- [ ] Test at multiple widths using developer tools.
- [ ] Fix horizontal scrolling caused by your layout.

### ✅ Completion check

Your page remains readable and usable on small and large screens.

---

## 📍 Step 9 — Borders, Effects, and Transitions

**Goal:** Add visual polish without sacrificing usability.

### Learn these concepts

- [ ] Borders and border radius
- [ ] Box shadows and text shadows
- [ ] Gradients
- [ ] Opacity
- [ ] Transforms
- [ ] Transitions
- [ ] Basic keyframe animations
- [ ] Hover and focus states
- [ ] Respecting reduced-motion preferences

### 🎥 Video lesson

[Find: CSS Transitions, Transforms, Shadows and Animations](https://www.youtube.com/results?search_query=CSS+transitions+transforms+box+shadow+keyframes+animations+tutorial)

Use a focused lesson for animations if your main CSS course covers only static styling.

### 🧪 Practice

- [ ] Add a subtle shadow to a card.
- [ ] Round the corners of buttons.
- [ ] Add a transition to a hover state.
- [ ] Create a simple loading animation.
- [ ] Ensure keyboard focus remains visible.
- [ ] Avoid animations that make content difficult to use.

### ✅ Completion check

Your page uses visual effects consistently and keeps interactive elements clear and accessible.

---

## 📍 Step 10 — CSS Variables and Maintainable Styles

**Goal:** Organize CSS so projects remain easy to update.

### Learn these concepts

- [ ] CSS custom properties
- [ ] The `:root` selector
- [ ] Reusing colours, spacing, and font values
- [ ] Organizing styles into logical sections
- [ ] Reusable component classes
- [ ] Avoiding unnecessary specificity
- [ ] Understanding when to use CSS variables
- [ ] Basic debugging with browser developer tools

### 🎥 Video lesson

[Find: CSS Variables and Clean CSS Architecture](https://www.youtube.com/results?search_query=CSS+custom+properties+variables+maintainable+CSS+beginners)

### 🧪 Practice

- [ ] Define colour variables in `:root`.
- [ ] Create reusable button styles.
- [ ] Reuse spacing values.
- [ ] Organize your stylesheet into sections.
- [ ] Change one variable and observe how the design updates.

### Example

```css
:root {
    --color-primary: #2457c5;
    --color-background: #f4f7fb;
    --spacing-medium: 1rem;
    --radius-card: 0.75rem;
}

.card {
    padding: var(--spacing-medium);
    border-radius: var(--radius-card);
}
```

### ✅ Completion check

You can maintain a consistent design without repeating the same values throughout your stylesheet.

---

## 🏗️ Step 11 — Build a Responsive Website

**Goal:** Apply your CSS knowledge to a complete design.

### Project: SYK Studio Learning Landing Page

Create a landing page for a fictional learning community.

### Requirements

- [ ] A header with navigation
- [ ] A hero section with a heading and call-to-action button
- [ ] A section describing the community
- [ ] A responsive grid of learning-roadmap cards
- [ ] A section featuring learning benefits
- [ ] A footer with useful links
- [ ] A consistent colour palette and typography
- [ ] Flexbox and Grid used where appropriate
- [ ] Responsive layouts for mobile and desktop
- [ ] Visible hover and keyboard focus states
- [ ] Clean, organized CSS
- [ ] No unintended horizontal overflow

### 🎥 Need additional help?

[Find: Responsive Landing Page HTML and CSS Project](https://www.youtube.com/results?search_query=responsive+landing+page+HTML+CSS+beginner+project)

Try building the page yourself first. Use tutorials to understand difficult parts, then implement your own layout and design.

### 📋 Final project checklist

- [ ] The layout works on mobile and desktop.
- [ ] Spacing and typography are consistent.
- [ ] Cards and navigation align correctly.
- [ ] Flexbox and Grid are used appropriately.
- [ ] CSS is readable and organized.
- [ ] Interactive states are visible.
- [ ] The HTML and CSS are saved in GitHub.
- [ ] The project is ready to connect to JavaScript in the next phase.

---

## 🎯 Phase 2 Completion Criteria

You are ready for JavaScript Fundamentals when you can:

- [ ] Connect CSS to HTML.
- [ ] Select elements and understand the cascade.
- [ ] Style text, colours, and backgrounds.
- [ ] Explain the CSS box model.
- [ ] Use display and positioning appropriately.
- [ ] Build layouts with Flexbox.
- [ ] Build layouts with Grid.
- [ ] Create responsive pages.
- [ ] Use transitions and CSS variables.
- [ ] Complete the responsive landing page independently.

If a concept is still confusing, revisit its lesson and repeat the practice task.

---

## 📚 Recommended References

- [MDN: CSS Styling Basics](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics)
- [MDN: CSS Layout](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/CSS_layout)
- [MDN: CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [web.dev: Learn CSS](https://web.dev/learn/css)

## ➡️ Next Phase

When you meet the completion criteria, continue to [Phase 3 — JavaScript Fundamentals](03-javascript-fundamentals.md).

*Learn step by step. Build as you learn. Grow together.*

**SYK Studio — Scale Your Knowledge**

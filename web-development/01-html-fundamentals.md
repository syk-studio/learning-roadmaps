
# 🧱 Phase 1: HTML Fundamentals

Welcome to HTML Fundamentals at **SYK Studio — Scale Your Knowledge**!

HTML stands for **HyperText Markup Language**. It provides the structure and meaning of content on a webpage.

In this phase, you will progress from writing your first HTML elements to building a complete, well-structured webpage with links, images, lists, tables, forms, and semantic elements.

**Prerequisites:** Complete [Phase 0 — Getting Started](00-getting-started.md).

**Estimated time:** 1–2 weeks, depending on your pace.

**Goal:** Build accessible, meaningful webpages using HTML without relying on copied templates.

---

## 🧭 Learning Path

1. [Step 1 — HTML Document Structure](#-step-1--html-document-structure)
2. [Step 2 — Headings, Paragraphs, and Text](#-step-2--headings-paragraphs-and-text)
3. [Step 3 — Links and Navigation](#-step-3--links-and-navigation)
4. [Step 4 — Images and Media](#-step-4--images-and-media)
5. [Step 5 — Lists](#-step-5--lists)
6. [Step 6 — Semantic HTML](#-step-6--semantic-html)
7. [Step 7 — Tables](#-step-7--tables)
8. [Step 8 — Forms and User Input](#-step-8--forms-and-user-input)
9. [Step 9 — Accessibility and Good HTML Practices](#-step-9--accessibility-and-good-html-practices)
10. [Step 10 — Complete HTML Project](#-step-10--complete-html-project)

---

## 📍 Step 1 — HTML Document Structure

**Goal:** Understand the basic structure of an HTML document.

### Learn these concepts

- [ ] What HTML is and why it is used
- [ ] Elements, tags, and attributes
- [ ] Opening tags and closing tags
- [ ] Nesting elements correctly
- [ ] The purpose of `<!DOCTYPE html>`
- [ ] The `<html>`, `<head>`, and `<body>` elements
- [ ] The `<title>` and `<meta>` elements
- [ ] Saving and opening an HTML file

### 🎥 YouTube lesson

Start with one complete beginner HTML lesson that covers document structure and basic elements.

[Find: HTML Full Course for Beginners](https://www.youtube.com/results?search_query=HTML+full+course+beginners+document+structure)

Choose a lesson that explains the code as it is written. You do not need multiple full HTML courses.

### 🧠 Understand the example

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Website</title>
</head>
<body>
    <h1>Welcome to My Website</h1>
    <p>I am learning HTML with SYK Studio.</p>
</body>
</html>
```

Notice that the document has a head section for metadata and a body section for the content displayed on the page.

### 🧪 Practice

- [ ] Create `index.html`.
- [ ] Write the basic document structure.
- [ ] Change the page title.
- [ ] Add a heading and two paragraphs.
- [ ] Open the page in your browser.

### ✅ Completion check

You can create a valid basic HTML document and explain the purpose of its main elements.

---

## 📍 Step 2 — Headings, Paragraphs, and Text

**Goal:** Organize text into a readable structure.

### Learn these concepts

- [ ] Headings from `<h1>` through `<h6>`
- [ ] Paragraphs using `<p>`
- [ ] Line breaks using `<br>` when appropriate
- [ ] Thematic breaks using `<hr>`
- [ ] Importance using `<strong>`
- [ ] Emphasis using `<em>`
- [ ] Inline code using `<code>`
- [ ] Quotations and the `<blockquote>` element
- [ ] Choosing elements based on meaning rather than appearance

### 🎥 YouTube lesson

If your main HTML course already explains these elements clearly, continue with it. Otherwise:

[Find: HTML Text Formatting and Headings](https://www.youtube.com/results?search_query=HTML+headings+paragraphs+strong+em+text+elements+tutorial)

### 🧪 Practice

Create an article page containing:

- [ ] One main heading
- [ ] At least three section headings
- [ ] Several paragraphs
- [ ] Important text marked with `<strong>`
- [ ] Emphasized text marked with `<em>`
- [ ] A quotation

Use headings in a logical order. Do not select heading levels merely to change the text size; CSS will handle appearance later.

### ✅ Completion check

Your article has a clear, meaningful heading hierarchy and readable content.

---

## 📍 Step 3 — Links and Navigation

**Goal:** Connect webpages and resources using hyperlinks.

### Learn these concepts

- [ ] The `<a>` element and its `href` attribute
- [ ] Absolute URLs and relative URLs
- [ ] Linking to another page in your project
- [ ] Linking to a section using an element ID
- [ ] Creating navigation menus
- [ ] Email links using `mailto:`
- [ ] Opening links in a new tab when appropriate
- [ ] Writing descriptive link text

### 🎥 YouTube lesson

[Find: HTML Links and Navigation Tutorial](https://www.youtube.com/results?search_query=HTML+links+href+relative+absolute+URLs+navigation+beginners)

A separate lesson is only needed if your primary course does not cover relative paths or in-page links.

### 🧪 Practice

- [ ] Add a link to a learning resource.
- [ ] Link two HTML pages in your project.
- [ ] Create a navigation section.
- [ ] Add a link that jumps to a section lower on the page.
- [ ] Test every link in your browser.

### ✅ Completion check

Your links navigate to the intended pages or sections and use meaningful text.

---

## 📍 Step 4 — Images and Media

**Goal:** Add images and understand basic media elements.

### Learn these concepts

- [ ] The `<img>` element
- [ ] Image paths and file organization
- [ ] The `src` and `alt` attributes
- [ ] Width and height attributes
- [ ] The `<figure>` and `<figcaption>` elements
- [ ] Basic audio and video elements
- [ ] Choosing appropriate alternative text
- [ ] Why image optimization matters

### 🎥 YouTube lesson

[Find: HTML Images, Alt Text, Audio and Video](https://www.youtube.com/results?search_query=HTML+images+alt+text+figure+audio+video+tutorial)

Choose a lesson that demonstrates both local image paths and alternative text.

### 🧪 Practice

- [ ] Add an image to your article.
- [ ] Store the image in a project assets folder.
- [ ] Write meaningful alternative text when the image conveys information.
- [ ] Use empty alternative text for purely decorative images.
- [ ] Add a caption using `<figure>` and `<figcaption>`.

### ✅ Completion check

Your image displays correctly, its path works, and its alternative text serves the intended purpose.

---

## 📍 Step 5 — Lists

**Goal:** Organize related information into lists.

### Learn these concepts

- [ ] Unordered lists using `<ul>`
- [ ] Ordered lists using `<ol>`
- [ ] List items using `<li>`
- [ ] Nested lists
- [ ] Description lists using `<dl>`, `<dt>`, and `<dd>`
- [ ] Choosing a list based on the content's meaning

### 🎥 YouTube lesson

[Find: HTML Lists Tutorial](https://www.youtube.com/results?search_query=HTML+ordered+unordered+nested+description+lists+tutorial)

Use a focused lesson if your main HTML lecture does not explain nested lists or description lists.

### 🧪 Practice

- [ ] Create a list of technologies you want to learn.
- [ ] Create numbered instructions for a simple task.
- [ ] Make a nested list of roadmap phases and topics.
- [ ] Create a description list of five web development terms.

### ✅ Completion check

You can choose and create the appropriate HTML list for different types of content.

---

## 📍 Step 6 — Semantic HTML

**Goal:** Structure webpages using elements that describe the purpose of their content.

### Learn these concepts

- [ ] What semantic HTML means
- [ ] `<header>` and `<footer>`
- [ ] `<nav>` and `<main>`
- [ ] `<section>` and `<article>`
- [ ] `<aside>`
- [ ] `<figure>` and `<figcaption>`
- [ ] The difference between generic `<div>` elements and meaningful semantic elements
- [ ] Logical page structure and landmarks

### 🎥 YouTube lesson

[Find: Semantic HTML Complete Explanation](https://www.youtube.com/results?search_query=semantic+HTML+header+nav+main+section+article+footer+explained)

Choose a lesson that explains when and why to use each element, rather than only showing syntax.

### 🧪 Practice

Take your earlier article and reorganize it using:

- [ ] A header containing the page title
- [ ] Navigation for important links
- [ ] One main content area
- [ ] Sections for related content
- [ ] An article where appropriate
- [ ] A footer with useful information

### ✅ Completion check

Your page uses meaningful elements that describe the content and create a logical structure.

---

## 📍 Step 7 — Tables

**Goal:** Present genuinely tabular information.

### Learn these concepts

- [ ] The `<table>` element
- [ ] Table rows and cells
- [ ] `<th>` and `<td>`
- [ ] `<thead>`, `<tbody>`, and `<tfoot>`
- [ ] Table captions
- [ ] Row and column headers
- [ ] The `scope` attribute
- [ ] When a table is appropriate and when it is not

### 🎥 YouTube lesson

[Find: HTML Tables Tutorial for Beginners](https://www.youtube.com/results?search_query=HTML+tables+thead+tbody+th+td+caption+scope+tutorial)

### 🧪 Practice

Build a table showing a weekly study schedule with columns for:

- Day
- Topic
- Learning activity
- Planned duration

Include a caption and meaningful column headers.

### ✅ Completion check

Your table presents related data clearly and uses proper headers.

---

## 📍 Step 8 — Forms and User Input

**Goal:** Collect user information using accessible HTML forms.

### Learn these concepts

- [ ] The `<form>` element
- [ ] Labels and inputs
- [ ] Text, email, password, number, date, and checkbox inputs
- [ ] Radio buttons and select menus
- [ ] Text areas and buttons
- [ ] The `name`, `value`, and `required` attributes
- [ ] Placeholder text versus actual labels
- [ ] Basic built-in browser validation
- [ ] Form submission and the roles of `action` and `method`
- [ ] The difference between frontend validation and server-side validation

### 🎥 YouTube lesson

[Find: HTML Forms Complete Tutorial](https://www.youtube.com/results?search_query=HTML+forms+labels+input+types+validation+select+textarea+beginners)

Choose one lesson that demonstrates forms from beginning to end. Add a separate lesson for form submission if the main lecture skips it.

### 🧪 Practice

Build a student registration form with:

- [ ] Full name
- [ ] Email address
- [ ] Password field
- [ ] A course selection
- [ ] A learning-mode choice
- [ ] A terms acceptance checkbox
- [ ] A submit button

Make sure every input has an associated label and appropriate attributes.

**Important:** A form built with HTML alone does not automatically store information or create a working registration system. That requires additional behaviour and usually a backend.

### ✅ Completion check

Your form has properly associated labels, appropriate input types, and basic validation.

---

## 📍 Step 9 — Accessibility and Good HTML Practices

**Goal:** Make your HTML easier for people and browsers to understand.

### Learn these concepts

- [ ] Why semantic HTML supports accessibility
- [ ] Meaningful headings and landmarks
- [ ] Descriptive link text
- [ ] Alternative text for informative images
- [ ] Labels for form controls
- [ ] Keyboard navigation basics
- [ ] Avoiding unnecessary or invalid markup
- [ ] Using the correct element for its purpose
- [ ] Checking HTML with a validator
- [ ] Understanding that accessibility involves more than HTML alone

### 🎥 Learning resources

- [MDN: HTML — Structuring the Web](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)
- [W3C: Web Accessibility Initiative](https://www.w3.org/WAI/)
- [W3C: Nu HTML Checker](https://validator.w3.org/nu/)

Use the official documentation for reference. If you need a video explanation, use:

[Find: HTML Accessibility for Beginners](https://www.youtube.com/results?search_query=HTML+accessibility+semantic+elements+labels+alt+text+beginners)

### 🧪 Practice

- [ ] Review your article and form.
- [ ] Check headings and page structure.
- [ ] Verify every form control has a label.
- [ ] Test navigation using the keyboard.
- [ ] Validate your HTML.
- [ ] Fix errors that you understand and review any warnings.

### ✅ Completion check

Your page has meaningful structure, accessible form labels, appropriate image text, and no known validation errors left unexplained.

---

## 🏗️ Step 10 — Build a Complete HTML Project

**Goal:** Combine your HTML knowledge into one project.

### Project: Student Learning Profile

Create a multi-section webpage that introduces a learner and presents their learning journey.

### Requirements

- [ ] A proper HTML document structure
- [ ] A meaningful page title and language attribute
- [ ] A header and navigation area
- [ ] An introduction with headings and paragraphs
- [ ] A profile image with appropriate alternative text
- [ ] A list of skills or learning goals
- [ ] A table showing a weekly study schedule
- [ ] A registration or contact form
- [ ] Semantic page sections
- [ ] Working links
- [ ] Accessible form labels
- [ ] Consistent indentation and readable markup

### 🎥 Need additional help?

Use your existing lessons to review any topics you find difficult.

[Find: HTML Portfolio Project for Beginners](https://www.youtube.com/results?search_query=HTML+only+portfolio+project+for+beginners)

**Challenge:** Try to build your own version before following a project tutorial. Use tutorials to understand concepts, not just copy the finished code.

### 📋 Final project checklist

- [ ] The page opens successfully in a browser.
- [ ] All local images and links work.
- [ ] The HTML is structured logically.
- [ ] Forms have appropriate labels.
- [ ] The page uses semantic elements where appropriate.
- [ ] The HTML validator reports no unexplained errors.
- [ ] The project files are organized and readable.
- [ ] The project is committed to GitHub.

---

## 🎯 Phase 1 Completion Criteria

You are ready to move to CSS Fundamentals when you can:

- [ ] Write a basic HTML document from scratch.
- [ ] Structure content with headings, paragraphs, lists, and semantic elements.
- [ ] Add images and working links.
- [ ] Create tables for tabular data.
- [ ] Build a form with labels and basic validation.
- [ ] Explain basic accessibility practices.
- [ ] Complete the Student Learning Profile project independently.

If you cannot complete a task yet, revisit the relevant step and practise again. Learning is not a race.

---

## 📚 Recommended Reference

- [MDN: HTML — Structuring the Web](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content)
- [MDN: HTML Elements Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements)
- [W3C: Nu HTML Checker](https://validator.w3.org/nu/)

## ➡️ Next Phase

When you meet the completion criteria, continue to [Phase 2 — CSS Fundamentals](02-css-fundamentals.md).

*Learn step by step. Build as you learn. Grow together.*

**SYK Studio — Scale Your Knowledge**

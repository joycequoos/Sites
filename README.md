# Building a Website with Visual Studio Code

[← Back to Web Development](https://github.com/joycequoos/Development)

Step-by-step guide to structuring a web project from scratch — HTML, CSS, and JavaScript — using Visual Studio Code and the Live Server extension.

Reference video: https://www.youtube.com/watch?v=fmhz4nqGK4E

## Table of Contents

- [1. Create the Project Folder](#1-create-the-project-folder)
- [2. Open the Folder in VS Code](#2-open-the-folder-in-vs-code)
- [3. Create the index.html File](#3-create-the-indexhtml-file)
- [4. Generate the Basic HTML Structure](#4-generate-the-basic-html-structure)
- [5. Build the HTML Content](#5-build-the-html-content)
- [6. Install the Live Server Extension](#6-install-the-live-server-extension)
- [7. View the Page with Live Server](#7-view-the-page-with-live-server)
- [8. Create the CSS File](#8-create-the-css-file)
- [9. Create the JavaScript File](#9-create-the-javascript-file)
- [10. Connect CSS and JS to the HTML](#10-connect-css-and-js-to-the-html)
- [11. Test the Complete Project](#11-test-the-complete-project)

---

## 1. Create the Project Folder

Before opening VS Code, create a folder on your computer to store all the project's files.

![Create the project folder](01_CriarPasta.GIF)

**Example path:** `C:\API_GITHUB\javascript\GITHUB`

---

## 2. Open the Folder in VS Code

Select this folder directly through Visual Studio Code (`File > Open Folder`), so that all the project's files are organized in the side explorer.

![Select the folder in VS Code](02_Acessar_Pasta.GIF)

---

## 3. Create the index.html File

Inside the project folder, create the page's main file: `index.html`.

![Create index.html](03_Index_HTML.GIF)

The file appears in the project's folder structure:

![File created in the folder](04_Arquivo_Pasta.GIF)

---

## 4. Generate the Basic HTML Structure

VS Code (via the Emmet extension, built into the editor) lets you automatically generate the standard skeleton of an HTML document. Simply type `!` and press **Enter** inside the `index.html` file.

![Generating the basic HTML structure](05_Estrutura_BasicaHTML.GIF)

This automatically creates the `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>` tags, ready to receive the page's content.

---

## 5. Build the HTML Content

With the basic structure ready, start adding the page's content inside the `<body>` tag — headings, paragraphs, images, links, lists, and so on.

![Starting to build the HTML](06_Comecando_HTML.GIF)

---

## 6. Install the Live Server Extension

**Live Server** is a VS Code extension that automatically refreshes the page in the browser every time you save a change to the code — essential for seeing the result in real time.

![Search for the Live Server extension](07_Extensao.GIF)

![Installing the extension](08_Instalando.GIF)

---

## 7. View the Page with Live Server

Once installed, right-click on `index.html` and select **"Open with Live Server"**.

![Opening with Live Server](09_Open_LiveServer.GIF)

The browser opens automatically, displaying the rendered HTML page.

---

## 8. Create the CSS File

To style the page, create a `.css` file (e.g., `style.css`) in the same project folder — use `Ctrl + Click` on the folder and then **"New File"**.

![Creating the CSS file](10_Criar_Arquivo.GIF)

---

## 9. Create the JavaScript File

Similarly, create the `scripts.js` file to add interactivity to the page.

![Creating the JavaScript file](11_Criar_ArquivoJS.GIF)

Use `Ctrl + Click` on the folder and select **"Create File"** to confirm the creation:

![Select Create File](12_Selecionar_CreateFile.GIF)

---

## 10. Connect CSS and JS to the HTML

Creating the `style.css` and `scripts.js` files isn't enough — you need to link them to `index.html` so the browser actually loads them.

**Linking the CSS** — inside the `<head>` tag:

```html
<head>
  <meta charset="UTF-8">
  <title>My Website</title>
  <link rel="stylesheet" href="style.css">
</head>
```

**Linking the JavaScript** — right before the closing `</body>` tag (this ensures the HTML has already loaded before the script runs):

```html
  <script src="scripts.js"></script>
</body>
</html>
```

With this, the project's final structure looks like this:

```
my-project/
├── index.html
├── style.css
└── scripts.js
```

---

## 11. Test the Complete Project

With the three files connected, open `index.html` again with **Live Server** and confirm that:

- The `style.css` styling is being applied to the page
- A test `console.log()` in `scripts.js` shows up in the browser console (F12 → Console tab)
- Any change saved to any of the three files updates the page automatically

```javascript
// scripts.js — quick test to confirm the file is connected
console.log('JavaScript successfully connected!');
```

If the message appears in the console, the project has the complete structure and is ready to receive the site's actual content, styling, and interactivity.

---

## Key Takeaways

- Organizing a web project from scratch: separate folder, HTML, CSS, and JavaScript
- Quickly generating an HTML structure with Emmet (`!` + Enter)
- Using Live Server for real-time preview during development
- Correctly linking CSS (`<link>` in `<head>`) and JavaScript (`<script>` before `</body>`)
- Verifying that the files are actually connected via the browser console

**Next steps:** dive deeper into CSS (Flexbox, Grid, responsiveness) and JavaScript (DOM manipulation, events) to turn this basic structure into a fully interactive website.

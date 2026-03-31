# Maintenance Guide

Welcome! This guide is written to help you easily update, modify, and expand your portfolio website without needing to be an expert coder. Your site uses a tool called **Hugo**, which turns simple text files into a fast, beautiful website.

---

## 🚀 1. How to Run the Website on Your Computer

Before you make any changes, you'll need to run the website locally on your computer. This lets you see your edits in real-time before you share them with the world.

### Step 1: Install Hugo

If you haven't installed Hugo yet, you'll need to install it once.

- **On Mac (using Homebrew):** Open the `Terminal` app and type:
  ```bash
  brew install hugo
  ```
- **On Windows:** Follow the official installation guide [here](https://gohugo.io/installation/windows/), or use a package manager like Chocolatey.
- **On Linux / Chromebook (Pixelbook):** Open the `Terminal` app and type:
  ```bash
  sudo apt-get update
  sudo apt-get install hugo
  ```

### Step 2: Start the Website

1. Open your `Terminal` (Mac) or `Command Prompt` (Windows).
2. Navigate to your website folder:
   ```bash
   cd path/to/nkemok.github.io
   ```
3. Run the Hugo "server" command:
   ```bash
   hugo server -D
   ```
4. Open your web browser and go to: `http://localhost:1313`.

Any time you save a file in this folder, your browser will immediately refresh and show you the changes! When you're done working, go back to the terminal and press `Ctrl + C` to stop the server.

---

## 📝 2. Adding or Editing Projects

Your main projects (like "Concur AI" or "Hybrid Cloud Mesh") live in the `content/projects/` folder.

**To edit an existing project:**

1. Open the file (for example, `content/projects/concur.md`) in a text editor (like VS Code, Notepad, or TextEdit).
2. The file is written in **Markdown**—a simple way to format text.
   - Type `####` to create a section heading.
   - Type `![Image Description](/assets/projects/your-image.png)` to insert an image.
3. Save the file and check your browser!

**To create a completely new project:**

1. Copy an existing project file (like `flow.md`) and rename it for your new project.
2. Open your new file and update the **YAML Frontmatter** (the block of settings at the very top between the `---` lines). Update the `title`, `company`, `role`, and `thumbnail` paths.
3. Replace the text and images below the `---` lines with your new content.

---

## 🎨 3. Adding to the Artboard Carousel

Your "Artboard" page is built dynamically. You do not need to write any HTML code to update the infinite-scrolling carousel!

1. Open `content/artboard.md`.
2. Look at the top of the file inside the `---` lines. You will see a list under `carousel:`.
3. To add a new image to the artboard, simply add a new entry to the bottom of the list like this:
   ```yaml
   - title: "My New Design"
     image: "https://link-to-your-image.com/my-design.png"
   ```
4. Save the file. Hugo will automatically handle all the complex duplication and presentation needed for the CSS infinite scrolling trick.

---

## 📄 4. Creating a New Page Type

If you ever want to add a brand new page (like a "Services" or "Blog" page):

1. **Create the Content.**
   Create a new file in the `content/` folder named `services.md`.
   Add frontmatter at the top like this:
   ```yaml
   ---
   title: "Services"
   type: "services"
   ---
   Here is the content of my new page!
   ```
2. **Create the Layout.**
   Because you used `type: "services"`, Hugo won't know what it should look like until you tell it.
   Create a new folder and file at: `layouts/services/single.html`.
   You can copy the code from `layouts/_default/single.html` into your new file, and then customize the HTML structure inside to your liking.

---

## 💅 5. Changing the Website's Design (CSS)

The website's colors, fonts, and spacing are handled by CSS styles located securely inside the `static/css/` folder. The styles are split into manageable pieces:

- **`base.css`**: Holds global colors (`--bg-color`, `--text-primary`), fonts, and generic resets. If you want to change the neon yellow accent color or the background color of the whole site, edit the `:root` variables here!
- **`layout.css`**: Controls how elements sit on the page (like standard padding and margins).
- **`home.css`**: Controls only the big "nkem okafor" homepage hero text.
- **`projects.css`**: Controls the grids of project thumbnails.
- **`artboard.css`**: Controls the carousel layout and scrolling animation.

**To add a new CSS rule:**
Open the appropriate CSS file, scroll to the bottom, and type your new style:

```css
.my-new-button {
  background-color: #ff0000;
  color: #ffffff;
  padding: 10px 20px;
  border-radius: 5px;
}
```

If you ever need to create an entirely _new_ CSS file (like for a future blog), simply add `my-blog.css` into the `static/css/` folder and make sure it is linked inside `layouts/partials/head.html` so the website loads it!

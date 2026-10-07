# Hide in Plain Sight

## Build and Customize an Image Steganography Tool with AI

This workshop walks you through building a browser-based steganography application using AI-assisted coding.

You will start with an empty folder, use a provided prompt to generate a working application, test it, customize it with your own prompt, and publish the finished project.

By the end, you will have a project you can share through GitHub and showcase on your AWS Builder Center profile.

---

## What You'll Build

Your application will be able to:

- Upload a PNG image
- Hide a text message inside the image
- Download the encoded image
- Upload an encoded image
- Recover the hidden message
- Handle invalid or unsupported input
- Run entirely inside the browser
- Be customized with your own design and features

The project uses:

- HTML
- CSS
- Vanilla JavaScript
- HTML Canvas API
- Least Significant Bit steganography

No backend is required.

---

## No Complicated Setup

You do **not** need:

- Node.js
- npm
- Python
- React
- Vite
- A database
- A development server
- Git installed on your computer

The final application will consist of only:

```text
index.html
style.css
script.js
```

You will be able to run it by opening:

```text
index.html
```

directly in your browser.

---

# Workshop Flow

```text
Create AWS Builder Profile
        ↓
Create Empty Project Folder
        ↓
Use Prompt 1
        ↓
Build the Base Application
        ↓
Test the Application
        ↓
Use Prompt 2
        ↓
Customize Your Project
        ↓
Test Again
        ↓
Publish
        ↓
Showcase Your Work
```

---

# 1. Set Up Your AWS Builder Profile

Before starting the project, create your AWS Builder identity and Builder Center profile.

Your finished project can later be added to your profile as something you built during the workshop.

Once your profile is ready, continue to the coding portion.

---

# 2. Create Your Project Folder

Create a new folder somewhere on your computer.

You can name it anything you want.

For example:

```text
steg-project
```

Your folder should initially be empty.

Do not worry about creating any code files yourself.

Prompt 1 will instruct your AI coding assistant to create them.

---

# 3. Open the Folder in Your AI Coding Tool

Open your empty project folder in the AI coding environment you are using for the workshop.

Make sure the AI has permission to create and modify files inside that folder.

You should still have an empty directory at this point.

---

# 4. Build the Base Application

Open:

[`prompts/prompt-1-build.md`](./prompts/prompt-1-build.md)

Copy the entire prompt and provide it to your AI coding assistant.

Prompt 1 will instruct the AI to create:

```text
index.html
style.css
script.js
```

and build the first version of your steganography application.

The base version should focus on functionality rather than visual customization.

---

## Expected Project Structure

After Prompt 1 finishes, your folder should look like this:

```text
steg-project/
│
├── index.html
├── style.css
└── script.js
```

There should be no:

```text
package.json
node_modules/
package-lock.json
```

or other Node.js-related files.

If your AI generates them, stop and remind it that the project must use only HTML, CSS, and vanilla JavaScript.

---

# 5. Run the Application

Open:

```text
index.html
```

in a modern web browser.

There should be:

- no installation
- no terminal commands
- no package setup
- no local server

The application should run directly in the browser.

---

# 6. Understand What You Built

The project uses image steganography.

Steganography is the practice of hiding information inside another piece of data.

In this project, your secret message is stored inside the pixel values of a PNG image.

A pixel may contain RGB values represented in binary:

```text
Red:   10110110
Green: 01100101
Blue:  11010010
```

The application changes the final bit of selected color values.

For example:

```text
10110110
```

may become:

```text
10110111
```

This is called modifying the **Least Significant Bit**, or LSB.

The change is extremely small, so the image should appear visually unchanged while still containing hidden data.

---

## Steganography vs. Encryption

They are not the same thing.

**Encryption** attempts to make the contents of a message unreadable.

**Steganography** attempts to hide the fact that a message exists.

This project focuses on steganography.

---

# 7. Test the Base Project

Do not move on to customization until the basic application works.

## Test 1 — Basic Message

Upload a PNG and encode:

```text
Hello World
```

Download the resulting image.

Upload that encoded image into the Decode section.

You should recover:

```text
Hello World
```

---

## Test 2 — Unicode

Try:

```text
Hello 👋 cybersecurity 🔐
```

The application should recover the exact same message.

---

## Test 3 — Empty Input

Try encoding without entering a message.

The application should display an error instead of continuing.

---

## Test 4 — Normal Image

Try decoding a PNG that has never been encoded by your application.

The application should report that no valid hidden message was found.

It should not display random characters.

---

## Test 5 — Capacity

Try entering a message that is too large for the selected image.

The application should detect that the image does not have enough capacity.

---

# 8. Review the AI-Generated Code

Before customizing your project, take a few minutes to inspect what the AI created.

You do not need to understand every line.

Try to identify:

### `index.html`

Where are the:

- image upload controls
- message input
- Encode button
- Decode button
- output areas

### `style.css`

Where are the:

- colors
- spacing
- layout
- button styles
- image preview styles

### `script.js`

Try to locate functions related to:

- image loading
- encoding
- decoding
- capacity calculation
- downloading the PNG

The purpose of this workshop is not only to generate code.

You should have a basic understanding of what the generated application is doing.

---

# 9. Make the Project Your Own

Once the base application works, open:

[`prompts/prompt-2-customize.md`](./prompts/prompt-2-customize.md)

Prompt 2 allows you to define your own:

- project name
- visual style
- theme
- features
- user experience

You should customize the prompt before giving it to your AI assistant.

---

## Example

Instead of writing:

```text
Make the website cooler.
```

give the AI a clear direction:

```text
Rename the project to GhostPixel.

Redesign the application to resemble a classified 1980s intelligence
terminal.

Use monochrome typography, terminal-style panels, subtle scanlines,
and restrained animations.

Add an image capacity meter and an educational panel explaining how
LSB steganography works.

Do not change the existing encoding or decoding algorithm.
```

Specific instructions usually produce better results.

---

# 10. Customization Ideas

## Visual Styles

You could try:

- Retro terminal
- Y2K
- Frutiger Aero
- Windows XP
- Minimalist
- Cyberpunk
- Classified intelligence system
- Vaporwave
- Sci-fi interface
- Early-2000s web design
- Futuristic laboratory
- Brutalist interface
- Something completely original

---

## Feature Ideas

Try adding one or more features such as:

- Drag-and-drop image upload
- Message capacity meter
- Character counter
- Before-and-after image comparison
- Custom download filename
- Image information panel
- Dark/light mode
- Animated encoding sequence
- Binary visualization
- Steganography explanation panel
- Full-screen image preview
- Better success and error feedback

Your final project should have at least one meaningful difference from the base version.

---

# 11. Test Again

Customization can accidentally break working code.

After using Prompt 2, repeat your tests.

Before publishing, confirm:

- [ ] PNG upload works
- [ ] Image preview works
- [ ] Messages can be encoded
- [ ] Encoded PNG downloads correctly
- [ ] Downloaded images can be decoded
- [ ] Unicode messages work
- [ ] Normal images are rejected correctly
- [ ] Capacity checking still works
- [ ] Your new features work
- [ ] The interface is usable
- [ ] No Node.js was added
- [ ] No npm dependencies were added
- [ ] No backend was added
- [ ] No images or messages are being uploaded
- [ ] `index.html` still runs directly in the browser

---

# 12. Privacy

This project is intentionally designed to operate locally.

The expected flow is:

```text
Your Image
    ↓
Your Browser
    ↓
JavaScript + Canvas
    ↓
Encoded Image
```

Your application should not need to send the image or hidden message to an external server.

This is one of the reasons the project uses browser-native technologies.

---

# Why This Project Uses PNG

PNG uses lossless image compression.

LSB steganography depends on preserving precise pixel values.

Lossy formats such as JPEG may modify those values and destroy the hidden data.

For this workshop:

```text
PNG  → Recommended
JPEG → Do not use for encoded output
```

---

# 13. Name Your Project

Give your project its own identity before publishing it.

Examples:

```text
GhostPixel
PixelVault
HiddenFrame
StegLab
CipherCanvas
GhostByte
ShadowPixel
Veil
```

These are examples only.

Try to create something unique.

---

# 14. Publish to GitHub

You do **not** need Git installed.

Go to GitHub in your browser and create a new repository.

Example:

```text
ghostpixel-steganography
```

Then use GitHub's browser interface to upload:

```text
index.html
style.css
script.js
```

You can also create your own project README.

Your repository should eventually look something like:

```text
ghostpixel-steganography/
│
├── index.html
├── style.css
├── script.js
└── README.md
```

---

# 15. Optional — Publish the Website

Because your project is a static website, you can optionally publish it using a static hosting service such as GitHub Pages.

That turns your local project into something others can open in their browser.

```text
Local Project
     ↓
GitHub Repository
     ↓
Published Website
```

---

# 16. Showcase Your Project

Once your project is complete, add it to your AWS Builder Center profile.

Consider including:

## Project Name

Your custom project name.

## Description

Example:

```text
A browser-based image steganography application that hides text
inside PNG images using Least Significant Bit encoding.
```

## Technologies

```text
HTML
CSS
JavaScript
Canvas API
```

## Concepts

```text
Steganography
LSB Encoding
Browser Image Processing
AI-Assisted Development
Testing
Debugging
Prompt Engineering
```

You can also include links to your GitHub repository and published application if available.

---

# Final Challenge

Have someone else try your application without explaining how to use it.

Ask them to:

1. Upload an image
2. Hide a message
3. Download the encoded image
4. Decode the message

If they cannot understand the workflow, improve your interface.

A project should not only work.

It should also be understandable.

---

# What You Practiced

By completing this workshop, you worked with:

- Basic steganography
- Least Significant Bit encoding
- Image pixel manipulation
- HTML
- CSS
- JavaScript
- Browser APIs
- AI-assisted development
- Prompt writing
- Testing
- Debugging
- GitHub
- AWS Builder Center
- Project publishing

More importantly, you followed a real development loop:

```text
Define
  ↓
Build
  ↓
Test
  ↓
Customize
  ↓
Debug
  ↓
Publish
```

---

# Workshop Files

```text
.
├── README.md
│
└── prompts/
    ├── prompt-1-build.md
    └── prompt-2-customize.md
```

---

## Educational Use

This workshop is intended for learning and experimentation.

Do not use the project to conceal malicious content, bypass security controls, or violate applicable rules, policies, or laws.

The goal is to understand how steganography works, how AI can assist with development, and why generated code should still be reviewed and tested.

---

## Start Here

Open:

[`prompts/prompt-1-build.md`](./prompts/prompt-1-build.md)

Create an empty project folder, give Prompt 1 to your AI coding assistant, and start building.
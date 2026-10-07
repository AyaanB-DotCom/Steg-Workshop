# 👻 Hide in Plain Sight

### Build Your Own Image Steganography Tool with AI

> A beginner-friendly cybersecurity workshop where you'll use AI-assisted coding to build, customize, test, and publish your own browser-based steganography application.

---

<p align="center">

**HTML** • **CSS** • **JavaScript** • **Cybersecurity** • **AI-Assisted Development**

</p>

---

## 🚀 What You'll Build

By the end of this workshop, you'll have your own web application capable of hiding secret text inside PNG images using **Least Significant Bit (LSB) steganography**.

Your application will be able to:

- 🖼️ Upload PNG images
- ✍️ Enter a secret message
- 👻 Hide the message inside the image
- 💾 Download the encoded PNG
- 🔎 Upload an encoded image
- 🔓 Recover the hidden message
- 🎨 Customize the design and features
- 🌐 Publish your finished project
- ☁️ Showcase your work on AWS Builder Center

And the best part?

**No Python. No Node.js. No npm. No complicated setup.**

Everything runs directly inside your browser.

---

# 🧠 What Is Steganography?

**Steganography** is the practice of hiding information inside another piece of data.

In this workshop, we'll hide text inside the individual pixels of an image.

A pixel may contain values similar to:

```text
Red:   10110110
Green: 01100101
Blue:  11010010
```

By changing only the **Least Significant Bit**:

```text
10110110 → 10110111
```

we can store information while making an extremely small change to the image.

The image still looks essentially identical to the human eye.

### Encryption vs. Steganography

```text
Encryption
────────────────────────────
Hides the CONTENT of a message.

Steganography
────────────────────────────
Attempts to hide the EXISTENCE
of the message.
```

In this project, you'll explore the second technique.

---

# 🎯 Workshop Goal

This workshop isn't just about copying AI-generated code.

You'll follow the full development process:

```text
        IDEA
          ↓
      PROMPT AI
          ↓
     BUILD THE APP
          ↓
        TEST IT
          ↓
      BREAK THINGS
          ↓
        FIX IT
          ↓
      CUSTOMIZE IT
          ↓
       PUBLISH IT
          ↓
   SHOWCASE YOUR WORK
```

You'll start with the same core project as everyone else.

Then you'll make it **your own**.

---

# ✅ What You'll Need

Before getting started, make sure you have:

- 💻 A laptop
- 🌐 A modern web browser
- 🤖 Access to an AI coding assistant
- 🐙 A GitHub account
- ☁️ An AWS Builder ID

### You do NOT need:

- ❌ Node.js
- ❌ npm
- ❌ Python
- ❌ React
- ❌ Vite
- ❌ A database
- ❌ A web server
- ❌ Previous cybersecurity experience

---

# 📁 Project Structure

Your project will use only three core files:

```text
your-project/
│
├── index.html
├── style.css
└── script.js
```

### What does each file do?

| File | Purpose |
|---|---|
| `index.html` | Defines the structure and content of your application |
| `style.css` | Controls how your application looks |
| `script.js` | Contains the steganography logic and functionality |

That's it.

No package installation.

No build process.

No server.

---

# 🗺️ Workshop Roadmap

## 01 — Create Your AWS Builder Identity

Before building anything, create your AWS Builder ID and set up your Builder Center profile.

By the end of the workshop, you'll have a project that you can showcase as part of your builder portfolio.

### Your goal:

```text
AWS Builder ID
      ↓
Builder Center Profile
      ↓
Your Public Builder Identity
```

Once you're set up, move on to the project.

---

# 02 — Get the Starter Files

Open the [`starter/`](./starter/) folder.

You should see:

```text
starter/
│
├── index.html
├── style.css
├── script.js
└── sample-image.png
```

Download or copy these files into your own project folder.

The starter files intentionally contain almost no code.

That's because **you're going to build the application yourself with AI.**

---

# 03 — Build the Base Application

Open:

### 👉 [`prompts/prompt-1-build.md`](./prompts/prompt-1-build.md)

Copy **Prompt 1** into your AI coding assistant.

Prompt 1 contains the technical requirements for your application.

Your AI should build a working steganography tool using only:

```text
HTML
CSS
Vanilla JavaScript
```

### Important

Your application should **NOT** use:

```text
Node.js
npm
npx
React
Vite
Python
Backend Servers
Databases
External Frameworks
```

If your AI tries to introduce any of these, remind it:

> This project must run by simply opening `index.html` in a browser.

---

# 04 — Run Your Application

Once the AI finishes generating your project, open:

```text
index.html
```

in your browser.

No terminal commands are required.

No installation is required.

No development server is required.

Just:

```text
Double-click index.html
        ↓
Browser opens
        ↓
App runs
```

---

# 05 — Test the Base Project

Before customizing anything, make sure your application actually works.

Use `sample-image.png` from the starter folder.

### Test #1 — Basic Message

Encode:

```text
Hello World
```

Download the encoded PNG.

Upload it to the Decode section.

You should recover:

```text
Hello World
```

---

### Test #2 — Unicode

Try:

```text
Hello 👋 cybersecurity 🔐
```

Your application should successfully recover the same message.

---

### Test #3 — Empty Message

Try pressing Encode without entering a message.

Your application should show a clear error.

---

### Test #4 — Wrong Image

Try decoding a normal image that doesn't contain a hidden message.

The application should handle this gracefully.

---

### Test #5 — Too Much Data

Try entering a very long message into a small image.

The application should detect that the image does not have enough capacity.

---

# 🧪 Don't Trust AI Automatically

AI-generated code can be wrong.

Part of this workshop is learning how to **test what AI creates**.

Ask yourself:

- Does encoding actually work?
- Does decoding return the exact original message?
- Does the downloaded image still look normal?
- Does Unicode work?
- Can the application handle errors?
- Did the AI accidentally add external dependencies?
- Is anything being uploaded somewhere?

If something breaks, don't immediately restart.

Try to **debug it with the AI.**

---

# 06 — Make It Yours

Now comes the fun part.

Open:

### 👉 [`prompts/prompt-2-customize.md`](./prompts/prompt-2-customize.md)

Prompt 2 gives you a framework for designing your **own AI prompt**.

Instead of everyone producing the exact same project, you will choose:

- 🎨 Your own visual style
- 🏷️ Your own project name
- 🧩 Your own additional features
- ✨ Your own user experience

---

# 🎨 Design Inspiration

Your project could look like:

```text
┌──────────────────────────────┐
│  CLASSIFIED // STEG SYSTEM   │
│                              │
│  > SELECT IMAGE              │
│  > ENTER PAYLOAD             │
│                              │
│  [ ENCODE ]      [ DECODE ]  │
│                              │
│  STATUS: READY               │
└──────────────────────────────┘
```

Or something completely different.

Some ideas:

- 🟢 Retro hacker terminal
- 🌊 Frutiger Aero
- 💿 Y2K
- 🖥️ Windows XP
- 🕵️ Classified intelligence terminal
- 👾 Arcade
- 🌌 Sci-fi spaceship interface
- 💜 Vaporwave
- 🍎 Minimalist modern UI
- 🧪 Cyber laboratory
- 👻 Horror / paranormal interface
- 🛰️ Satellite communications system
- 🧊 Glassmorphism

Or invent something completely original.

---

# 🧩 Feature Ideas

Choose at least **one feature** to make your application different.

### Beginner

- Drag-and-drop image upload
- Character counter
- Clear/reset button
- Better image preview
- Custom download filename
- Dark/light mode
- Copy confirmation

### Intermediate

- Image capacity meter
- Before/after image comparison
- Image information panel
- Animated encoding effect
- Binary visualization
- Steganography explanation panel
- Improved error feedback

### Challenge

Create your own feature idea.

Try asking:

> What would make this application more useful, educational, or interesting?

---

# 🧠 Writing a Better AI Prompt

Avoid prompts like:

```text
make it cooler
```

Instead, communicate exactly what you want.

### Weak Prompt

```text
Make my site cyberpunk.
```

### Better Prompt

```text
Redesign my existing steganography application to resemble
a classified 1980s intelligence terminal.

Use a dark interface, monochrome green typography, subtle
CRT scanlines, terminal-style buttons, and restrained animations.

Keep the application easy to navigate.

Do not modify the existing encoding or decoding logic.

Add a message-capacity meter and an educational panel explaining
how LSB steganography works.
```

Specific prompts usually produce better results.

---

# 07 — Test Again

Customization can break previously working code.

After Prompt 2, test everything again.

### Required final checks

- [ ] PNG uploads correctly
- [ ] Image preview works
- [ ] Secret message can be encoded
- [ ] Encoded PNG downloads
- [ ] Downloaded PNG can be reopened
- [ ] Hidden message decodes correctly
- [ ] Unicode text works
- [ ] Error handling works
- [ ] New features work
- [ ] No Node.js was added
- [ ] No npm dependencies were added
- [ ] Nothing is uploaded to an external server
- [ ] `index.html` still opens directly in the browser

If something stopped working, fix it before publishing.

---

# 🔐 Privacy

One of the important design choices in this project is that processing happens **locally**.

```text
YOUR IMAGE
    ↓
YOUR BROWSER
    ↓
STEGANOGRAPHY
    ↓
ENCODED IMAGE
```

Your image does not need to leave your device.

Your application should not send images or secret messages to an external server.

This is why we're using browser-native technologies such as:

- JavaScript
- Canvas API
- TextEncoder
- TextDecoder

---

# ⚠️ Why PNG?

This project uses **PNG images** for a reason.

PNG uses lossless compression.

LSB steganography depends on preserving very small changes to pixel values.

Formats using lossy compression can modify those values.

For example:

```text
PNG
✓ Lossless
✓ Pixel values preserved
✓ Good for this project

JPEG
✗ Lossy
✗ Pixel values may change
✗ Hidden LSB data may be destroyed
```

So for this workshop:

> **Stick with PNG.**

---

# 08 — Give Your Project an Identity

Before publishing, choose a name.

Examples:

```text
GhostPixel
PixelVault
StegHide
CipherCanvas
GhostByte
HiddenFrame
PixelGhost
Veil
StegLab
ShadowPixel
```

Try creating something unique instead of using one of these directly.

---

# 09 — Create Your GitHub Repository

Create a new GitHub repository for your finished project.

Example:

```text
ghostpixel-steganography
```

Your repository should contain:

```text
ghostpixel-steganography/
│
├── index.html
├── style.css
├── script.js
└── README.md
```

### Your README should explain:

- What your project does
- What steganography is
- What technologies you used
- What features you added
- What you learned
- How to run the project

---

# 🌐 Optional — Publish with GitHub Pages

Because your application is completely static, it can be hosted easily with GitHub Pages.

Once published, you'll have a live URL that other people can visit.

Your project can go from:

```text
Local Files
```

to:

```text
GitHub Repository
       ↓
GitHub Pages
       ↓
Live Web Application
```

---

# ☁️ 10 — Showcase Your Project on AWS Builder Center

Once your project is finished, add it to your Builder Center profile.

Consider including:

### Project Name

```text
GhostPixel
```

### Description

```text
A browser-based image steganography application that hides
text inside PNG images using Least Significant Bit encoding.
```

### Technologies

```text
HTML
CSS
JavaScript
Canvas API
```

### Skills Demonstrated

```text
Steganography
Web Development
AI-Assisted Development
Testing
Debugging
Prompt Engineering
```

### Links

Add your:

- GitHub repository
- Live project, if you deployed it

---

# 🏆 Final Challenge

Before you're finished, find another student.

Give them your application.

Don't explain how to use it.

See whether they can figure out how to:

1. Upload an image
2. Hide a message
3. Download the image
4. Decode the message

If they can't figure it out easily, consider improving your user interface.

Good software isn't just functional.

It should also be understandable.

---

# ✅ You Made It

If you completed the workshop, you now have experience with:

- 🔐 Basic steganography
- 🧠 Least Significant Bit encoding
- 🖼️ Browser image manipulation
- ⚡ Vanilla JavaScript
- 🎨 Front-end design
- 🤖 AI-assisted development
- 🧪 Software testing
- 🐛 Debugging AI-generated code
- ✍️ Prompt engineering
- 🐙 GitHub
- ☁️ AWS Builder Center
- 🚀 Publishing a technical project

More importantly, you didn't just ask AI to generate something.

You:

```text
DEFINED
   ↓
BUILT
   ↓
TESTED
   ↓
CUSTOMIZED
   ↓
DEBUGGED
   ↓
PUBLISHED
```

That's the workflow.

---

# 📚 Workshop Files

```text
.
├── README.md
│
├── starter/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   └── sample-image.png
│
├── prompts/
│   ├── prompt-1-build.md
│   └── prompt-2-customize.md
│
├── guides/
│   ├── testing.md
│   ├── github-pages.md
│   └── builder-center.md
│
└── assets/
    └── screenshots/
```

---

# 🛡️ Educational Use

This project is intended for educational purposes.

The goal is to learn:

- how steganography works
- how web applications process data
- how AI can assist development
- why AI-generated code should still be tested
- how to build and publish technical projects

Do not use this project to conceal malicious content, bypass security controls, or violate rules, policies, or laws.

---

<p align="center">

### 👻 Hide Something. Break Something. Fix Something. Build Something.

**Happy Building.**

</p>
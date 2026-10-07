<h1 align="center">Hide in Plain Sight</h1>

<p align="center">
  Build a steganography tool with AI. Customize it. Test it. Publish it.
</p>

<p align="center">
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square">
  <img alt="CSS3" src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square">
  <img alt="Runs in the browser" src="https://img.shields.io/badge/Runs_in-Browser-1f2937?style=flat-square">
  <img alt="Beginner friendly" src="https://img.shields.io/badge/Level-Beginner_Friendly-2ea043?style=flat-square">
</p>

<p align="center">
  A hands-on cybersecurity workshop: start with an empty folder, finish with a live web app.
</p>

---

```text
SETUP  →  BUILD  →  TEST  →  CUSTOMIZE  →  PUBLISH
```

### Start here

**[Prompt 1: Build the Base App](./prompts/prompt-1-build.md)**  
Start with an empty folder and generate the working steganography application.

**[Prompt 2: Customize Your App](./prompts/prompt-2-customize.md)**  
Transform the working project with your own theme, name, and features.

---

## What You're Building

A browser-based tool that hides text inside PNG images using Least Significant Bit (LSB) steganography. Everything runs locally. Nothing is uploaded anywhere.

| Capability | Description |
| :--- | :--- |
| **Encode** | Upload a PNG, hide a text message, download the encoded image |
| **Decode** | Upload an encoded PNG and recover the hidden message |
| **Validate** | Handle empty input, oversized messages, and images with no hidden data |
| **Customize** | Add your own name, visual theme, and features |

The finished project is three files:

```text
index.html
style.css
script.js
```

---

## Zero Setup

> **Open `index.html` in a modern browser. That's it.**
> No installs, no terminal, no local server.

| Used | Not required |
| :--- | :--- |
| HTML | Node.js |
| CSS | npm |
| Vanilla JavaScript | Python |
| Canvas API | React / Vite |
| TextEncoder / TextDecoder | Backend or database |
| | Git installed locally |

> [!NOTE]
> If your AI assistant generates `package.json`, `node_modules/`, or `package-lock.json`, stop it. Remind it that the project must use only HTML, CSS, and vanilla JavaScript.

---

## Workshop Flow

| Phase | What happens |
| :--- | :--- |
| **1. Setup** | Create your AWS Builder profile. Create an empty folder (for example `steg-project`) and open it in your AI coding tool with permission to create and edit files. |
| **2. Build** | Give the AI **Prompt 1**. It creates `index.html`, `style.css`, and `script.js`. |
| **3. Test** | Run the five tests below. Skim the generated code. Fix what breaks. |
| **4. Customize** | Edit **Prompt 2** with your own name, theme, and features, then give it to the AI. |
| **5. Publish** | Retest, upload to GitHub from your browser, optionally deploy with GitHub Pages, and add the project to AWS Builder Center. |

---

## Workshop Prompts

| Prompt | Purpose |
| :--- | :--- |
| [Prompt 1: Build](./prompts/prompt-1-build.md) | Builds the first working application from an empty folder. |
| [Prompt 2: Customize](./prompts/prompt-2-customize.md) | Customizes the working project while preserving its steganography functionality. |

### Using Prompt 1

Copy the **entire** prompt into your AI coding assistant. When it finishes, your folder should look like this:

```text
steg-project/
├── index.html
├── style.css
└── script.js
```

Open `index.html` in your browser. The base version focuses on function, not looks.

---

## What Is Steganography?

Steganography hides information inside other data. Here, the message lives in the pixel values of a PNG.

Each pixel stores red, green, and blue values as binary. The app changes only the **last bit** of selected values:

```text
Original:   10110110
Encoded:    10110111
                   ▲
          Least Significant Bit
```

That change is too small to see, but across thousands of pixels it is enough to store a message.

| Technique | Goal |
| :--- | :--- |
| **Encryption** | Hides the *meaning* of information |
| **Steganography** | Hides the *existence* of information |

<details>
<summary><b>Why PNG?</b></summary>

<br>

PNG is lossless, so exact pixel values are preserved. JPEG is lossy and can alter those values, destroying the hidden data.

```text
PNG   →  Recommended
JPEG  →  Do not use for encoded output
```

</details>

<details>
<summary><b>Privacy</b></summary>

<br>

The app is designed to work entirely on your device. Your image and message never need to leave your browser.

```text
Your Image  →  Browser  →  JavaScript + Canvas  →  Encoded Image
```

</details>

---

## Test Before You Customize

> **AI-generated code is not automatically correct.**
> Build, test, break, fix, then customize.

Do not move on until the base application passes every test.

| # | Test | Input | Expected result |
| :-: | :--- | :--- | :--- |
| 1 | **Basic message** | Encode `Hello World`, download the PNG, upload it to Decode | Recovers `Hello World` |
| 2 | **Unicode** | `Hello 👋 cybersecurity 🔐` | Recovers the exact same message |
| 3 | **Empty input** | Click Encode with no message | Shows an error and stops |
| 4 | **Normal PNG** | Decode a PNG that was never encoded | Reports no valid hidden message, with no random characters |
| 5 | **Capacity** | A message too large for the image | Detects insufficient capacity |

### Review the generated code

You don't need to understand every line. Find these:

| File | Locate |
| :--- | :--- |
| `index.html` | Upload controls, message input, Encode and Decode buttons, output areas |
| `style.css` | Colors, spacing, layout, button styles, image preview styles |
| `script.js` | Image loading, encoding, decoding, capacity calculation, PNG download |

---

## Customize

Open [Prompt 2](./prompts/prompt-2-customize.md) and edit it before giving it to your AI. Choose:

- **A project name**
- **A visual theme**
- **1 to 3 custom features**

Your final project needs at least one meaningful difference from the base version.

| Themes | Features |
| :--- | :--- |
| Retro terminal | Drag-and-drop upload |
| Classified intelligence system | Message capacity meter |
| Cyberpunk | Before/after comparison |
| Sci-fi interface | Custom download filename |
| Y2K | Image metadata panel |
| Frutiger Aero | Binary visualization |
| Windows XP | LSB explanation panel |
| Early-2000s web | Improved success and error feedback |
| Brutalist | Dark/light mode |
| Minimal | Character counter, full-screen preview |

**Project name ideas:** `GhostPixel`, `PixelVault`, `HiddenFrame`, `StegLab`, `GhostByte`, `Veil`. Make up your own.

### Be specific

Vague prompts get vague results.

```text
Weak:    Make the website cooler.

Strong:  Rename the project to GhostPixel.

         Redesign the application to resemble a classified 1980s
         intelligence terminal. Use monochrome typography,
         terminal-style panels, subtle scanlines, and restrained
         animations.

         Add an image capacity meter and an educational panel
         explaining how LSB steganography works.

         Do not change the existing encoding or decoding algorithm.
```

---

## Final Validation Checklist

Customization can break working code. Repeat your tests, then confirm everything below before publishing.

**Functionality**

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

**Constraints**

- [ ] No Node.js added
- [ ] No npm dependencies added
- [ ] No backend added
- [ ] No images or messages are uploaded anywhere
- [ ] `index.html` still runs directly in the browser

> [!TIP]
> **Final challenge:** hand your app to someone else without explaining it. Can they upload an image, hide a message, download it, and decode it? If not, improve the interface.

---

## Publish to GitHub

No Git required. Everything happens in your browser.

1. Go to [github.com](https://github.com) and create a new repository, for example `ghostpixel-steganography`.
2. Choose **Add file → Upload files**.
3. Upload:
   - `index.html`
   - `style.css`
   - `script.js`
   - `README.md` (optional, your own project README)
4. Commit the changes through the GitHub interface.

```text
ghostpixel-steganography/
├── index.html
├── style.css
├── script.js
└── README.md
```

---

## Optional: GitHub Pages

Because the project is a static site, GitHub Pages can turn your repository into a live web app that anyone can open.

```text
Local Project  →  GitHub Repository  →  Live Website
```

In your repository, open **Settings → Pages** and publish from your main branch.

---

## Showcase on AWS Builder Center

Add the finished project to your Builder Center profile.

| Field | What to include |
| :--- | :--- |
| **Project name** | Your custom name |
| **Description** | One or two plain sentences on what it does |
| **Technologies** | HTML, CSS, JavaScript, Canvas API |
| **Concepts** | Steganography, LSB encoding, browser image processing, AI-assisted development, testing, debugging, prompt engineering |
| **GitHub link** | Your repository URL |
| **Live link** | Your GitHub Pages URL, if deployed |

**Example description**

> A browser-based image steganography application that hides text inside PNG images using Least Significant Bit encoding.

---

## What You Practiced

| Skills | Concepts |
| :--- | :--- |
| HTML, CSS, JavaScript | Steganography and LSB encoding |
| Canvas and browser APIs | Image pixel manipulation |
| Prompt writing | AI-assisted development |
| Testing and debugging | Publishing with GitHub |

```text
Define  →  Build  →  Test  →  Customize  →  Debug  →  Publish
```

---

## Educational Use

This workshop is for learning: steganography, browser image manipulation, AI-assisted development, prompting, testing, debugging, and publishing.

Do not use it to conceal malicious content, bypass security controls, or violate applicable rules, policies, or laws.

---

## Start Here

Create an empty folder, open it in your AI coding tool, and give it Prompt 1.

**[Open Prompt 1: Build the Base App →](./prompts/prompt-1-build.md)**

<details>
<summary><b>Repository files</b></summary>

<br>

```text
.
├── README.md
└── prompts/
    ├── prompt-1-build.md
    └── prompt-2-customize.md
```

</details>
I already have a working browser-based steganography application built from my workshop starter files.

My existing project contains:

`index.html`

`style.css`

`script.js`

The application currently works correctly.

Your task is to MODIFY these existing files and customize the application based on the design and feature choices I provide below.

Do NOT create a new project.

Do NOT rebuild the application from scratch.

Do NOT replace working steganography logic unnecessarily.

The goal is to make the existing project feel uniquely mine while preserving its functionality.

---

# Most Important Rule

The existing Encode and Decode functionality already works.

Protect it.

Do not rewrite the core steganography algorithm simply because you are changing the interface.

Modify existing code carefully.

If a requested visual change does not require changes to the encoding or decoding logic, leave that logic alone.

---

# Existing Core Features

The current application already supports:

- PNG image upload
- image previews
- LSB steganography
- UTF-8 / Unicode messages
- message-capacity checking
- encoded PNG downloads
- decoding hidden messages
- validation of encoded images
- copy-to-clipboard
- reset functionality
- local browser processing
- error handling

All of these features must continue working after customization.

---

# My Project Identity

### Project Name

`[ENTER YOUR PROJECT NAME]`

### Visual Theme

`[ENTER YOUR VISUAL THEME]`

Possible examples:

- retro hacker terminal
- cyberpunk
- Y2K
- Frutiger Aero
- Windows XP
- classified intelligence system
- vaporwave
- futuristic laboratory
- arcade
- sci-fi spaceship
- minimalist
- brutalist
- early-2000s web
- modern glass interface
- horror terminal
- satellite control system
- custom original idea

### I Want the Application to Feel

`[ADJECTIVE 1]`

`[ADJECTIVE 2]`

`[ADJECTIVE 3]`

Examples:

- mysterious
- polished
- nostalgic
- playful
- technical
- futuristic
- minimal
- experimental
- cinematic

---

# Design Direction

Redesign the existing interface to fit my chosen visual theme.

You may modify:

- page layout
- typography
- spacing
- backgrounds
- cards
- panels
- buttons
- upload controls
- Encode and Decode sections
- image-preview styling
- status indicators
- error messages
- success messages
- navigation
- animations
- hover states
- responsive layout

The theme should feel cohesive.

Do not simply apply random colors or effects.

The project should still be easy to use.

Visual design must not make important controls difficult to find or read.

---

# Features I Want to Add

### Feature 1

`[DESCRIBE FEATURE]`

### Feature 2

`[DESCRIBE FEATURE]`

### Optional Feature 3

`[DESCRIBE FEATURE OR LEAVE BLANK]`

Examples of appropriate additions include:

- drag-and-drop image uploads
- message capacity meter
- animated encoding sequence
- character counter improvements
- before/after image comparison
- image dimensions and file-size display
- custom download filenames
- dark/light mode toggle
- binary-data visualization
- LSB educational panel
- improved mobile layout
- full-screen image preview
- copy-success feedback
- keyboard shortcuts
- collapsible information panels
- subtle soundless visual effects
- improved onboarding instructions

Do not add major unrelated functionality unless I explicitly request it.

---

# Preserve the Existing Files

Continue editing:

`index.html`

`style.css`

`script.js`

Do not introduce a new folder structure.

Do not generate a new application separately.

Do not rename the existing files.

Keep:

`index.html` → structure

`style.css` → styling

`script.js` → application behavior

Do not place all CSS and JavaScript directly into the HTML file.

---

# Critical Technology Constraints

The project must continue using only:

- HTML
- CSS
- Vanilla JavaScript
- built-in browser APIs

Do NOT introduce:

- Node.js
- npm
- npx
- yarn
- pnpm
- package.json
- package-lock.json
- node_modules
- React
- Next.js
- Vue
- Angular
- TypeScript
- Python
- Vite
- Webpack
- Parcel
- backend servers
- databases
- external frameworks
- external JavaScript libraries
- build tools
- package managers

Do not provide any Node.js or npm setup instructions.

The completed project must still work by simply opening:

`index.html`

in a modern browser.

---

# Preserve Privacy

The existing application performs image processing locally.

Keep it that way.

Do NOT:

- upload images
- upload messages
- add analytics
- add tracking
- send information to APIs
- create user accounts
- add cloud storage
- add databases
- store secret messages persistently

Keep the application's privacy notice visible.

---

# Preserve PNG and LSB Behavior

Do not change the application in a way that breaks its ability to:

1. encode text into PNG pixel data
2. export the encoded result as PNG
3. reopen that PNG later
4. recover the original message

Do not convert encoded output to JPEG.

Do not replace the LSB technique with an unrelated implementation.

Do not modify the encoded-data format unless one of my requested features truly requires it.

If you must change the format, update both the encoder and decoder consistently and explain the reason.

---

# Improve the Experience

The customized version should still make the workflow obvious.

A new user should quickly understand:

### Encoding

Upload Image

→ Enter Secret Message

→ Encode

→ Download PNG

### Decoding

Upload Encoded PNG

→ Decode

→ Read Hidden Message

Customization should improve this workflow, not hide it.

---

# Responsive Design

Make sure the customized interface remains usable on:

- standard laptops
- smaller laptops
- tablets
- reasonably narrow browser windows

Avoid layouts that only work at one exact screen size.

---

# Code Editing Rules

Work from the existing implementation.

Preserve working functions whenever possible.

Do not rewrite the entire `script.js` just because the visual design changed.

If adding new JavaScript functionality:

- keep functions organized
- use descriptive names
- avoid unnecessary global variables
- preserve useful existing comments
- add comments for meaningful new logic

If most of the requested customization is visual, prefer making those changes in `style.css`.

---

# Test the Project After Customization

Before finishing, mentally review and verify these workflows.

## Encoding Test

Upload a PNG.

Enter:

`Hello World`

Encode it.

Download the result.

## Decoding Test

Upload the downloaded encoded PNG.

Decode it.

The result should still be:

`Hello World`

## Unicode Test

Test:

`Hello 👋 cybersecurity 🔐`

The exact text should be recovered.

## Error Test

Try decoding a normal PNG.

The application should still correctly report that no valid hidden message exists.

## Capacity Test

Try encoding a message too large for the image.

The capacity protection should still work.

## Custom Feature Test

Verify each new feature I requested works without breaking existing features.

---

# Final Technical Check

Before completing the customization, confirm:

- no Node.js was introduced
- no npm was introduced
- no package files were created
- no frameworks were introduced
- no network requests were introduced
- no backend was introduced
- `index.html` still opens directly
- Encode still works
- Decode still works
- Unicode still works
- PNG export still works
- error handling still works
- my requested new features work
- the project looks substantially different from the starter design

---

# My Customization Choices

Fill in and follow these instructions:

### Project Name

`[TYPE HERE]`

### Visual Theme

`[TYPE HERE]`

### I Want It to Feel

`[TYPE HERE]`

### Feature 1

`[TYPE HERE]`

### Feature 2

`[TYPE HERE]`

### Optional Feature 3

`[TYPE HERE]`

### Other Changes I Want

`[TYPE HERE]`

---

# Before Editing

Before modifying the files, briefly summarize:

1. the theme you understood
2. the features you will add
3. the parts of the existing application you will preserve

Then make the changes.

---

# How to Respond

Modify the existing:

`index.html`

`style.css`

`script.js`

Return the complete updated contents of each file.

Clearly label each file.

Do not create a replacement project.

Do not provide Node.js, npm, or package-installation instructions.

After the code, briefly summarize:

- what you customized
- what features you added
- what existing functionality you intentionally preserved

The completed application must still run by simply opening:

`index.html`

in a modern web browser.
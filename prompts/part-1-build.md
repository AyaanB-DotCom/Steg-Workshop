You are helping me complete an existing beginner-friendly cybersecurity workshop project.

I already have a starter project containing these files:

`index.html`

`style.css`

`script.js`

The files are intentionally minimal and are already connected to each other.

Your job is to MODIFY these existing files and turn them into a complete browser-based image steganography application.

Do NOT create a new project structure.

Do NOT create additional required files.

Do NOT rename the existing files.

---

# Critical Technology Constraint

This project must use only:

- HTML
- CSS
- Vanilla JavaScript
- Built-in browser APIs

This project must NOT use Node.js in any form.

Do NOT use:

- Node.js
- npm
- npx
- yarn
- pnpm
- package.json
- package-lock.json
- node_modules
- Vite
- Webpack
- Parcel
- React
- Next.js
- Vue
- Angular
- TypeScript
- Python
- backend servers
- databases
- external frameworks
- external JavaScript libraries
- build tools
- package managers

Do not generate Node.js setup instructions.

Do not tell me to run:

`npm install`

`npm run dev`

`npx ...`

`node ...`

or any similar command.

The completed application must require:

**ZERO package installation**

**ZERO terminal setup**

**ZERO development servers**

A student must be able to open:

`index.html`

directly in a modern browser and use the application.

---

# Existing Starter Files

You are working with these existing files:

### `index.html`

This already contains the basic HTML document structure and links to:

`style.css`

and:

`script.js`

Preserve those connections.

Add the application's interface inside the existing HTML document.

### `style.css`

This file currently contains little or no styling.

Add all required application styling here.

### `script.js`

This file currently contains little or no JavaScript.

Add all application logic here.

Do not place large amounts of CSS or JavaScript directly inside `index.html`.

Keep the responsibilities separated:

`index.html` → structure

`style.css` → appearance

`script.js` → functionality

---

# Project Goal

Turn the starter files into a browser-based image steganography application.

The application should allow a user to hide a text message inside a PNG image using Least Significant Bit, or LSB, steganography.

The application should also be able to recover a previously hidden message from an encoded PNG image.

All processing must happen locally inside the user's browser.

Images and messages must NEVER be uploaded to an external server.

---

# Core Application Structure

Create two primary workflows:

## Encode

The user should be able to:

1. Select or upload a PNG image.
2. Preview the selected image.
3. Enter a secret text message.
4. See the current message length.
5. See whether the selected image has enough capacity for the message.
6. Encode the message into the image using LSB steganography.
7. Preview or confirm the encoded result.
8. Download the newly encoded image as a PNG.
9. Reset the Encode section.

## Decode

The user should be able to:

1. Select or upload a PNG image.
2. Preview the selected image.
3. Click a Decode button.
4. Recover the hidden message.
5. Display the decoded message clearly.
6. Copy the decoded message to the clipboard.
7. Reset the Decode section.

---

# Steganography Implementation

Use browser-native JavaScript and the HTML Canvas API.

The general encoding process should be:

Secret text

→ UTF-8 bytes

→ binary bits

→ image pixel data

→ Least Significant Bit modification

→ encoded PNG

Use `TextEncoder` and `TextDecoder` so Unicode text works correctly.

Examples that should work include:

`Hello World`

`Cybersecurity is awesome!`

`Hello 👋 cybersecurity 🔐`

Do not assume every character is a single byte.

---

# Hidden Data Format

Do not rely only on a terminating character to determine where the message ends.

Use a structured format.

At minimum, store:

1. A small recognizable header or magic value indicating that this image was encoded by the application.
2. The message length.
3. The message bytes.

For example, conceptually:

`MAGIC HEADER | MESSAGE LENGTH | MESSAGE DATA`

The decoder should first check for the expected header.

If the header is not present, display a message such as:

`No valid hidden message was detected in this image.`

This prevents the decoder from displaying random garbage when a normal PNG is uploaded.

---

# Least Significant Bit Requirements

Use RGB pixel channels for storing hidden bits.

Avoid modifying the alpha channel.

The encoder and decoder must use the exact same method for traversing pixel data.

Make sure the implementation clearly distinguishes between:

- image bytes
- message bytes
- individual bits

Add comments explaining the important parts of the algorithm.

---

# Capacity Checking

Before encoding, calculate whether the selected image can hold the full hidden payload.

The calculation must account for:

- the magic/header data
- message-length metadata
- the UTF-8 encoded message bytes

If the message is too large, do not attempt to encode it.

Display a clear message explaining that a larger image or shorter message is required.

If possible, show useful information such as:

`Estimated capacity: 4,210 bytes`

or:

`Message uses 38% of available capacity`

Keep this beginner-friendly.

---

# PNG Requirement

The encoded image must be exported as PNG.

Use:

`image/png`

when generating the output.

Do not convert the encoded image to JPEG.

LSB steganography depends on exact pixel values, and lossy image compression may destroy the hidden information.

---

# Error Handling

Handle these situations gracefully:

- no image selected
- unsupported file type
- empty message
- message too large for the selected image
- decoding a normal image with no hidden data
- malformed or corrupted hidden data
- invalid message length
- image-loading errors
- clipboard-copy failure

Display errors and status messages inside the application.

Do not rely only on `alert()`.

---

# User Interface

Keep the initial design intentionally simple.

This is the base application and will be redesigned later using Prompt 2.

Create a clean interface containing:

- application title
- short explanation of steganography
- privacy notice
- Encode section
- Decode section
- image upload controls
- image previews
- secret-message textarea
- character count
- capacity information
- Encode button
- Download button
- Decode button
- decoded-message output
- Copy button
- Reset buttons
- clear success and error messages

Make the layout responsive enough to work on laptops and smaller screens.

Do not create an elaborate theme yet.

---

# Privacy Requirements

Display a short privacy statement such as:

`All image processing happens locally in your browser. Your images and messages are never uploaded.`

Do not make any network requests.

Do not use analytics.

Do not use external APIs.

Do not store secret messages or uploaded images in:

- localStorage
- sessionStorage
- cookies
- IndexedDB

Keep sensitive data in memory only for the current session.

---

# Code Quality

Keep the code understandable for students who may be new to programming.

Use descriptive functions such as:

`loadImage()`

`encodeMessage()`

`decodeMessage()`

`calculateCapacity()`

`downloadEncodedImage()`

`resetEncodeSection()`

The exact names may differ, but keep functionality organized.

Avoid one enormous function containing the entire application.

Add useful comments explaining:

- what LSB means
- how the Canvas API exposes pixel data
- how text becomes UTF-8 bytes
- how bytes become individual bits
- how the metadata/header works
- how bits are written into RGB values
- how decoding reconstructs bytes
- why PNG is used

Do not add unnecessary abstraction that makes the code harder for beginners to understand.

---

# Preserve the Starter Project

Because this is an existing starter project:

- edit the existing `index.html`
- edit the existing `style.css`
- edit the existing `script.js`
- preserve the links between them
- do not create a replacement project
- do not create a framework-based application
- do not move the project into another folder structure
- do not introduce configuration files

If the starter files already contain comments, keep useful workshop comments unless they interfere with the completed application.

---

# Testing Requirements

Before considering the implementation complete, review the code against these tests:

## Test 1

Encode:

`Hello World`

Download the generated PNG.

Upload that PNG to the Decode section.

The exact message should be recovered.

## Test 2

Encode:

`Hello 👋 cybersecurity 🔐`

The exact Unicode message should be recovered.

## Test 3

Attempt to encode an empty message.

A clear error should appear.

## Test 4

Attempt to decode a normal PNG that has never been encoded.

The application should report that no valid hidden message was found.

It should not output random text.

## Test 5

Attempt to store a message larger than the image capacity.

The application should reject it before modifying the image.

## Test 6

Encode a message, download the PNG, close/reopen or reselect the downloaded file, and decode it.

The message should still be recoverable.

---

# Final Review

Before finishing, confirm that:

- the project still consists of the existing three core files
- `index.html` works when opened directly
- no Node.js is used
- no npm is used
- no packages are required
- no framework was introduced
- no server is required
- encoding works
- decoding works
- Unicode works
- the output remains PNG
- normal PNG files do not produce random decoded text
- images and messages remain local
- the code is readable for beginners

---

# How to Respond

Modify the existing starter files.

Return the completed contents of:

1. `index.html`
2. `style.css`
3. `script.js`

Clearly label each file so I know what content belongs where.

Do not create any additional setup files.

Do not provide npm or Node.js commands.

At the end, give a short explanation of:

- how the LSB implementation works
- how the application's header and message-length format works
- how to test the project

For running the application, the only required instruction should be:

**Open `index.html` in a modern web browser.**
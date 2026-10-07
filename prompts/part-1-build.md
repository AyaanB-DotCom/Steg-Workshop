You are building a beginner-friendly cybersecurity project for a student workshop.

Create a complete browser-based image steganography application using only:

- HTML
- CSS
- Vanilla JavaScript

## Critical Technology Constraint

This project must NOT use Node.js in any form.

Do NOT use:

- Node.js
- npm
- npx
- yarn
- pnpm
- package.json
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

Do not generate any Node.js setup instructions.

Do not tell the user to run commands such as:

`npm install`

`npm run dev`

`npx ...`

`node ...`

The finished application must require ZERO package installation and ZERO command-line setup.

It must work by simply opening `index.html` in a modern web browser.

## Goal

Build a web application that allows a user to hide a text message inside a PNG image using Least Significant Bit (LSB) steganography and later recover that message from the encoded image.

All processing must happen locally in the user's browser.

Images and messages must NEVER be uploaded or sent to any external server.

## Required Files

Create exactly these three files:

`index.html`

`style.css`

`script.js`

Do not create:

- `package.json`
- `package-lock.json`
- `node_modules`
- configuration files
- server files
- build scripts

Keep the code organized, readable, and beginner-friendly.

## Core Features

The application must have two main sections:

### Encode

Allow the user to:

1. Upload a PNG image.
2. Preview the uploaded image.
3. Enter a secret text message.
4. See the number of characters in the message.
5. Encode the message into the image using Least Significant Bit steganography.
6. Download the newly encoded image as a PNG file.
7. Reset the Encode section.

Use the browser's built-in HTML Canvas API to access and modify image pixel data.

Before encoding, determine whether the uploaded image has enough capacity to store the message.

If the message is too large for the selected image, display a clear error instead of attempting to encode it.

### Decode

Allow the user to:

1. Upload a PNG image that may contain a hidden message.
2. Preview the uploaded image.
3. Click a Decode button.
4. Recover and display the hidden message.
5. Copy the decoded message to the clipboard.
6. Reset the Decode section.

If no valid hidden message is detected, display a clear and user-friendly message instead of producing random characters.

## Steganography Requirements

Use Least Significant Bit steganography.

Convert the user's text into bytes and then binary data.

Store the hidden data inside the least significant bits of the image's pixel color values.

Do not modify the alpha channel unless necessary.

Create a reliable method for determining where the hidden message ends.

Prefer storing the message length in the image before the message data instead of relying only on a special terminating character.

Make sure the encoder and decoder use the exact same format.

Support normal text as well as Unicode characters such as:

- emojis
- accented characters
- non-English characters

Use browser-native APIs such as `TextEncoder` and `TextDecoder` where appropriate.

The encoded image must be exported as PNG.

Do not convert the image to JPEG because lossy compression can destroy hidden LSB data.

## Error Handling

The application should gracefully handle:

- no image selected
- wrong file type
- empty message
- image too small for the message
- invalid encoded image
- image containing no recognizable hidden message
- corrupted hidden data
- unexpectedly large messages

Errors should appear inside the interface and should not rely only on browser alert boxes.

## Interface

Keep the initial visual design intentionally simple because it will be customized later in the workshop.

The page should include:

- application title
- short explanation of what steganography is
- Encode section
- Decode section
- file upload controls
- image previews
- message input
- Encode button
- Decode button
- Download button
- Copy Message button
- Reset buttons
- clear status and error messages

Use a clean, modern layout that works well on both desktop and smaller screens.

Do not make the visual design overly elaborate yet.

This is the base version that students will customize later.

## Security and Privacy

Clearly display a short notice explaining:

"All processing happens locally in your browser. Your images and messages are never uploaded."

Do not make any network requests.

Do not use analytics.

Do not use third-party APIs.

Do not store the user's images or secret messages in localStorage, cookies, or any persistent browser storage.

## Code Quality

Write code that a beginner can reasonably follow.

Use:

- descriptive function names
- meaningful variable names
- comments around important logic
- separate functions for encoding and decoding
- separate functions for file handling and UI updates

Avoid putting the entire application inside one massive function.

Add comments specifically explaining:

- how text becomes bytes
- how bytes become bits
- what the Least Significant Bit is
- how image pixel data is modified
- how message length is stored
- how the decoder reconstructs the message

## Testing

Before considering the project complete, verify that the logic should correctly handle:

1. A simple message such as:
   `Hello World`

2. A message containing punctuation.

3. A Unicode message such as:
   `Hello 👋 cybersecurity 🔐`

4. An image that is too small.

5. An empty message.

6. Trying to decode an image that contains no hidden message.

7. Encoding an image, downloading it, reopening the downloaded PNG, and successfully decoding the original message.

## Final Constraints

This must remain a static browser project.

Do NOT use Node.js.

Do NOT use npm.

Do NOT use any package manager.

Do NOT use any build process.

Do NOT use a local development server as a requirement.

Do NOT generate terminal commands for setup.

A student should be able to:

1. Create the three files.
2. Paste in the generated code.
3. Double-click `index.html`.
4. Use the application immediately in their browser.

## Final Output

Provide the complete code for:

1. `index.html`
2. `style.css`
3. `script.js`

Clearly separate each file.

After the code, briefly explain:

- how the steganography implementation works
- how the message length is stored
- how to run the project
- how to test that encoding and decoding work correctly

For the "how to run" section, the instructions should simply tell the user to open `index.html` in a modern browser.

Do not provide any Node.js, npm, server, or package-installation instructions.

Do not redesign or personalize the app beyond a basic clean interface. Customization will happen in the next stage of the workshop.
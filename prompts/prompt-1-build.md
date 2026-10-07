You are helping me build a beginner-friendly cybersecurity project from scratch.

I currently have an empty project folder.

Create a complete browser-based image steganography application inside this folder.

Create exactly these three required files:

`index.html`

`style.css`

`script.js`

The application must use only:

- HTML
- CSS
- Vanilla JavaScript
- Built-in browser APIs

## CRITICAL REQUIREMENT

This project must NOT use Node.js in any form.

Do NOT use or create:

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

Do NOT require any terminal commands.

Do NOT require a development server.

Do NOT provide instructions such as:

`npm install`

`npm run dev`

`npx ...`

`node ...`

The finished project must work by simply opening:

`index.html`

in a modern web browser.

---

# Project Goal

Build a browser-based image steganography application that allows a user to hide text inside a PNG image using Least Significant Bit (LSB) steganography and later recover that hidden text.

Everything must run locally inside the browser.

Images and secret messages must never be uploaded to an external server.

---

# File Structure

Create:

`index.html`

Use this file for the structure and content of the application.

`style.css`

Use this file for all application styling.

`script.js`

Use this file for the application's JavaScript and steganography logic.

Make sure `index.html` correctly links to both `style.css` and `script.js`.

Do not place the entire project inside one HTML file.

---

# Encode Feature

Create an Encode section that allows the user to:

1. Upload a PNG image.
2. Preview the selected image.
3. Enter a secret text message.
4. See the current character count.
5. See the approximate available capacity of the image.
6. Encode the secret message into the image using LSB steganography.
7. Download the encoded image as a new PNG.
8. Reset the Encode section.

Before encoding, verify that the image has enough capacity to contain the complete hidden message.

If the image is too small, show a clear error.

---

# Decode Feature

Create a Decode section that allows the user to:

1. Upload an encoded PNG image.
2. Preview the image.
3. Click a Decode button.
4. Recover the hidden text.
5. Display the recovered message clearly.
6. Copy the recovered message to the clipboard.
7. Reset the Decode section.

If the uploaded image does not contain a valid message created by this application, display:

`No valid hidden message was detected in this image.`

Do not display random characters.

---

# Steganography Implementation

Use the browser's built-in HTML Canvas API to access the image's pixel data.

Use Least Significant Bit steganography.

Conceptually:

Secret Message
→ UTF-8 Bytes
→ Individual Bits
→ RGB Pixel Values
→ Encoded PNG

Use `TextEncoder` and `TextDecoder` so the application correctly supports Unicode.

For example, this should work:

`Hello 👋 cybersecurity 🔐`

Use RGB color channels to store data.

Avoid modifying the alpha channel.

The encoder and decoder must traverse the pixel data using the exact same method.

---

# Hidden Message Format

Use a structured hidden-data format instead of relying only on a terminating character.

Store:

1. A recognizable magic header.
2. The length of the secret message in bytes.
3. The UTF-8 message bytes.

Conceptually:

`MAGIC HEADER | MESSAGE LENGTH | MESSAGE DATA`

The decoder must first check for the expected magic header.

If the header is missing or invalid, treat the image as not containing a valid hidden message.

Validate the stored message length before attempting to decode it.

---

# Capacity Checking

Calculate the available storage capacity based on the number of RGB channels available for LSB storage.

Remember that the hidden payload includes:

- magic header
- length metadata
- message bytes

Do not attempt to encode a message if the image does not have enough capacity.

Display useful capacity information in a beginner-friendly way.

For example:

`Available Capacity: 4.2 KB`

or:

`Message uses 35% of available capacity`

---

# PNG Requirement

The encoded image must be downloaded as a PNG.

Use:

`image/png`

when exporting the Canvas.

Do NOT export the encoded image as JPEG.

Lossy compression can alter pixel values and destroy hidden LSB information.

---

# Error Handling

Gracefully handle:

- no image selected
- non-PNG files
- empty messages
- messages that exceed image capacity
- image-loading failures
- normal images with no hidden message
- corrupted hidden data
- impossible or invalid stored message lengths
- clipboard-copy failure

Display feedback inside the interface.

Do not rely only on browser `alert()` messages.

---

# Interface

Create a clean, simple starter interface.

Include:

- project title
- brief explanation of steganography
- Encode section
- Decode section
- PNG upload controls
- image previews
- secret-message text area
- character counter
- capacity indicator
- Encode button
- Download button
- Decode button
- decoded-message display
- Copy button
- Reset buttons
- status messages
- error messages

Keep the initial design intentionally simple.

Do NOT create an extremely elaborate visual theme because I will customize the design in the next stage of the workshop.

Make the interface responsive and usable on laptops and reasonably narrow browser windows.

---

# Privacy

Display this message somewhere in the interface:

`All processing happens locally in your browser. Your images and messages are never uploaded.`

Do not:

- make network requests
- use analytics
- use external APIs
- upload images
- upload messages
- create accounts
- use cloud storage

Do not store uploaded images or secret messages in persistent browser storage such as:

- localStorage
- sessionStorage
- cookies
- IndexedDB

---

# Code Quality

This project is being used by students, including beginners.

Keep the code readable.

Use descriptive function names.

Separate responsibilities into reasonable functions for tasks such as:

- loading images
- calculating capacity
- converting data
- encoding messages
- decoding messages
- downloading images
- updating the interface
- resetting sections

Add comments explaining the important concepts.

In particular, explain:

- what a Least Significant Bit is
- how Canvas exposes RGB pixel values
- how text becomes UTF-8 bytes
- how bytes become bits
- how bits are stored in RGB values
- how the magic header works
- how the message length is stored
- how decoding reconstructs the original text

Do not over-engineer the application.

---

# Testing

Before considering the application complete, review the implementation against these tests.

### Test 1

Encode:

`Hello World`

Download the PNG.

Upload the downloaded PNG into the Decode section.

The application should recover:

`Hello World`

### Test 2

Encode:

`Hello 👋 cybersecurity 🔐`

The exact Unicode message should be recovered.

### Test 3

Try encoding an empty message.

The application should show an error.

### Test 4

Try decoding a normal PNG that has never been encoded.

The application should report that no valid hidden message was detected.

### Test 5

Try storing more data than an image can contain.

The application should reject the operation before modifying the image.

### Test 6

Encode a message, download the resulting PNG, reopen that file later, and decode it.

The hidden message should remain recoverable.

---

# Final Requirements

Before finishing, confirm that:

- `index.html` exists
- `style.css` exists
- `script.js` exists
- the three files are correctly connected
- opening `index.html` directly runs the application
- no Node.js is used
- no npm is used
- no package manager is required
- no frameworks are used
- no backend exists
- no server is required
- no external dependencies are required
- Encode works
- Decode works
- Unicode works
- PNG download works
- capacity validation works
- invalid images are handled correctly
- all processing remains local

Create the three files directly inside my project folder.

Do not just describe what the code should look like. Implement the application.

When finished, briefly explain what you created and tell me to test the application by opening `index.html` in my browser.
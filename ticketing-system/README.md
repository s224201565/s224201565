# Ticketing System — house party tickets

A single-page web app for running the guest list at a house party: create a party, issue a ticket per guest, send it, and check it at the door.

## Features

- **Parties:** name, address, start time, guest limit, entry fee and host name, with live counts of tickets issued, guests checked in and spots left.
- **Tickets:** each guest gets a random 6-character code (ambiguous characters such as `0/O` and `1/I` are excluded), drawn as a shareable PNG ticket with a QR code. Tiers are General, VIP, Plus-one and Crew.
- **Sharing:** sends the ticket image through the device share sheet (e.g. WhatsApp), or copies a ready-made message.
- **Door check:** scan the QR with the camera or type the code. Scanning uses the browser's native `BarcodeDetector` where available and falls back to a bundled JavaScript decoder (jsQR) everywhere else, so it works on desktop browsers too. The app shows whether the ticket is valid, already used or cancelled, and marks it used on entry, so a copied ticket is refused the second time.
- **Cancelling:** the host can void a ticket so it is refused at the door.
- Light and dark themes, works at phone width, accessible focus states.

## Tech

- Plain HTML, CSS and JavaScript in one file (`index.html`), no build step.
- QR generation: [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (MIT) inlined into the page and drawn directly onto the ticket canvas, so QR codes render with no external dependency (works offline).
- QR scanning: [jsQR](https://github.com/cozmo/jsQR) (Apache-2.0), bundled as `jsQR.min.js`, decodes camera frames when the browser has no native `BarcodeDetector`. Fonts: Bricolage Grotesque and DM Mono from Google Fonts.
- Storage: when hosted as a Claude artifact it uses the artifact's shared database, so the host and door crew see the same list live. Anywhere else it falls back to `localStorage`, which keeps data on that one device only.

## Run it

Serve the folder with any static host (e.g. GitHub Pages) so the whole app — including the `jsQR.min.js` scanner file — loads together. Camera scanning needs the page served over HTTPS (GitHub Pages qualifies) and camera permission; if the camera is unavailable, type the code instead. Opening `index.html` on its own still works for issuing and sharing tickets.

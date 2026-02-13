# Privacy Shield

Privacy Shield is a privacy-first web app that uses on-device face detection to spot unauthorized viewers and instantly protect your screen. When someone else looks at your display, the app can blur the UI, show a bold warning overlay, and play an alert—while keeping all face data on your device.

## Why it’s different
- **On-device only**: No face images or embeddings are sent to a server.
- **Instant protection**: Blurs content and blocks interaction the moment a stranger appears.
- **Owner verification**: Long‑press dismiss to prevent quick bypass by a peeker.
- **Tunable sensitivity**: Adjust detection confidence to fit your environment.

## Key features
- **Face registration**: Register your face once and authorize yourself locally.
- **Real-time detection**: Continuous monitoring with live face count and overlays.
- **Privacy alert**: Warning overlay + optional sound + vibration (mobile).
- **Background mode**: Wake Lock support to keep monitoring while minimized.
- **PWA-ready**: Installable and cached for quick launches.

## How it works (high level)
1. Load face detection/recognition models in the browser.
2. Capture live camera frames with `getUserMedia`.
3. Compare detected faces to the locally registered face descriptor.
4. Trigger privacy mode if any unauthorized face is present.

## Privacy notes
- All face descriptors are stored **locally** in your browser storage.
- No analytics, no uploads, no server-side processing.

## Run locally
1. Start a static server in the project folder (for example):
	- `python -m http.server 8000`
2. Open `http://localhost:8000` in your browser.
3. Register your face, then enable Privacy Protection.

## PWA behavior
- The app includes a Web App Manifest and a service worker for caching.
- You can install it from the browser’s “Install App” prompt.

## Tech stack
- HTML + JavaScript (vanilla)
- Tailwind CSS
- face-api.js
- Service Worker + Web App Manifest

## Ideal use cases
- Working in shared spaces (cafés, offices, classrooms)
- Protecting sensitive content during screen sharing
- Quick privacy guard on mobile

## Hashtags
#privacy #security #face-recognition #computer-vision #pwa #webapp #javascript #tailwindcss #privacytech #ondevice

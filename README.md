# Wigglegram Maker (3D Stereoscopic GIF Tool)

Access the app: https://hilyafesmia.github.io/Wigglegram-Maker/

A client-side web application to create stabilized 3D "Wigglegram" GIFs from burst series.

Designed specifically for analog 3D camera users (Nishika N8000, Nimslo 3D, Reto 3D, Kalimar), this tool solves the tedious process of manually aligning scanned film frames in Photoshop.

## Features
- Automatically picks the middle frame as the geometric anchor to minimize distortion.
- Two Alignment Modes:
 - Auto-Detect (AI): Uses face-api.js to detect faces and align images automatically.
 - Manual Pinning (Film Friendly): A robust fallback for grainy/noisy film scans. Simply click the nose on each frame to align perfectly when AI fails.
- Uses a static background composition strategy. If aligning an image leaves a blank gap on the edge, the background layer fills it in, preventing flashing white artifacts.
- Automatically sequences frames (1 → 2 → 3 → 4 → 3 → 2) for smooth stereoscopic motion.
- 100% Client-Side. No server uploads. All processing happens in your browser for maximum privacy and speed.

## Tech Stack
- HTML5 / CSS3 / Vanilla JavaScript
- face-api.js: For browser-based facial landmark detection.
- gif.js: For rendering and encoding the final GIF binary.

## How to Use
- Upload Images: Select your 4 scanned .JPG files (e.g., Scan_23.jpg, Scan_24.jpg...). The app sorts them alphanumerically.
- Alignment:
 - The app will try to detect faces in the reference image.
 - If AI works: Click the face you want to stabilize.
 - If AI fails (Grain/Noise): Switch to "Manual Mode" and click the nose tip on each image sequentially.
- Preview & Download: The app generates a boomerang GIF. You can preview the result and download it immediately.

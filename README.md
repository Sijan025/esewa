# 🛡️ AI-Powered Real-Time KYC Document Quality Detection

A highly responsive, modern web prototype for real-time Know Your Customer (KYC) identity document validation. Built to run entirely in the browser using plain HTML, CSS, and JavaScript without needing a backend.

![Preview](https://img.shields.io/badge/UI-Neon_Glassmorphism-00f0ff?style=flat-square)
![Stack](https://img.shields.io/badge/Stack-HTML5_|_CSS3_|_Vanilla_JS-0d1117?style=flat-square)
![OCR](https://img.shields.io/badge/OCR-Tesseract.js-00ff66?style=flat-square)

## ✨ Features

- **Futuristic AI Aesthetic**: Features a premium dark-mode UI with glassmorphism and glowing neon accents.
- **Client-Side Image Processing**: Leverages the browser's native `Canvas API` to run fast heuristic algorithms on live camera feeds.
- **Real-Time Quality Checks**:
  - **Sharpness/Blur Analysis**: Calculates Laplacian variance approximations to ensure the image is in focus.
  - **Glare Detection**: Analyzes pixel brightness thresholds to warn against reflective hotspots.
  - **Framing & Alignment**: Detects edges to ensure all four corners of the document are visible within the bounding box.
- **On-Device OCR**: Integrates **Tesseract.js** to extract text directly from the captured image and verifies if it matches the user's registered name.

## 🚀 Getting Started

Since this prototype relies entirely on client-side JavaScript, there are no dependencies to install or servers to run!

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/kyc-document-scanner.git
   ```
2. Navigate to the project folder.
3. Open `kyc.html` directly in any modern web browser.
   *(Note: Camera access might require the file to be served over `localhost` or `https` depending on your browser's security policies. If the camera doesn't start, use a simple local server like `npx serve` or VS Code Live Server).*

## 💡 How It Works

1. **Registration**: The user enters their registered full name and selects an ID type.
2. **Live Capture**: The UI overlays a dynamic neon bounding box. The Canvas API samples frames at 60fps to calculate blur, glare, and framing. 
3. **Validation & Extraction**: Once the image passes all quality thresholds, the capture button unlocks. Upon capture, Tesseract.js runs OCR on the image to read the text.
4. **Name Matching**: The extracted text is parsed, and the system verifies if the user's registered name is physically present on the document.

## 🛠️ Tech Stack

- **HTML5 & CSS3**: Custom styles, responsive flexbox/grid layouts, and advanced CSS variables for the neon themes.
- **Vanilla JavaScript (ES6+)**: Core application logic and media stream handling.
- **Canvas API**: For pixel-by-pixel image processing heuristics.
- **Tesseract.js**: For offline, browser-based Optical Character Recognition (OCR).

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

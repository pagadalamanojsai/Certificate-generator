# Automated Certificate Generator

Welcome to the **Automated Certificate Generator**, a lightweight, client‑side web app that turns HTML, CSS, and JavaScript into beautifully styled, PDF certificates at the click of a button. Perfect for educators, HR teams, event organizers, and anyone who needs to issue certificates quickly and professionally.

---

## 🚀 Features

* **Fully client‑side**
  No backend required—runs entirely in the browser with [html2canvas](https://html2canvas.hertzen.com/) and [jsPDF](https://github.com/parallax/jsPDF).

* **Live preview**
  Instantly see your changes in the on‑page certificate canvas before downloading.

* **Custom fields**

  * Recipient name
  * Program or course name
  * Duration dates

* **Auto‑generated ID**
  Unique six‑digit ID number on each certificate.

* **Dynamic date stamp**
  Automatically inserts today’s date (in the user’s locale format).

* **Stylish design**

  * Elegant typography (Playfair Display, Cinzel, Italianno)
  * Customizable background template and gold seal
  * Centered official stamp, signature, and seal for authenticity

* **One‑click PDF download**
  Generates a high‑resolution, 1000 × 700 px PDF suitable for printing or emailing.

---

## 📂 Project Structure

```
certificate-generator/
├── assets/                # Background, stamp, seal, and logo images
│   ├── CERTIFICATE-2.png
│   ├── stamp.png
│   └── GreatHireLogo-preview.png
├── certificate.html             # Main HTML + inline CSS + JS, which is (index.html)
├── README.md              # This file
└── package.json           # (Optional) for dependency versions if you later add npm scripts
```

---

## 💻 Getting Started

### Prerequisites

* A modern web browser (Chrome, Firefox, Safari, Edge)
* \[Optional] Node.js & npm if you want to serve via `http-server`

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/pagadalamanojsai/Certificate-generator.git
   cd Certificate-generator
   ```

2. **Serve the files**

   * **Option A: Local HTTP server** (recommended to avoid CORS issues)

     ```bash
     # Using Python 3
     python -m http.server 8000

     # Or using npm
     npm install -g http-server
     http-server . -p 8000
     ```

   * **Option B: Open directly** (may cause canvas/CORS errors in some browsers)

     ```bash
     open index.html
     ```

3. **Open in browser**
   Navigate to `http://localhost:8000` (or your path) and start customizing!

---

## 🎨 Customization

* **Background template**: Swap out `assets/CERTIFICATE-2.png` for your own design. Ensure it’s 1000 × 700 px for best results.
* **Fonts**: Edit the `<link>` tags in the `<head>` to include or change Google Fonts.
* **Seal & Stamp**: Replace `assets/gold-seal.png` and `assets/stamp.png` with your organization’s logos.
* **Signature**: Update `assets/image.png` with your authorized signatory’s signature.
* **Text & Layout**: Tweak the CSS under the `.certificate-container` and `.certificate-content` classes to reposition or restyle elements.

---

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests:

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/my-cool-feature`)
3. Commit your changes (`git commit -m "Add my cool feature"`)
4. Push to the branch (`git push origin feature/my-cool-feature`)
5. Open a Pull Request

Please follow standard GitHub flow and ensure any new code is well-documented.

---

## 🛠️ Troubleshooting

* **Blank PDF or missing images**: Be sure to serve over HTTP with CORS enabled (`useCORS: true` in `html2canvas`).
* **Fonts not loading**: Check your internet connection or font URL; you can also self-host fonts.
* **Misaligned elements**: Inspect the CSS positioning rules and adjust `left`, `top`, margins, or container dimensions.

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use, modify, and distribute!

---

> Crafted by [pagadalamanojsai](https://github.com/pagadalamanojsai)

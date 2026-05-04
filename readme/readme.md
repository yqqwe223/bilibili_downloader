# 🎬 Bilibili Video Parser

> A lightweight, fast, and versatile tool for extracting video content from Bilibili (Educational & Research Version)

[🌐 Online Demo](https://twittervideodownloaderx.com/bilibili_downloader) • [📝 Usage Guide](#-usage-guide) • [❓ FAQ](#-faq)

---

## 📋 Project Overview

This project is a web-based video parsing tool designed to safely extract media resource metadata from public videos on the Bilibili platform (哔哩哔哩), while providing options for format conversion and local saving. No client software installation or account registration required—use it directly through your browser.

> ⚠️ **Important Notice**: This tool is intended exclusively for personal learning, technical research, and use within reasonable limits. Please comply with the [Bilibili Community Guidelines](https://www.bilibili.com/blackboard/protocol.html), the 《Copyright Law of the People's Republic of China》, and other applicable regulations. Respect creators' work; do not use downloaded content for commercial purposes or to infringe upon others' rights.

---

## ✨ Key Features

- 🔗 **Link Parsing**: Supports standard Bilibili video/animation URLs; automatically detects episodes and available resolution options
- 📥 **Multi-Format Export**:
  - Original video stream (supports public resolutions like 1080P/720P, etc.)
  - Audio extraction → MP3 format (convenient for offline listening to lectures/music)
  - Video clip → Animated GIF conversion (ideal for creating memes/educational demos)
- 🌍 **Multilingual Interface**: Supports English, Chinese, Japanese, Korean, and more
- 📱 **Cross-Platform Compatibility**: Works seamlessly on Chrome / Firefox / Safari / Edge; optimized experience for mobile devices and tablets
- 🔒 **Privacy-First**: No Bilibili account login required, no personal data collection; fully anonymous parsing process
- ⚡ **Fast Processing**: Analysis completes in an average of 5-10 seconds; supports concurrent requests and batch processing

---

## 🚀 Quick Start

### Online Usage (Recommended)
1. Visit [https://twittervideodownloaderx.com/bilibili_downloader](https://twittervideodownloaderx.com/bilibili_downloader)
2. Copy the target video link (e.g., `https://www.bilibili.com/video/BV1xx411c7mD`)
3. Paste the link into the input field → Click the 「Parse」button
4. Select your desired resolution and format → Save the file following your browser's instructions

### Local Deployment (For Developers)
```bash
# Clone the repository
git clone https://github.com/your-repo/bili-video-parser.git

# Install dependencies
cd bili-video-parser && npm install

# Configure environment variables (optional)
cp .env.example .env

# Start the development server
npm run dev
```

> 💡 Note: This project uses a Node.js + Express architecture. Please refer to `/docs/DEPLOY.md` for detailed deployment documentation.

---

## 🛠 Technology Stack

| Module | Technologies Used |
|--------|------------------|
| Frontend | Vue 3 + TypeScript + Vite |
| Backend | Node.js + Express + Axios |
| Video Processing | ffmpeg.wasm (lightweight client-side conversion) |
| Proxy Forwarding | Cloudflare Workers / Custom Middleware |
| Internationalization | vue-i18n + JSON Language Packs |

---

## 📚 Usage Guide

### Basic Workflow
```
1. Obtain the video link
   └─ Open the target video on Bilibili → Copy the URL from your browser's address bar

2. Submit parsing request
   └─ Paste the link into the tool's input field → Click 「Start Parsing」

3. Select output configuration
   ├─ 🎬 Download Video: Choose resolution (360P/720P/1080P, etc. - public options only)
   ├─ 🎵 Extract Audio: Generate MP3 file (ideal for offline lecture/music listening)
   └─ 🎞 Generate GIF: Create animation from specified time range (recommended: ≤15 seconds)

4. Save the file
   └─ Resource opens in a new tab → Right-click/menu → 「Save As」
```

### Mobile Usage Tips
- iOS Safari: Share button → 「Save to Files」
- Android Chrome: Long-press video preview → 「Download video」
- If video auto-plays: Tap `⋮` in the player's top-right corner → Select 「Download」

---

## ❓ Frequently Asked Questions

**Q: Where are downloaded files saved?**  
A: Files are saved to the download folder configured in your browser. You can check or modify this path in your browser settings.

**Q: Can I parse member-exclusive or login-required content?**  
A: No. This tool only works with videos set to public and respects the access permissions of the original content.

**Q: Does conversion reduce image/audio quality?**  
A: Video downloads maintain the original bitrate of the selected resolution. MP3 uses standard 128kbps encoding. GIF optimizes frame rate based on duration to balance file size and smoothness.

**Q: Is download history or cache stored?**  
A: No. All resources are transmitted directly to the user's device via a temporary proxy; the server does not store any requests or media files.

**Q: What should I do if parsing fails?**  
A: Please verify: ① The link points to a valid public video ② Your internet connection is stable ③ Try using a different browser. If the issue persists, feel free to report it via an Issue.

---

## ⚖️ Compliance & Disclaimer

- This tool **does not bypass or violate any technical protection measures** of the platform; it only obtains metadata through public interfaces
- Users are responsible for ensuring their use complies with local laws and the platform's terms of service
- Recommended use cases: Personal learning archives, educational demonstrations, reference materials for content creation... always within the framework of fair use
- If you discover content that may infringe upon rights, please contact the official channel via [Bilibili's copyright report form](https://www.bilibili.com/blackboard/help.html#copyright)

---

## 🤝 Contributing

We welcome your Pull Requests and Issue reports! Before contributing, please review:
- [Code Standards](/CONTRIBUTING.md)
- [Multilingual Translation Guide](/locales/README.md)
- [Security & Compliance Requirements](/SECURITY.md)

---

## 📄 License

This project is released under the [MIT License](/LICENSE). It may be used freely for educational and research purposes. For commercial use, please carefully verify compliance with applicable legal regulations.

---

> 🌟 If this tool has been helpful to you, please ✨give it a Star! Your support is the greatest motivation for us to continue maintaining and improving this project~

*Last updated: May 2026 | Version: v1.0.0*
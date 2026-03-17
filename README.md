<div align="center">

<br/>

```
 ██████╗  ██████╗ ██╗     ██╗     ██╗███╗   ██╗ █████╗ ████████╗██╗ ██████╗ ███╗   ██╗███████╗
 ██╔══██╗██╔═══██╗██║     ██║     ██║████╗  ██║██╔══██╗╚══██╔══╝██║██╔═══██╗████╗  ██║██╔════╝
 ██████╔╝██║   ██║██║     ██║     ██║██╔██╗ ██║███████║   ██║   ██║██║   ██║██╔██╗ ██║███████╗
 ██╔═══╝ ██║   ██║██║     ██║     ██║██║╚██╗██║██╔══██║   ██║   ██║██║   ██║██║╚██╗██║╚════██║
 ██║     ╚██████╔╝███████╗███████╗██║██║ ╚████║██║  ██║   ██║   ██║╚██████╔╝██║ ╚████║███████║
 ╚═╝      ╚═════╝ ╚══════╝╚══════╝╚═╝╚═╝  ╚═══╝╚═╝  ╚═╝   ╚═╝   ╚═╝ ╚═════╝ ╚═╝  ╚═══╝╚══════╝
```

### A free, open collection of AI-powered tools — built on [Pollinations.ai](https://pollinations.ai)

<br/>

[![Live Demo](https://img.shields.io/badge/Live_Demo-lokiodinson.netlify.app-black?style=for-the-badge&logo=netlify&logoColor=white)](https://lokiodinson.netlify.app/ai)
[![Powered by Pollinations](https://img.shields.io/badge/Powered_by-Pollinations.ai-F0E040?style=for-the-badge)](https://pollinations.ai)
[![Tier](https://img.shields.io/badge/Tier-🌱_Seed-4CAF50?style=for-the-badge)](https://enter.pollinations.ai)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

<br/>

</div>

---

## 🌸 What is Pollinations?

> **No sign-up. No API key required for visitors. Just AI.**

All tools in this repo are powered by **[Pollinations.ai](https://pollinations.ai)** — a free, open-source generative AI platform providing access to image, text, audio, and video models through a simple REST API. No paywalls, no credit cards, no tracking.

---

## 🛠️ Tools

| # | Tool | Description | Model | Live |
|---|------|-------------|-------|------|
| 01 | [📄 Document Translator](#-document-translator) | Translate any text into 20+ languages | Gemini 2.5 Flash-Lite | [→ Open](https://lokiodinson.netlify.app/ai/translator) |
| 02 | [🎙️ Voice Studio](#️-voice-studio) | Convert text to speech with 40+ voices | tts-1 · OpenAI + ElevenLabs | [→ Open](https://lokiodinson.netlify.app/ai/text2audio) |
| 03 | [🌄 Image Studio](#-image-studio) | Generate images with AI-enhanced prompts | zimage + Gemini 2.5 Flash-Lite | [→ Open](https://lokiodinson.netlify.app/ai/text2image) |

<br/>

---

## 📄 Document Translator

**Live →** [lokiodinson.netlify.app/ai/translator](https://lokiodinson.netlify.app/ai/translator)

Paste any document, article, or text and get an instant translation into 20+ languages — preserving tone, formatting, and paragraph structure.

**Features**
- 20 preset language buttons (Arabic, French, Spanish, Chinese, Japanese...)
- Free-text field for any language not in the presets
- Copy-to-clipboard output
- Optional custom API key for higher rate limits
- Zero data storage — nothing is logged or saved

**Model:** `gemini-2.5-flash-lite` via `gen.pollinations.ai/v1/chat/completions`

---

## 🎙️ Voice Studio

**Live →** [lokiodinson.netlify.app/ai/text2audio](https://lokiodinson.netlify.app/ai/text2audio)

Type or paste any text and hear it spoken by a natural AI voice. Choose from 40+ voices split across two providers.

**Features**
- 11 OpenAI voices (Alloy, Echo, Nova, Onyx, Shimmer, Ash, Ballad, Coral, Sage, Verse, Fable)
- 24 ElevenLabs voices (Rachel, Daniel, Charlotte, Josh, Bella...)
- In-browser audio player with seek bar and timer
- Download as MP3
- Animated waveform visualization
- Optional custom API key

**Model:** `tts-1` via `gen.pollinations.ai/v1/audio/speech`

---

## 🌄 Image Studio

**Live →** [lokiodinson.netlify.app/ai/text2image](https://lokiodinson.netlify.app/ai/text2image)

Describe any image and generate it instantly. Uses Gemini to intelligently enhance your prompt before sending it to the image model.

**Features**
- **Prompt Enhancer** — powered by Gemini 2.5 Flash-Lite
  - 5 enhancement modes: Cinematic, Detailed, Artistic, Photorealistic, Minimal
  - Enhanced prompt is editable before generation
- Aspect ratio selector (1:1, 16:9, 9:16, 4:3, 3:2, 21:9)
- Resolution picker (768 / 1024 / 1280px)
- Negative prompt support
- Seed control for reproducible results
- Image history strip (last 4 generations)
- Download generated image
- Optional custom API key

**Models:** `zimage` + `gemini-2.5-flash-lite` via `gen.pollinations.ai`

---

## 🚀 Getting Started

These are plain HTML files — no build step, no dependencies, no npm.

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/pollinations-tools.git

# Open any tool directly in your browser
open ai/translator/index.html
open ai/text2audio/index.html
open ai/text2image/index.html
```

Or deploy instantly to Netlify, Vercel, or GitHub Pages by dropping the files in.

---

## 📁 Project Structure

```
pollinations-tools/
│
├── ai/
│   ├── index.html          ← Tools hub / landing page
│   ├── translator/
│   │   └── index.html      ← Document Translator
│   ├── text2audio/
│   │   └── index.html      ← Voice Studio
│   └── text2image/
│       └── index.html      ← Image Studio
│
├── README.md
└── LICENSE
```

---

## 🔑 API Keys

All tools work **out of the box** with a baked-in publishable key. Visitors can optionally enter their own [Pollinations publishable key](https://enter.pollinations.ai) for better personal rate limits.

| Key Type | Used For | Safe in Frontend? |
|----------|----------|-------------------|
| `pk_...` Publishable | All tools (default) | ✅ Yes |
| `sk_...` Secret | Never used in frontend | ❌ No |

---

## 🤝 Contributing

Want to add a tool? It's easy:

1. Build your tool as a single HTML file
2. Add it to the `ai/` folder
3. Add one entry to the `TOOLS` array in `ai/index.html`:

```js
{
  id: "my-tool",
  title: "My Tool Name",
  desc: "One sentence description.",
  icon: "✨",
  tags: ["Tag1", "Tag2"],
  model: "Model used",
  url: "/ai/my-tool",
  category: "Text",   // Text | Audio | Image | Video
}
```

That's it — the card, filter button, and tool count all update automatically.

---

## ⚡ Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Vanilla HTML + CSS + JavaScript |
| AI Platform | [Pollinations.ai](https://pollinations.ai) |
| Text Model | Gemini 2.5 Flash-Lite |
| Audio Model | tts-1 (OpenAI + ElevenLabs voices) |
| Image Model | zimage |
| Hosting | Netlify |

---

## 📜 License

MIT — free to use, fork, and modify.

---

<div align="center">

Built with ❤️ using **[Pollinations.ai](https://pollinations.ai)**

*Free AI for everyone.*

</div>

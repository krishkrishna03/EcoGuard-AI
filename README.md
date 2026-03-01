# 🌍 EcoGuard AI — Environmental Crisis Chatbot

> An intelligent, deep learning-powered chatbot built to educate, alert, and inspire action on the world's most urgent environmental crises.

![EcoGuard AI](https://img.shields.io/badge/Powered%20By-Claude%20AI-3dff7a?style=for-the-badge&logo=anthropic)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

---

## 📌 Overview

**EcoGuard AI** is a single-file, browser-based chatbot that uses the **Anthropic Claude API** (claude-sonnet-4) to provide real-time, science-based responses about environmental crises. It features a robust multi-layer fallback system to gracefully handle off-topic, harmful, vague, and real-time queries — making it reliable and safe for public deployment.

---

## ✨ Features

### 🤖 AI-Powered Intelligence
- Powered by **Claude Sonnet 4** (Anthropic's deep learning model)
- Expert knowledge across **12+ environmental domains**
- Severity classification: Critical / High / Medium / Low for every response
- Science-based, solutions-focused answers

### 🛡️ Smart Fallback System (4-Layer)

| Layer | Trigger | Response |
|-------|---------|----------|
| 🚫 **Harmful** | Toxic/inappropriate keywords | Blocked instantly, no API call |
| ⚪ **Vague** | Under 4 characters or ambiguous | Asks for clarification |
| 🟣 **Real-time** | "today", "breaking", "latest news" | Caveat + trusted live sources |
| 🔵 **Off-topic** | Sports, cooking, finance etc. | Warm redirect with env. angle |

### 🎨 UI/UX Highlights
- Dark eco-themed interface with animated noise texture & gradient backgrounds
- Live crisis ticker with real global environmental alerts
- Quick-topic chips for instant exploration
- Clickable AI-generated suggestion chips
- Typing indicator with smooth animations
- Fully responsive for mobile and desktop

### 📚 Topics Covered
- 🌡️ Climate Change & Global Warming
- 🦋 Biodiversity Loss & Species Extinction
- 🌊 Ocean Acidification & Marine Pollution
- 💨 Air Quality & Industrial Pollution
- 🌳 Deforestation & Land Degradation
- 💧 Water Scarcity & Freshwater Threats
- 🔥 Wildfire Patterns & Drought Cycles
- ⚡ Renewable Energy & Green Technology
- 🌐 Environmental Policy & International Agreements
- 🧑‍🤝‍🧑 Environmental Justice & Climate Action

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Edge, Safari)
- An [Anthropic API key](https://console.anthropic.com/)

### Option 1 — Use the Live Demo (No Setup Required)

👉 **[Try EcoGuard AI Live → your-deployment-link.netlify.app](https://your-deployment-link.netlify.app)**

Just open the link in any browser and start chatting instantly — no installation, no API key needed.

---

### Option 2 — Run Locally

1. **Download the file**
   
   [⬇️ Download eco-crisis-chatbot.html](https://your-deployment-link.netlify.app/eco-crisis-chatbot.html)
   
   Or save the file directly from your browser: `File → Save Page As`

2. **Open in your browser**
   ```bash
   open eco-crisis-chatbot.html
   # or just double-click the downloaded file
   ```

3. **Start chatting!**
   
   Ask EcoGuard AI anything about our planet's environmental crises — no setup required.

---

## 🏗️ Project Structure

```
ecoguard-ai/
│
├── eco-crisis-chatbot.html     # Main application (single-file)
├── README.md                   # This file
└── LICENSE                     # MIT License
```

Everything — HTML, CSS, and JavaScript — lives in a single self-contained file for easy deployment and sharing.

---

## 🧠 How It Works

```
User Input
    │
    ▼
┌─────────────────────────────┐
│   Client-Side Intent Check  │  ← Instant, no API call
│   • Harmful? → Block        │
│   • Vague? → Clarify        │
│   • Real-time? → Flag       │
│   • Off-topic? → Redirect   │
└──────────────┬──────────────┘
               │ On-topic or Unknown
               ▼
┌─────────────────────────────┐
│    Anthropic Claude API     │  ← Deep learning model
│    (claude-sonnet-4)        │
│    + System Prompt with     │
│      intent context         │
└──────────────┬──────────────┘
               │
               ▼
┌─────────────────────────────┐
│    Formatted Response       │
│    • Severity badge         │
│    • Markdown rendered      │
│    • Suggestion chips       │
└─────────────────────────────┘
```

---

## 🔧 Configuration

You can customize EcoGuard AI by modifying the constants at the top of the `<script>` section:

```javascript
// Add more environmental keywords for better intent detection
const ENV_KEYWORDS = [ 'climate', 'carbon', ... ];

// Add more off-topic keywords to catch
const OFFTOPIC_KEYWORDS = [ 'recipe', 'sport', ... ];

// Adjust the AI system prompt for different tones or focus areas
const SYSTEM_PROMPT = `You are EcoGuard AI...`;
```

---

## 🌐 Live Deployment

👉 **[EcoGuard AI is live → your-deployment-link.netlify.app](https://your-deployment-link.netlify.app)**

The app is deployed as a single HTML file — no server, no build step, no dependencies. Just open the URL and it works.

### Host Your Own Copy

The single HTML file can be deployed to any static host in under 2 minutes:

| Platform | How |
|----------|-----|
| **Netlify** | Drag & drop the HTML file at [netlify.com/drop](https://app.netlify.com/drop) |
| **Vercel** | `npx vercel eco-crisis-chatbot.html` |
| **GitHub Pages** | Upload to a repo → Settings → Pages → Deploy from branch |
| **AWS S3** | Upload file → Enable static website hosting |

### Production Note
The live deployment uses a secure backend proxy to protect the API key. If self-hosting for public use, set up a simple proxy endpoint instead of exposing your key client-side:

```javascript
// Replace the direct Anthropic call with your own endpoint:
fetch('/api/chat', { method: 'POST', body: JSON.stringify({ messages }) })
```

---

## 📊 Severity Classification System

| Badge | Level | Description |
|-------|-------|-------------|
| 🔴 CRITICAL THREAT | Extinction / Collapse risk | Irreversible, catastrophic scenarios |
| 🟠 HIGH CONCERN | Active crisis / Emergency | Severe, urgent environmental threats |
| 🟡 MODERATE RISK | Ongoing concern | Declining trends, manageable risks |
| 🟢 INFORMATIONAL | General knowledge | Educational, solution-focused content |
| 🔵 OUT OF SCOPE | Off-topic redirect | Non-environmental queries |
| 🟣 LIVE DATA CAVEAT | Real-time data request | Knowledge cutoff acknowledged |
| ⚪ CLARIFICATION | Vague input | Bot requesting more detail |
| 🚫 BLOCKED | Harmful content | Immediately rejected |

---

## 🤝 Contributing

To contribute, download the HTML file from the live deployment, make your changes locally, then open a discussion or share your fork link.

Contributions are welcome! Here are some ways to help:

1. **Expand the keyword lists** for better intent detection
2. **Add new topic chips** for emerging environmental issues
3. **Improve the UI** for better accessibility
4. **Add multilingual support** for global reach
5. **Create a backend proxy** for secure API key handling

---

## 🌱 Why This Matters

> "We are the first generation to feel the impact of climate change and the last generation that can do something about it." — Barack Obama

Environmental crises are accelerating. EcoGuard AI exists to make environmental education **accessible, immediate, and actionable** — meeting people where they are and guiding them toward understanding and action.

**Current planetary stats our AI tracks:**
- 🌡️ +1.2°C above pre-industrial temperature
- 💨 421 ppm CO₂ in the atmosphere
- 🌿 40% of natural habitats lost
- 🌊 8 million tonnes of plastic entering oceans annually

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- **Anthropic** for the Claude AI API
- **IPCC, NASA, NOAA** for environmental data referenced in AI responses
- **Google Fonts** (Syne + Space Mono) for typography
- The global community of environmental scientists and activists

---

<p align="center">Built with 💚 for our planet · <a href="https://your-deployment-link.netlify.app">🌍 Live Demo</a> · <a href="https://console.anthropic.com">Anthropic API</a></p>

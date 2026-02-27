# 📚 LearnBoard

> **Watch · Think · Note · Remember**

A powerful single-file web application built for taking notes while watching YouTube videos. No installation required — just open the HTML file in your browser!

---

## 🚀 Quick Start

```bash
# Simply double-click the file or drag it into your browser
learnboard.html
```

No server. No installation. No internet required (except for loading videos) — **runs directly in the browser.**

---

## ✨ Features

### 🎬 Video Player
- Paste a YouTube URL → press **LOAD**
- Supports both `youtube.com/watch?v=...` and `youtu.be/...` formats
- Uses privacy-enhanced embed (`youtube-nocookie.com`)
- **Error 153 handling** — when embed is blocked:
  - Video thumbnail is displayed
  - **"Open on YouTube"** button appears
  - Retry option available
- **↗ YT** button in footer — open video on YouTube anytime
- Last loaded video URL is auto-saved (localStorage)

### 📝 Notepad
- **Handwritten font** (Caveat) — feels like writing on paper
- **Ruled lines** + red margin line — actual notebook look
- **Multi-tab** support — manage multiple notes at once
  - Add / delete tabs
  - Rename tabs
- **Auto-save** — 500ms debounce, persisted in localStorage
- Live **word count** and **line count**
- **Download options:**
  - 📄 `.TXT` — download current note as plain text
  - 📕 `PDF` — download current note as a styled dark-themed PDF
  - 📄 `ALL TXT` — download all notes combined as a text file
  - 📕 `ALL PDF` — download all notes as a single PDF (one note per page)
- **CLEAR** button — clears current note (with confirmation)

### ⏱️ Study Timer
- Built-in timer in the topbar
- Start / Pause / Reset controls
- Displays in hh:mm:ss format (for sessions over 1 hour)

### 🎭 Splash Screen (Opening Animation)
An animated intro screen shown when the app opens:
- Custom **Shivmudra logo** — animates in with scale + rotation
- **3 spinning rings** orbiting the logo
- **Orange glow pulse** effect
- "LEARNBOARD" title fade-in
- Loading progress bar
- Floating orange spark particles
- Auto-dismisses after 2.6 seconds

---

## 🖥️ Layout

```
┌──────────────────────────────────────────────────────────────┐
│  [LOGO]  LearnBoard  │  YouTube URL input  │  LOAD  │  TIMER │
├───────────────────────────┬──────────────────────────────────┤
│                           │  📄 NOTEPAD    ALL PDF  ALL TXT  │
│   YouTube Video           ├──────────────────────────────────┤
│   Player                  │  [Tab 1]  [Tab 2]  [+]           │
│                           ├──────────────────────────────────┤
│   (16:9 embed)            │                                  │
│                           │   Handwritten notes              │
│                           │   with ruled lines               │
│                           │                                  │
├───────────────────────────┼──────────────────────────────────┤
│  ● youtube.com/...  ↗YT   │  ● saved  12 words  PDF TXT CLEAR│
└───────────────────────────┴──────────────────────────────────┘
```

---

## 💾 Data Storage

All data is saved in the **browser's localStorage**:

| Key | Content |
|-----|---------|
| `learnboard_video_v2` | Last loaded YouTube URL |
| `learnboard_notes_v3` | All tabs and notes (JSON) |

> ⚠️ Clearing browser cache will erase saved data. **Export important notes as PDF or TXT.**

---

## 📤 Export Formats

### TXT Export
```
=== Note 1 ===

Your notes here...


=== Note 2 ===

More notes here...
```

### PDF Export
- Matches the app's dark theme
- Orange accent bar + LEARNBOARD branding at the top
- Bold note title + divider line
- Body text with automatic word-wrapping
- Multi-page support for long notes
- Page numbers in the footer

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **React 18** (CDN) | UI components |
| **Babel Standalone** | JSX transpilation in browser |
| **jsPDF 2.5.1** | PDF generation |
| **JetBrains Mono** | Monospace / code font |
| **Rajdhani** | Heading font |
| **Caveat** | Handwritten notepad font |
| **localStorage** | Data persistence |

---

## ⚡ Browser Support

| Browser | Status |
|---------|--------|
| Chrome / Edge | ✅ Full support |
| Firefox | ✅ Full support |
| Safari | ✅ Full support |
| Mobile Chrome | ✅ Mostly supported |

---

## 📋 Keyboard Tips

| Shortcut | Action |
|----------|--------|
| `Ctrl + A` | Select all text in the notepad |
| `Tab` | Indent text in the textarea |
| `Enter` (in URL input) | Load the YouTube video |

---

## 🎨 Design

| Property | Value |
|----------|-------|
| **Theme** | Dark hacker aesthetic |
| **Primary color** | `#f97316` (Orange) |
| **Background** | `#0a0b0d` (Near black) |
| **Notepad ink** | `#e8dcc8` (Warm cream) |
| **Effect** | Subtle CRT scanline texture |

---

## 🔧 Customization

Open `learnboard.html` and modify the `:root` CSS variables:

```css
:root {
  --orange: #f97316;   /* Primary accent color */
  --bg:     #0a0b0d;   /* Background color */
  --text:   #d4d8e0;   /* Default text color */
}
```

---

## 📁 File Structure

```
learnboard.html    ← The entire application (single file!)
README.md          ← This document
```

---

## ⚠️ YouTube Embed Limitations

Some YouTube videos cannot be embedded due to:
- The creator has disabled embedding
- Age-restricted content
- Regional restrictions
- Copyright claims

**Solution:** Use the **"Open on YouTube"** button — the video will open in a new tab while you continue taking notes in LearnBoard.

---

## 🤝 Contributing

Since this is a single HTML file project:

1. Open `learnboard.html` in any text editor
2. Make your changes inside the `<script type="text/babel">` block
3. Test by opening in a browser
4. Submit a pull request

---

## 📜 License

MIT License — free to use, modify, and distribute.

---

## 👨‍💻 Built With

Generated with **Claude by Anthropic** — complete application in a single HTML file.

---

*LearnBoard — Because learning isn't just watching, it's writing too.* ✍️

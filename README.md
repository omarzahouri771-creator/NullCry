<div align="center">

<img src="./assets/logo.png" alt="NullCry Logo" width="140"/>

# NullCry

**Build complete, production-ready software projects with AI — from a single prompt to a downloadable ZIP.**

[![Website](https://img.shields.io/badge/website-nullcry.com-blueviolet)](https://nullcry.com)
[![Twitter](https://img.shields.io/badge/X-@nullcryai-black)](https://x.com/nullcryai)


</div>

---

## 📖 Overview

**NullCry V4** is an AI-powered project generation platform that turns natural-language descriptions (and even screenshots or wireframes) into complete, structured, and functional codebases. It plans the file architecture, generates production-quality code file-by-file, validates and self-corrects the output, and packages everything into a ready-to-download ZIP — no boilerplate, no manual setup.

It supports building brand-new projects from scratch **and** editing existing codebases (upload a folder or a ZIP and describe the changes you want).

## 🖼️ Screenshots

<div align="center">
<img src="./assets/screenshot-1.png" alt="NullCry main interface" width="720"/>
<br/><br/>
<img src="./assets/screenshot-2.png" alt="NullCry build pipeline in action" width="720"/>
</div>

## ✨ Key Features

### 🧠 Dual AI Engine — Fast & Deep Thinking
- **Fast Mode** — generates each file directly for quick, efficient results.
- **Deep Thinking Mode** — a multi-stage pipeline that first produces a full **architectural blueprint** (data flow, dependency graph, integration map, security/UX standards), then generates each file against that blueprint, and finally **validates and auto-fixes** every file (including a client-side syntax/bracket checker) before it's marked complete.

### 🎯 Multiple Project Types
Choose the target stack before generating:
- Web App (HTML/CSS/JS)
- PHP + MySQL Web App
- Python App (Flask/Django/Script)
- Node.js REST API (Express)
- React App
- SQL Database (schema + queries)
- Custom (any language/stack)

### 🖥️ Language-Aware Code Generation
NullCry auto-detects the target language of every file (JS, TS, JSX/TSX, Python, PHP, Java, Kotlin, Go, Rust, C/C++, SQL, HTML/CSS, Shell, JSON, and more) and applies a dedicated **senior-engineer expert prompt** per language — enforcing best practices like strict typing, PSR-12, PEP 8, prepared statements, idiomatic error handling, and memory safety.

### 🗂️ Two Modes: New Project & Edit Existing Project
- **New** — describe your idea → AI plans the file structure → review/edit the plan → build.
- **Edit** — upload a project folder or a `.zip` → describe the changes → AI analyzes existing files, decides what to rebuild/keep/create/delete → applies surgical, dependency-safe edits while preserving working functionality.

### 🖼️ Visual Understanding (Vision Input)
Attach screenshots, UI mockups, or wireframes directly in the chat input — the AI analyzes layout, spacing, typography, colors, and components to guide code generation (available in both Fast and Deep Thinking modes).

### 🔌 Flexible API Routing
Two ways to power generation, switchable at any time from the topbar:
- **Token-based** — use NullCry's built-in DeepSeek token packages (purchasable via PayPal).
- **Bring Your Own Key** — plug in your own API key for OpenAI (GPT), xAI (Grok), Google (Gemini), or DeepSeek. Keys are stored locally in the browser only.

### 📊 Live Build Pipeline
Real-time progress bar, per-file streaming log (build/validate/fix/error events), and a **Stop** control to cancel an in-progress build at any time.

### 🗃️ Interactive File Explorer & Export
Generated projects open in a VS Code–style folder tree with syntax-highlighted code preview, one-click copy, and a **Download ZIP** button that packages the full project (plus an auto-generated `README.md`) for instant use.

### 👤 Accounts, Projects & Payments
- Google Sign-In authentication
- Per-user token balance synced with a backend (Firebase-ready)
- Saved project history in the sidebar, reloadable anytime
- Secure PayPal checkout for token package purchases

### 📱 Fully Responsive
A native-feeling mobile layout with a slide-in sidebar, adaptive topbar, and touch-optimized modals.

## 🚀 How It Works

1. **Choose a project type** (Web, PHP, Python, Node.js, React, SQL, or Custom)
2. **Describe your project** — optionally attach reference images
3. **Review the AI-generated file plan** (add, remove, or edit entries)
4. **Build** — watch the live pipeline generate, validate, and fix each file
5. **Explore & download** — browse the file tree and export a complete ZIP

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla JS, HTML5, CSS3 (custom design system) |
| Icons | Phosphor Icons |
| Fonts | Geist / Geist Mono |
| ZIP handling | JSZip |
| Auth & Data | Google Identity Services, Firebase Firestore |
| Payments | PayPal SDK |
| AI Providers | DeepSeek (native), OpenAI, xAI (Grok), Google Gemini |

## 📌 Roadmap

- [ ] Additional project templates (mobile apps, browser extensions)
- [ ] Direct GitHub repository push after generation
- [ ] Team/workspace collaboration
- [ ] More granular per-file regeneration in Edit mode

## 🤝 Contributing

Contributions, issues, and feature requests are welcome — feel free to open an Issue or a Pull Request.

## 📬 Contact

- 🌐 Website: [nullcry.com](https://nullcry.com)
- 🐦 X: [@nullcryai](https://x.com/nullcryai)
- 📸 Instagram: [nullcryai](https://instagram.com/nullcryai)

## 📄 License

Released under the [MIT License](./LICENSE).

---

<div align="center">
Made with ❤️ by the NullCry team
</div>

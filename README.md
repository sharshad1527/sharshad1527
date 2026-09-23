## Systems Builder & Automation Engineer

**Bridging the gap between AI-assisted development and core computer science fundamentals.** I am a self-taught developer focused on **Python architecture**, **headless automation**, and **application security**.. I learn by reverse-engineering software, optimizing complex systems, and building desktop tools from the ground up to solve my own bottlenecks..

---

### Current Execution

* **Flow NextGen (Live on Chrome Web Store):** Maintaining and scaling my browser automation extension for Google Flow.. Focus is on user feedback, bug fixing, and adding requested workflow features..
* **H.I.V.E NextGen (Paused):** Custom PySide6 video editor development is on hold for now..
* **Studies & Security Labs:** Completing 12th NIOS (Computer Science) while spending time on web application security, ethical hacking labs, and low-level system design..

---

### Engineering History

#### Phase 4: The Systems Architect (2025–2026)

**Flow NextGen: Bulk Queue & Workflow Automation Extension (Jun–Sep 2026)**  
* **Chrome Web Store:** [Install Extension](https://chromewebstore.google.com/detail/flow-nextgen/jolnapkhihjecpgideikgpkhgfkbeagp) · **Website:** [flownextgen.netlify.app](https://flownextgen.netlify.app)

* **Multi-Context Architecture:** Built an MV3 Chrome extension using React and TypeScript.. The Sidepanel UI, Background Service Worker, and Page scripts talk through a custom typed JSON bridge so state stays synced without race conditions..
* **Protocol Reverse-Engineering:** Google Flow has no public API, and automating the UI directly was too brittle.. I used the Network tab, Console probing, and proxy tools to reverse-engineer their private batch RPC requests and streaming response chunks.. Built a custom parser so the extension talks directly to Google's backend to dispatch prompts and extract direct signed media URLs..
* **Bulk Queue & Auto-Download:** Built an automated task engine that can queue 100+ prompts, poll async generation states in the background, and auto-download finished images and videos with custom naming templates so users don't have to save files one by one..
* **Security & Quotas:** Tested the app from an attacker's perspective and found a vulnerability where a user could bypass generation limits by sending database updates straight from DevTools console.. I locked it down by writing custom Supabase Row Level Security (RLS) policies and atomic database functions so quota checks are enforced entirely on the backend.. First time applying practical web security to my own live product.

**Autonomous Media Pipeline & H.A.V.E. Pro (Jan–May 2026)**

* **Impact:** Replaced a 20+ hours manual video production workflow with a Python-based pipeline, reducing human input strictly to curation and quality control..
* **Network Mocking:** Built a local Python mock-server to intercept a DOM-automator's API.. Ensures a stable, rate-limit-free bulk image-generation workflow without paying for expensive tiers.
* **Data-to-Render Engine:** Engineered a PySide6 visual bridge (*ExpressoSort*) to map raw assets to script lines via CSV.. This feeds *H.A.V.E. Pro*—a custom matrix using local Whisper NLP for audio-syncing and multi-threaded FFmpeg for final assembly..
* ➡️ **[Read the full Systems Architecture Deep-Dive](HAVE_AUTONOMOUS_PIPELINE.md)**

**Adversarial AI Test Harness & Middleware (Archived Lab · Mar 2026)**

* **The Experiment:** An exploratory weekend lab where I guided AI to build a lightweight Python middleware.. I wanted to study how open-weight LLMs handle guardrails, but got tired of manually testing prompts and tweaking parameters by hand, so I designed the pipeline to automate the whole loop..
* **Deflection Logic:** Designed Regex heuristics (`RefusalDetector` & `RelevanceChecker`) to catch when a model dodges a question or gives fake generic advice instead of a direct answer..
* **Adaptive Retry Engine:** Set up multi-pass prompt reframing and temperature variance on retries, letting the script run structured batch tests unattended without manual intervention..

**Daily Selfie (v1 & v2) (2025)**

* **v1:** Built initial prototype using standard Tkinter..
* **v2:** Re-architected in PySide6.. Developed a custom theming engine that parses JSON exports from Google's Material Theme Builder to dynamically apply comprehensive Material Design themes across the desktop application.. It utilizes dark modes with juicy orange and black/dark gray, or coffee themes..

#### Phase 3: Software Deconstruction (2024)
**Reverse Engineering & Protocol Analysis**
* Deconstructed compiled software to understand execution flow, memory management, and licensing protocols..
* Studied how application restrictions are built and bypassed to build a strong foundational understanding of application security.. This helped me a lot in Phase 4 when deconstructing other extensions..

#### Phase 2: Linux Infrastructure (2023)
**OS Deployment & Web Security**
* Developed a unified bash script to automate the complex installation, initialization, and status monitoring of Waydroid (Android container layer on Linux)..
* Conducted self-directed studies into Web Application Security, utilizing tools like Burp Suite to understand OWASP Top 10 vulnerabilities..
* Extensive deep-dives into Linux environments, package management, and system customization..

#### Phase 1: The App & OS Tinkerer (2019–2022)
**Early Software Development**
* **Desktop Automation:** Built a custom Python voice assistant integrating `pyautogui` for desktop GUI automation and OpenCV for facial recognition..
* **Android Chat Application:** Developed a fully functional chat application featuring live voice/video calls and message reactions, utilizing Java and Firebase.. This was long ago when I started my developer journey..

---

### Certifications & Practical Labs

* **TryHackMe Advent of Cyber 2025** — Completed 24 hands-on cybersecurity challenges across web exploitation, network forensics, and defensive security (Certificate ID: `THM-2BGHUQRNUB`).
  
---

### Technical Arsenal

* **Languages:** Python, TypeScript (Orchestrated), Bash, Java (Historical)
* **Frameworks & Libraries:** React, PySide6, Zustand, PyAV, OpenCV, FFmpeg
* **Architecture:** Chrome Extension MV3, CDP (Chrome DevTools Protocol), Network Protocol Interception, GUI Automation, Reverse Engineering
* **Environments:** Windows, Linux

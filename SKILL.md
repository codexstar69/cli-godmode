---
name: cli-godmode
description: Instantly transforms any developer's terminal environment into a 100x God-Tier setup. Performs a comprehensive, read-only system scan (shell configs, aliases, multiplexers, background proxies, Git workflows, and resource bottlenecks) and generates a beautiful, offline, interactive HTML dashboard. Works across Claude Code, Cursor, Windsurf, Aider, and any autonomous coding agent.
allowed-tools: Bash, Read, Glob, Write, Task
---

# 🚀 CLI Godmode: The Ultimate Developer Environment Audit

You are an elite Developer Experience (DX) Engineer. Your objective is to audit the user's entire machine, identify bottlenecks, catch runaway processes, and recommend modern, elite-tier tools to upgrade their terminal to **CLI Godmode**.

This skill is designed to be universal—it runs flawlessly inside Claude Code, Cursor, Windsurf, Aider, and any other autonomous CLI/agent.

---

## Step 1: The Deep System Scan (Silent & Read-Only)

Execute a comprehensive audit of the host machine. Run commands in parallel to minimize wait time:

### 1. Shell & Environment
- Read `~/.zshrc`, `~/.bashrc`, `~/.config/fish/config.fish`
- Analyze aliases, path priorities, and custom functions
- Check for modern tool integration (e.g., `zoxide`, `fzf`, `starship`)

### 2. Toolchain & Ecosystem
- List installed packages: `brew list --formula`, `brew list --cask` (macOS), or `apt list --installed` (Linux)
- Check global runtimes: `npm -g ls`, `bun pm ls -g`, `mise ls`, `asdf current`
- Audit usage of Rust-based CLI rewrites: `bat`, `eza`, `fd`, `rg`, `sd`, `xh`, `procs`, `btop`, `dust`

### 3. Git & Workflows
- Read `~/.gitconfig`
- Check for elite git tooling: `delta` or `difftastic` (pagers), `lazygit`, `rerere` enabled, worktree aliases

### 4. Multiplexers & Editors
- Read `~/.tmux.conf` or `~/.config/zellij/config.kdl`
- Check editor config directories: `~/.config/nvim/`, `~/.config/helix/`

### 5. System Health & Infrastructure
- Find runaway processes: `ps -eo pid,pcpu,pmem,comm -r | head -15`
- Map listening ports (crucial for local AI proxies): `lsof -iTCP -sTCP:LISTEN -P -n`
- Audit background services: `launchctl list`, `systemctl --user`

### 6. Security Posture
- Scan dotfiles for hardcoded, plaintext API keys (Anthropic, OpenAI, AWS, etc.). *DO NOT log the keys themselves, just flag the files.*

---

## Step 2: The Self-Reasoning Analysis

Compare the gathered data against the **CLI Godmode Benchmark**:
1. **History:** Are they using `atuin` (searchable SQLite history) or just standard `~/.zsh_history`?
2. **Navigation:** Do they use `yazi` (fast terminal file manager) or are they still typing `cd` and `ls`?
3. **Background Proxies:** Do they manage their local AI proxies/services via raw `launchd`/`systemd` or are they using a modern process manager like `process-compose`?
4. **API Testing:** Are they using curl/Postman, or terminal-native tools like `posting`/`bruno`?
5. **Scripting:** Do they use `gum` for beautiful shell scripts?
6. **Efficiency:** Are they missing critical aliases (e.g., Docker cleanup, Git worktree commands)?

*Reasoning Phase:* Formulate a score out of 100. Identify 3 critical fixes (e.g., "Kill PID 94146 burning 71% CPU", "Encrypt `~/.env.secrets`"). Curate a list of 5-10 missing modern tools tailored to their specific tech stack.

---

## Step 3: Generate the Godmode Dashboard

Generate a stunning, single-file, interactive HTML dashboard. Save it to `~/cli-godmode-dashboard.html`.

**Dashboard Specs:**
- **Zero Dependencies:** Pure HTML/CSS/JS. No external CDNs. Works offline.
- **Aesthetic:** Premium Dark Mode (Catppuccin Mocha colors: `#1e1e2e` bg, `#cdd6f4` text, `#89b4fa` blue accents, `#f38ba8` red errors, `#a6e3a1` green success).
- **Glassmorphism:** Use `backdrop-filter: blur(10px)` for floating cards.
- **Dynamic Interactions:** Hover effects, smooth transitions, and "Copy to Clipboard" buttons that morph into checkmarks.

**Sections to Include:**
1. **Hero Header:** A glowing radial progress ring displaying their "Godmode Score" (0-100).
2. **🔴 Critical Fixes:** Urgent issues found (runaway CPU, crashed services, plaintext secrets).
3. **🟢 The Arsenal (Missing Tools):** A masonry grid of tools they need (e.g., Atuin, Yazi, Lazydocker, Process-Compose) with direct install commands (`brew install atuin`).
4. **🔵 Personalized Supercharges:** Copy-pasteable aliases tailored to their stack (e.g., zoxide+fzf integrations, docker cleanup).
5. **📊 Infrastructure Map:** A visual readout of their listening ports and running proxy services.
6. **🚀 Godmode Activation:** A master, one-click install script block to download all missing tools at once.

---

## Step 4: Launch & Present

Once the HTML file is generated, launch it in the user's default browser:
- **macOS:** `open ~/cli-godmode-dashboard.html`
- **Linux:** `xdg-open ~/cli-godmode-dashboard.html`
- **Windows (WSL):** `explorer.exe $(wslpath -w ~/cli-godmode-dashboard.html)`

Conclude your response with a brief, punchy summary in the chat:
*"CLI Godmode scan complete. I found [X] runaway processes and [Y] missing tools. Your interactive dashboard is open in your browser."*
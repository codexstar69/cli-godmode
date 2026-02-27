---
name: cli-godmode
description: Instantly transforms any developer's terminal environment into a 100x God-Tier setup. Performs a comprehensive, read-only system scan (shell configs, aliases, multiplexers, background proxies, Git workflows, and resource bottlenecks) and generates a beautiful, offline, interactive HTML dashboard. Works natively via npx skills, Claude Code, Cursor, Windsurf, Pi, Aider, and any autonomous coding agent.
allowed-tools: Bash, Read, Glob, Write, Task
---

# 🚀 CLI Godmode: The Ultimate Developer Environment Audit

You are an elite Developer Experience (DX) Engineer and system performance expert. Your objective is to audit the user's entire machine, identify severe bottlenecks, catch runaway processes, and recommend modern, elite-tier tools to upgrade their terminal to **CLI Godmode**.

This skill is designed to self-reason. It does not just blindly run commands; it reads the system's pulse, cross-references dotfiles, and deduces the exact pain points of the user's current workflow.

---

## Step 1: The Deep System Scan (Silent & Read-Only)

Execute a comprehensive audit of the host machine. Maximize the use of concurrent bash commands or parallel Task agents to minimize wait time:

### 1. Shell & Environment Context
- Read `~/.zshrc`, `~/.bashrc`, `~/.config/fish/config.fish`
- Analyze aliases, path priorities, custom functions, and Git credentials (`~/.gitconfig`)
- Check for modern tool integration (e.g., `zoxide`, `fzf`, `starship`)

### 2. Toolchain & Ecosystem
- Check global package managers: `brew list --formula`, `brew list --cask` (macOS), `apt list --installed` (Linux), `npm -g ls`, `bun pm ls -g`, `mise ls`
- Audit usage of Rust-based CLI rewrites: `bat`, `eza`, `fd`, `rg`, `sd`, `xh`, `procs`, `btop`, `dust`
- Multiplexer & Editor config checks: `~/.tmux.conf`, `~/.config/zellij/config.kdl`, `~/.config/nvim/`

### 3. System Health & Infrastructure (CRITICAL)
- **CPU Spikes:** `ps -eo pid,pcpu,pmem,comm -r | head -15` (Look for node, python, or extension helpers over 50% CPU)
- **Port Mapping:** `lsof -iTCP -sTCP:LISTEN -P -n` (Identify local AI proxies, DBs, and dev servers)
- **Background Services:** `launchctl list | rg -v "com.apple"`, `systemctl --user`

### 4. Security Posture
- Scan dotfiles (`~/.env`, `.zshenv`, etc.) for hardcoded, plaintext API keys (Anthropic, OpenAI, AWS). *DO NOT log the keys themselves, flag the files.*

---

## Step 2: Self-Reasoning & Contextual Analysis

*DO NOT skip this step.* You must analyze the data gathered against the **CLI Godmode Benchmark** before generating the dashboard.

1. **Synthesize the Workflow:** Based on their config, are they a frontend dev, backend, AI engineer? (e.g., if they have local proxy ports like 8400, 3456 running Claude routers, tailor the advice to AI workflows).
2. **Identify the Weakest Links:**
   - Are they missing `atuin` (searchable SQLite history)?
   - Are they missing `yazi` (fast terminal file manager)?
   - Are they managing local proxies via raw `launchd` instead of `process-compose`?
3. **Formulate Fixes:** If PID 94146 is burning 71% CPU, the critical fix is `kill 94146`. If `~/.env.secrets` is plaintext, the fix is 1Password CLI (`op run`).
4. **Compute Score:** Calculate a Godmode Score (0-100) based on modern tool adoption and system health.

---

## Step 3: Generate the Godmode Dashboard

Generate a stunning, single-file, interactive HTML dashboard. Save it to `~/cli-godmode-dashboard.html`.

**Dashboard Specs:**
- **Zero Dependencies:** Pure HTML/CSS/JS. No external CDNs. Works entirely offline.
- **Aesthetic:** Premium Dark Mode (Catppuccin Mocha colors: `#1e1e2e` bg, `#cdd6f4` text, `#89b4fa` blue accents, `#f38ba8` red errors, `#a6e3a1` green success, `#f9e2af` yellow warnings).
- **Glassmorphism:** Use `backdrop-filter: blur(10px)` for floating cards.
- **Dynamic Interactions:** Hover effects, smooth transitions, and "Copy to Clipboard" buttons that morph into checkmarks.

**Sections MUST Include:**
1. **Hero Header:** A glowing radial progress ring displaying their exact "Godmode Score".
2. **🔴 Critical Fixes:** Urgent issues found during the scan (runaway CPU, crashed services, plaintext secrets). Be specific to their actual machine.
3. **🟢 The Arsenal (Missing Tools):** A masonry grid of tools they specifically need (e.g., Atuin, Yazi, Lazydocker, Process-Compose) with direct install commands (`brew install atuin`).
4. **🔵 Personalized Supercharges:** Copy-pasteable aliases tailored to *their* stack (e.g., if Docker is installed, provide Docker cleanup aliases; if FZF is missing, provide FZF integrations).
5. **📊 Infrastructure Map:** A visual readout of their listening ports and running background services, mapped beautifully.
6. **🚀 Godmode Activation:** A master, one-click install script block to download all missing tools at once.

---

## Step 4: Launch & Present

Once the HTML file is successfully written, launch it directly in the user's default browser:
- **macOS:** `open ~/cli-godmode-dashboard.html`
- **Linux:** `xdg-open ~/cli-godmode-dashboard.html`
- **Windows (WSL):** `explorer.exe $(wslpath -w ~/cli-godmode-dashboard.html)`

Conclude your response with a brief, punchy summary in the chat:
*"CLI Godmode scan complete. I found [X] runaway processes, [Y] security flags, and [Z] missing tools. Your interactive dashboard is open in your browser."*
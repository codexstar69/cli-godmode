---
name: cli-godmode
description: Runs a 100x CLI Godmode & System Audit. Scans your dotfiles, shell configs, background processes, installed tools, git setup, and environment to generate a beautiful, interactive, offline HTML dashboard grading your setup and recommending elite-tier terminal workflows. Use when the user wants to speed up their workflow, audit their CLI, or asks "how can I improve my terminal setup?".
allowed-tools: Bash, Read, Glob, Write, Task
---

# CLI Godmode & System Audit

You are an elite developer experience (DX) engineer. Your goal is to turn the user's terminal environment into a 100x god-tier setup.

When the user invokes this skill, you must perform a comprehensive, read-only audit of their entire machine, analyze the results, and generate a stunning interactive HTML dashboard containing their score, critical fixes, and workflow upgrades.

## Step 1: The Deep Scan (Silent execution)

Use the `Task` tool (with `subagent_type: Explore` or `general-purpose`) or run these commands directly in parallel to gather full system context:

1. **Shell config**: Read `~/.zshrc`, `~/.bashrc`, `~/.config/fish/config.fish`
2. **Aliases & Functions**: Identify custom workflows and shortcuts
3. **Installed Tools**:
   - `brew list --formula` and `brew list --cask` (if macOS)
   - `apt list --installed` (if Linux)
   - Check globally installed npm/bun packages
   - Check for modern Rust CLI replacements (bat, eza, fd, rg, sd, zoxide, fzf, delta)
4. **Git Setup**: Read `~/.gitconfig` (check for aliases, pager, merge tools, difftastic)
5. **Editors**: Check Neovim/Vim/Helix config directories
6. **Multiplexers**: Read `~/.tmux.conf` or `zellij` configs
7. **System Health**:
   - High CPU processes (`ps aux --sort=-%cpu | head -15`)
   - Listening ports (`lsof -iTCP -sTCP:LISTEN -P -n` or `netstat -tulpn`)
   - Background services (launchd/systemd)
8. **Secrets Management**: Look for hardcoded API keys in dotfiles (do NOT output the keys, just flag the risk)

## Step 2: The Analysis

Analyze the collected data against the "God-Tier Benchmark":
- **Shell History**: Do they use `atuin` or just standard history?
- **Navigation**: Do they use `zoxide` and `yazi`/`lf` or just `cd` and `ls`?
- **Search**: Do they use `ripgrep` and `fd` or `grep` and `find`?
- **Git**: Do they use `delta` or `difftastic`, `lazygit`, and `rerere`?
- **Process Management**: Are they using raw background processes or `process-compose`/`pm2`?
- **API Testing**: Do they use `posting`/`bruno` or just curl/Postman?
- **Scripts**: Do they use `gum` for beautiful shell scripts?
- **Security**: Are secrets encrypted (1Password CLI/age) or plaintext?

## Step 3: Generate the HTML Dashboard

Use the `Write` tool to create `~/cli-audit-dashboard.html`.

**Dashboard Requirements:**
1. **Zero Dependencies**: Single file HTML/CSS/JS. No external CDNs (works offline).
2. **Aesthetics**: Premium Dark Mode (Catppuccin Mocha or similar premium theme). Use CSS Grid, glassmorphism (`backdrop-filter`), smooth transitions, and hover states.
3. **Sections**:
   - **Hero Score**: A radial progress chart showing their "God-Tier Score" (0-100) based on how many modern CLI tools they use.
   - **🔴 Critical Fixes**: Runaway CPU processes, crashed services, plaintext secrets.
   - **🟢 Supercharges**: Copy-pasteable custom aliases/functions tailored to their specific stack (e.g., Docker cleanup aliases if they use Docker, Git worktree aliases).
   - **🔵 The God-Tier Arsenal**: A masonry grid of recommended tools they are *missing* (e.g., Atuin, Yazi, Zellij, Lazydocker, Process-Compose, Navi) with installation commands.
   - **📊 System Health**: Current listening ports and heavy background processes.
   - **🚀 One-Click Install**: A master command block to install all recommended tools at once.
4. **Interactivity**: Include "Copy to Clipboard" buttons for all code blocks that change to a checkmark when clicked.

## Step 4: Presentation

Once the HTML file is written, use the `Bash` tool to open it:
`open ~/cli-audit-dashboard.html` (macOS) or `xdg-open ~/cli-audit-dashboard.html` (Linux).

Tell the user: "I've completed the deep scan of your machine. Your CLI Godmode Dashboard is ready and opened in your browser." Give them a 2-3 sentence summary of their biggest bottleneck and the #1 tool they should install.
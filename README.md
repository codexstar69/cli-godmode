<div align="center">
  <img src="assets/banner.png" alt="CLI Godmode Banner" width="100%" style="border-radius: 10px; max-height: 300px; object-fit: cover;">

  <h1>🚀 CLI Godmode</h1>
  <p><b>The Ultimate Developer Environment Audit Skill for AI Agents</b></p>

  <a href="#installation">Installation</a> •
  <a href="#how-it-works">How it Works</a> •
  <a href="#supported-agents">Supported Agents</a> •
  <a href="#the-god-tier-stack">The God-Tier Stack</a>
</div>

---

## What is CLI Godmode?

**CLI Godmode** is a powerful skill/plugin designed for autonomous coding agents (Claude Code, Cursor, Windsurf, Aider). It transforms any standard terminal environment into a 100x elite setup.

When invoked, the agent performs a deep, read-only audit of your entire machine—scanning dotfiles, background processes, proxy servers, Git configs, and toolchains. It then generates a stunning, offline, interactive HTML dashboard grading your setup and providing exact, copy-pasteable commands to upgrade your workflow.

### 🔍 What it Catches
- **Runaway CPU Processes:** Finds rogue background tasks burning your battery (like crashed node proxies or runaway extension helpers).
- **Security Risks:** Flags plaintext API keys sitting in `~/.env` or `.zshrc`.
- **Infrastructure Audits:** Maps out all local listening ports and background proxies (crucial for devs running local LLM routing).
- **Missing Modern Tools:** Analyzes your installed tools and compares them against the ultimate 2025 modern CLI benchmark.

## 📸 The Dashboard

The skill generates a zero-dependency, Catppuccin-themed HTML dashboard locally on your machine, featuring:
- Your overall **Godmode Score**
- Urgent **Critical Fixes** (processes to kill, secrets to hide)
- A personalized **Missing Arsenal** grid (e.g., Atuin, Yazi, Lazydocker)
- Custom **Supercharge Aliases** tailored to your exact tech stack
- A **One-Click Master Install** script

---

## ⚡ Installation

This skill is designed to be universal across modern AI CLI tools and IDE agents.

### For Claude Code
Clone the repository into your Claude skills directory:
```bash
git clone https://github.com/codexstar69/cli-godmode.git ~/.claude/skills/cli-godmode
```
*Alternatively, load it directly if using the Anthropic allowlist:*
```bash
claude -p /path/to/cli-godmode
```

### For Cursor / Windsurf / Aider
Simply copy the `SKILL.md` file into your project's `.cursorrules` or global agent instructions, or prompt your agent directly:
*"Read the CLI Godmode instructions from `https://raw.githubusercontent.com/codexstar69/cli-godmode/main/SKILL.md` and execute the audit."*

---

## 🎮 Usage

Simply invoke the skill in your chat prompt:

```text
> /cli-godmode
```

Or use natural language:
- *"Audit my terminal setup"*
- *"Activate CLI godmode"*
- *"Find out why my fans are spinning and speed up my workflow"*

The agent will silently scan your system, crunch the data, generate `~/cli-godmode-dashboard.html`, and pop it open in your default browser.

---

## 🛠️ The God-Tier Stack Benchmark

This skill measures your setup against the modern Rust-based terminal revolution. It looks for the adoption of:
- **[Atuin](https://github.com/atuinsh/atuin):** SQLite-backed, syncable shell history
- **[Yazi](https://github.com/sxyazi/yazi):** Blazing fast terminal file manager
- **[Process-Compose](https://github.com/F1bonacc1/process-compose):** Modern background process management
- **[Eza](https://github.com/eza-community/eza), [Bat](https://github.com/sharkdp/bat), [Ripgrep](https://github.com/BurntSushi/ripgrep):** Modern replacements for `ls`, `cat`, and `grep`
- **[Difftastic](https://github.com/Wilfred/difftastic) & [Lazygit](https://github.com/jesseduffield/lazygit):** Elite git workflows
- **[Gum](https://github.com/charmbracelet/gum):** Beautiful shell scripts

---

## 🔒 Security & Privacy

**CLI Godmode is 100% Read-Only during the scan phase.**
- It reads dotfiles to understand your aliases and tools.
- It runs standard system commands (`ps`, `lsof`, `brew list`) to check health.
- It writes exactly **one** file (`~/cli-godmode-dashboard.html`) to present the results.
- **Zero API keys or secrets are ever exposed** in the generated dashboard or sent to external servers; the script merely flags the file path if it detects plaintext secrets.

---
*Built with ❤️ for devs who want to move at the speed of thought.*
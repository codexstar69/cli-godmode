# God-Tier CLI Audit Skill for Claude Code

Turn your terminal environment into a 100x god-tier setup.

This Claude Code skill performs a deep, comprehensive read-only audit of your entire machine, dotfiles, shell configs, git setup, background processes, and installed tools. It analyzes your workflow against the ultimate modern developer benchmark and generates a stunning, interactive, offline HTML dashboard with your score, critical system fixes, and personalized elite-tier workflow upgrades.

![Dashboard Preview Placeholder](https://via.placeholder.com/800x400/1e1e2e/cdd6f4?text=God-Tier+CLI+Dashboard)

## What it Audits
- **Shell Configs** (zsh, bash, fish, aliases, functions)
- **Modern CLI Adoption** (rg, fd, bat, eza, zoxide, fzf, etc.)
- **Git Workflow** (delta, difftastic, lazygit, rerere)
- **System Health** (Runaway CPU processes, rogue listening ports, crashed background services)
- **Security Risks** (Plaintext API keys in dotfiles)
- **Multiplexers & Editors** (Tmux, Zellij, Neovim)

## What it Recommends
The skill will identify exactly what you are missing to achieve a "God-Tier" setup, recommending tools like:
- **Atuin** (Searchable, SQLite-backed, syncable shell history)
- **Yazi** (Blazing fast terminal file manager)
- **Process-Compose** (Manage background proxy services efficiently)
- **Posting/Bruno** (Modern terminal API testing)
- **Gum** (Beautiful TUI components for your shell scripts)
- **Lazydocker** (TUI for containers)
- ...and highly-customized, copy-pasteable aliases based on your specific stack.

## Installation

Install the skill directly using the Claude Code CLI:

```bash
claude -p /god-tier-cli-audit
```

*Alternatively, if you use the [Anthropic Skills allowlist](https://github.com/anthropics/claude-code):*
```bash
claude mcp add god-tier-cli-audit
```

## Usage

Simply ask Claude to audit your setup:

```
> /god-tier-cli-audit
```

Or just use natural language:
- *"Audit my CLI"*
- *"How can I speed up my terminal workflow?"*
- *"Run the god-tier system scan"*

Claude will silently scan your system, crunch the data, generate the interactive `~/cli-audit-dashboard.html` file, and pop it open in your default browser.

---

### Security Note
This skill is **Read-Only** during the audit phase. It reads your dotfiles to understand your workflow and uses `ps` and `lsof` to check system health. It writes exactly one file (`~/cli-audit-dashboard.html`) to present the results. It will *never* expose your API keys or secrets in the dashboard—it only flags if they are stored insecurely.

Created with ❤️ by [codexstar69](https://github.com/codexstar69) for the Claude Code community.
# Claude Skills Quick Start Guide

Last updated: November 2, 2025

A beginner-friendly guide to getting started with Claude Skills.

> **Note**: This guide has been tested on macOS Sonoma. Steps may vary on other operating systems.

## What are Claude Skills?

Skills let you extend Claude's capabilities for specific tasks. Once created, skills can be:
- Reused across conversations
- Shared with your team
- Used on both Claude Web and Claude Code

## Quick Start

### Claude Web (Easiest)
1. Log into [Claude](https://claude.ai) (requires Pro, Max, Team, or Enterprise)
2. Go to **Settings → Capabilities**, then turn on "Code Execution and File Creation" and "Skills" if needed
3. In a new chat, ask Claude: "Create a skill that [performs this task] for [this purpose]. Ask me questions, one at a time, until you have enough context to create a useful skill."
4. Download the Skill file (zip format) that Claude creates
5. Go back to **Settings → Capabilities**, scroll to the Skills section, and upload the Skill file
6. Turn on your newly-uploaded Skill

### Claude Code
1. Open Terminal on your Mac (press Command + Space, type "Terminal", and press Enter)
2. Install Claude Code: `curl -fsSL https://claude.ai/install.sh | bash`
3. Create a skills folder: `mkdir -p ~/.claude/skills`
4. See the [detailed guide](skills-quick-start.md) for next steps

## Need More Help?

- **Detailed walkthrough**: See [Skills Quick Start Guide](skills-quick-start.md)
- **Official documentation**: [Claude Skills Documentation](https://docs.claude.com/en/docs/claude-code/skills)
- **Claude Code docs**: [docs.claude.com](https://docs.claude.com)

## Common Issues

**Skills not working?**
- Make sure you have Pro, Max, Team, or Enterprise subscription
- Try restarting Claude Code after adding Skills
- Check the [troubleshooting section](skills-quick-start.md#troubleshooting) in the detailed guide

---

**Note**: Skills require a Claude Pro, Max, Team, or Enterprise subscription.

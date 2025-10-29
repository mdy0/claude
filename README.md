# Claude Skills Quick Start Guide

A comprehensive guide to creating, installing, and using custom Skills in Claude for both Claude Web and Claude Code.

## Overview

This repository provides step-by-step instructions for working with Claude Skills - a powerful feature that allows you to extend Claude's capabilities with custom, reusable tools tailored to your specific needs.

**What are Claude Skills?**

Claude Skills are custom tools that you can create to enhance Claude's functionality for specific tasks. Once created, these skills can be:
- Reused across multiple conversations
- Shared with others
- Used on both Claude Web and Claude Code platforms

## Prerequisites

**For Claude Web:**
- Active Claude subscription (Pro, Max, Team, or Enterprise)
- Access to Skills feature in Claude Settings

**For Claude Code:**
- Claude Code version 2.0.22 or later
- Mac OS environment
- Skills directory set up under `.claude`

## Quick Start

For detailed step-by-step instructions, see the [Skills Quick Start Guide](skills-quick-start.md).

### Creating a Skill (Claude Web)

1. **Enable the skill-creator** in Settings → Capabilities
2. **Start a new chat** and prompt:
   ```
   Use #skill-creator to create a skill that [performs this task] for [this purpose]
   ```
3. **Download the generated skill file** (zip format)
4. **Upload to your Claude account** via Settings → Capabilities → Upload Skill

### Using Skills

**On Claude Web:**
```
Use the [skill-name] skill to do [task] using these inputs: [your inputs]
```
or
```
Use #your-skill-name to do [task] using these inputs: [your inputs]
```

**On Claude Code:**
```
use the [skillname] skill to [perform this task]
```

## Installation

### Claude Web Setup

1. Log into [Claude](https://claude.ai)
2. Navigate to **Settings → Capabilities**
3. Enable:
   - "Code Execution and File Creation"
   - "Skills"
   - "skill-creator" skill (scroll down to find it)

### Claude Code Setup

1. **Install Claude Code** (version 2.0.22+):
   ```bash
   curl -fsSL https://claude.ai/install.sh | bash
   ```

2. **Create skills directory**:
   ```bash
   mkdir -p ~/.claude/skills
   ```

3. **Add your skill**:
   - Copy the skill zip file to `~/.claude/skills/`
   - Unzip the file
   - Delete the zip file (Claude uses the unzipped files)
   - Restart Claude Code

## Troubleshooting

### Claude Code Issues

**Problem**: Skills not working with npm-installed Claude Code

**Solution**: Uninstall the npm version and use the native installer:
```bash
# Uninstall npm version
npm uninstall -g @anthropic-ai/claude-code

# Install native version
curl -fsSL https://claude.ai/install.sh | bash
```

### Common Issues

- **Skills not appearing**: Ensure you've restarted Claude Code after adding new skills
- **Feature not available**: Verify you have a Pro, Max, Team, or Enterprise subscription
- **Version compatibility**: Confirm Claude Code is version 2.0.22 or later

## Documentation

- [Skills Quick Start Guide](skills-quick-start.md) - Detailed walkthrough for both platforms

## Platform Support

| Feature | Claude Web | Claude Code |
|---------|------------|-------------|
| Create Skills | ✓ | - |
| Use Skills | ✓ | ✓ |
| Share Skills | ✓ | ✓ |
| Skill Creator | ✓ | - |

## Contributing

This is a documentation repository for Claude Skills. For feature requests or bug reports related to Claude itself, please contact Anthropic support.

## License

Documentation provided as-is for Claude users.

## Additional Resources

- [Claude Documentation](https://docs.claude.ai)
- [Anthropic Website](https://anthropic.com)

---

**Note**: Skills functionality requires Claude Pro, Max, Team, or Enterprise subscription. The skill-creator tool is available on Claude Web to help you build custom skills through an interactive conversation.

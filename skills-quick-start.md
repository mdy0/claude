Last updated: November 2, 2025

> **Note**: The Claude Code section of this guide has been tested on macOS Sonoma. Steps may vary on other operating systems.

## On Claude Web

**One-time configuration**:
- Log into Claude (must be Pro, Max, Team, or Enterprise for this feature to work).
- Go to Settings → Capabilities
- In the screen that appears\
   -- turn on "Code Execution and File Creation"\
   -- turn on "Skills" if needed.

**To create a Skill file**
- Start a new chat
- **Prompt**: Create a skill that [performs this task] for [this purpose]. Ask me questions, one at a time, until you have enough context to create a useful skill.

At the end of the chat conversation, Claude will give you a Skill file (in zip format) that you can download (and share).

**To add your new Skill to your Claude Web account**
- Go back to Claude Settings → Capabilities
- Scroll down to the Skills section and hit the "Upload Skill" button.
- Upload the Skill file you created in the previous step.
- Turn on the newly-uploaded Skill.

**To use the Skill**
- **In a new chat, simply ask Claude naturally**: Skills are automatically invoked when your request matches the Skill's description. For example: "Analyze this data" or "Generate a report from these inputs" - Claude will automatically use the relevant Skill if appropriate.
- **Note**: You can also explicitly invoke a Skill by name if you wish: "Use the [skill-name] skill to do [task] using these inputs: [inputs]."

**Understanding the Skill Structure**

A `skills` folder consists of a directory containing:
- **Required**: a `SKILL.md` file with prescribed frontmatter
- **Optional**: Supporting files (scripts, templates, reference documents)

The entire `skills` folder can be zipped for uploading to Claude.ai. In Claude Code, you'll work with the unzipped directory structure.


## On Claude Code

To get the newly-created Skill working in Claude Code:

**One time setup**
- **Install the latest version of Claude Code**.
- **Understand skill directory types**:

```
Your computer:
├── ~/.claude/skills/            # Personal skills (all projects)
│   └── my-personal-skill/
│       └── SKILL.md
│
├── ~/projects/ecommerce-app/    # Project A
│   └── .claude/skills/          # Project-specific skills
│       └── ecommerce-helper/
│           └── SKILL.md
│
└── ~/projects/blog-site/        # Project B
    └── .claude/skills/          # Different project-specific skills
        └── blog-formatter/
            └── SKILL.md
```

  - **Personal skills** (`~/.claude/skills/`): Available across all your projects, stored in your home directory
  - **Project skills** (`.claude/skills/`): Located in each project's root directory, shared with your team via git
  - **Plugin skills**: Bundled with Claude Code plugins (installed automatically)

**To add your newly-created skill to Claude Code**
- **Extract the skill directory** from the zip file you downloaded or received
- **Choose your location**:
  - For personal use: `~/.claude/skills/your-skill-name/` (available in all projects)
  - For team sharing: `.claude/skills/your-skill-name/` (in your project root, committed to git)
- **Copy the extracted skill directory** (containing `SKILL.md` and any supporting files) to your chosen location
- **Delete the zip file** (though you may want to keep a backup somewhere) - Claude Code works with the directory structure, not zip files
- **Restart Claude Code** (optional but recommended) so that the new skill is recognized

**To use the new Skill in Claude Code**
- **Inside Claude Code, ask naturally**: Simply describe what you want to do (e.g., "perform this task"). Claude will automatically use the relevant Skill based on your request and the Skill's description.
- **Note**: You can also explicitly invoke a Skill by name if you wish: "Use the [skill-name] skill to do [task] using these inputs: [inputs]."

**Troubleshooting**

If you installed Claude Code via npm and Skills aren't working:
1. Uninstall the npm version:
   ```bash
   npm uninstall -g @anthropic-ai/claude-code
   ```
2. Install the latest version via the native installer:
   ```bash
   curl -fsSL https://claude.ai/install.sh | bash
   ```

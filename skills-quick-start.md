## On Claude Web

**One-time configuration**:
- Log into Claude (must be Pro, Max, Team, or Enterprise for this feature to work).
- Go to Settings --> Capabilities
- In the screen that appears
   -- turn on “Code Execution and File Creation”
   -- turn on “Skills”
   -- Then scroll down further and turn on the “skill-creator” skill

Now that the skill-creator skill has been enabled, you can use it to create a skill file.

**To create a skill file**
- Start a new chat
- *Prompt*: Use #skill-creator to create a skill that [performs this task] for [this purpose]. Ask me questions, one at a time, until you have enough context to create a useful skill.

At the end of the chat conversation, Claude will give you a skill file (in zip format) that you can download (and share).

**To add your new skill to your Claude account**
- Go back to Claude Settings --> Capabilities
- Scroll down to the Skills section and hit the “Upload Skill” button.
- Upload the skill file you created in the previous step,
- Turn on the newly uploaded skill.

**To use the skill**
- In a new chat, use the prompt format: Use the [skill-name] skill to do [task] using these inputs: [paste or attach your input files]
- Or alternatively: Use #your-skill-name to do [task] using these inputs: [paste or attach your input files]

## On Claude Code for the Mac

To get my newly-created Skill working in Claude Code on Mac OS:

**One time setup**
- **Install the latest version of Claude Code** (must be 2.0.22 or later).
- **Create a skills directory** under the .claude directory

**To add your newly-created skill to Claude Code**
- **Copy the new skill zip file** into the skills folder
- **Unzip the skills file, then delete the zip**, leaving only the unzipped skill files, since Claude doesn’t use the zip file.
- **Restart Claude Code** so that the new skill is recognized.

**To use the new skill in Claude Code**
- **Inside Claude Code, invoke the skill by name**: use the [skillname] skill to [perform this task]. Claude Code will respond and confirm that it is using the skill.

**Troubleshooting**
- I had used the npm installer for my previous Claude Code install, and that version does not play nice with Skills for some reason, even when I installed the latest version
- So I had to use Terminal to uninstall my old version:\
`npm uninstall -g @anthropic-ai/claude-code` 
- Then install the latest version via the native Anthropic installer\
`curl -fsSL https://claude.ai/install.sh | bash`

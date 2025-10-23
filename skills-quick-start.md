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
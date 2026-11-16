# Roblox Game Playtest QA

A Claude skill for hands-on Roblox game QA. It guides a tester through the experience, checks the major gameplay and presentation systems, and writes a prioritized report of bugs, rough edges, lag, visual issues, and ideas to fix them.

## Use with Claude Code

Copy `.claude/skills/roblox-game-qa` into the same path in your project or Claude skills directory. Then ask Claude to playtest your Roblox game and provide its Roblox experience link, the expected player experience, and any test limits. Claude needs a way to actually access and interact with the game; this skill does not automate Roblox or provide access to your account.

Never send passwords, session cookies, or account recovery information. Use a test account and a private test server when possible.

## What it covers

- First-time entry, onboarding, and the main gameplay loop
- Movement, controls, interaction, camera, UI, and feedback
- Progression, rewards, saving, and multiplayer behavior where available
- Visual polish, audio, readability, accessibility, and performance symptoms
- Reproducible steps, impact, severity, evidence, and a practical fix idea for every finding

The report distinguishes confirmed findings from suspicions and explicitly lists areas that were not tested. No playtest can prove that every possible state is bug-free.

## Repo contents

- `.claude/skills/roblox-game-qa/SKILL.md`: the playtest workflow and reporting rules
- `templates/qa-report.md`: a ready-to-fill report format

## GitHub repository

Published at [JAcodesStuff/Roblox-playtest-claude](https://github.com/JAcodesStuff/Roblox-playtest-claude). Review files before sharing and do not add credentials or private player data.
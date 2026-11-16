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

## Share on GitHub

Create an empty GitHub repository, then from this folder run:

```sh
git init
git add README.md .claude templates
git commit -m "Add Roblox gameplay QA skill"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/roblox-gameplay-qa.git
git push -u origin main
```

Replace the remote URL with your repository's URL. Review the files before sharing and do not add credentials or private player data.
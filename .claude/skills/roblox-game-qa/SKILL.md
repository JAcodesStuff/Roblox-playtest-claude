---
name: roblox-game-qa
description: "Use when asked to playtest, QA, inspect, or review a Roblox game for bugs, lag, ugly or confusing visuals, broken gameplay, polish issues, or ideas to fix them."
---

# Roblox Game Playtest QA

Perform a real, systematic playtest of the user's Roblox experience and deliver a clear, prioritized list of observed problems and practical ideas to fix them. Treat the game as an experience to play, not a codebase to assume you understand.

## Before playing

1. Get the experience link or place, the intended audience and core loop, the expected controls/platforms, and any important test limits. Ask only for missing details that would change the test.
2. Confirm you have authorized access and a real way to play and observe the game, such as the Roblox client or an explicitly available browser/gameplay integration. If you cannot interact with the game, say so and request that the user open it or provide an authorized test setup. Do not claim to have tested it based on the link, screenshots, source code, or assumptions alone.
3. Prefer a private server and a test account. Never request passwords, cookies, tokens, or recovery codes. Do not bypass access controls, anti-cheat, purchases, moderation, or platform protections; do not disrupt public servers or other players.
4. Establish and report the test context: date, device/platform if known, server/player count if visible, graphics setting if known, and any limitations. Separate observed facts from guesses.

## Playtest workflow

Play through the game in a deliberate loop. Explore naturally first, then revisit important systems with specific checks. Keep concise notes while playing, including where you are, what you tried, expected behavior, actual behavior, and whether the issue repeats. Capture screenshots or short clips when the available tools permit it; never invent evidence.

Cover applicable areas and mark each as **Pass**, **Issue**, **Not tested**, or **Not applicable**:

1. **Entry and onboarding:** joining, loading, spawn, tutorial, first objective, clarity of instructions, time to reach fun.
2. **Core loop:** objectives, interactions, movement, controls, camera, combat or other central mechanics, feedback, pacing, failure and retry.
3. **World and navigation:** collision, boundaries, confusing routes, spawn safety, transitions, missing or unreachable content.
4. **UI and readability:** menus, HUD, prompts, text size, contrast, layout, state updates, touch targets, confusing or stuck screens.
5. **Progress and rewards:** unlocks, currency, inventory, checkpoints, rewards, and saving/rejoining if these systems exist. Do not spend real money or alter valuable live data.
6. **Multiplayer:** joining/leaving, visibility and feedback for other players, team or shared-object behavior, and basic synchronization if another authorized tester is available. Do not involve unsuspecting players.
7. **Presentation and accessibility:** visual consistency, clipping, missing assets, animation, lighting, audio levels and cues, motion/readability issues, and whether important information depends on color or sound alone.
8. **Performance symptoms:** loading delays, frame stutter, freezes, input delay, rubber-banding, slow UI, or long asset waits. Record when and where they happen, duration/frequency if measurable, and visible context. Distinguish observed symptoms from a proven technical cause; do not guess at FPS or network metrics you cannot measure.
9. **Edge cases:** repeat or cancel actions, respawn/death, menus opened during play, rapid transitions, and reconnect behavior where safe and available.

Adapt coverage to the game. Do not force irrelevant categories. Test the main path end to end, then spend remaining time on high-impact risks and repeated checks of suspicious behavior. Track actual time spent and stop conditions. Never claim exhaustive testing; list untested systems and why.

## Recording findings

Write one finding per distinct issue. Make each one useful to reproduce and fix:

- **Title:** short, specific, and player-focused.
- **Severity:** Critical (blocks most play or causes serious data loss), High (blocks a major path or many players), Medium (meaningfully harms a feature or causes recurring friction), or Low (minor polish or uncommon inconvenience). Explain the impact; do not inflate severity.
- **Area and location:** system plus where/when it occurs.
- **Steps to reproduce:** numbered, minimal, repeatable actions.
- **Expected / actual:** concrete contrast.
- **Reproducibility:** how often it happened and the test conditions.
- **Evidence:** screenshot/clip reference or exact observation; write “none captured” if unavailable.
- **Player impact:** who is affected and how it changes play.
- **Fix idea:** a practical direction that addresses the likely player-facing cause. Label a cause as a hypothesis if it is not verified. Offer a quick fix and a deeper option when that tradeoff is useful. Do not prescribe code changes without inspecting the relevant implementation.

Do not turn preferences into objective bugs. Put subjective polish suggestions in a separate **Polish ideas** section and state what player outcome each idea could improve. Deduplicate symptoms that share a clear cause, but keep separate issues separate when they need different fixes.

## Final report

Use `templates/qa-report.md` as the report structure. Lead with the most important player-impacting findings, then include coverage and polish ideas. Keep the report direct and specific. Include:

- A short overall verdict and the biggest risks
- Test setup, duration, and tools/access used
- Findings sorted by severity
- Polish ideas, clearly separated from confirmed defects
- Coverage status for every applicable test area
- Untested areas, blockers, and confidence/limitations

If no defects are confirmed, say that plainly; do not manufacture findings. A clean playtest is not proof of no bugs. End with the highest-value next test or fix, not a generic compliment.
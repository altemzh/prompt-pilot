# Prompt Pilot

Flappy Bird where typing is the jump button. A small AI robot flies through server racks, and it only boosts up when you type the next correct letter of an AI word like `token` or `prompt`.

**Play it:** https://altemzh.github.io/prompt-pilot/ (needs a physical keyboard)
Or download `index.html` and double-click it. It works offline with nothing to install.

![Playing Prompt Pilot](evidence/screenshots/02_playing.png)

Temirlan Ramazanov · AIE1101 Vibe Coding: Build Apps with AI · Flappy Bird track

## How to play
- Type the highlighted letter to boost the robot up. A wrong letter gives no boost, so you fall.
- Fly through the gaps between the server racks.
- Press Space to play again after a crash.
- Switch word packs with the buttons under the game: **AI Basics** or **Vibe Coding**.

## What I changed from the class Flappy Bird
| Change | Why |
|---|---|
| Typing the next letter replaces the jump key | Makes the game typing practice |
| AI theme: robot, server racks, AI word packs | Connects the project to this course |
| Live WPM, accuracy and best score | The player can see their typing improve |
| Easier version 2: wider gap, half the gravity, capped falling speed | Version 1 was too hard when I played it |

WPM = (correct letters ÷ 5) ÷ minutes. Accuracy = correct keys ÷ all keys.

## One bug I fixed
Holding a key down made the browser send repeated key events, and each repeat counted as a wrong letter, so accuracy dropped even when typing was correct. The fix is one line at the top of the key handler: `if (e.repeat) return;`. Before/after screenshots are in [`evidence/screenshots`](evidence/screenshots).

## Files
| Path | Contents |
|---|---|
| `index.html` | The whole game (HTML, CSS and JavaScript) |
| `docs/Prompt_Pilot_Slides.pdf` | 3-slide presentation |
| `docs/Prompt_Pilot_Reflection_Report.pdf` | Reflection report |
| `docs/interactive-presentation.html` | Presentation with the gameplay video |
| `evidence/` | Screenshots, AI prompts and decisions, test results, version 1 |
| `media/` | Gameplay video and bug before/after video |

Built with help from Claude (AI assistant). My prompts and decisions are in [`evidence/ai-prompts-and-decisions.txt`](evidence/ai-prompts-and-decisions.txt).

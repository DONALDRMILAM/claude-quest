# Claude Quest 🤖🎓

A playable phone quiz game built from two Anthropic courses:
**Claude 101** (https://academy.claude.com/courses/claude-101) — 13 worlds, and
**Claude Code 101** (https://academy.claude.com/courses/claude-code-101) — 12 worlds.
25 worlds, 125 quiz levels total, every question drawn from the real lesson content.

## Play
1. Open `claude-quest.html` on your phone (Chrome on Android works best).
2. Pick a world (lesson), tap a level, answer the quiz question.
3. **3 hearts per level** — a wrong answer costs a heart; lose all 3 and you retry the level.
4. **100 XP per correct answer** (+25 streak bonus at 3+ in a row). Badges per level, a crown per finished world.
5. Progress saves on the phone automatically (localStorage).

## Audio narration (Teri's voice)
The game can read lesson intros, questions, and outros aloud:
1. Download the 5 audio packs (`claude-quest-audio-1.zip` … `claude-quest-audio-5.zip`)
   and extract them into one folder next to `claude-quest.html`.
2. In the game, tap **📁 Find my audio files** and pick that folder.
3. Tap the 🔊 buttons to listen. (175 MP3s total across both courses:
   25 intros + 25 outros + 125 questions.)

`voice-map.json` maps every game event to its audio file.

## Android fix
The audio folder picker uses a hidden `webkitdirectory` file input, which works
on Android Chrome. `showDirectoryPicker` is desktop-only and is never used.

## Worlds

**Claude 101** (worlds 1–13):
1. What is Claude? · 2. Your First Conversation · 3. Getting Better Results ·
4. Chat, Cowork, Code · 5. Projects · 6. Artifacts · 7. Skills ·
8. Connecting Your Tools · 9. Enterprise Search · 10. Research Mode ·
11. Use Cases by Role · 12. What's Next? · 13. Other Ways to Work

**Claude Code 101** (worlds 14–25):
1. What is Claude Code? · 2. How Claude Code Works · 3. Installing Claude Code ·
4. Your First Prompt · 5. Explore → Plan → Code → Commit · 6. Context Management ·
7. Code Review · 8. The CLAUDE.md File · 9. Subagents · 10. Skills · 11. MCP · 12. Hooks

Every level links back to the real course for deeper reading.

## Building
`build_html.py` is the v1 (Claude 101 only) generator, kept as the v1 record.
`build_html_v2.py` builds `claude-quest.html` from both courses
(`questions.json` + `narration.json` + `questions-code101.json` + `narration-code101.json`).
Just run `python3 build_html_v2.py` to regenerate `claude-quest.html`.

<!-- Adapted by Teri, powered by Muse Spark (Meta). -->

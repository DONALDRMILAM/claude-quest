# Claude Quest 🤖🎓

A playable phone quiz game built from Anthropic's **Claude 101** course
(https://academy.claude.com/courses/claude-101) — 13 worlds, 65 quiz levels,
every question drawn from the real lesson content.

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
3. Tap the 🔊 buttons to listen. (91 MP3s total: 13 intros + 13 outros + 65 questions.)

`voice-map.json` maps every game event to its audio file.

## Android fix
The audio folder picker uses a hidden `webkitdirectory` file input, which works
on Android Chrome. `showDirectoryPicker` is desktop-only and is never used.

## Worlds
1. What is Claude? · 2. Your First Conversation · 3. Getting Better Results ·
4. Chat, Cowork, Code · 5. Projects · 6. Artifacts · 7. Skills ·
8. Connecting Your Tools · 9. Enterprise Search · 10. Research Mode ·
11. Use Cases by Role · 12. What's Next? · 13. Other Ways to Work

Every level links back to the real course for deeper reading.

<!-- Adapted by Teri, powered by Muse Spark (Meta). -->

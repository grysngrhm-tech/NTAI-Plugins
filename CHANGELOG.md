# Changelog

What changed in NTA's plugins. Each plugin's version is in its `.claude-plugin/plugin.json`; it goes up with every release, and Claude updates plugins installed from this marketplace by it.

## 2026-10-07

### nta-student 2.0.0
- **One study session (NTAI):** `study` is now your study session for each lesson: `home` (where you are and what to do next), `lesson` (the lesson's objectives and your progress on each), `check` (the lesson check, two questions on each objective), `results`, `guide` (a study guide on what you have not mastered yet) and `practice` (a round on your weakest objectives), alongside `explain` and `flashcards`. When you master every objective the lesson says so, and its next step is the next lesson.
- **New tools:** `answer_question` answers, gives a hint for, or shows the answer to a session question (it replaces `check_answer` and `get_hint`; a hint is noted in your record), and `update_study_settings` sets a workshop date or turns sharing your progress with your instructors on or off (it replaces `update_study_plan`). `my_study` is gone: `study` home shows where you are. `clear_study_record` clears one lesson or your whole record.
- **Skill and starters:** rewritten around the session ("Where am I?", "Check me on my current lesson", "Help me with my weak spots"). Your app may ask you once to allow `answer_question`, because it writes to your own record. Nothing to reconnect.

### nta-student 1.3.2, nta-staff 1.4.1
- **Search reaches completed modules (NTAI):** a student's `search` now finds passages in the modules they have completed (a graduate's, in their completed programs and on-demand courses), not in the module they are learning now; for that, `study` explains and practises it. The skills say so. Nothing to reconnect.

### nta-student 1.3.1
- **Study record (NTAI):** the first check of each practice question now goes into your study record whether you answer in NTAI's view or in the chat, and nothing done after the answer is shown can change it. `check_answer` writes to your own record, so your app may ask you once to allow it. The skill says so.

### nta-staff 1.4.0
- **Suggest a change to NTAI (staff suggestions):** `suggest_change` sends NTA a correction (a wrong fact, a gap, wording), a problem in a lesson, or an idea; a named NTA reviewer approves or declines it, and nothing in NTAI changes until then. `same_as` adds "me too" to an existing suggestion instead of a duplicate. `list_suggestions` shows every staff suggestion with its status, through to live in NTAI. Suggestions with a name, contact detail or health detail about a person are refused.
- **Skill:** when to suggest, to search first and pass the result's `report_ref` and passage number, and to check for the same suggestion before filing. A new starter, "Suggest a change to NTAI". Nothing to reconnect.

### nta-student 1.3.0, nta-staff 1.3.0
- **Clearer tool names (NTAI):** `ask` is now `search`, `check_practice_answer` is `check_answer` and `practice_hint` is `get_hint`. The skills use the new names. Nothing to reconnect.
- **Search for students:** NTA Student now has `search`, which finds the passages on a topic in the lessons your account has unlocked (NTA's own curriculum only), with the course and lesson for each. It opens when NTA releases it; until then it says it isn't open yet.
- **Skills:** when to use `study` (to understand and practise) and when to use `search` (to find passages); staff can point students to `study` for learning.

## 2026-10-06

### nta-student 1.2.0, nta-staff 1.2.0
- **One connection per plugin:** each plugin now connects to its own NTAI address with only its own tools, named after the plugin (`nta-student`, `nta-staff`). You can install both and connect each; NTA Staff no longer offers practice questions, and NTA Student does not offer staff search. Reconnect after updating: choose **Connect** in the plugin's **Connectors** tab.

## 2026-10-05

### nta-student 1.1.0, nta-staff 1.1.0
- **Sign-in upgrade (NTAI):** the connector bundled in each plugin now signs in by itself: NTAI registers Claude automatically, so you no longer add the NTAI connector by hand before connecting the plugin. Every connection shows a consent page naming the NTA account you signed in with, so you can check it before choosing Allow. You can sign in with a passkey (Face ID, Touch ID or your device's PIN) instead of waiting for an emailed code.
- **Skills:** "Another question" on the same topic (`study` with `avoid`); reporting a wrong or unclear answer with `report_answer` or the view's Report a problem button; confirming before `clear_study_record`; clearing the old plan before saving a new one; which practice results reach the study record; the "NTA fact" and "Research" source labels; for staff, following the wording rules that come with `ask`'s passages (`ask` is `search` from 1.3.0).
- **Metadata:** repository, licence and keywords in each `plugin.json`; install steps for the marketplace and for file upload in each README.

### nta-student 1.0.0, nta-staff 1.0.0
- The student plugin is renamed from `nta-study-companion` to **NTA Student** (`nta-student`), for students and graduates; the staff plugin is **NTA Staff** (`nta-staff`). The marketplace is `ntai`, published at `grysngrhm-tech/NTAI-Plugins`. If you installed `nta-study-companion`, remove it and install NTA Student.

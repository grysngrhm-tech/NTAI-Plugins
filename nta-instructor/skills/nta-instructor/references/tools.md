# NTAI's instructor tools

Every tool works only for the programs the instructor or TA teaches. Results are complete as text; use them as they come.

| Tool | Arguments | What it returns |
|---|---|---|
| `show_progress` | Nothing | The modules the person teaches, each named by its first lesson, with its lessons, its number of learning objectives and its `course_ref` |
| `show_progress` | `course_ref` | The module's group summary: for each learning objective, how many learners have mastered it, are getting there, need work, have review suggested or are not checked yet. Counts only; a group below NTAI's minimum size shows none |
| `show_progress` | `learner` (profile link, email or `learner_ref`), optional `course_ref` | That learner's progress: for each learning objective they have practised, its state and the day it was first mastered; their readiness review results and the day they last practised; and their open practice sets. With a `course_ref`, every objective of the module, numbered by lesson and objective ("2.1" is lesson 2's first objective) |
| `find_gaps` | `course_ref` | The module's hardest objectives (most learners not yet mastered among those checked) and the wrong answers most often chosen on NTA's practice questions, with NTA's note on each mix-up. A wrong answer is shown only when at least NTAI's minimum number of learners chose it and at least that many chose something else |
| `prepare_class` | `course_ref`, optional `questions` (1 to 20, default 8) | A workshop brief: the group summary, points to discuss and a practice set of NTA's approved questions with their answers, for the instructor |
| `draft_message` | `learner`, optional `course_ref` | A short check-in note to the learner naming what they most need to work on, for the instructor to edit and send themselves. Never sent or kept by NTAI |
| `assign_practice` | `learner`, `course_ref`, `objectives` (1 to 10 numbers such as "2.1"), optional `due_on` (YYYY-MM-DD) | The practice set's objectives. It appears on the learner's NTAI home if they can receive it (in a program the instructor teaches, sharing their progress); the answer is the same either way. NTAI sends no message |
| `about_ntai` | Nothing | What NTAI is, what this account can do, and where to get help |

A `roster` (a list of up to 60 learners, each a profile link, email or `learner_ref`) narrows `show_progress`, `find_gaps` and `prepare_class` to one workshop's learners, until NTA Connect provides workshop rosters. A roster shows group figures only when it has at least NTAI's minimum number of learners who practised, and never the most chosen wrong answers. Each learner included can see that their progress was viewed in a group summary.

If a tool says something isn't available, pass that on; do not try another way to reach the same information.

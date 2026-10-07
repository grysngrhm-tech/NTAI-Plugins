# NTAI's tools for learners and graduates

All tools act only for the signed-in person and only on the NTA material their account includes.

## `study`
- `mode`:
  - `home`: the learner's lessons with their progress, where to continue, refreshes ready, assignments from an instructor or TA. `course_ref` (optional) limits it to one module.
  - `lesson`: a lesson's objectives, each with its state, and the next step. When every objective is mastered, it says the lesson is mastered and the next step is the next lesson (or the workshop); practice stays as "Keep it fresh".
  - `check`: the lesson check, two questions on each objective (a round).
  - `results`: the lesson's map with each objective's state, and the score line for a round (`round_ref`).
  - `guide`: a study guide on the objectives not mastered yet, weakest first: a checked explanation from that objective's passages, and a note on the wrong option the learner chose last time, when NTA has one.
  - `practice`: with a `lesson_ref`, a practice round on the weakest objectives (two questions each, plus a refresh when one is due); with a `message`, or on a lesson with no lesson check yet, one practice question.
  - `explain`: a checked explanation of the learner's question (`depth: "deeper"` for a fuller one, when NTA has released it).
  - `flashcards`: a few flashcards whose answers are checked.
- `lesson_ref`: the NTA Connect lesson (required for `lesson`, `check`, `results` and `guide`).
- `message`: the learner's question or topic, in their words (for `explain`, `flashcards` and practice on a topic).
- `round_ref` (with `results`): the round just finished.
- `similar_to` and `avoid` (with practice on a topic): the `question_ref` of a missed question for a similar one, or of up to five recent questions for another, different one.

A round lists numbered questions with lettered options, each with its `question_ref`, and the round's `round_ref`. Never the answers. A lesson with no lesson check yet says the check is coming soon; explanations, practice questions and flashcards still work. Answers, questions and flashcards carry a `report_ref` for `report_answer`.

## `answer_question`
- `question_ref` and `round_ref`: from the round.
- `action`: `answer` (with `choice`, a letter), `hint` (with `level` 1 or 2) or `give_up`.

Returns whether the answer was right, the answer, the checked explanation with its sources, a note on the wrong option chosen when NTA has one, the objective's state once both of its questions in the round are answered, and the round's progress and next step. The first answer to each question counts; answering again changes nothing and returns the first result. A hint before answering is noted, and a right answer after a hint does not count toward mastery. A round works for the same learner for about a day. It writes to the learner's own record, so their app may ask them to allow it.

## `update_study_settings`
- `workshop`: a module's `course_ref` and a `date` (YYYY-MM-DD), or `null` to remove it.
- `share_with_instructors`: `true` or `false`: whether their NTA instructors and TAs can see their progress by objective (on unless they turn it off).

## `search`
- `question`: what to look up, in the learner's words.

Returns numbered excerpts from the NTA modules the learner has completed (for a graduate, their completed programs; NTA's own curriculum only), each with its course and lesson, the wording to keep to, and a `report_ref`; or a notice (not covered, a graded question declined, or search not open yet). It writes no answer: answer only from the excerpts and cite them by number. The module they are learning now, locked lessons and reference books are not searched (search opens a module once they have completed it). To explain or practise the topic, use `study`.

## `clear_study_record`
`what`: `lesson` (with `lesson_ref`: that lesson's progress and answers) or `everything` (progress on every objective, answers, workshop dates and assignments). Their choice about sharing with instructors stays. Deletes and cannot be undone: confirm with the learner before calling it. Their app may also ask them to confirm.

## `report_answer`
`report_ref` (from the answer, question, guide, flashcards or search excerpts being reported) and `category`: `wrong`, `unclear`, `not_covered` or `other`. NTA's curriculum team sees the kind of problem and which lessons the answer used, never the question or the answer. Do not add the learner's words.

## `about_ntai`
What NTAI is, what the person's account allows, how NTAI uses AI, and where to get help.

# NTAI's tools for learners and graduates

All tools act only for the signed-in person and only on the NTA material their account includes.

## `study`
- `mode`: `explain`, `quiz_me`, `check`, `plan` or `flashcards`.
- `message`: the topic or question, in the learner's words.
- `lesson_ref` (optional): an NTA Connect lesson, when known.
- `similar_to` (optional, with `quiz_me`): the `quiz_id` of an earlier question, for a different question on the same idea (after a miss).
- `avoid` (optional, with `quiz_me`): the `quiz_id`s of up to five recent questions on the topic, for another question that is different from them ("Another question").

Returns a checked answer with numbered sources, a practice question (question and options only, with a `quiz_id`), flashcards, or a notice (not covered, a lesson not unlocked yet, a graded question declined, or emergency guidance). A study plan answer includes a `plan_ref` the learner can save. Answers, practice questions and flashcards carry a `report_ref` for `report_answer`.

## `search`
- `question`: what to look up, in the learner's words.

Returns numbered excerpts from the NTA modules the learner has completed (for a graduate, their completed programs; NTA's own curriculum only), each with its course and lesson, the wording to keep to, and a `report_ref`; or a notice (not covered, a graded question declined, or search not open yet). It writes no answer: answer only from the excerpts and cite them by number. The module they are learning now, locked lessons and reference books are not searched (search opens a module once they have completed it). To explain or practise the topic, use `study`.

## `get_hint`
`quiz_id` and `level` (1 or 2). Level 1 names the lesson; level 2 quotes a short passage. Never the answer. Some questions have fewer hints; NTAI says when there are no more.

## `check_answer`
`quiz_id` and `choice` (a letter), or `give_up: true`. Returns whether the choice was right, the answer, and the explanation with its sources. A `quiz_id` works for the same learner for about a day. The first check of each question goes into the learner's study record (right, not right, or given up); checking the same question again changes nothing. It writes to the learner's own record, so their app may ask them to allow it.

## `my_study`
`view`: `resume` (where to continue), `review` (lessons due for review), `progress` (practice by course or module) or `plan` (the saved study plan). Read only from NTAI's record of the learner's practice.

## `update_study_plan`
`action`: `save` (with a `plan_ref`), `move` (`position`, `to`) or `mark_done` (`position`, `done`; `false` undoes it). Never deletes. Saving is refused while another plan is saved: the learner clears the old one first (`clear_study_record` with `what: "plan"`).

## `clear_study_record`
`what`: `plan` (the saved plan only) or `everything` (the plan, practice results and review dates). Deletes and cannot be undone: confirm with the learner before calling it. Their app may also ask them to confirm.

## `report_answer`
`report_ref` (from the answer, practice question, flashcards or search excerpts being reported) and `category`: `wrong`, `unclear`, `not_covered` or `other`. NTA's curriculum team sees the kind of problem and which lessons the answer used, never the question or the answer. Do not add the learner's words.

## `about_ntai`
What NTAI is, what the person's account allows, how NTAI uses AI, and where to get help.

The study record grows from practice questions checked with `check_answer` (in the chat or in NTAI's view) and from saved plans.

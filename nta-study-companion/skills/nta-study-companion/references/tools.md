# NTAI's tools for learners and graduates

All tools act only for the signed-in person and only on the NTA material their account includes.

## `study`
- `mode`: `explain`, `quiz_me`, `check`, `plan` or `flashcards`.
- `message`: the topic or question, in the learner's words.
- `lesson_ref` (optional): an NTA Connect lesson, when known.
- `similar_to` (optional, with `quiz_me`): the `quiz_id` of an earlier question, for a different question on the same idea.

Returns a checked answer with numbered sources, a practice question (question and options only, with a `quiz_id`), flashcards, or a notice (not covered, a lesson not unlocked yet, a graded question declined, or emergency guidance). A study plan answer includes a `plan_ref` the learner can save.

## `practice_hint`
`quiz_id` and `level` (1 or 2). Level 1 names the lesson; level 2 quotes a short passage. Never the answer.

## `check_practice_answer`
`quiz_id` and `choice` (a letter), or `give_up: true`. Returns whether the choice was right, the answer, and the explanation with its sources.

## `my_study`
`view`: `resume` (where to continue), `review` (lessons due for review), `progress` (practice by course or module) or `plan` (the saved study plan). Read only from NTAI's record of the learner's practice.

## `update_study_plan`
`action`: `save` (with a `plan_ref`; refused while another plan is saved), `move` (`position`, `to`) or `mark_done` (`position`, `done`). Never deletes.

## `clear_study_record`
`what`: `plan` or `everything`. Deletes; the learner's app will ask them to confirm.

## `about_ntai`
What NTAI is, what the person's account allows, how NTAI uses AI, and where to get help.

`record_practice` is used only by NTAI's own view; you will not see it.

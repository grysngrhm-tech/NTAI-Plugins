# NTA Instructor

For Nutritional Therapy Association instructors and TAs. Adds a skill that teaches your AI app how to use NTAI's instructor tools, and the NTAI connector.

- **A learner's progress** by learning objective (`show_progress`), found by their NTA Connect profile link or email. Never their questions, answers or chats; learners who turned sharing off show no record.
- **A module's group summary** (`show_progress`) and **where learners struggle** (`find_gaps`): counts only, never who; small groups show no figures.
- **A workshop brief** (`prepare_class`): the group's progress, points to discuss and a practice set of NTA's approved questions with their answers, for you.
- **A check-in message** (`draft_message`) for you to edit and send yourself. NTAI never sends or keeps it.
- **A practice set** for one learner (`assign_practice`), when you ask for one. It appears on the learner's NTAI home if they can receive it; NTAI answers the same either way, so a learner's choice not to share stays private.
- **Privacy:** never paste a learner's name or progress into other tools; group figures hide small groups; each view of a learner's progress is shown to the learner (your role and the time).

Needs an NTA account with the instructor or TA role for the programs you teach, and a paid Claude plan (Pro, Max, Team or Enterprise). Without one, use NTAI for instructors in your browser: https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/teach

What the connector sends: your tool requests (a module, or a learner's profile link or email) go to NTAI and nowhere else.

## Install in Claude

1. In Claude, open **Customize → Plugins**, choose **Add → Add marketplace** and enter `grysngrhm-tech/NTAI-Plugins`. Install **NTA Instructor**. It updates itself from then on.
   Or download `nta-instructor.plugin` from https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help and choose **Add → Upload plugin** (an uploaded plugin does not update itself).
2. Installing does not connect NTAI: open the plugin's **Connectors** tab and choose **Connect** (the connection is named `nta-instructor`).
3. Sign in with your NTA account (an emailed code or your passkey), check the NTA account NTAI names, and choose **Allow**.

If you are also NTA staff, install NTA Staff too for `search`; each plugin has its own connection, so connect each. On a Claude Team or Enterprise plan, an Owner adds the NTAI connector first (Organization settings → Connectors). Help: https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help.

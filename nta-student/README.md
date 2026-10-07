# NTA Student

For learners and graduates of the Nutritional Therapy Association. Adds a skill that teaches your AI app how to study NTA's curriculum with NTAI, and the NTAI connector.

- **Cited answers** from the NTA lessons your account has unlocked, checked before you see them (`study`).
- **Search the modules you've completed** for the passages on a topic, with the course and lesson of each (`search`).
- **A study session** for each lesson: where you are, the lesson's objectives, a lesson check, results by objective, a study guide on what you have not mastered yet, practice rounds on your weak spots, and a clear finish line when you master the lesson. Hints come before answers.
- **Workshop readiness** for each module: where you are by lesson and objective, a countdown and a plan to your workshop date, a readiness review (practice, not NTA's module test), a short round after the workshop, and practice your instructor or TA assigns you.
- **Graded test questions are taught, never answered:** bring one to NTAI and it teaches the idea behind it, with practice on other questions.
- **Your study settings:** workshop dates, and whether your instructors and TAs can see your progress. Clear a lesson or your whole record at any time.
- **Report a problem** with any answer, so NTA's curriculum team can fix it.
- **NTA's rules:** academic integrity (no graded work written for you), the NTP scope of practice (educate and support; never diagnose, treat or prescribe), and emergency guidance.

Needs an NTA account with a program enrollment, or a graduate's NTA membership, and a paid Claude plan (Pro, Max, Team or Enterprise).

## Install in Claude

1. In Claude, open **Customize → Plugins**, choose **Add → Add marketplace** and enter `grysngrhm-tech/NTAI-Plugins`. Install **NTA Student**. It updates itself from then on.
   Or download `nta-student.plugin` from https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help and choose **Add → Upload plugin** (an uploaded plugin does not update itself).
2. Installing does not connect NTAI: open the plugin's **Connectors** tab and choose **Connect** (the connection is named `nta-student`).
3. Sign in with your NTA account (an emailed code or your passkey), check the NTA account NTAI names, and choose **Allow**.

On a Claude Team or Enterprise plan, an Owner adds the NTAI connector first (Organization settings → Connectors). Help: https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help.

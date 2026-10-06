# NTA plugins for AI apps

Plugins from the Nutritional Therapy Association (NTA) for working with NTA's material through **NTAI**, NTA's assistant. Each plugin installs NTAI's connector together with NTA's skills.

## Install in Claude (Pro, Max, Team or Enterprise)

1. In Claude on the web or the desktop app, open **Customize → Plugins**.
2. Choose **Add → Add marketplace** and enter this repository (`grysngrhm-tech/nta-ai-plugins`). Plugins from a marketplace update themselves.
3. Choose **Add** on the plugin for you (below).
4. Open the plugin's **Connectors** tab and choose **Connect** next to NTAI. Sign in with your NTA account (an emailed code or your passkey) and allow NTAI.

On a Team or Enterprise plan, an Owner adds the NTAI connector first (Organization settings → Connectors). A plugin can also be uploaded as a file from NTAI's help page.

| Plugin | For | What it adds |
|---|---|---|
| [`nta-study-companion`](nta-study-companion/) | NTA learners and graduates | A skill for studying with NTAI: cited answers, hints before answers, academic integrity, the NTP scope of practice, emergencies; the NTAI connector |
| [`nta-staff`](nta-staff/) | NTA staff | A skill for finding and citing NTA material with NTAI's `ask`, what goes to a person, and keeping health information out; the NTAI connector |

Each plugin needs an NTA account: a program enrollment for the study companion, a staff account for the staff plugin. Help: https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help.

**These plugins guide your AI app; they do not grant access.** NTAI itself decides what each person may see and checks every answer against NTA's material. The plugins contain no NTA curriculum.

# NTA plugins for AI apps

Plugins from the Nutritional Therapy Association (NTA) for working with NTA's material through **NTAI**, NTA's assistant. Each plugin installs NTAI's connector together with NTA's skills.

| Plugin | For | What it adds |
|---|---|---|
| [NTA Student](nta-student/) (`nta-student`) | NTA students and graduates | A skill for studying with NTAI: cited answers, searching the modules you have completed, hints before answers, academic integrity, the NTP scope of practice, emergencies; the NTAI connector |
| [NTA Staff](nta-staff/) (`nta-staff`) | All NTA staff | A skill for finding and citing NTA material with NTAI's `search`, what goes to a person, and keeping health information out; the NTAI connector |

Planned: NTA Instructor (`nta-instructor`: student progress, curriculum gaps and classroom tools for instructors) and NTA Practitioner (`nta-practitioner`: Nutri-Q and practice tools, in NTAI's clinical zone).

## Install in Claude

Plugins work on Claude's paid plans (Pro, Max, Team and Enterprise), on the web and in the desktop app.

**From this marketplace (recommended; updates arrive by themselves):**
1. Open **Customize → Plugins**.
2. Choose **Add → Add marketplace** and enter `grysngrhm-tech/NTAI-Plugins`.
3. Install the plugin for you from the list above.
4. Installing does not connect NTAI. Open the plugin's **Connectors** tab and choose **Connect** (the connection is named after the plugin, such as `nta-student`).
5. Sign in with your NTA account (an emailed code or your passkey). NTAI then shows which NTA account you signed in with and asks you to allow the connection; choose **Allow**.

Marketplace plugins update automatically. To update sooner, use **Check for updates** on the marketplace (or turn **Sync automatically** on if it is off).

**More than one plugin:** install every plugin that fits you, for example NTA Staff and NTA Student if you work at NTA and also study. Each plugin has its own NTAI connection with its own tools, so connect each one; after the first, you are usually still signed in and only choose Allow. What each offers still depends on your NTA account.

**From a file:** download `nta-student.plugin` or `nta-staff.plugin` from NTAI's help page (https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help), choose **Add → Upload plugin** in **Customize → Plugins**, then connect as in steps 4 and 5. An uploaded plugin does not update itself; upload the new file to update.

**Claude Team or Enterprise:** an Owner of your organization adds the NTAI connector first (Organization settings → Connectors). Then each person connects with their own NTA account.

Each plugin needs an NTA account: a program enrollment (or a graduate's NTA membership) for NTA Student, a staff account for NTA Staff. Help: https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help. What changed in each version: [CHANGELOG.md](CHANGELOG.md).

**These plugins guide your AI app; they do not grant access.** NTAI itself decides what each person may see and checks every answer against NTA's material. The plugins contain no NTA curriculum.

Licence: proprietary. Copyright Nutritional Therapy Association. May be used with NTAI; not for redistribution.

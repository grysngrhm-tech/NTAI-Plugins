# NTA Staff

For Nutritional Therapy Association staff. Adds a skill for finding what NTA's curriculum, program information and references say with NTAI's `ask` tool, citing it in replies, reporting a problem with what it found, routing what needs a person, and keeping health information out of AI tools; and the NTAI connector.

Needs an NTA staff account and a paid Claude plan (Pro, Max, Team or Enterprise).

## Install in Claude

1. In Claude, open **Customize → Plugins**, choose **Add → Add marketplace** and enter `grysngrhm-tech/NTAI-Plugins`. Install **NTA Staff**. It updates itself from then on.
   Or download `nta-staff.plugin` from https://nt-a678963363c4463291b3051c5b5e011c.ecs.us-west-2.on.aws/help and choose **Add → Upload plugin** (an uploaded plugin does not update itself).
2. Installing does not connect NTAI: open the plugin's **Connectors** tab and choose **Connect** next to NTAI.
3. Sign in with your NTA staff account (an emailed code or your passkey), check the NTA account NTAI names, and choose **Allow**.

On a Claude Team or Enterprise plan, an Owner adds the NTAI connector first (Organization settings → Connectors). NTA's Claude administrators can make this plugin Required for staff and attach it, with the NTAI connector, to staff channels in Claude in Slack (`docs/v2/PLUGINS.md` in NTAI's repository).

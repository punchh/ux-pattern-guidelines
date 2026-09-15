---
description: >-
  Skills and markdown files for AI design reviews, AI prototyping, and vibe
  coding
---

# AI skills

### Using with AI tools

Before using the [individual skill files](ai-skills.md#individual-skills-for-each-ux-pattern-guideline) below, get your AI tool ready to use them.

{% hint style="warning" %}
**Don't let your AI agent hard code the&#x20;**_**contents**_**&#x20;of any UX pattern guideline page to your own skill files.**

These pages get updated often, so it would quickly become out of date. Each skill file is crafted to do runtime lookups to the live UX pattern guidelines on this website each time it's invoked so that it gets the latest and greatest.
{% endhint %}

<details>

<summary>Without any specific tool</summary>

Just copy the URL from the desired guideline page(s) and paste to your agent.

Ask your agent to use it to shape your design. That's it.

You don't even _need_ the skill files.

Otherwise, some tools also let you drag and drop .md files into the agent prompt.

</details>

<details>

<summary>With <strong>Claude Code</strong></summary>

Download `CLAUDE.md` and place it in the same folder as your skill files. Claude Code will automatically discover any `ux-*.md` skill files in that folder and apply the relevant ones to your work — no additional setup needed.

{% hint style="info" %}
**If you already have a CLAUDE.md file** in your project, don't replace it — copy the contents of this file and paste them at the bottom of your existing one.
{% endhint %}

When you download new skills, just drop them in the same folder. `CLAUDE.md` picks them up automatically.

{% file src="/broken/files/KzohCgP09VvykDnvCoQt" %}

</details>

<details>

<summary>With <strong>Cursor</strong></summary>

Each UX pattern guideline below is a markdown file with a short description at the top so the AI knows when it applies.

1. (Create the `skills` folder if it doesn’t exist.)
2. Add our starter `SKILL.md` to that folder _once_ (we provide it—it tells Cursor how to find and use every other `.md` in the same folder).
3. Drop in whichever guideline `.md` files you downloaded. You can add more anytime—no need to edit `SKILL.md` each time.

In Cursor, mention the skill (e.g. type `@` and choose ux pattern guidelines) or ask the agent to follow your UX pattern guidelines before you review or build UI.

That’s it.

{% file src="/broken/files/KFG6WDNUZeLgd7eg6i5a" %}

</details>

<details>

<summary>With <strong>GitHub Copilot in VS Code</strong></summary>

Download the skill files plus `copilot-instructions.md`. Place `copilot-instructions.md` in a `.github/` folder at your project root (so the path is `.github/copilot-instructions.md`) and put the skill files in a dedicated folder in your project, such as `docs/ux-skills/` or wherever fits your project's structure. The instructions file tells Copilot to scan recursively, so any folder location works.

If you already have a `.github/copilot-instructions.md` file, don't replace it — copy the contents of this file and paste them at the bottom of your existing one.

When you download new skills, drop them into the same folder. Copilot picks them up automatically.

{% hint style="info" %}
Setup varies across Copilot configurations and team settings. If this path doesn't work in your environment, check with your team for how custom instructions are configured.
{% endhint %}

{% file src="/broken/files/1xmAeaBuTQkJDXqyoLIM" %}

</details>

***

### Individual skills for each UX pattern guideline

Pick and choose which skills are relevant for your scope. Download as many or as few as are relevant.

#### Layout and navigation

{% file src="/broken/files/2pizy71dg4WhFGJVBMQv" %}

{% file src="/broken/files/NMuN4sqg0yDsZQyvx87d" %}

{% file src="/broken/files/Z9pHqEs4A9K3EV88FGpe" %}

{% file src="/broken/files/muKsA4W26Xte7wr8fQiB" %}

{% file src="/broken/files/3bjmBNCJRI4ZplKCWBYp" %}

{% file src="/broken/files/S1qNJ5bTeEfQkeFXFKxl" %}

{% file src="/broken/files/4zILgXpt6ABexkjOq0fM" %}

{% file src="/broken/files/AzLWFS38bPM8WsqQOVOh" %}

#### Lists and tables

{% file src="/broken/files/RrIXZs4ycfdcUiLn6Arj" %}

{% file src="/broken/files/25DXRgSuec6hfoAaR1DM" %}

{% file src="/broken/files/aVotcderBaAHBKEhBbIt" %}

{% file src="/broken/files/12942vJhkPqHCY59c8Et" %}

{% file src="/broken/files/gWLz58MFc1Jnj2EO0Ios" %}

#### Reading information

{% file src="/broken/files/Etl9fBvJYGw2cUHkqjMf" %}

{% file src="/broken/files/0h1ABK2G8dLjSCxSkgRZ" %}

{% file src="/broken/files/dIt8Q8L3l7NprtnNoigq" %}

{% file src="/broken/files/iCu4ohjYhNtjjWdjdgUQ" %}

{% file src="/broken/files/j12LpZUwaho6Vkl2Y3j8" %}

{% file src="/broken/files/0TbNtp466cBjavFaBLYf" %}

{% file src="/broken/files/iYbsJdLYW95PPmORwKn9" %}

{% file src="/broken/files/Hh235Awsf42z6lY8Gm4U" %}

{% file src="/broken/files/E3pjgtRDFJ5vmzlQXk4K" %}

{% file src="/broken/files/vOxGz8ev1aQLOt1BgYZy" %}

{% file src="/broken/files/ziCGZE0Kou1B3YLoDWsj" %}

{% file src="/broken/files/21qPgPhbOnlAYZOLnoTr" %}

#### Form experience

{% file src="/broken/files/JxnNT7QKDKatnCMHT9nK" %}

{% file src="/broken/files/FA3uhE1txr89ExN90KIK" %}

{% file src="/broken/files/ljD7VTMKR8NiaAdJqmmN" %}

{% file src="/broken/files/d1Dj4eFViE398rRNGMbD" %}

{% file src="/broken/files/tujSd3cKoDmz90QCiYP0" %}

{% file src="/broken/files/WFyCZSDRfEAvRatRTZ95" %}

{% file src="/broken/files/nlfAfFhbmXjFFV2PMfyN" %}

{% file src="/broken/files/AA1v1UQXlFNhfv2NWztm" %}

{% file src="/broken/files/Xamoz2MbQm91FhmWyue3" %}

{% file src="/broken/files/xmOjO9ODQyOXMjGXnDBR" %}

{% file src="/broken/files/oI5YsMTdTTbYBA6DTsJV" %}

{% file src="/broken/files/hT9Xq0RHML26YoJBEeak" %}

{% file src="/broken/files/DQAJBdhPvi67EE9ISpeJ" %}

{% file src="/broken/files/so0una0vsJMQ0Ye6qPBh" %}

#### Entering information

{% file src="/broken/files/BJ3L4NOPo2Qei0pVEZ42" %}

{% file src="/broken/files/FmRe1miIceFJh6xRaf8h" %}

{% file src="/broken/files/OLKcYacxUeHJKb5AnHjK" %}

{% file src="/broken/files/KCnEQcb5IxIkZdjQZDih" %}

{% file src="/broken/files/wFxWUGnaBozIkzHb64nW" %}

{% file src="/broken/files/BFHk2H7caqeOnqbGYEUO" %}

{% file src="/broken/files/385G4FLDt3uWwhodYlNz" %}

{% file src="/broken/files/w1f8QODoBMGRGz0dJ8Ka" %}

{% file src="/broken/files/gQ5Hk4yGqiQkbkYrs3bY" %}

{% file src="/broken/files/zf16wxNmoHsOZdPITnu9" %}

{% file src="/broken/files/f8LUy53lzSkDFjuHjrj0" %}

{% file src="/broken/files/ix3IIwS6WDQyVoxmQv4X" %}

{% file src="/broken/files/FUGNjzLplpaSjBBXAvve" %}

{% file src="/broken/files/WVgtoR9KnfNj5sPOaP7q" %}

{% file src="/broken/files/4OZX4tkYoFp6PnHnzUc3" %}

{% file src="/broken/files/I77BVHJ3T27yDWsMrDb1" %}

{% file src="/broken/files/sVic04sVAGf2hCCh69Uu" %}

{% file src="/broken/files/sCqtKgpqnSgDVbfP7Uh7" %}

{% file src="/broken/files/wuqRxkkfJ2blJl80NDhO" %}

***

### Contact

**Dan Owens**\
Principal UX Designer

PAR Engagement

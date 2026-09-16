---
description: How and when to implement automatic saving of changes to a form
---

# Autosaving

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](autosaving.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Autosaving means to passively save a user’s form entries without the user performing any deliberate Save/Submit/[Next/Back](multi-step-forms.md#navigation-bar) interaction.  

Autosave triggers may include:

<i class="fa-timer">:timer:</i> Time delay

<i class="fa-eye">:eye:</i> Changing focus

<i class="fa-circle-x">:circle-x:</i> Closing a modal

The other patterns we’ve established in these guidelines limit the opportunity to responsibly recommend autosaving, as our guidelines always call for the user to click or tap on a discrete Save button or action.

In the unlikely event we encounter autosave opportunity in our products, follow these rules:

#### ✅ A [toggle switch](../entering-information/toggle-switches.md) control is the most relevant field type for autosaving

[Toggle switches ](../entering-information/toggle-switches.md)are designed exclusively to convey autosaving, using the metaphor of a light switch (where the lights come on or off instantly upon operating the switch).

#### 🚫 Don’t mix autosave controls on the same page (or modal) as explicit save controls.

That means no toggle switches (an autosave-only field type) on a form that also has checkboxes. A page should be either entirely manual save, or entirely autosave - never a mix of both.

#### 🚫 Don’t use autosave on any form containing checkboxes, radio buttons, or drop-down lists.

These control types are deliberately intended for manual save only.

#### 🚫 Don’t autosave without giving the user feedback that changes were saved successfully.

Use a [success toast](success-notification.md) notification when autosaving.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-autosaving.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

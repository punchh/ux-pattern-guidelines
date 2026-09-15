---
description: Why we almost never disable buttons
---

# Disabled buttons

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](disabled-buttons.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### 🚫 **tl;dr Don't disable buttons**

* Disabled buttons perform poorly in usability testing because users don’t understand why the button is disabled
* Disabled buttons have also been shown to pose a challenge to people with disabilities - with the reasons ranging from poor contrast ratio to poor interpretation by screen readers
* Don't even disable buttons when a form fails field validation

{% hint style="info" %}
One exception is for [Saving state on buttons](saving-state-on-buttons.md) that permits a very temporary disabled state
{% endhint %}

### ✅ Leave form buttons enabled even when an error is present

We keep a form's submit button enabled even when an error validation occurs (including unpopulated fields) because studies have shown too often a user has trouble discerning why the button is disabled. Our Error validation pattern guideline explains how to handle error validation instead.

### ✅ Hide buttons entirely when its action isn’t relevant to the current selection or context

A good example of this is on a table with [bulk actions](../lists-and-tables/bulk-actions.md). Bulk actions are only relevant when one or more item in the table is selected. So when no items are selected, the bulk action buttons aren’t visible at all.

***

### Sources

#### [Usable error message presentation in the World Wide Web: Do not show errors right away](https://www.sciencedirect.com/science/article/abs/pii/S0953543807000100)

Interacting with Computers, 2007

### Inspiration

But not taken verbatim because it lacks an actual study

#### [Disabled buttons suck](https://axesslab.com/disabled-buttons-suck/)

Hampus Sethfors, 2017

#### [Why you shouldn’t include disabled interaction elements in your design system](https://uxdesign.cc/why-you-shouldnt-include-disabled-interaction-elements-in-your-design-system-76a2d4307faf)

UX Collective, 2019

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-disabled-buttons (1).md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

---
description: >-
  How to properly design for fields that should only surface when a specific
  selection is made on another field
---

# Conditional fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](conditional-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Usage

Conditional fields should manifest in accordance with progressive disclosure principles: Only show them when relevant.

That means a conditional field should only be visible when the selection made on another field qualifies it to be present.

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>A user selects an option from the dropdown list that exposes fields specific to that selection</p></figcaption></figure>

### Layout

* Always place conditional fields **immediately following** the field that triggers it. Don’t place it further down in the form (or worse, on another page of a multi-step form) - the user needs to see the condition fire adjacent to the qualifying condition.
* Use a graphical element to indent the conditional field(s) - such as a vertical line spanning their height - to visually emphasize their dependency on and association with the parent field

### Behavior

* **Preserve values** that a user populates into a conditional field even if the conditional field visibility changes. Moreover, if the user changes their mind about the qualifying field, but then changes their mind _again_, we don't want to make the user populate the conditional field from scratch.
* **Hide conditional fields** when the qualifying condition makes it irrelevant. Don't disable it; hide it (progressive disclosure).

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/BFHk2H7caqeOnqbGYEUO" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

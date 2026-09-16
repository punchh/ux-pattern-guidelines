---
description: >-
  How to design the single-select experience when there are quite a few options
  to choose from - and of varying lengths, too
---

# Dropdown lists

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](dropdown-lists.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (162).png" alt=""><figcaption><p>A classic dropdown list field shown with a subheading to organize the values</p></figcaption></figure>

### Implementation

* **Toggle the menu** by clicking anywhere on the input region or spacebar on the keyboard
* **Show up to 6 items**, after which use a scrollbar
* **Don't wrap text** for values in a dropdown list; use [truncation](../reading-information/truncation-and-overflow.md) rules instead
* The dropdown menu **width** is determined by the designer based on the project context - it should accommodate the median value length, or _most_ items without needing [truncation](../reading-information/truncation-and-overflow.md)
* **Focus through items and scroll** the menu using the keyboard’s up and down arrows.
* **Make a selection** using the Enter key (which also closes the menu and populates the field)

### Usage

* Useful with about 7-14 options to choose from, especially if the values are widely variable in length (for fewer options use a [radio button](radio-button-fields.md) or [button group](button-groups.md); for more options use a [combo box](combo-box-fields.md))
* Sometimes with just 2-6 options, a [radio button field](radio-button-fields.md) may be prohibitive because of the context (like as a filter among other filters, where we don't want 1 filter to dominate the vertical footprint). Use a dropdown list instead.
* Another strong case for a dropdown list is when there's a default, likely, or recommended option when the user starts the form
* Set the width of the populated field and menu based on the median value length, or a length that fits _most_ of values in the list. If some subset require [truncation](../reading-information/truncation-and-overflow.md), that’s okay.
* With the menu open and an item in the list selected, the Enter key should select the value and close the menu, but not submit the form.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-dropdown-lists.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

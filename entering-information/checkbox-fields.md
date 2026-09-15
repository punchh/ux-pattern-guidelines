---
description: How and when to use the classic boolean form field control
---

# Checkbox fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](checkbox-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

### Usage

#### As a multi-select field

* When zero, 1, or many options may be selected from a list
* There's a decent likelihood the user will select 1 or more option
* When there are 9 or fewer options total (if there are 10+ options and/or the opportunity to search, use a Multi-Select Combo Box)
* Must have an accompanying Save or Apply button on the form page or modal (if no Save or Apply button, then use a Toggle Switch)

#### As a single-option confirmation field

* When the user needs to acknowledge, approve, or turn on an individual option or feature (but DON’T disabled the button - see Buttons and links)
* Always using a statement phrased in the positive ("Sign up" not "Don't subscribe me")

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption><p>An individual checkbox field with other form field elements like a Tooltip and Description directly on the label</p></figcaption></figure>

***

### Interaction

The entire checkbox AND the text value are interactive to toggle the selection (not just the checkbox).

### Layout

Always align checkbox options vertically along the same left-aligned edge for scannability.

***

### Indeterminate state

Imagine you’re performing a bulk edit.  

One of the options you want to modify across the selection is for a boolean property.

In the bulk of items in your selection, some of them have this boolean property turned on, but others have it turned off.

This means you have “mixed” values for the same property. Represent this state using an indeterminate symbol in the checkbox region (usually a filled checkbox with a hyphen or minus sign across the middle).

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption><p>A checkbox field with an indeterminate selection - implying some items in context are set to checked for this value, and others are not checked for this value</p></figcaption></figure>

Ticking an indeterminate checkbox once turns the property to ‘on’ (checked) for all items.   Now the indeterminate state is gone. It now behaves as a normal check / not-checked checkbox.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/KCnEQcb5IxIkZdjQZDih" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Checkboxes vs. Radio Buttons](https://www.nngroup.com/articles/checkboxes-vs-radio-buttons/)

Nielsen Norman Group, 2004

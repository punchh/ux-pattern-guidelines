---
description: >-
  How to design for the single-select experience when there are only a handful
  of options - each of varying length (asymmetrical)
---

# Radio button fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](radio-button-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption><p>A radio button field with a selection made, and hovering over another option</p></figcaption></figure>

### Usage

* For single-select situations only
* Useful for when it's important for the user to see and read all options
* Intended for about 2-6 options to choose from when each option is of 2+ words and of varying lengths (the options are asymmetrical)
  * When there are more options to choose from, use a [dropdown list](dropdown-lists.md) or [combo box](combo-box-fields.md)
  * When the options are very consistent in length, 1-2 words each, and are largely symmetrical, use a [button group field](button-groups.md)
  * Even with just 2-6 options, you may want to use a [dropdown list](dropdown-lists.md) if the context calls for limiting the total height of the field (vertical footprint) to just one line. For example, a cluster of filters may necessitate limiting vertical height of any individual filter so that it doesn't overcompete with the other filters
* Use a radio button field when there's no default or recommended option. Radio button fields are for avoiding making assumptions and to reduce bias (use a [dropdown list field](dropdown-lists.md) if there's a default)

### Behavior and layout

* Like a [button group field](button-groups.md), the user cannot deselect a selection
* If needed, offer a “no choice” selection. Don’t permit the user to clear their selection by clicking again
* Options always follow a vertical single column layout to maximize scannability (never horizontal!)
* Allow the user to interact with the entire row, icon and text label included to make a selection (not just the radio icon alone)

***

### Variants

When each option in a radio field necessitates its own description, we can offer users a "complex radio button field".

Place descriptions underneath each radio options (in the same pattern as we do for [field labels and descriptions](anatomy-of-form-field.md#description-text)), then encapsulate the entire option (radio icon, option, and description) in some sort of border or fill to group it separate from other options.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption><p>A complex radio button field with a selection made, and hovering over another option</p></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-radio-button-fields.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Checkboxes vs. Radio Buttons](https://www.nngroup.com/articles/checkboxes-vs-radio-buttons/)

Nielsen Norman Group, 2004

#### [Radio buttons UX design](https://uxplanet.org/radio-buttons-ux-design-588e5c0a50dc)

UX Planet, 2016

#### [Radio Buttons: Always Select One?](https://www.nngroup.com/articles/radio-buttons-default-selection/)

Nielsen Norman Group, 2023

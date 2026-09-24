---
description: >-
  How to align form fields to optimize readability and maximize successful and
  accurate form completion
---

# Field alignment and column layout

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](field-alignment-and-column-layout.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Use a single vertical column (a single, straight line path to completion) to maximize readability, completion success, and scalability for narrower viewports.

<figure><img src="../.gitbook/assets/image (133).png" alt=""><figcaption><p>A sample form page depicting all form field elements left aligned along a single column, straight down to the Save button. A reference pane - read-only display field information used to assist filling the form - is okay to be right-aligned next to the form fields.</p></figcaption></figure>

✅ Align all form fields along the left edge, lining up perfectly with the Save button at the bottom of a [single page form](editing-and-saving-forms.md)

🚫 Don't be tempted to add more columns of fields to "fill in white space" or "balance the page" - this harms scannability and increases error rates

✅ If needed, it's okay to include a reference pane containing read-only display information along the right side of fields. We usually manifest a reference pane in a callout box.

### Exceptions

In rare cases, 2 fields side-by-side in the same row are a boon for usability.

#### Logically connected fields

When 2 or more fields are so tightly connected - so much so that in most read-only display formats they are concatenated (strung together on the same line) - present them on a form side by side.

Examples:

* expiry date and CVV for payment inputs
* City and post / postal code

The latter goes beyond logical connection: The value entered for zip code often dictates the city.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-field-alignment.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Form Field Usability: Avoid Multi-Column Layouts (13% Make This Form Usability Mistake)](https://baymard.com/blog/avoid-multi-column-forms)

Baymard Institute, 2018

#### [Form Field Usability: Should You Use Single or Multi-Column Forms?](https://speero.com/post/form-field-usability-should-you-use-single-or-multi-column-forms-original-research)

CXL, 2016

#### [Elements of good form design: single-column beats multi-column forms](https://www.foxit.com/blog/elements-of-good-form-design-single-column-beats-multi-column-forms/)

Foxit, 2021

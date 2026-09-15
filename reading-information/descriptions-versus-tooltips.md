---
description: >-
  How to choose between these 2 form field elements for communicating helpful
  information when filling forms
---

# Descriptions versus tooltips

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](descriptions-versus-tooltips.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Field descriptions

Generally we use the Description element for when the product needs to convey very concise instruction for properly populating a field.

<figure><img src="../.gitbook/assets/image (97).png" alt=""><figcaption><p>This content - explaining how to properly populate the field - meets the criteria for being a field description (rather than a tooltip), and is just about as long as we’d ever want a field description to be.</p></figcaption></figure>

The other utility is for conveying must-know implications that affect user trust or decision making.

The information must still be very concise.

<figure><img src="../.gitbook/assets/image (98).png" alt=""><figcaption><p>Here we’re still in field description territory - the content is very concise and communicates trust-building information</p></figcaption></figure>

### Tooltips

Think of Tooltips as leaning more “nice to know” or “dig deeper” that would clutter the form if always visible.\
\
It could be a bit of extra explanation about why you’re asking for something - helpful but not strictly required to complete the field. Think of it as “documentation lite”.\
\
More examples:<br>

* How data will be used or stored
* Definitions of jargon
* Detailed rules
* Exception cases or situations affecting just a small subset of users
* Anything you can’t articulate so succinctly it could have been a Description

<figure><img src="../.gitbook/assets/image (99).png" alt=""><figcaption><p>The tooltip contains useful information, but not critical to the field’s completion. It mentions exception cases and detailed rules. And it’s way too long to be in the description.</p></figcaption></figure>

### Summary

#### Descriptions

✅ Very concise - usually just a short phrase

✅ Mostly for how to populate the field properly (and often starting with a verb)

✅ Also for must-know trust or decision making implications (but still very succinct!)

#### Tooltips

✅ For when an explanation necessitates 2+ short sentences (or even 1 long sentence)

✅ Better for helpful deep dive info, but not information strictly required to complete the field

✅ Think data usage, storage, security, definitions, detailed rules, exception cases, or anything that you can’t make short enough to be a succinct description

### Decision guide for choosing

<details>

<summary>Is this information critical for most users to correctly complete the field?</summary>

Use the **Description**

</details>

<details>

<summary>Will users need to see this information literally while typing in the field?</summary>

Use the **Description**

</details>

<details>

<summary>Am I writing a Description so long that I have to wonder about how to handle wrapping to a 2nd line?</summary>

Use the **Tooltip**

</details>

<details>

<summary>Am I writing a Description so long I have to wonder about having a period at the end of the sentence?</summary>

Use the **Tooltip**

</details>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/dIt8Q8L3l7NprtnNoigq" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

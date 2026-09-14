---
description: >-
  How to handle excessively long text values and long lists of items in a small
  area
---

# Truncation and overflow

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](truncation-and-overflow.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Single-value truncation

Indicate truncation using an ellipsis (...)

Use End Truncation only. Never in the middle, never in the beginning.

<figure><img src="../.gitbook/assets/image (126).png" alt=""><figcaption><p>Truncate at the end of the value using an ellipsis (...)</p></figcaption></figure>

{% hint style="info" %}
When designing the width of the overarching container (like the dropdown list), it should still be designed to fit _most_ items in a group/list without needing truncation. Truncated items should be the exception case, not the norm. An exception to this might be a data table column where most values can't fit without truncation, though you could fit more than you'd think by wrapping the value in the cell.
{% endhint %}

<figure><img src="../.gitbook/assets/image (127).png" alt=""><figcaption><p>Show the full value while <a href="../hover-interactions.md">hovering</a> anywhere on the truncated value (not just the ellipsis). It's okay to <a href="line-lengths-and-text-wrapping.md">wrap text</a> while displaying the untruncated value, too</p></figcaption></figure>

{% hint style="info" icon="accessible-icon" %}
Screen readers should always read full text without truncation
{% endhint %}

### Lists and multiple value truncation

When conveying read-only information (like in a data table) where there are multiple values for a single cell, use “+n more, where n = the number of values in addition to the ones being displayed.

#### Chips in a table cell

Since chip elements appear in a very limited space, prioritize showing 1 sample value from the set as a regular chip, followed by a text label denoting the presence of additional values (the "+n more" from above).  

How do you choose which sample value should be shown? This will vary by context (for example, it could be by most recent or newest value first), so every feature may have different logic for displaying the sample value.

<figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption><p>In a table cell chip truncation scenario, only the displayed value is illustrated as a chip, whereas the overflow count is plain text. We do this to reduce cognitive load and to avoid having too many competing chips in an already-dense table space.</p></figcaption></figure>

#### Chips in a field or horizontal layout

In a [combo box](../entering-information/combo-box-fields.md) or other horizontal layouts, we encapsulate overflow values in a single collective chip. So 1 regular value first, then 1 truncation value (still styled as a chip) following the same label and logic as above.

<figure><img src="../.gitbook/assets/image (129).png" alt=""><figcaption><p>In this context, a hover tooltp on the overflow chip shows the user some more values. Here, if there were even more values than shown, truncation logic could be applied again.</p></figcaption></figure>



#### Vertical lists

The number of sample items - and the logic behind which items are sampled (e.g. most recent first) - before the truncation indicator will vary by feature depending on context. The overflow text follow the same label and logic as described above.

<figure><img src="../.gitbook/assets/image (130).png" alt=""><figcaption></figcaption></figure>

### Usage checklist

✅ Denote text-based truncation using an **ellipsis**

✅ Apply the truncation at the **end of the value**

✅ [**Hover**](../hover-interactions.md) **anywhere** on the truncated text value to read the full value

✅ The **default width of the overarching container** that houses the truncated item will vary by context, and most of the time should still support the full width of most items in the list/group without needing truncation (exception: tables)

✅ There is **no universal minimum or maximum width**, otherwise follow [text line length guidelines](line-lengths-and-text-wrapping.md) to maximize readability

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-truncation-and-overflow (1).md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

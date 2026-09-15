---
description: How to design for time value capture in a form
---

# Time fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](time-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Interaction

Depending on the context, a time field may be typed only, or typed + dropdown list selected.

Completely free-form type input is typed only.

Interval-based time options are typed and dropdown list selected in one.

When typing, allow valid “clock numerics” on hours and minutes, and only “A” and “P” on AM/PM:  

* When focused on the Hours portion, and the user types “9”, populate 9 as the hour, then advance focus to the Minutes portion.  
* Likewise, if the user types “7” on the minutes portion, populate “07” as the minutes, then advance focus to the AM/PM portion.   
* Allow the user to move from hours to minutes to AM/PM by typing numerics - without pressing tab or any other focus change.  
* Allow the user to skip to the next “segment” (hours, minutes, AM/PM) using the Tab key or by typing ":"

<figure><img src="../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

### Menu interaction

Time options are selectable like any other dropdown list option.

Options are left-aligned, following [column alignment](../lists-and-tables/column-alignment.md) guidelines.

<figure><img src="../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

### Type ahead behavior

In a time field with selectable intervals, as the user types, pop the dropdown list and show matching options, using the entry region as a search field.

<figure><img src="../.gitbook/assets/image (188).png" alt=""><figcaption></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/sVic04sVAGf2hCCh69Uu" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Tailwind CSS Time Picker](https://flowbite.com/docs/forms/timepicker/)

Flowbite, 2026

---
description: How to design for picking a time zone
---

# Time zone fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](time-zone-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Usage

Time zone selectors are powerful form fields for consuming report data, or scheduling work to be done.  

They behave largely like a single-select [dropdown list](dropdown-lists.md) with a [search menu](combo-box-fields.md#menu-invoked-unpopulated-1), but with additional elements and hierarchies for the elements contained within.

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

Generally, a scheduling-based time zone field (like on a form) will be unpopulated by default.   

In a reporting context, there's usually a default value populated from the outset.

### Selecting a time zone

Upon invoking the dropdown menu, the form focuses on the search/filter field, permitting the user to type-ahead to the desired option.

Be sure to support matching on time zone name, abbreviation, and offset (more on this coming up)

<figure><img src="../.gitbook/assets/image (190).png" alt=""><figcaption><p>A time zone field in the open state uses a search menu to facilitate jumping to the desired option</p></figcaption></figure>

#### Organizing time zones

1. Organize by continent (for example, North America) when options span more than 1 continent)
2. List time zones by:
   * Time zone name (omit "standard" and "daylight" and "time")
   * Time zone abbreviation (omit any "ST" and "DT" suffixes that stand for standard and daylight time)
   * UTC/GMT offset hours and minutes<br>
3. Use official time zone names only.
4. Sort by most likely selected continent/region first (when using continental subheadings), then alphabetically by time zone name (not offset number!)

{% hint style="warning" %}
**Don't list time zones by countries or cities** (unless country or city is literally in the official time zone name). This eliminates redundant entries and makes the list more predictable overall (as opposed to making the user guess which cities/countries are or are not included.
{% endhint %}

### Viewing a selected/populated time zone

With the time zone populated, help the user validate the desired choice was made accurately by showing the full time zone name, abbreviation, and offset.  

This helps distinguish linguistically similar time zone names (like the United States’ “Central” time zone, but also Europe’s similarly name “Central European”).

<figure><img src="../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/sCqtKgpqnSgDVbfP7Uh7" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [It’s Time We Addressed Time-Zone Selectors](https://www.nngroup.com/articles/time-zone-selectors/)

Nielsen Norman Group, 2022

---
description: >-
  How to choreograph interactions fired by the mouse cursor hovering over an
  element
---

# Hover interactions

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](hover-interactions.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Do:

✅ For revealing or showing elements like [Tooltips](../reading-information/tooltips.md) that are hidden/not visible without user interaction, wait 500ms after the cursor has come to a complete stop in the hover region before firing

✅ That said, make sure it's obvious that an element has a hover interaction _immediately_ upon the mouse cursor entering the hover region (0ms). We call this an affordance. Some design systems use a glow, stroke, or shadow to signal an element's interactivity. This facilitates discoverability.

✅ Make sure that whatever content was exposed by a hover action persists until _after_ the user has exited the hover zone for a full 500ms without returning. Moreover, keep something like a [Tooltip](../reading-information/tooltips.md) visible for just that brief moment even after the mouse leaves.

✅ The hover zone should include both the originating element, and the exposed content (in the case of a [tooltip](../reading-information/tooltips.md) it would be the tooltip icon, and the tooltip itself)

### Don't:

🚫 Don't show hover content the _instant_ (0 milliseconds) the mouse cursor enters the hover zone. That’s too jarring.

🚫 Don't neglect to include an affordance of an element having a hover interaction immediately upon the cursor entering the hover zone - failure to do so harms discoverability. This could be as simple as the same way a cursor changes when hovering over a hyperlink, coupled with a hover state color or shadow change on the element.

🚫 Don't hide content exposed by a hover action immediately upon the cursor leaving the hover zone. That’s also too jarring.

🚫 Don't forget to include the exposed element (like the [tooltip](../reading-information/tooltips.md) from a tooltip icon) as part of the hover region

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/muKsA4W26Xte7wr8fQiB" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Timing Guidelines for Exposing Hidden Content](https://www.nngroup.com/articles/timing-exposing-content/)

Nielsen Norman Group, 2015

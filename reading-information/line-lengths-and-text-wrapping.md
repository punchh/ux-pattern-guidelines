---
description: >-
  Knowing the right amount of characters to have on each line of text to
  maximize readability
---

# Line lengths and text wrapping

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](line-lengths-and-text-wrapping.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

> **tl;dr:** Wrap body content text and long-form passages after 72 characters. For components with narrow visible containers (like cards, tooltips, and onboarding dialogs), it’s okay to wrap sooner as their containers aren't as wide anyway. For short passages in wide containers (like information banners and footnotes), it's okay to wrap well beyond 72 characters.

In a desktop experience, imagine viewing text content on a particularly wide device, like a super-widescreen cinema scope aspect ratio monitor.

The human eye doesn't do so well attempting to read a string of text that spans the full width of that monitor's size.

In reality, the human eye reads most effectively (readability) when the string of text breaks to the next line much sooner than monitor widths are technically capable of.

<figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption><p>Not too short, not too long: A diagram illustrating the sweet spot for readability and text line length</p></figcaption></figure>

### Why we wrap text

✅ Studies have shown 50-75 characters is optimal for reading text

✅ We’re going with around 72 because its divisible by the base unit of 8 used by some of our products and design systems. If your design system uses a different base unit or foundational body text size, your wrap number may vary.

### Why we don't wrap text much narrower or wider

🚫 Shorter than 50-75 characters risks breaking the reader’s rhythm and cause stress

🚫 Longer than 50-75 characters is at risk of being perceived to be overwhelming and intimidating, and are less likely to be read at all

### Exceptions

Some page level callout-style elements with short passages of text - like [information banners](information-banners.md) - usually they have a background color fill that spans the width of the viewport - are more visually accommodating of longer text line lengths. Remember, if you're following [Grammar, voice, and tone guidelines](grammar-voice-and-tone.md), the text content in elements like these should be very succinct anyway, so should rarely need to reach the point of spanning the entire viewport width on a large desktop monitor, even if the container/background fill spans the full width.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-line-lengths (1).md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Readability: The Optimal Line Length](https://baymard.com/blog/line-length-readability)

Baymard Institute, 2022

#### [Typography](line-lengths-and-text-wrapping.md)

U.S. Digital Service, 2025

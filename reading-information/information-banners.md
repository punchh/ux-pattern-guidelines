---
description: Knowing when and how to call out systemic exception case information
---

# Information banners

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](information-banners.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

### Usage

* Use sparingly to avoid banner blindness - most pages should not have banners 
* Include a back-end expiration date for informational and warning variants  so that it's not forgotten
* Information banners should almost always be at the page level, as they are system-wide in nature and utility. Leave field level information for field descriptions and tooltips. There are rare exceptions that allow for information banners at an individual field level somewhere within body content (more on this below)

### Page level

Information banners usually come right after the page title region - including any element that uniquely identifies the page - like subtitle or other metadata.

If the information is tab-specific, the information banner is the first element underneath the tab bar.

They span the full width of body contents to maximize visibility.

### Feature or field level

In the rare case that a condition is absolutely limited in scope to affecting just a single field on the page, and is NOT a validation error, then there is a case for having a field-level information banner.

Further, if to place the banner at the page level would lead a user to believe that the entire form or process or content is affected, then perhaps a field level banner is a more honest representation of the scope.

<figure><img src="../.gitbook/assets/image (112).png" alt=""><figcaption><p>In this example, an AI chatbot is working fine - but there's information worth raising right where the user types their prompt</p></figcaption></figure>

### Variants

We generally offer information banners in varying color tones to match the psychological significance and impact we wish to achieve.

#### Informational

<figure><img src="../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

A non-urgent piece of status information to signal an out-of-the-ordinary situation, but not urgent or harmful.

In many design systems, these banners are styled with a light blue background fill - just enough contrast against a white background to standout, but with a hue that's psychologically safe and calming.

#### Warning

<figure><img src="../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

Something bad could happen but hasn’t yet - maybe scheduled down time or a long potential wait ahead.

In many design systems, these banners have a more "urgent" looking background fill color, often yellow. It's not to the level of an error (traditionally red), but psychologically impactful enough to make sure it gets attention.

#### Tip

<figure><img src="../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

A strategic tip for making the most out of this page or experience (not for field-level instructions though).

In many design systems, these banners are neutral styled with a grey background fill, so not to overcompete with other content.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/0TbNtp466cBjavFaBLYf" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

---
description: How to capture long form text entry
---

# Paragraph fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](paragraph-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Anatomy

<figure><img src="../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

Paragraph fields share most of the same [anatomy as a regular form field](anatomy-of-form-field.md), but with a couple notable additional elements

#### Hint text

Hint text isn't unique to paragraph fields, but presents a particularly useful opportunity to give the user some inspiration. Populate the hint text with the first few words of a paragraph field's hint text with how their actual input might read, followed by an ellipsis.

#### Character counter

While paragraph fields offer longer form entries, we still need to control for input excess. Show the user how many characters remain from the outset, usually just below the input region. "_n_ characters left" where n=the maximum number of characters is brief and effective.

As they type, update the counter dynamically to show the remaining number of characters.

Once the user gets within 80% of the character count limit, change the counter text color to an urgent or error style (often red).

Allow the user to type beyond the character limit, but keep the counter text red until the user reduces their entry under the counter limit.

When the user has an entry beyond the limit, change the text to "_n_ characters too many" where n=the number of characters beyond the limit.

<figure><img src="../.gitbook/assets/image (169).png" alt=""><figcaption><p>A paragraph field with an entry beyond the maximum number of allowed characters</p></figcaption></figure>

#### Resize grabber

Drag the grabber handle icon in the bottom right of the input region to resize the vertical dimension (height) manually. Users appreciate this functionality for viewing longer inputs in without needing to scroll.

The minimum height is equal to the height of the default instance / variant size being used (more on this later)

The maximum height should not exceed your 85% of your user base's median desktop viewport height. For example, in an environment where the median viewport device height is 900px, make the maximum paragraph resize height equal to about 764px.

The horizontal dimension (width) cannot be resized, and is determined by the context (i.e. the designer should make it so wider anticipated inputs are wide, and narrower anticipated inputs are narrow).

<figure><img src="../.gitbook/assets/image (170).png" alt=""><figcaption><p>The resize grabber allows the user to manually increase the height of a paragraph input field region</p></figcaption></figure>

### Variant default sizes

The designer should choose an initial height that matches the anticipated user input.

For example, when the input is only expected to be a brief phrase or sentence, use a smaller footprint paragraph field.

When the user needs to enter many sentences, use a larger footprint input region.

Make sure the character counter has a corresponding number of characters to match the height (moreover, smaller paragraph fields would have a lower number of supported characters, and larger paragraph fields would have a higher number of supported characters).

<figure><img src="../.gitbook/assets/image (171).png" alt=""><figcaption><p>In this design system, there are 3 variants for paragraph fields to accommodate varying anticipated input lengths</p></figcaption></figure>

### Interaction and behavior

As the user types, small and medium input regions grow vertically, maxing out at a design system's largest variant paragraph field.

<figure><img src="../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/f8LUy53lzSkDFjuHjrj0" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

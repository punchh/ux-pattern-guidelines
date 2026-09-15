---
description: >-
  How and when to leverage the classic progressive disclosure technique for
  showing and hiding information.
---

# Accordions

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](accordions.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Accordions are ideal for housing supplementary text information that's not critical to the core objective of a page or feature. Think of it as a mechanism to access "further reading" or information relevant to a subset of a page's target audience.

***

### Anatomy

<figure><img src="../.gitbook/assets/image (206).png" alt=""><figcaption><p>3 accordions, each in a closed state</p></figcaption></figure>

#### Icon

The accordion title is prepended by an icon - often a chevron.

In the closed state, the chevron points right.

In the open state, it points down.

**Why not use a +/- icon?**

While studies show a +/- icon is most effective for conveying the presence of an accordion action, "+" and "-" are also frequently used for other actions like adding and removing respectively. The potential confusion between the 2 functions isn't worth the tradeoff. For that reason we go with the 2nd most effective icon: the chevron.

**Why pointing to the right for closed, and downward for open?**

Studies show that these directions most reliably communicate to users the presence of underlying content without navigating away from the page. Notably, these icons are state icons rather than action icons. Meaning: Since accordions don't submit a form nor execute a transaction, we're safe to use state icons (whereas buttons for form submissions and transactions necessitate using action icons).

**Why a prepended icon and not a trailing icon?**

We use a leading prepended icon to more reliably signal to the user that they may click or tap anywhere in the accordion "row" to fire the accordion interaction. Studies have shown that trailing icons - especially icons that are the far right side of the accordion row - lead users to believe they must click on a smaller target to fire the interaction. A prepended icon is more effective at saying "click _anywhere_ on the icon or text title".

#### Title

Effectively a subheading level.

#### Click/tap region

Note that the entire region spanning the icon and title, filling the width of the entire container (up to the [line length](line-lengths-and-text-wrapping.md)) serves as the click/tap region. This is the maximize the click target for the user.

***

### Do

✅ Use for text content

✅ 1 topic per accordion

✅ Allow the user to expand more than 1 accordion at at time

✅ Include a expand all/collapse all link button at the bottom of an accordion array when there are 3 or more accordions

### Don't

🚫 Don't include images, video, media or any non-text content inside an accordion (downloadable files are okay)

🚫 Don't include multiple topics

🚫 Don't prohibit the user from opening more than 1 accordion at a time (so don't autocollapse an open accordion when opening a different one)

🚫 Don't use accordions on table rows. Use a side panel or navigate to a new page to show details for content in a table row.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/Etl9fBvJYGw2cUHkqjMf" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

[Testing accordion designs and iconography](https://www.viget.com/articles/testing-accordion-menu-designs-iconography/)

Viget, 2015

[Where to place your accordion menu icons](https://uxmovement.com/navigation/where-to-place-your-accordion-menu-icons/)

UX Movement, 2016

---
description: Choosing the right navigation behavior for the right context
---

# Opening links in same vs new tab

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](opening-links-in-same-vs-new-tab.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Links (and buttons!) offer the opportunity to open the destination page in either the same browser tab (or window), or a new one (preserving the original page).  

We should be thoughtful about designing a predictable but flexible experience for users depending on the context.

### Load in the same tab

✅ The destination is still within the same website, application, or product. This will likely be the overwhelming majority of cases.

### Load in a new tab

✅ The destination is “off site” (different domain name or entirely different application or product)

✅ The destination is on site, but navigates to a binary file that traditionally opens in a 3rd party non-browser application (like PDFs and media files). Some browsers interpret this as a download.

### Do

✅ Give the user the control to choose to open any link or button in a new tab (using their browser’s native context menu) to facilitate manual comparison - even for on-site links that don’t open in a new tab by default

✅ For off-site links, **include iconography to the right of text** to convey that it opens in a new tab by default

<figure><img src="../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

### Don't

🚫 Don't prohibit the user from using their browser’s native right-click context menu to access “Open in a new tab” options, even for links designed to open in the same tab by default.

<figure><img src="../.gitbook/assets/image (73).png" alt="" width="563"><figcaption></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/4zILgXpt6ABexkjOq0fM" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Links and Hypertext: Links to New Windows, Pop-ups, Other Frames, or External Web Sites](https://webaim.org/techniques/hypertext/hypertext_links#new_window)

Institute for Disability Research, Policy, and Practice, 2024

#### [Opening Links in New Browser Windows and Tabs](https://www.nngroup.com/articles/new-browser-windows-and-tabs/)

Nielsen Norman Group, 2020

#### [Should Links Open in New Windows?](https://www.smashingmagazine.com/2008/07/should-links-open-in-new-windows/)

Vitaly Friedman, 2019

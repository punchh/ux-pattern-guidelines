---
description: Giving users feedback about successful completion of a form or action
---

# Success notification

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](success-notification.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

After the user submits a form or completes and action, it's important for the system to let the user know whatever transaction they attempted was completed successfully.

Our vehicle for this feedback is a success toast.

<figure><img src="../.gitbook/assets/image (131).png" alt=""><figcaption><p>A success toast floats over the top of page content, sticking to one position, centered horizontally, and offset vertically to favor the eye level (so not quite vertical middle - about 10% from the top of the viewport)</p></figcaption></figure>

Refer to [Grammar, Voice, and Tone guidelines](../reading-information/grammar-voice-and-tone.md) for how to write effective success toast copy.

### Implementation choreography

✅ Fade IN over 500ms.

✅ Persist for 5 seconds (add 1 second of persistence for every 120 words).

✅ Fade OUT over 2000ms

✅ Stack subsequent notifications vertically (adding to the bottom). After the previous notification fades out completely, slide the next notification(s) up a slot, moving over 500ms. Move multiple notifications together in a single animation

{% hint style="info" icon="accessible-icon" %}
New to WCAG 2.1, satisfying [Guideline 4.1.3](https://www.w3.org/TR/WCAG21/#status-messages) requires that:<br>

* In content implemented using markup languages, status messages can be programmatically determined through role or properties such that they can be presented to the user by assistive technologies without receiving focus.
* Using ARIA techniques such as role alert and aria-live, toast messages can be made available for screen reading technologies as soon as they are displayed.
{% endhint %}

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-success-notification.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Typography](https://designsystem.digital.gov/components/typography/#typefaces)

U.S. Digital Service, 2025

#### [Web Content Accessibility Guidelines (WCAG) 2.1](https://www.w3.org/TR/WCAG21/#status-messages)

W3C, 2028

---
description: >-
  How to give users feedback and confidence that their changes are being saved
  when saving, submitting, or advancing a multi-step form
---

# Saving state on buttons

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](saving-state-on-buttons.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src=".gitbook/assets/image (57).png" alt=""><figcaption><p>On click of a Save button or equivalent, the state and text changes briefly</p></figcaption></figure>

✅ Make it so all buttons that perform a "Save" or "Submit" (or similar) action exhibit a Saving state on click or tap. This is for single page forms and [multi-step](multi-step-forms.md) forms that commit a record or execute a transaction, but not temporary state forms like applying filters.

✅ On click or tap, briefly change the button state to disabled during the saving state to prevent subsequent clicks/taps

✅ Prepend an animated spinner/loader icon

✅ Change the text to "Saving..." or whatever the equivalent present participle verb is (like "Creating..." or "Sending...")

✅ Persist for a minimum of 2 seconds

{% hint style="info" %}
Even with a very low latency action, product, or network environment, show and persist the saving state button for a minimum of 2 seconds even if that means using an artificial delay before loading the next page.
{% endhint %}

### Application

* Save buttons
* Submit buttons
* Next/Back buttons (multi-step form buttons)
* Save as draft buttons
* Any where the user wants confidence that their work won’t be lost

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src=".gitbook/assets/ux-saving-state-buttons (1).md" %}

[Learn how to use](resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [When You Need to Show a Button’s Loading State](https://uxmovement.com/buttons/when-you-need-to-show-a-buttons-loading-state/)

UX Movement, 2019


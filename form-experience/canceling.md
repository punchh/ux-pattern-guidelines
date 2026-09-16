---
description: >-
  How we offer the user a chance to cancel changes - and how we warn them about
  potentially undesired consequences
---

# Canceling

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](canceling.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

### Anatomy of a cancel confirmation dialog

<figure><img src="../.gitbook/assets/image (56).png" alt=""><figcaption><p>Cancel confirmation dialogs should manifest as a <a href="../layout-and-navigation/modals-lightboxes-and-dialogs.md">modal lightbox</a></p></figcaption></figure>

Cancel confirmations should manifest as a [modal confirmation dialog](../layout-and-navigation/modals-lightboxes-and-dialogs.md).

#### Title

Phrased as a succinct question, repeating the clicked action text. "Cancel changes?" makes a good default.

#### Description

Briefly and directly explain the consequence of confirming the selected action. "The changes you made will be lost" makes a good default.

#### Primary button

This is the button the user chooses to confirm the cancellation. Make deliberate use of the word “yes”, and repeat the verb “cancel” for emphasis. "Yes, cancel changes" makes a good default.

#### Secondary button

Phrased using conversational language, and without using the word “cancel” again to distinguish it from the primary button. "Nevermind, keep working" makes a good default.

#### Close button

Used to close the confirmation dialog, returning the user to the underlying form with unsaved changes

***

### Usage

✅ Offer a labeled **cancel action** whenever a user is in a create or edit experience (meaning the user is genuinely creating or modifying a record

🚫 Don't offer cancel on a temporary state form like filters, filtering, or search

✅ Only offer a cancel confirmation prompt when the user has modified the form by populating a field or changing a value

🚫 No need for a confirmation prompt on a form with 3 or fewer fields AND all fields are short length values or 1-click controls

***

### Inspiration

But not taken verbatim

#### [Are you sure you want to do this? Microcopy for confirmation dialogues](https://uxdesign.cc/are-you-sure-you-want-to-do-this-microcopy-for-confirmation-dialogues-1d94a0f73ac6)

UX Collective, 2019

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-canceling.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

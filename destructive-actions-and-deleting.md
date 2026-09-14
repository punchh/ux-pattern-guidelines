---
description: How we protect the user from inadvertently performing destructive actions
---

# Destructive actions and deleting

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](destructive-actions-and-deleting.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Any time we offer a user the chance to permanently delete a record or item, we should confirm their intent. These are often irreversible changes, so better to err on the side of caution.

<figure><img src=".gitbook/assets/image (53).png" alt=""><figcaption><p>We often place destructive action inside of an overflow menu (3 vertical dots icon button) to reduce accidental taps, and because it's a seldom used action</p></figcaption></figure>

### When to offer deletion

✅ When browsing a list of items on a list page

✅ When examining an item's detail page



### How to label

✅ Literally use the word "delete" when labeling the action button or link that leads to permanently destroying a record. Don't be ambiguous or gentle about it; users need to understand the severity

{% hint style="info" %}
Use the word "**Remove**" for removing an selected item from a list. For example, if the user is building an array of lookup values (like selecting tags, or populating a list of users for a permission), the user may want to remove an item - meaning disassociate it from the record being built. That doesn't delete the item from the system, though.
{% endhint %}

### How to confirm

✅ Always follow a click of a delete action with a confirmation prompt - including the same destructive verb on the positive confirmation button.

### Anatomy of a delete confirmation dialog

<figure><img src=".gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

Delete confirmations should manifest as a [modal confirmation dialog](modals-lightboxes-and-dialogs.md).

#### Title

Phrased as a succinct question, repeating the clicked action text

#### Description

Briefly and directly explain the consequence of confirming the selected action

#### Primary button

This is the button the user chooses to confirm the cancellation. Make deliberate use of the word “yes”, and repeat the verb “delete” for emphasis.

#### Secondary button

Phrased using conversational language, and without using the word “delete” again to distinguish it from the primary button

#### Close button

Used to close the confirmation dialog, returning the user to the underlying form

***

### Bulk delete

Refer to [Bulk Action guidelines](lists-and-tables/bulk-actions.md) for the nuances of the bulk deletion experience.

***

### Inspiration

But not taken verbatim

#### [Are you sure you want to do this? Microcopy for confirmation dialogues](https://uxdesign.cc/are-you-sure-you-want-to-do-this-microcopy-for-confirmation-dialogues-1d94a0f73ac6)

UX Collective, 2019

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src=".gitbook/assets/ux-destructive-actions (1).md" %}

[Learn how to use](resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

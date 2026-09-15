---
description: >-
  Performing the same action on multiple selections at one time - usually in a
  table or list
---

# Bulk actions

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](bulk-actions.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

### Context and usage

Bulk actions are almost always in the context of a list or table.

Imagine the user is looking at items in a list.

The user needs to perform some action on a group of items together (usually some subset of the list).

Without access to some kind of bulk actions interface, the user would have to perform the desired action to each item one at a time.

Instead, when the experience supports bulk actions, the user can apply a single action to multiple items in one interaction.

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption><p>A bulk action bar remains hidden until at least 1 item is selected</p></figcaption></figure>

{% hint style="warning" %}
Only selections in the current view can invoke / are affected by bulk actions. We don't apply bulk actions to items on another page of pagination, nor items filtered out by any actively applied filters.
{% endhint %}

### Anatomy of a bulk actions bar and experience

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

Keeping in mind progressive disclosure, the user only sees the bulk actions interface when they've selected 1 or more items. So as a pre-requisite, the list or table must have some mechanism for the user to select items - usually via a leading checkbox at the start of each item's row or card.

Why do we surface the bulk action interface with just 1 item selected since that's not really "bulk"? Mostly to enhance discoverability of bulk actions since its interface remains hidden until 1 or more items is selected.

We'll call this bulk actions interface a "bulk actions bar".

The action bar contains a counter, action buttons, and a clear selection link.

Ideally, the action bar floats and sticks near the bottom edge of the viewport (centered), and is presented in a high contrast visual style on top of the bottom most item in the list.

The moment all selections are de-selected (or eliminated by filters), the bulk action bar disappears (it does _not_ persist without selections present).

#### The item and checkbox

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

Not part of the bulk actions bar but essential to the bulk actions experience, checkboxes in a table are for bulk operations only. Don’t use checkboxes in a table to set status or any other value for individual items to avoid conflict with the universal bulk actions pattern.

#### Counter

<figure><img src="../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

Usually left-aligned in the action bar, the counter tracks the number of items selected, regardless of eligibility for any actions (more on this coming up). "_n_ selected" is a good generic text label. where n= the count of items selected.

#### Button cluster

<figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

Usually centered in the bulk action bar. Each button appears as long as at least 1 item in the selection is eligible for the action. It is NOT a requirement for ALL items in the selection to be eligible for the action to appear.

Read more about [handling mixed eligibility](bulk-actions.md#handling-mixed-eligibility).

#### Clear selection link button

<figure><img src="../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

Usually right-aligned in the action bar, allow the user to bulk de-select any items - which would in turn hide the bulk actions bar.

***

### Handling mixed eligibility

What if only _some_ items in the user’s selection are  eligible for an action?  

When the user initiates an action on a bulk selection containing items of mixed eligibility, the system should let the  user know before proceeding with that action via an [acknowledgement prompt](../layout-and-navigation/modals-lightboxes-and-dialogs.md#acknowledgement-with-1-2-lines-of-text). Something along the lines of:

> We skipped 3 items in your selection because they’re ineligible for that action.

Then list the reason for ineligibility, followed by the names/titles of ineligible items.

To emphasize: this is _not_ an error condition. Eligible selections  get processed, and ineligible ones don't.

For mixed eligibility selections for a destructive action, see [bulk deletion](bulk-actions.md#bulk-deletion) below.

### Bulk deletion

When performing a bulk delete, we generally follow the same principles as defined by [Destructive Actions guidelines](../form-experience/destructive-actions-and-deleting.md) - that means showing a [confirmation prompt](../layout-and-navigation/modals-lightboxes-and-dialogs.md#confirmation-prompt) to give the user a chance to back out before doing something irreversible.

Here are some nuances unique to bulk deletions:

<figure><img src="../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

#### Title bar

Generically use the label:

> Delete _n_ items

Where n=the number of items selected in the list.

For the remaining elements on the [confirmation prompt](../layout-and-navigation/modals-lightboxes-and-dialogs.md#confirmation-prompt), use the guidance provided in [destructive actions](../form-experience/destructive-actions-and-deleting.md).

After confirming to delete, the system should show an [acknowledgement prompt](../layout-and-navigation/modals-lightboxes-and-dialogs.md#acknowledgement) if there were any ineligible items in the selection. See "[Handling mixed eligibility](bulk-actions.md#handling-mixed-eligibility)" above for details.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/RrIXZs4ycfdcUiLn6Arj" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

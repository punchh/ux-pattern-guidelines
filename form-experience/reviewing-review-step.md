---
description: >-
  How to help users review their entries before submitting or finalizing a
  multi-step form
---

# Reviewing / review step

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](reviewing-review-step.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

After going through a [multi-step form](multi-step-forms.md), it's important that we let users review their entries before committing or finalizing the content they've created.

To facilitate, we offer a distinct pattern for reviewing information entered on previous steps, and allowing for easy navigation back to corresponding sections to make updates.

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption><p>The flow for navigating from the review step back to an earlier step</p></figcaption></figure>

### Organization

We organize information on the Review step page of a [multi-step form](multi-step-forms.md) by Step Title. Underneath each step title, we list the field name, and the value populated by the user in read-only / display-only format.

Excessively long values like paragraph fields can be shown as [truncated](../reading-information/truncation-and-overflow.md) initially, with a toggle to Read more / Read less.

Binary file formats like images manifest as a file name and Preview link (to open a modal window showing the content in full).

At the bottom of each Step section, we offer a button to Revisit, which navigates to the corresponding step page in edit mode for making changes.

### Revisiting a section

The edit experience of a section accessed from the Revisit button of the review step is largely unchanged - except for the navigation bar.

Since the user is coming from the review step, we allow them only 2 distinct actions: "Save and return to review", and "Nevermind - return to review" (which is effectively canceling the Revisit action).

#### When changes trigger new conditional fields on subsequent steps

During a revisit, if the user edits a field that introduces a new conditional field on a subsequent step of the form, fire a confirmation prompt letting the user know there's more work on a later step. Allow them the choice of jumping to said step ("Save and go to next step"), or staying put ("Stay here and keep working").

If the user chooses to jump to the next affected step, the navigation bar persists as the Revisit state mentioned above.

<figure><img src="../.gitbook/assets/image (45).png" alt=""><figcaption><p>In this flow, the user has made changes during a Revisit from the Review Step. One or more of the changes has introduced a new conditional field on a subsequent step, so the system prompts the user with the illustrated choice.</p></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-review-step.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

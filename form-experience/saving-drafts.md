---
description: How to facilitate saving incomplete work on a form
---

# Saving drafts

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](saving-drafts.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Sometimes a user needs to save incomplete information on a form in progress, go perform another task, then return to the form later.

For that reason, we should support the ability to save a draft in more complex forms - especially multi-step forms.

<figure><img src="../.gitbook/assets/image (138).png" alt=""><figcaption><p>In a multi-step form, the "Save and close" button facilitates saving as a draft</p></figcaption></figure>

### [Multi-step forms](multi-step-forms.md)

Surface a "Save and close" button as soon as the user has populated minimally required information for identifying the record or item they're creating. This is usually on the 2nd step and onward, but possible on the 1st step if sufficient identifying information has been entered. Just be mindful about not letting users inadvertently save nearly blank drafts so not to clutter up a list page with effectively empty items.

#### Save and close button

Clicking the Save and close button navigates the user to the originating page (usually a list page), and pops a [success toast notification message ](success-notification.md)indicating "draft saved successfully".

#### Back and Next buttons

In a mutli-step form, understand that the Back and Next buttons also save a draft in progress. They just don't navigate the user back to the list page. Reinforce this behavior by implementing [Saving state on buttons](saving-state-on-buttons.md).

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/oI5YsMTdTTbYBA6DTsJV" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

---
description: When and how to break a form experience into multiple pages or steps
---

# Multi-step forms

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](multi-step-forms.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Studies have shown better form completion rates and accuracy when many fields are spread out across multiple pages. There's also noticeable psychological comfort with tackling fewer fields on a single page, as the experience feels less daunting and overwhelming when entries are broken up into digestible chunks.

### Number of fields per step

Strive for at most 4-6 fields per step in a first draft. It's okay to have as few as 1 field on a single step if the particular field is highly impactful on the content being created, or necessitates deep thought or preparation.

Available secondary research overwhelmingly shows the efficacy of this approach, but those studies are almost always performed using B2C conversion forms and seldom focused on the SaaS/enterprise application context.

For that reason, usability test and only add more fields per step as indicated by your results.

### Multi-step form anatomy

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption><p>When moving from step 1 to step 2 in a multi-step form, observe that new controls become available - like a Back button, and S<a href="saving-drafts.md">ave and close for drafts</a></p></figcaption></figure>

#### Stepper

Help the user understand their progress in the overall form using a [stepper](steppers.md).

Learn more about stepper anatomy and experience in our [Steppers pattern guideline](steppers.md).

#### Navigation bar

At the bottom of the form the user accesses navigation controls for the form.

The first step only offers Next and cancel.

Subsequent steps offer Back, and sometimes the opportunity to [save a draft (Save and close)](saving-drafts.md).

The Back and Next buttons should exhibit [Saving state on buttons](saving-state-on-buttons.md) when clicked.

The Back and Next buttons are oriented left and right at the outer edges of the navigation bar respectively to match the linear progression of the form left to right. Position and alignment of these buttons matter - review the [Button Alignment guidelines](../layout-and-navigation/button-alignment.md#multi-step-forms).

### The Review Step

Finish most multi-step forms with a review of information entered on previous steps. Refer to the [Review Step guideline](reviewing-review-step.md) for more details on this experience.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/AA1v1UQXlFNhfv2NWztm" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Better Form Design: One Thing Per Page (Case Study)](https://www.smashingmagazine.com/2017/05/better-form-design-one-thing-per-page/)

Venture Harbor, 2023

#### [Why Multi-Step Lead Forms Get up to 300% More Conversions](https://www.smashingmagazine.com/2017/05/better-form-design-one-thing-per-page/)

Smashing Magazine, 2017

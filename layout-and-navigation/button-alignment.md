---
description: >-
  How to align buttons on forms to maximize scannability and reduce form
  submission errors
---

# Button alignment

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](button-alignment.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Single page forms

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption><p>A single page form with a bottom-left aligned submit button. This example uses a floating sticky "save bar" for its submit and cancel buttons</p></figcaption></figure>

Align the primary action button left, at the bottom of the form, after the fields.

We do this to prioritize single-column, straight line vertical scanning - just like the [fields are aligned](../form-experience/field-alignment-and-column-layout.md). This is the submit button, often labeled "Saved".

Secondary actions - often the "Cancel" button - sit next to the submit button, on the same row, just to the right.

{% hint style="info" %}
In products with form pages long enough to have scrolling, you may find it useful to design a floating "save bar" that sticks near the bottom edge of the form, no matter what the scroll position. That way the user has immediate access to submit regardless of where they are on the page.
{% endhint %}

### Multi-step forms

In [multi-step forms](../form-experience/multi-step-forms.md) we prioritize the convention of rightward linear progression to determine button alignment.  

"Next" or equivalent buttons aligned at the bottom-right of the page.

"Back" or equivalent buttons at the bottom-left of the page.

The left-to-right linear alignment (for Back and Save buttons respectively) also matches the [stepper navigation pattern](../form-experience/steppers.md) present on all multi-step forms.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>A multi-step form on the first step (so it has a Next button, but not Back button)</p></figcaption></figure>

In a multi-step form, we keep the Cancel button aligned to the bottom left. We move the Next button (form submit) to the bottom right.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption><p>A multi-step form on the 2nd step - so it has a Next button AND a Back button in its save bar / region</p></figcaption></figure>

On steps 2 and onward of a multi-step form, a Back button appears in the bottom left, just before the Cancel button. Next button stays on the right.

Buttons that support the submit ("Next") button - like [Save and close for drafts](../form-experience/saving-drafts.md) - can come just before the Next button on the bottom right.

### Confirmation prompts and dialog boxes

This is not a form. The user isn’t populating any values.

#### [Acknowledgement](modals-lightboxes-and-dialogs.md#acknowledgement) popup

For this experience - almost always in a [modal](modals-lightboxes-and-dialogs.md) - we center align the acknowledgement button at the bottom. We often label this button [casually](../reading-information/grammar-voice-and-tone.md) as "Got it".

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption><p>A confirmation pop up modal</p></figcaption></figure>

#### [Confirmation](modals-lightboxes-and-dialogs.md#confirmation-prompt) popup

A primary button (confirm) and secondary button (decline) pair, we center align these buttons at the bottom.

A [generic casual ](../reading-information/grammar-voice-and-tone.md)way we sometimes label these buttons is "Let's go" and "Nevermind" respectively.

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption><p>An acknowledgement modal</p></figcaption></figure>

### [Modal forms](modals-lightboxes-and-dialogs.md#id-1-field-form)

Unlike forms on a regular page, eye tracking studies have shown that in a modal window, forms are more effectively filled out when the buttons are aligned to follow the "z pattern".

That means the form submit button (usually labeled "Save") is aligned bottom **right**, with the Cancel button just next to it on its left (still bottom-right aligned overall).

This holds true for any number of fields on the modal window - 1 or many.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>A modal form showing the z pattern for <a href="../form-experience/field-alignment-and-column-layout.md">field</a> and button alignment</p></figcaption></figure>

### Side panels

Sometimes we invoke a form as a slide out side panel from the right edge of the screen. A modal panel of sorts.

Center align buttons, and stack vertically if there are more than one (primary button on top). Make this region a sticky frame that stays in place as the user scrolls the contents on the side panel.

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption><p>A slide out side panel form showing center aligned buttons</p></figcaption></figure>

### In-field buttons

Refer to [field anatomy guidelines](../entering-information/anatomy-of-form-field.md), or for an exception case, [phone number fields](../entering-information/phone-number-fields.md).

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

#### Use this guideline with AI tools

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-button-alignment.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources and inspiration

#### [Button Ambiguity: Alignment & Order](https://medium.theoremone.co/button-ambiguity-alignment-order-a42736e25334)

TheoremOne, 2021

#### [Buttons on the web: placement and order](https://uxdesign.cc/buttons-placement-and-order-bb1c4abadfcb)

UX Collective, 2019

#### [Primer Interface Guidelines (Github design system)](https://primer.style/design/ui-patterns/saving)

Github, 2023

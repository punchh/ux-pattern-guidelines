---
description: How to communicate the presence of errors in a form submission
---

# Error validation

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](error-validation.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Validation types

#### Inline validation (don't do this)

Gives the user feedback field by field when changing focus to another field (or even before that), before the user even attempts to submit the form. **We don't do this** because studies have shown inline validation causes:

* premature error messages before the user has had a chance to finish or validate their own input
* higher cognitive load during input
* false negatives on complex fields
* disruption for assistive technology users (accessibility issues)

{% hint style="warning" %}
Exception: [Confirm password fields](../entering-information/password-fields-and-sign-in.md#with-complex-password-requirements) should validate inline the moment the user changes focus
{% endhint %}

#### Summary validation or form-level validation (do this)

Gives the user feedback about any errors only when they attempt to [submit the form](editing-and-saving-forms.md).

### Experience

#### On the submit button

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

**Pop an error-styled tooltip on the submit button**

Tell the user how many errors need to be fixed.

Position the tool-tip adjacent to the submit button at top, right, or where ever there's room for it at the current scroll position.

Don't automatically scroll.

Persist it until the user focuses on a field.

**Shake the button using a bounce effect**

Briefly animate/shake the button to reinforce inability to submit the form under the current conditions. 

Bounce <- 1 REM over 50ms. \
Bounce -> 2 REM over 50ms. \
Bounce <- 2 REM over 50ms. \
Bounce -> 2 REM over 50ms. \
Bounce <- 2 REM over 50ms. \
Bounce -> 1 REM over 50ms.   \
\
Total duration 300ms.\
\
Button finishes in same position as start.

**Don't disable the button**

See our pattern guideline for [Disabled buttons](disabled-buttons.md) to learn why.

#### With a toast

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption><p>An error toast appearing near the top of a form</p></figcaption></figure>

Briefly state whatever action couldn't be completed (for example: "We couldn't save your changes"), then list the affected fields and corresponding error messages for each one.

We only need to use the toast message when there are 4 or more fields on a form page. If omitting the error toast, then the experience should certainly have the [submit button shake](error-validation.md#on-the-submit-button).

For persistence and timing of an error toast, use the same guidelines as a [Success notification toast](success-notification.md).

#### On the field

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption><p>Anatomy of a text field under an error condition state</p></figcaption></figure>

During an error condition, style the affected field's label text and input region border (if applicable) using a red or "danger" equivalent color.

Just below the input region on a new line, state the error validation message (usually with a preceding error-style icon, too).

{% hint style="info" %}
Your design system may have slightly different aesthetic treatment and styling for a field in error state - that's okay.
{% endhint %}

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-error-validation.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Inline Validation in Web Forms](https://alistapart.com/article/inline-validation-in-web-forms/)

Luke Wroblewski via A List Apart, 2009

#### [Usability Testing of Inline Form Validation: 31% Don't Have It, 4% Get It Wrong](https://baymard.com/blog/inline-form-validation)

Baymard Institute, 2024

#### [Designing Toast Messages for Accessibility](https://sheribyrnehaber.medium.com/designing-toast-messages-for-accessibility-fb610ac364be)

Sheri Byrne-Haber, 2019

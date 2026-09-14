---
description: Showing a user their progress and position in a multi-step form
---

# Steppers

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](steppers.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src=".gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

### Anatomy

The stepper should contain the following elements and affordances:

**Number for each step**

Gives the user confidence they're making progress

**Name for each step**

Helps the user anticipate the type of content expected. Shoot for 1-2 words max.

**Description of each step**

Optional. Shoot for 2-4 words max.

**Progress status for each step**

Helps the user understand their position and progress in the flow.

* Complete
* Current
* Future
* Error

### Error handling

If the multi-step form you're working with supports advancing to subsequent step when errors are present on previous steps (this will vary by business context), have an affordance on the stepper to indicate as much.

<figure><img src=".gitbook/assets/image (144).png" alt=""><figcaption><p>The step name with an error condition shows styling indicative of error or danger, with a simplified error message and icon in place of the step description</p></figcaption></figure>

### Page orientation and layout

* main body region
* above the form
* center aligned
* no max width (unlike the regular body content beneath it)
* okay to span the entire body container (unlike the rest of body content which is usually limited by [line length)](reading-information/line-lengths-and-text-wrapping.md)

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src=".gitbook/assets/ux-steppers (1).md" %}

[Learn how to use](resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

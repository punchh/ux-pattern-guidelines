---
description: >-
  Introducing users to a new feature (either new for the product, or new for
  them)
---

# Onboarding

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](onboarding.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

### Usage

Onboarding elements are tempting for product managers to show off new work, but ideally an experience should be intuitive without needing extra instructions at all.

One-time instructional messages are more likely to signal a discovery design flaw rather than serve a genuine utility.

It's better to usability test and iterate before introducing onboarding.

#### If you must still use onboarding, use it incredibly sparingly

Onboarding elements have a high interaction cost and a low memory retention rate.

#### Fire an onboarding element once - then never again

Onboarding elements are one-time experiences. Don’t re-fire the same onboarding element twice for the same user.

### When to use onboarding

#### ✅ A feature is dependent on an up-front preference setting

One of the only good reasons to use onboarding is when the user needs to set custom tailored preferences to begin work.

#### ✅ You’re introducing a truly never-before-seen pattern or feature

Remember when banks started letting users take a photo of a paper check to make a deposit? That’s a good example of a novel pattern warranting onboarding (the first time...but never again).

#### ✅ You’re introducing a subtle new feature on an existing page

Imagine introducing a new data element on an existing record detail view page. It may not warrant top placement in the information hierarchy, and its composition may just be another piece of text among other pieces of text on the same page: users might not even catch its presence if they’ve developed “pattern blindness”.

### What not to do with onboarding

#### 🚫 Chains of tooltips

Studies have shown forced-chain onboarding tooltips (a series of tooltip style onboarding elements the user must click through in sequence) make users dismiss them more quickly and without reading or retaining information.

#### 🚫 Implement without an overlay or highly contrasted visual style

Don’t let any tooltip implementation be introduced using a visual style that blends in with the underlying interface. Fade out the rest of the background like you would with most modal windows.

### Types

#### Modal style

Functionally, modal style onboarding experiences are just a [modal](onboarding.md#modal-style) that appears automatically upon loading opening a app or one of its pages.

It usually contains at least one button on it to dismiss the onboarding ("Got it" is a good casual way to label the button), and sometimes an accompanying button to direct the user to "Read more" about the feature, or to "Try now".  The destination and label may vary by your product's context.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

#### Tooltip style

[Tooltip](tooltips.md)-style onboarding helps users focus on a specific area of a page. In implementation, they probably look more link a very small card with a notch pointing toward the relevant element. There's also at least one button on it to dismiss the onboarding ("Got it" is a good casual way to label the button), and sometimes an accompanying button to direct the user to "Read more" about the feature, or to "Try now".&#x20;

It appears automatically upon loading the page.&#x20;

While present, the page background is dimmed like a [lightbox](onboarding.md#modal-style)

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-onboarding (1).md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Mobile-App Onboarding: An Analysis of Components and Techniques](https://www.nngroup.com/articles/mobile-app-onboarding/)

Niesen Norman Group, 2020

#### [Instructional Overlays and Coach Marks for Mobile Apps](https://www.nngroup.com/articles/mobile-instructional-overlay/)

Niesen Norman Group, 2014

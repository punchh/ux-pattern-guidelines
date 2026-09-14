---
description: >-
  How to manage user perception and anxiety during longer wait times and higher
  latency content while loading a page
---

# Skeleton loaders

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](skeleton-loaders.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

{% embed url="https://cdnl.iconscout.com/lottie/premium/preview-watermark/short-text-ui-skeleton-loader-animation-gif-download-14387166.mp4?h=240" %}

### Usage

Skeleton loaders serve several key purposes in UX design.<br>

#### Perceived Performance

They make apps feel faster by immediately showing the shape of content that's loading, rather than a blank screen. Users perceive the wait as shorter because something is happening visually.<br>

#### Reduced Cognitive Load

By previewing the layout structure, users understand what's coming without having to mentally adjust when content suddenly appears. It sets expectations before the real content loads.<br>

#### Preventing Layout Shift

Skeleton screens hold space for content, preventing jarring layout jumps when elements pop in — a major source of user frustration.

In short, skeleton loaders are really about managing user perception and anxiety during unavoidable wait times — making the experience feel smoother and more predictable.

***

### Do

✅ Use neutral colors as skeleton elements

✅ Use on pages where content will take 2 or more seconds to appear in the page body

✅ Use slow, “wave” or “shimmer” left-to-right color animations on skeleton elements to decrease perceived loading time

✅ Remove individual skeleton elements as soon as its content is loaded - even if other content hasn’t loaded yet

### Don't

🚫 Use brand or primary colors to fill skeleton elements

🚫 Persist individual skeleton elements after its underlying content has loaded (don’t wait for the rest of page)

🚫 Use when load time is less than 2 seconds

🚫 Move or resize skeleton elements as an animation

🚫 “Pulse” skeleton element colors

🚫 Show rapid animations or color changes

***

### Animation specifications

* Using a semi-transparent white vertical bar (spanning the height of the body content), move the vertical bar from left to right across the width of the page body, linearly, over 1.5 seconds.
* Pause 0.5 seconds
* Repeat on loop
* See source below for CSS specification/inspiration

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-skeleton-loaders (1).md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Everything you need to know about skeleton screens](https://uxdesign.cc/what-you-should-know-about-skeleton-screens-a820c45a571a)

UX Collective, 2018

#### [CSS skeleton loading screen animation](https://dev.to/michaelburrows/css-skeleton-loading-screen-animation-gj3)

Michael Burros, 2021

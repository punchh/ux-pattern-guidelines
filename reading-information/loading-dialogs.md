---
description: >-
  How to handle high-latency actions and give the user useful feedback about why
  something's taking so long
---

# Loading dialogs

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](loading-dialogs.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (124).png" alt=""><figcaption><p>Use an animated spinner / loader icon along with a short phrase to convey that the system is working on the request</p></figcaption></figure>

Some high-compute actions - often found in context menus - necessitate an API call.

That means a potentially high latency load time for users.

The designer has properly included for a [Success](../form-experience/success-notification.md) Toast (or failure) to close the feedback loop after the action is attempted.

However, if it takes the system a few moments to determine success or failure, that might be a few moments too many for the user - leaving them confused about why the system is taking so long to give them a response.

For these situations, use an interstitial loading dialog in between the action and the destination page (where the [success](../form-experience/success-notification.md) toast message eventually appears) - or whatever the next feedback element is.

In implementation, that probably looks a bit like a small [lightbox](../layout-and-navigation/modals-lightboxes-and-dialogs.md), containing just an animated spinner/loader icon, and some friendly text to explain what's going on. No other modal controls or elements.

A good generic message for this situation might be:

> Working on it...

### Sample situations

The situations in your product that have so much latency (details below) will vary. In the mockup excerpt below, we see a context menu with some actions. "Export" is one example of an action we've seen take awhile, so could be a good candidate for a loading dialog.

<figure><img src="../.gitbook/assets/image (125).png" alt=""><figcaption><p>An Export action is just one example of a higher-latency action that would lend itself to an interstitial loading dialog</p></figcaption></figure>

### Usage

✅ Use only for actions that will always take >1000ms to conclude

✅ If fired, persist the dialog for no less than 2000ms (we don't want it disappearing to quickly - that would risk the user not seeing it in its entirety, leading them to believe they missed something important)

✅ Dim the background the same way as a modal window dims the background

✅ Don’t let the user dismiss or evade the loading dialog

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/Hh235Awsf42z6lY8Gm4U" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

---
description: >-
  How to design for personalized placeholder text - like a customer's name or
  account number - in the body of a text field
---

# Placeholder variables

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](placeholder-variables.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Placeholder variables - sometimes called “tags” in other products - are lookup values in the midst of a regular text field.

Placeholders are commonly used when composing the body text for a mass promotional message and the user wants it to contain the recipient's real name so it feels personalized.

{% hint style="warning" %}
In case you're tempted, d on’t use the word “tag” for this utility in UI. We already use “tag” for completely unrelated features - like category labels on a list page (to organize content), and PAR Punchh's proprietary “receipt tags” feature. We don't need a 3rd competing use of "tag".
{% endhint %}

In many products with placeholder features, the user can invoke a placeholder by manually typing the name of the variable encapsulated with squiggly brackets on both sides.

However, since most users haven't memorized placeholder variable names, we should offer them a menu to look up their desired value.

Use a link button just below the input region (text and [paragraph fields](paragraph-fields.md) are usually the vehicle for placeholders) labeled "Add placeholder", usually with a leading icon representing code.

When clicking or tapping the link button, show a search menu allowing the user to filter by name or description for a placeholder. Having a brief description to correspond to each official placeholder variable name is useful when the placeholder name alone isn't descriptive enough to match plain language notions of what the variable is all about.

<figure><img src="../.gitbook/assets/image (184).png" alt=""><figcaption><p>A paragraph field with the Add Placeholder search menu open</p></figcaption></figure>

In the menu, show the placeholder names along with any leading and trailing symbols (like squiggly brackets) so the user gets familiar with the syntax.

<figure><img src="../.gitbook/assets/image (185).png" alt=""><figcaption><p>A paragraph field with a placeholder variable populated</p></figcaption></figure>

Once selected from the search menu, the menu closes, and the selection manifests as plain text like any other typed entry.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/WVgtoR9KnfNj5sPOaP7q" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

---
description: Communicating server side issues
---

# Environmental errors

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](environmental-errors.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

Sometimes our own servers encounter problems that prevent users from submitting a form or loading content in our apps.

They’re usually brief and temporary - but complex to explain.  

Rather than attempt translating the technical details to users, follow our grammar, voice, and tone guidelines for taking ownership of the problem and offering help.

### Generic problem loading or saving

#### For the entire page or feature

Use a toast message to convey the issue.

**Main toast text**

> We ran into a problem on our side

**Descriptive toast text**

> Try again in a few moments.\
> If the problem persists, contact support so we can help.

<figure><img src="../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

#### The problem is isolated to a specific portion of the page

This often occurs when an array or list content is trying to be loaded.

Use an empty state style layout in the region affected by the issue. Be sure to offer solutions or escalation paths.

**Main empty state text**

> We ran into a problem loading this content

**Descriptive toast text**

> Try again in a few moments

<figure><img src="../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

***

### Deadlock

A deadlock occurs when another user has made changes to content that the current user is trying to work with.

**Main toast text**

> We can't load that because another user made changes

**Descriptive toast text**

> Try refreshing the page in a moment.

<figure><img src="../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

***

### Missing content or lookup record

Content can go missing if another user deleted referenced record in someone else's flow.

For example, imagine building a marketing campaign where on step 1 the user selected a target segment. By the time the user gets to the last step of the campaign builder, another user has deleted the segment identified on the earlier step.

**Main toast text**

> Your selection no longer exists - select another option

**Descriptive toast text**

> {field name} "{value}" isn't available anymore

<figure><img src="../.gitbook/assets/image (120).png" alt=""><figcaption><p>Truncate {Value} with an ellipsis (...) after 16 characters.</p></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-environmental-errors.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

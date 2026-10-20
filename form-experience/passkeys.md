---
description: How to surface and lay out the passkey authentication method during sign-in
---

# Passkeys

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](passkeys.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

This guideline covers the passkey option on a sign-in form: the passkey button, accompanying text, its icon, and where it sits relative to the traditional password form.

Any "sheet" that fires to facilitate the actual passkey authentication is handled by the user's browser and OS, so is out of scope for this guideline.

{% hint style="info" %}
For password fields, the "Sign in" button and sign-in wording, follow [Password fields and sign in](../entering-information/password-fields-and-sign-in.md) guidelines and [Grammar, voice, and tone for word choice](../reading-information/grammar-voice-and-tone.md#sign-in-versus-log-in).
{% endhint %}

### Hierarchy

The sequence of elements in a passkey-supported sign-in form depends on how the product prioritizes passkeys versus traditional password sign-in.

#### Password-first

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure></div>

In a product that prioritizes traditional password sign in, lead with the traditional authentication fields (username or equivalent and password field).

Following the authentication fields, lead with a primary-styled Sign in button.

It's important that this button immediately follow the authentication fields to emphasize its intrinsic relationship to those fields only.

Omit any leading icon on the button (we'll save an icon for the passkey button to better distinguish it from regular sign in).

Omit any clarifying text on the button: the label "Sign in" alone suffices. No need to include "with a password" as that would be redundant of the password field just above.

Next in the hierarchy, include a subdued separator with the word "or" to emphasize what comes next is a completely separate means for signing in, completely unrelated to the cluster of elements above.

Finally, surface a button labeled "Sign in with a passkey", including a leading icon to signify "key" or similar.

Style this button as an outline, secondary style, or anything distinct from the regular Sign in button's primary style.

Follow the passkey Sign in button with a brief text phrase explaining how passkey sign-in works (as of this writing, passkeys are still rather novel for users).

Suggested text:

> Use your fingerprint, face, or screen lock

#### Passkey-forward

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure></div>

In a product that wants to drive passkey adoption, lead with the passkey button.

Use the same button style, leading icon, and text label for the passkey button as described above.

Follow it with a brief text phrase explaining how passkey sign in works, using the same suggested text as above.

Next in the hierarchy, include a subdued separator with the word "or" to emphasize what comes next is a completely separate means for signing in, completely unrelated to the passkey button just above.

Follow the separator with the authentication field cluster and traditional Sign in button, still using the same primary button style as described above.



***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-passkeys.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.



***

### Sources

[**Sign In with a Passkey**](https://www.passkeycentral.org/design-user-journeys/required-patterns/sign-in-with-a-passkey)\
FIDO Alliance (Passkey Central), 2023

[**Design guidelines for passkeys**](https://learn.microsoft.com/en-us/windows/apps/develop/security/design)\
Microsoft Learn, 2024

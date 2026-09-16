---
description: How to design for phone number capture - across country codes, too
---

# Phone number fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](phone-number-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Single-country input

When designing a phone number field for a single country, auto-format the user’s input according to the local convention.

  In other words, use an input mask to auto-format the user’s entry. Convey the same format in the hint text, too.

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption><p>Precede the input with a phone icon to reinforce the context and numeric expectation.</p></figcaption></figure>

✅ Use hint text to convey the format / input mask

✅ Only accept numeric characters; ignore non-numerics

✅ Auto-format the user’s entry for the appropriate input mask

***

### Multi-country and international

Support country code and phone number input at the same time through a Composite Field: an experience where a single input region has multiple input types and values.

Composite fields combine discrete elements together to capture a single logical piece of information.

#### The default state

Phone number fields prepend new elements to the [input region](anatomy-of-form-field.md) of a text field. Country flag, country code, and a leading dropdown chevron.

✅ Precede the country code with the corresponding flag and a ‘+’

✅ Use a chevron to signal the presence of a dropdown list

✅ Clicking or tapping on the flag, code, or chevron toggle the visibility of the country code dropdown menu

<figure><img src="../.gitbook/assets/image (181).png" alt=""><figcaption><p>The pre-populated country code has a normal font weight, whereas the phone number is de-emphasized as hint text.</p></figcaption></figure>

✅ Follow the same hint text and input rules as single-country phone number field

✅ Pre-populate the country code and flag with a default. Use the most likely selection for your users (often the flag and code number for the United States)

#### Dropdown list open

The dropdown list surfaces a search-menu style dropdown, allowing the user to filter by country or code.

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption><p>The pre-populated country code has a normal font weight, whereas the phone number is de-emphasized as hint text.</p></figcaption></figure>

✅ Pin popular or highly-likely selections to the top

✅ Use a inline filter when more than a small handful of countries are available

✅ ...but omit the filter when there’s only a handful of countries in play

✅ Sort alphabetically by country name, not code

✅ ...but omit the filter when there’s only a handful of countries in play

✅ After making a selection, the code element changes size accordingly (for 1, 2, and 3 digit codes)

✅ After making a selection, the hint text and [input mask changes to match the country](https://github.com/ChristoPy/countries-phone-masks/blob/main/src/countries.json) (if not available, not hint text and no input mask)

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-phone-number-fields.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Consider Using Localized Input Masks for ‘Phone’ and Other Restricted Inputs (64% Aren’t Taking Advantage of Input Masking)](https://baymard.com/blog/input-masking-form-field)

Baymard, 2017

#### [Drop-Down Usability: When You Should (and Shouldn’t) Use Them](https://baymard.com/blog/drop-down-usability)

Baymard, 2017

#### [countries.json](https://github.com/ChristoPy/countries-phone-masks/blob/main/src/countries.json)

ChristoPy's countries-phone-masks github, 2024

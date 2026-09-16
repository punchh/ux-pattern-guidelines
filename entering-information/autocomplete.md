---
description: How to help a user fill a form field before they've finished typing
---

# Autocomplete

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](autocomplete.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### On focus

If the autocomplete menu you’re designing offers genuine suggestions or recommendations, then show the menu immediately upon focusing on the field - even before typing has begun.

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption><p>A field with suggestions on focus</p></figcaption></figure>

In absence of any recommendations or suggestions, no need to open the menu before typing has begun (unless the values are an uncommon format or syntax that the user would benefit from seeing to know how to type).

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption><p>A field with no suggestions on focus</p></figcaption></figure>

### While typing

Help users locate a desired piece of content more quickly by predicting titles as they type.

After the user types 2-3 characters, show a menu with items that match the typed phrase.

Let the user keep typing even with the autocomplete menu open.

[Combo box](combo-box-fields.md) fields by design are the best demonstration of autocomplete:

<figure><img src="../.gitbook/assets/image (147).png" alt=""><figcaption><p>The user has typed 2 or more characters, and can see matches. Show at most 6 items in one scroll position (implement scrollbar for items beyond 6)</p></figcaption></figure>

Search fields also lend themselves to an autocomplete experience:

<figure><img src="../.gitbook/assets/image (148).png" alt=""><figcaption><p>As the user types, matching items show in the menu</p></figcaption></figure>

### Highlighting partial matches

Help users more easily scan matches by emphasizing only the portion of the item titles that does not match.

In this example, the user has already typed in “gue”, so only the non-”gue” portion of matches are emphasized:

<figure><img src="../.gitbook/assets/image (150).png" alt=""><figcaption><p>Observe that the non-matching portion of the values/labels are emphasized to help the user more quickly see the differences between his entry and the matches</p></figcaption></figure>

***

### Sorting matches

This will vary by context.\
\
Options to consider:<br>

* Alphabetically (easiest to scan)
* Begins with typed phrase first (sometimes better for shorer titles)
* Relevancy (e.g. popularity, geo-proximity, etc.)

***

### Selecting an item

#### Keyboard

With the autocomplete menu open:<br>

1. Use the arrow keys to “hover” through items in the list
2. Enter key to select the item (any other keystroke just adds to the query)
3. Upon selecting an item, replace any types characters with the selection title
4. Don’t submit the form unless it’s a search field

#### Mouse or touch device

1. Click or tap on the desired match to select
2. Upon selecting an item, replace any types characters with the selection title
3. Don’t submit the form unless it’s a search field

***

### After typing

Make sure any values selected via autocomplete are distinctly styled in a populated field, often with an underline to emphasize the selection is a "known" record.

Refer to [Combo box field pattern guidelines](combo-box-fields.md) for more details about combo box interaction rules.

#### Single-select combo boxes

<figure><img src="../.gitbook/assets/image (151).png" alt=""><figcaption><p>The selection is styled with an underline to emphasize the populated value is a "known" item</p></figcaption></figure>

#### Multi-select

<figure><img src="../.gitbook/assets/image (152).png" alt=""><figcaption><p>The selected items are styled as a chip to emphasize being "known" items</p></figcaption></figure>

#### Search fields

Search fields are cleared as soon as the search is fired - meaning the moment the user selects an autocomplete match, the string is cleared

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-autocomplete.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### ["Highlight the Suggested Query Text" from Design Patterns for Autocomplete](https://baymard.com/blog/autocomplete-design)

Baymard, 2022

#### [Keyboard Accessibility](https://webaim.org/techniques/keyboard/)

WebAIM, 2024

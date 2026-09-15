---
description: When and how to use combo boxes
---

# Combo box fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](combo-box-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Usage

* For a single-select combo box, use when there are 15+ options to choose from (for fewer options, use a dropdown list or button group)
* For a multi-select combo box, use when there are 10+ options to choose from (for fewer options, use a [checkbox field)](checkbox-fields.md)

### Single select

#### Unpopulated

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

#### Menu invoked, unpopulated

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

* The **menu opens** after typing begins, or on click of the down arrow
* **Focus through items and scroll** the menu using the keyboard’s up and down arrows.
* **Make a selection** using the Enter key (which also closes the menu and populates the field)
* **Max height** 6 items (more than that use a scrollbar)

#### Typing

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Emphasize the **non-matching portion** of text (seen here as bold) to help the user focus on the difference between their typed entry and matches.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

The **selected value appears as underlined**. If the user modifies the value (by modifying any portion of the text), the underline is removed, and the search begins again.

***

### Multi-select

#### Unpopulated

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

#### Menu invoked, unpopulated

<figure><img src="../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

* The **menu opens** by clicking anywhere in the unpopulated field region
* **Cursor focus** automatically goes directly to the Search field and list
* **Focus through items and scroll** the menu using the keyboard’s up and down arrows. The user can type to search at the same time.
* **Make a selection** using the Enter key (menu stays open)
* **Max height 5 items** (more than that use a scrollbar)
* **Do not move checked items nor re-sort** the list during an active selection interaction. Also preserve the current scroll position. More on this later.
* **To close** the menu, click anywhere outside the menu region

#### Typing

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

Emphasize the **non-matching portion** of text (seen here as bold) to help the user focus on the difference between their typed entry and matches.

#### Populated, no truncation

<figure><img src="../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

Selected values manifest as chips in the entry region.

#### Populated with truncation applied

With multi-select, the populated view can get BIG. That’s potentially harmful for scannability and risks over-competing with other priority fields on the same page.\
\
As a workaround, consider [truncating](../reading-information/truncation-and-overflow.md) subsequent chips using the “+_n_ more" model.\
\
Refer to [Truncation and Overflow guidelines](https://www.figma.com/proto/J8CoHtuFZFFdlt6qFReNpM/UX-Pattern-Guidelines?page-id=26%3A2\&node-id=1814-11150\&viewport=-141%2C-875%2C0.32\&t=iFOsC3nhnHIq0MEQ-1\&scaling=scale-down\&content-scaling=fixed\&starting-point-node-id=26%3A38) for the authority on truncation handling.

<figure><img src="../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

* **Show at least 1 value**, then show others in a single “+_n_ more” chip. The number of chip values shown before invoking truncation will vary by your project context.
* The ‘x’ to close icon button at the end of the chip is optional - it may be too destructive to permit one-click removal depending on the project context.
* Hover over the truncated chip to see the list of values within via a tooltip

#### Menu invoked, already populated

<figure><img src="../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

* **Already-checked items** appear on top in alphabetical order
* **When unchecking a checked item**, it does not re-sort during this interaction; it stays in place. The current position is preserved until the user closes the menu and goes back into it again (at which point the original sorting is applied to non-checked items).
* **Also when unchecking a checked item**, keep the menu open and maintain the current scroll position.

***

### Exception cases

#### Loading state

<figure><img src="../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

For higher latency lookups during typing, give the user feedback via an animated spinner/loader and the text "Loading..." directly in the combo box menu where matches will eventually appear.

#### Single-select no matches

<figure><img src="../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

When the user's typed text doesn't yield any matches, let them know with iconography that signals no matches, along with text like "No matches found". Place it direclty in the menu where matches would appear.

#### Multi-select no matches

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

Same experience as single-select no matches.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/wFxWUGnaBozIkzHb64nW" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Combo box](https://designsystem.digital.gov/components/combo-box/)

Digital.gov, 2022

---
description: How to refine and pare down the items shown in a list
---

# Filters

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](filters.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

In any table or list page experience where the primary purpose of the page is to present the user with rows of items to see, compare, or choose from, it's important that we support narrowing down the list to expedite locating the desired record.

We call this experience "filtering" or "refinements".

Upon arriving on a list page, no filters are applied by default. You could make the argument that the presence of [tabs](../layout-and-navigation/tabs.md) implies active filtering from the outset, but we consider tabs to be a persistent navigational element not controlled by the user.

Filtering principally occurs _within_ a tab (if tabs are present at all) and applies to the content and metadata within that tab only.

### Unstructured filters

Our lone unstructured filter is effectively a text refinement.

This one warrants top-placement in the filter hierarchy (often just above the list or table in the left-most position) as its ease of use makes it highly attractive for making refinements.

The user types a few characters (usually 2 or 3), and the system shows items that contain a matching string (in title or some other element in the list). The user needn't press enter nor click any button to execute.

This is not to be confused with site search. Search implies looking through a broader dataset with no items pre-loaded.

**Search** is "find something I have a vague idea about".

**Free-form text filtering** is "narrow the options I already see in front of me." Text filtering refines an already-visible dataset to narrow it.

In a free-form text filtering field, use the [hint text](../entering-information/anatomy-of-form-field.md#hint-text) "Filter by x, y, z" where x, y, z are the names of fields or metadata types the user can search against. An example might be "Filter by employee name, title, office"

### Structured filters

Structured filters refer to an array of form fields that hone in on specific metadata, flags, options, and values. Each structured filter corresponds to a single data element represented in the table.

<figure><img src="../.gitbook/assets/image (205).png" alt=""><figcaption><p>The user can access a side panel of filter fields</p></figcaption></figure>

Since there can be many structured filters - many of which may never be used - we often use progressive disclosure to access them. For example, some list page experiences provide a button right next to the free-form text filter called "More filters..." that invokes a side panel where structured filter fields are stacked vertically.

This also makes the list of filters highly scalable to accommodate add-ons in the future, rather than trying to cram them all in next to the free-form text filter.

Finally, understand that any applied structured filters work _together_ with any value populated in the unstructured text filter. It's an "and" statement.

#### Showing when structured filters are active

If we're using progressive disclosure to house structured filters in a side panel that slides out of view, how does the user know when refinements from it are active?

<figure><img src="../.gitbook/assets/image (204).png" alt=""><figcaption><p>A list page with multiple structured filters applied</p></figcaption></figure>

Just above the table/list - and just below the unstructured text filter field and "More filters..." button - list each active refinement as a chip or similar component. 1 chip for every refinement, all in a row (wrap to next line if necessary).

Each chip should lead with the filter name, followed by the value(s) selected for it.

For example, if the user has applied a filter for a Status field, selecting Active and Draft, the chip would appear as:

> Status: Active, Draft

At the end of each chip, provide a small icon or button to allow the refinement to be removed (usually an 'x' icon).

If the user has selected more than a couple values or any value is particularly long, refer to [truncation](../reading-information/truncation-and-overflow.md) guidelines for handling.

#### Filtering on a multi-value field

For filter fields that support multiple value selection like a [combo box](../entering-information/combo-box-fields.md), some users wonder:

> Will this refinement function as a "and" statement, or an "or" statement?

A good example of a filter that might face this situation is a "label" filter - the user wants to refine their list by the cosmetic labels they've marked items with.

<figure><img src="../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>

Imagine a filter field named "Labeled with".

It's a multi-select combo box.

The user has selected "seasonal" and "new customer".

Should the filter behave as an "and" - requiring all matching items to be labeled with BOTH seasonal and new customer?

Or should it function as an "or", allowing matching items to contain _either_ of those labels?

Rather than leave it ambiguous, treat the filter as a [conditional field](../entering-information/conditional-fields.md), exposing an All or Any button group when in use.

Imagine once the user has selected 2 or more labels, a [button group](../entering-information/button-groups.md) field appears just below it:

> **\[All]** \[Any] of these

2 buttons in the [button group](../entering-information/button-groups.md) (All selected by default) using plain language labels and with trailing text "of these".

Now the behavior for this refinement is unambiguous.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-filters.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

[**Responsive Design: Getting Advanced Filtering Right**](https://medium.com/@mibosc/responsive-design-getting-advanced-filtering-right-bbd6c04f09e1)

Mikkel Bo Schmidt, 2014

[**Enterprise Filtering**](https://pencilandpaper.io/articles/ux-pattern-analysis-enterprise-filtering/)

Pencil & Paper, 2021

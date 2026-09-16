---
description: How to display a list of items or records in a tabular row-by-row presentation
---

# Tables

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](tables.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (223).png" alt=""><figcaption><p>A data table "landing page" in a business application</p></figcaption></figure></div>

Tables help users examine identifying information across many records ("items" here on out) at the same time.

Tables help users analyze performance data and trends, manage bulk sets of content, or locate an individual item for drilling down into more detail.

A table presumes content is loaded from the outset of arriving on the page or feature (so "browse an existing universe" rather than "search from a blank slate" - the latter being from a search experience).

We often use a table pattern to facilitate a landing page experience where the user needs to manage items (organize items, find a specific item to do work on, and perform tasks on several in one fell swoop).

{% hint style="danger" %}
**Don't put editable fields directly on a table row**

Table rows aren't forms. Allowing the user to make edits to an item directly on the row presents all sorts of usability issues like departing from form field anatomy guidelines and error validation complexities.

Save any editing needs for a side panel, modal, or navigable form page. More on this in [drill down to detail](tables.md#drill-down-to-detail).
{% endhint %}

***

### Page level actions

<figure><img src="../.gitbook/assets/image (224).png" alt=""><figcaption><p>A data table landing page with page level actions highlighted</p></figcaption></figure>

Page actions refer to the button(s) clustered up with the page title, usually on the same row as the H1 but aligned to the right edge. Page actions offer users access to tasks or navigation overarching to any tabs below.

This is often an opportune place for launching a "Create new" experience, where clicking said button navigates the user to a form for building out a new item.

The action is "page level" because it's overarching of any tabs below: Since tabs - as we'll learn - keep different types of items separate from each other, a page level action is tab agnostic.

***

### Tabs

<figure><img src="../.gitbook/assets/image (225).png" alt=""><figcaption><p>A data table landing page with tabs highlighted</p></figcaption></figure>

On a table page, tabs are the highest level of organization. They allow each tab to independently operate its own filters, tab-level actions, item counts, and data display.

Details are covered in the [tabs](../layout-and-navigation/tabs.md) UX pattern guideline, including their [usage in a table context](../layout-and-navigation/tabs.md#as-a-top-level-filter-on-table-and-list-pages).

***

### Filters

<figure><img src="../.gitbook/assets/image (226).png" alt=""><figcaption><p>A data table landing page with filters highlighted</p></figcaption></figure>

Filters are the highest ranking features in a table element hierarchy (within a tab, if present) since they're so useful for paring down content. As such, filter elements are often in the top most section above the table body (again, within the tab, if present) and left-aligned.

Details are covered in the [table filters](filters.md) UX pattern guideline.

***

### Table level actions

<figure><img src="../.gitbook/assets/image (227).png" alt=""><figcaption><p>A data table landing page with table level actions highlighted</p></figcaption></figure>

For actions or tasks that directly affect or are related to the table body itself (for the current tab, if present) offer the user buttons to facilitate table actions.

Some of the most common table actions include but are not limited to Export, Print, and Customize columns (column swap). We often place these options inside of a 3-dot overflow icon button as a context menu.

<figure><img src="../.gitbook/assets/image (228).png" alt=""><figcaption><p>A data table landing page with table level actions highlighted in a context menu</p></figcaption></figure>

More unique table level actions (or actions that warrant enhanced discoverability or that are very frequently used) can be surfaced as a persistently visible button. We can even use a small [button group](../entering-information/button-groups.md) here, like if the user needs to toggle between a table view and [cards](../reading-information/cards.md#lists-or-tables) view.

Both the overflow button and any persistent table action buttons can be placed side by side, on the same span as filters, but right-aligned.

***

### Item count

<figure><img src="../.gitbook/assets/image (229).png" alt=""><figcaption><p>A data table landing page with item count highlighted</p></figcaption></figure>

Just above the table body, left-aligned, communicate to the user how many items are present _with any filters applied_. For example, if the universe of items is 100, but the user has filtered the list down so there are only 25 matches, then the text should read:

> 25 items

***

### Sort selector

<figure><img src="../.gitbook/assets/image (230).png" alt=""><figcaption><p>A data table landing page with the sort selector dropdown field highlighted</p></figcaption></figure>

Also just above the table body, in the same span as Item count but right-aligned, offer the user the ability to sort items in the table via a [dropdown list](../entering-information/dropdown-lists.md).

The sort options should only contain sorting techniques that are actually useful for the data set.

For example:

* Name A-Z
* Name Z-A
* Highest amount
* Lowest amount
* Newest first
* Oldest first

Note that the sort options are deliberately in "plain language" and won't necessarily match the data table's column header.

Put the most frequently used sort options first.

Omit sorting options that are unlikely to be used. Some examples of those might include:

* Description (it's more useful to [filter](filters.md#unstructured-filters) on a string or phrase rather than to sort on a long-form text field)
* Status (users are more likely to filter for a specific status than sort on it)
* (any boolean data)

{% hint style="warning" %}
**Resist using column headers to facilitate sorting**

Sorting on column headers is great when the table is composed almost exclusively of numeric quantitative data, or data that's naturally sequential like dates.

It's a lot less useful when tables contain a variety of content types - like longer form text, or boolean values - where sorting doesn't make sense.

Further, column header sorting is a lot more _complicated_ when individual cells can contain multiple values (which value should it sort on?), or stacked data types in a single cell (how to pick which piece of data to sort on if they share a column?)
{% endhint %}

***

### Table body

<figure><img src="../.gitbook/assets/image (232).png" alt=""><figcaption><p>A data table landing page with the table body highlighted</p></figcaption></figure>

The table body refers to the grid of rows and columns.

#### Header row

<figure><img src="../.gitbook/assets/image (233).png" alt=""><figcaption><p>A data table with the header row highlighted</p></figcaption></figure>

The top-most row is for the column header. Remember, [sorting](tables.md#sort-selector) is usually best facilitated by a separate dropdown list.

#### Checkboxes column

<figure><img src="../.gitbook/assets/image (234).png" alt=""><figcaption><p>A data table with the checkboxes column highlighted</p></figcaption></figure>

The left-most column is for checkboxes if [bulk actions](bulk-actions.md) are needed. Notably the column header for checkboxes is a checkbox itself, with no text label. It's also unique in that interacting with this header checkbox performs a select all/deselect all toggle for all **visible items** on the current page of pagination.

Items excluded by filters or on other pages of pagination are **not** included in the selection.

#### Identifier column

<figure><img src="../.gitbook/assets/image (235).png" alt=""><figcaption><p>A data table with an identifier value highlighted</p></figcaption></figure>

The next left-most column is the item's identifying _label_. Emphasis on _label:_ In most contexts, this is probably a plain language text title rather than a numeric expression.

The goal is to use an identifier that's easily scannable, recognizable, and distinct from other rows.

Sometimes an identifying label is combined (in the same cell) with another piece of metadata like description or serial number (or similar). The identifying label is stacked on top of the metadata value (with the latter using a smaller font size and de-emphasized style to create hierarchy). This helps give the user more context about an item without needing to use a dedicated column for the piece of metadata alone.

#### Other data columns

<figure><img src="../.gitbook/assets/image (236).png" alt=""><figcaption><p>A data table with an assortment of data columns highlighted</p></figcaption></figure>

The sequence and composition of remaining data columns will vary by project context but generally:

✅ Higher priority columns go on the left, lower priority columns on the right

✅ Date and time columns usually take the right-most position (like "Last modified")

✅ Just like the identifier column (see above), don't be shy about combining/stacking closely related values in the same column/cell. For example, a column "Last modified" could contain the date/timestamp as the "main" value, with smaller text "by Jane Doe" just beneath it.

✅ Include multi-value data if useful. For example, users might find it useful to see which organizational categories or labels an item has been tagged with. Use a multi-value column to show the first few for each item, following [truncation guidelines](../reading-information/truncation-and-overflow.md#chips-in-a-table-cell) if necessary.

✅ For 1 or 2 columns, try to use styling or decoration more sophisticated than plain text. This adds differentiation to what otherwise is often a "boring" data grid. For example, a Status column makes a good candidate since there are just a small number of status values possible, and often just 1 word in length. Style these cells using a chip, pill, or tag component. Just don't over do it - applying non-text styling to more than 1 or 2 columns makes the table aesthetically noisy and increases cognitive load.

✅ Follow [column alignment guidelines](column-alignment.md) for how values are aligned in each cell.

#### Action menu column

<figure><img src="../.gitbook/assets/image (237).png" alt=""><figcaption><p>A data table with action menu for a row item opened</p></figcaption></figure>

The right-most column is reserved for the action menu icon button. Often represented by a 3-dot overflow icon, clicking this region in each row invokes a context menu with any tasks or actions that can be performed on an individual item.

Common examples might include but not limited to Edit, Delete, Archive, and Duplicate.

{% hint style="warning" %}
**Don't place specific action buttons directly on rows - use an overflow button and context menu**

Including specific action buttons directly on every row of a table is visually redundant and competes with the user's ability to scan table data.

Lean on a 3-dot overflow icon button and its context menu to house specific actions.
{% endhint %}

#### Empty states

The table body may be empty when no items exist, or when the user has applied filters such that there are no matches.

Details covered in the [empty states](empty-states.md) UX pattern guideline.

***

### Pagination

Covered in the pagination UX pattern guideline.

***

### Interaction and behavior

#### Drill-down to detail

<figure><img src="../.gitbook/assets/image (238).png" alt=""><figcaption><p>A data table landing page with the details side pane for a row opened</p></figcaption></figure>

Click or tap _anywhere_ on a row (except the checkbox and overflow buttons if present) to drill-down to its detail view.

{% hint style="warning" %}
**Don't make it so tapping on a row expands the row / opens the row as an accordion.**

Studies have shown this approach presents a myriad of usability and accessibility issues. Use a slide-out panel instead.
{% endhint %}

The detail view might be in the form of a slide-out side panel, or navigation to a dedicated detail view page for the selected item.

This is where you'd put things like:

* more data fields about the selected item
* expanded values without any truncation
* editable fields to make changes to the item

#### Bulk actions

<figure><img src="../.gitbook/assets/image (239).png" alt=""><figcaption><p>A depiction of a bulk actions bar on a data table</p></figcaption></figure>

Bulk actions are invoked through checkbox selections.

Details covered in the [bulk actions](bulk-actions.md) UX pattern guideline.

#### Resizing columns

We generally avoid allowing users to manually resize columns for several reasons:

* To protect the user from accidentally setting unfavorable column widths
* To avoid the complexities of remembering custom column sizes
* To reduce the number of interactive hit targets for users not interested in resizing columns

Instead, the designer should be thoughtful when designing column widths, and highly aware of data value lengths when determining the optimal experience.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-tables.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

[**Data Tables: Four Major User Tasks**](https://www.nngroup.com/articles/data-tables/)

Nielsen Norman Group, 2022

[**Data Table Design UX Patterns**](https://www.pencilandpaper.io/articles/ux-pattern-analysis-enterprise-data-tables)

Pencil & Paper, 2023

[**Users' Pagination Preferences and "View All"**](https://www.nngroup.com/articles/item-list-view-all/)

Nielsen Norman Group, 2023

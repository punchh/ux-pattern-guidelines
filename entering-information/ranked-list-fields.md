---
description: How to facilitate ranking, sequencing, or relative order in a set of items
---

# Ranked list fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](ranked-list-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>

A ranked list field lets users assign a relative order to a set of items. The user manipulates the items into a desired sequence, and the position of each item carries meaning. For example, but not limited to:

* first is most important, last is least important
* first is least important, last is most important
* first is for positioning a layout with a top or left-most item, last is for the bottom or right-most item

Ranking is different from sorting. Sorting a list reorders items based on a column or attribute (alphabetical, date, etc.) and doesn't persist as a user-defined value. Ranking, on the other hand, captures the user's deliberate ordering as the field's value - it's saved with the form, and the order itself is the data.

{% hint style="danger" %}
**Don't use a** [**listbox**](listbox-fields.md) **field for ranking**

Any semblance of a list box field that facilitates "shuttling" items from one box to another then exclusively relying on arrow buttons to move items up and down should not be used for ranking items ([list box fields shouldn't be used for anything anymore](listbox-fields.md)).
{% endhint %}

***

### When to use a ranked list field

Use a ranked list field when the user needs to express priority, preference, or sequence across a defined set of items, and the position of each item is meaningful information you intend to save.

Common examples:

* A user prioritizing campaign offers (most important offer at the top, least important at the bottom)
* A user defining the steps of a process or recipe in a specific order
* A user ranking preferences from a fixed list (favorite cuisines, communication channels, etc.)
* A user arranging items in a sequence that will be presented or processed in that order

🚫 Don't use a ranked list field when:

* The order isn't meaningful to save (users just want to scan a list - that's sorting, not ranking)

{% hint style="warning" %}
**Be wary of using a ranked list field for more than 15 items**

When the set of items is too large to comfortably scan or just plain painful to rank manually - consider breaking the ranking into categories, or rethinking whether ranking is the right model at all.

This is not a hard fast "never do it rule" - some rare situations may necessitate using a ranked fields for a [longer list of items](ranked-list-fields.md#longer-lists), but have some pause before going forward.
{% endhint %}

***

### Anatomy

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

A ranked list field often uses a design system's card component to represent the items being ranked, as users find the tangible nature of a card to be easy to manipulate and track. In that model, each item in the list is a card, and each card has the same anatomy as defined by the [cards guideline](../reading-information/cards.md#anatomy).&#x20;

In addition to the field label and description standard to a f[orm field's anatomy](anatomy-of-form-field.md), each item in the ranked list is composed of:

#### Grabber dots icon button

Each card in the ranked list has a "grabber dots" icon button (6 dots arranged in a 2×3 grid) on the leading edge of the card. This icon button serves three purposes:

1. **Affordance:** it signals to the user that the card is movable. Without this signal, users hesitate to discover the interaction. Research on drag-and-drop UX consistently emphasizes that movable elements must visually announce their movability.
2. **Hit target:** it provides a precise area for the user to click and hold when initiating a drag.
3. **Keyboard handle:** it's the element that receives keyboard focus to start a keyboard-driven move (see Accessibility below).

The cursor should change to a "grab" or "move" cursor when the user hovers over the grabber dots, and to a "grabbing" cursor while the user is actively dragging.

#### Context menu icon button

Depending on context, each card may have a context menu icon button (3 vertical dots) on the trailing edge, following the same pattern as defined in the cards guideline. In a ranked list, this menu serves two purposes:

1. Surface any per-item utility actions the host application provides (Edit, Delete, Duplicate, etc.)
2. Provide an accessible non-drag way to reorder the card (see [Accessibility](ranked-list-fields.md#reordering-via-the-context-menu-required-for-accessibility) below)

The context menu must be present on every card in a ranked list, even when the host application doesn't define any per-item utility actions, because the menu also hosts the Move up / Move down actions required for accessibility.

***

### Interactivity

#### Reordering via drag and drop

The user can drag any card up or down to a new position in the list. While the user drags:

* The dragged card lifts slightly (a subtle elevation/shadow effect) to indicate it's been picked up
* The remaining cards reflow in real time, opening a gap where the dragged card would land if dropped at the current cursor position
* As the user positions the dragged card mostly over the top of another card, that card slides up or down (\~100ms, ease out) to make room
* When the user releases, the card animates into its new position

Use a subtle tilt or scale effect on the dragged card during transit. This isn't decorative — it's a perceptual cue that the card is "in transit" rather than committed to a position.

#### Reordering via the context menu (required for accessibility)

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>An open context menu on an item on a ranked list field offers several "Move" actions for accessibility compliance and convenience.</p></figcaption></figure>

Drag and drop alone is not sufficient. Users with motor impairments, users on speech-controlled or eye-tracking input, and users who simply find dragging fiddly all need a non-drag alternative. WCAG 2.2 (Success Criterion 2.5.7, Level AA) makes this a compliance requirement: any function that uses dragging must also be achievable through a single pointer without dragging.

For ranked list fields, the non-drag alternative lives inside the context menu on each card. The menu always includes two actions:

* **Move to top:** moves the card to top-most position. Disabled when the card is already first.
* **Move up:** moves the card one position higher. Disabled when the card is already first.
* **Move down:** moves the card one position lower. Disabled when the card is already last.
* **Move to bottom:** moves the card to bottom-most position. Disabled when the card is already last.

Notably, "Move to top" and "Move to bottom" are usability boons for all users, regardless of accessibility.

These actions appear alongside any other per-item utility actions (Edit, Delete, etc.) defined by the host application. When the user selects any of the Move actions, the card moves immediately and focus follows the card to its new position, so the user can repeat the action to move multiple positions without re-navigating.

Why the context menu and not always-visible up/down arrow buttons? Two reasons:

1. **Visual economy:** the card already has a grabber on one edge and a context menu on the other. Adding two more icon buttons per card crowds the layout, especially at 10+ items.
2. **Accessible-control best practice:** directional arrow-key keyboard reordering, while implementable, is known to have cross-screen-reader inconsistencies. Accessible controls inside a menu on the other hand are more predictable across assistive technologies so we prioritize context menu actions.

#### Reordering via keyboard

Keyboard users reach the same Move actions by tabbing to the context menu, opening it with Space or Enter, navigating to the action, and selecting it. This is the same mechanism that mouse, touch, and assistive-tech users use - no separate keyboard model.

Screen readers should announce the card name, its old position, and its new position (for example: "Email moved to position 2 of 5").

{% hint style="danger" %}
**Don't rely on drag and drop alone**

Drag-and-drop-only ranking interfaces fail WCAG 2.5.7 at Level AA and exclude users on keyboards, screen readers, speech control, eye tracking, and touch devices where dragging is awkward. The context menu's Move up / Move down actions aren't optional.
{% endhint %}

#### Longer lists

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption><p>In a longer ranked list (described below), each item card in the ranked list also shows a position number, and the context menu offers a "Move to position" action </p></figcaption></figure>

With more than 15 items in a ranked list, consider offering the user a context menu action to "Move to position" where the user can enter a specific position number.

Upon choosing "Move to position" in the context menu, offer the user a [modal form](../modals-lightboxes-and-dialogs.md#id-1-field-form) for entering the position number, making sure to state the range of options for the list in context. For example, the text label above the lone numeric field in a modal like this would be:

> Enter a position (1-36).

36 in this example represents the number of items in this ranked list.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption><p>After choosing "Move to position", the user can enter the desired position number in a <a href="../modals-lightboxes-and-dialogs.md#id-1-field-form">modal </a>form.</p></figcaption></figure>

The lone field in the modal is focused from the outset, text selected selected for typing over (it's populated with the item's current position by default), allowing the user to type the desired position number immediately without having to click, select, or tab to the field.

#### Clicking the broader card body

On a ranked list card that strictly functions as a ranked list field alone, the broader card body (besides the dragger icon and context menu) is not clickable, as there's nothing to do.

However, in some contexts - like if [building an array on a form page](../reading-information/cards.md#form-design) AND the items in that array are "rankable" - then the broader card body may be clickable to invoke the modal (or whatever facilitates editing the item in the array).

<figure><img src="../.gitbook/assets/image (218).png" alt=""><figcaption><p>In this example, on a form page, the user has built an array of 2 items (the French Fries items), probably via a modal window containing a microform for each item. Each item manifests on this underlying page as a card. With the grabber handles on each card, the user can rank the items, too.</p></figcaption></figure>

***

### Saving behavior

The user's ranking should not be saved on every reorder — the user is likely still mid-decision. Treat the ranked list field like any other form field: the rank value is captured when the user submits or applies the form per your form's [saving pattern](../saving-state-on-buttons.md).

If the user navigates away or cancels mid-rank, follow the [canceling guidelines](../canceling.md) for unsaved changes.

***

### What not to do

🚫 **Don't use a ranked list field for sorting.** If the user just wants to view items in a different order without saving that order, use sort controls on a table or list, not a ranked list field.

🚫 **Don't use checkboxes or radio buttons for ranking.** Multi-select fields capture which items are chosen, not in what order. If order matters, use a ranked list field.

🚫 **Don't ask users to type a number into each item to assign rank.** This is technically accessible but it's a poor experience for the majority of users. Use cards with drag-and-drop plus the context menu reorder actions instead (when there are [many items in a ranked list](ranked-list-fields.md#longer-lists), this can include a "Move to position" option where the user may type a specific number _if they'd like to_, but not as the exclusive means for ranking).

🚫 **Don't omit the context menu from cards in a ranked list.** Even if the host application has no per-item utility actions, the menu must still be present to host the Move accessibility actions.

🚫 **Don't auto-save on each reorder.** The user is still deciding. Save when the form is submitted or applied.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-ranked-list-fields (1).md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

[**Drag–and–Drop: How to Design for Ease of Use**](https://www.nngroup.com/articles/drag-drop/)

Nielsen Norman Group, 2020

[**Understanding Success Criterion 2.5.7: Dragging Movements**](https://www.w3.org/WAI/WCAG22/Understanding/dragging-movements.html)

W3C Web Accessibility Initiative, 2023

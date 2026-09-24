---
description: The edit experience, and making sure changes are saved properly
---

# Editing and saving forms

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](editing-and-saving-forms.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

###

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

An "edit experience" is the pattern where a user changes the contents of a form and saves them. This guideline covers 3 related concerns: how the user _arrives_ at the edit experience, when save controls should _appear_, and what happens when the user _finishes_ editing.

The specific rules that follow are for single-page forms. Multi-step forms are governed by the [Multi-step forms guideline](multi-step-forms.md).

***

### The 3 ways a user arrives at an edit experience

The three entry paths matter because they determine what should happen when the user finishes editing.

#### 1. From an Edit action on a read-only page

The user is viewing the read-only version of a record's detail page and clicks an Edit action. The page either navigates to an editable version of itself, or shifts into edit mode in place. Either way, the user came from a read-only view of this specific record, and they're expected to return to it once they're done editing.

#### 2. From a parent list page

The user is on a landing page that houses a list of records (a list of stores, campaigns, offers, guests, etc.) and clicks into one of them to edit it. The user came from a list of siblings and is expected to return to that list once they're done editing - the list is the operational context they were in the middle of.

#### 3. Directly from primary navigation

The user clicks a link in the primary navigation (or a dashboard tile, or a deep link) that takes them straight to an editable form for a piece of content - like an "Account Settings" page or a "Store profile" page for the only store they administer. This entry path is rare, but it exists.

The user did not come from a read-only view or a parent list. There's no meaningful "origin" to return to when they're done editing - this page _is_ the destination.

***

### When save controls appear

Save controls - the button(s) that facilitate saving or abandoning changes made to a form - are the persistent sticky footer at the bottom of the page that contains the primary Save action, a Cancel action, and any secondary actions relevant to the current form. To reiterate: It is visible and sticky even if the form fields themselves are long enough to invoke a vertical scroll.

In a design system, this collection of controls may sometimes be referred to as a "Save Bar", and its conditions for appearing vary based on the entry path.

#### For paths 1 and 2: Save Bar visible from arrival

The user landed here specifically to edit something. Their intent is unambiguous, and the Save Bar should be visible as soon as the page loads. This confirms the user is in edit mode and puts the primary action within easy reach immediately.&#x20;

#### For path 3: Save Bar hidden until the form is modified

The user did not arrive with an unambiguous intent to edit. They may have navigated here just to view current values, or they may be about to make a change - the system doesn't know yet. The Save Bar is hidden on arrival to keep the interface calm.

The moment the user modifies any field on the form (types into a text field, changes a dropdown selection, toggles a switch, etc.), the Save Bar slides into view. This visibility change signals to the user that they now have unsaved changes.

***

### What happens on successful save

The behavior on successful save also depends on the entry path.

#### For paths 1 and 2: Auto-navigate back to the origin

The user came from somewhere — a read-only detail page (path 1) or a parent list page (path 2) — and the successful save should return them there. Show a brief [success toast](success-notification.md) to confirm the save succeeded, and navigate the user back to their originating page.

Do not require the user to click "Back" or "Close" after saving. The completed save action _is_ the signal to leave.

#### For path 3: Stay on the page

The user arrived directly and has no meaningful "origin" to return to. On successful save, hide the Save Bar (there are no more unsaved changes) and show a [success toast](success-notification.md). The user stays on the page and can continue viewing the current values or make additional edits.

The Save Bar reappears the moment the user modifies the form again.

***

### What happens on save failure

If a save fails — whether due to client-side [validation errors](error-validation.md), server-side errors, or network problems - follow the Error validation guidelines:

* Do not navigate away from the page regardless of entry path
* Follow [error validation pattern guidelines](error-validation.md) for communicating the presence of an error
* The Save Bar persists so the user can retry after correcting

The user should never lose their unsaved work because of a failed save.

***

### Anatomy of the Save Bar

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

The Save Bar is a sticky footer that spans the full width of the page's content area. It contains:

* A **Save** button, right-aligned, as the primary action
* A [**Cancel**](canceling.md) button, positioned per the [Button alignment guidelines](../layout-and-navigation/button-alignment.md)
* Any relevant secondary or [destructive actions](destructive-actions-and-deleting.md), positioned per the [Combining buttons and styles guidelines](combining-buttons-and-styles.md)
* Optionally, a brief text indicator of unsaved changes ("Unsaved changes" or similar)

The Save Bar is sticky - it stays visible as the user scrolls through a long form so the primary action is always within one click. Research on sticky form action patterns has consistently shown that placing form submission buttons in a persistent sticky footer meaningfully improves discovery and task completion versus placing them at the end of a scrolling page.

🚫 **Don't hide the Save Bar behind hover or scroll behaviors on desktop.** Once it should be visible, it stays visible.

🚫 **On mobile, be careful with the sticky Save Bar and the virtual keyboard.** When the user focuses a field and the virtual keyboard appears, the Save Bar can be either pushed above the keyboard (helpful — the user can still see it) or hidden behind the keyboard (problematic - the user has to dismiss the keyboard to save). Test both behaviors on the actual devices your users use, and choose the mobile pattern that keeps the Save Bar reachable.

***

### What happens on Cancel

Follow the [Canceling guidelines](canceling.md) for the specific behavior when the user clicks Cancel with unsaved changes, including the confirmation dialog and the correct destination to return to.

Broadly, canceling should:

* If there are no unsaved changes: return the user to their origin (paths 1 and 2) or leave the form as-is (path 3)
* If there are unsaved changes: prompt the user to confirm they want to discard changes before proceeding

***

### What not to do

🚫 **Don't require the user to scroll to find the Save button.** Long forms without a sticky Save Bar force the user to scroll to the bottom of the form to save. This is worse for both accessibility and efficiency.

🚫 **Don't show the Save Bar on path 3 before the user has made a change.** The Save Bar's purpose is to save unsaved changes. If there are no unsaved changes, showing it invites confusion - the user may wonder what they missed changing.

🚫 **Don't auto-navigate on path 3 after a save.** The user arrived directly at this page - there's no "back" for them to go to. Kicking them away from the page they intended to be on is disorienting.

🚫 **Don't skip the success toast.** On both auto-navigate and stay-on-page save behaviors, the success toast is what confirms to the user that their save actually persisted. Without it, users often re-click Save to be sure.

🚫 **Don't navigate away on save failure.** The user's unsaved work must remain visible so they can correct and retry.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}



[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

[**Designing Sticky Menus: UX Guidelines**](https://www.smashingmagazine.com/2023/05/sticky-menus-ux-guidelines/)

Smashing Magazine (Smart Interface Design Patterns), 2023

[**Why Users Miss Form Buttons Placed in the Action Bar**](https://uxmovement.com/mobile/why-users-miss-form-buttons-placed-in-the-action-bar/)

UX Movement, 2015

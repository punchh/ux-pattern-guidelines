---
description: How to orient users in their current depth of navigation
---

# Breadcrumbs

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](breadcrumbs.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<div data-with-frame="true"><figure><img src=".gitbook/assets/image (220).png" alt=""><figcaption><p>A business application with breadcrumbs navigation just above the page title.</p></figcaption></figure></div>

A breadcrumb is a secondary navigation aid that shows the user where the current page sits within the overall information hierarchy of the application, and provides one-click access back to any parent level.

The pattern looks like a horizontal trail of text links separated by a divider character (commonly a chevron-right icon), reading from the top-most level of the hierarchy on the left, narrowing down to the current page on the right.

Breadcrumbs have been recommended by studies since the advent of websites and web applications as one of the few UX patterns that studies have consistently shown to be problem-free: users may overlook them, but they almost never misinterpret them or have trouble operating them.

***

### When to use breadcrumbs

Use breadcrumbs when:

* Your application has a multi-level hierarchy 2 or more levels deep (not counting the homepage/product home)
* The page's place in the hierarchy is not obvious from the primary navigation alone
* Users frequently land on deep pages via search, deep links, or notifications, and benefit from a way to navigate "up" to a parent section without using the browser's back button
* The information architecture follows a clear parent-child structure (e.g. Content type page → Content detail page)
* The page or feature is a detail page child of an overarching content type landing page&#x20;

{% hint style="warning" %}
**Don't create a new breadcrumb node for going into "Edit" mode on a detail page**

Often when navigating from a landing page to a detail page, the information is in display-only/read-only mode. Permitted users might want to go into Edit mode (often by clicking a button labeled "Edit": The page usually refreshes or navigates to an editable form version of the same page). This should NOT introduce a new node on the breadcrumb trail.&#x20;

The breadcrumb remains the same as the display-only/read-only version of the same page.
{% endhint %}

🚫 Don't use breadcrumbs when:

* The application is flat - breadcrumbs there would add cognitive load without orienting users
* The page is a landing page or top-level dashboard with no parents above it
* The page (or feature) is a "create new" experience accessed directly from a content type landing page
* The user is on a multi-step form or wizard - use a [stepper](steppers.md) instead
* The primary navigation (often the left nav) already makes the current page's location unambiguous (e.g. a clearly highlighted active item in a left nav with full hierarchy visible)

***

### Hierarchy-based, not history-based

There are two ways breadcrumbs can be constructed, and only one is useful.

**Hierarchy-based breadcrumbs** show where the current page sits in the structure of the application - the path you'd take if you started from the home page and navigated down. This is the only kind of breadcrumb that should be used.

**History-based breadcrumbs** show the actual sequence of pages the user visited to arrive at the current page. These are confusing because they duplicate the function of the browser's back button while looking like something else, and the path is meaningless to anyone except the user who navigated it.

🚫 Don't build history-based breadcrumbs. Breadcrumbs should always reflect the application's hierarchy, regardless of how the user actually got to the current page.

***

### Anatomy

A breadcrumb is composed of:

#### Parent node links

Each level above the current page is rendered as a text link in a subdued color (less emphatic, lower contrast than regular link text and regular text), as these nodes are lower priority than the current page.

The user can click any parent node link to navigate directly to that level.

#### Dividers

Each parent node is followed by a divider character — most commonly a chevron-right icon (`>`). Dividers should not be hyperlinked, should not receive keyboard focus.

The slash character (`/`) is also acceptable but the chevron-right is preferred because it more clearly conveys directionality.

#### Current page node

The right-most node represents the current page. It is rendered in a heavier font weight and uses the normal body text color rather than the subdued color used for parent nodes. This visual emphasis tells the user at a glance which node represents "where you are."

The current page node is not a hyperlink - there's no destination to navigate to.

***

### Interactivity

#### Clicking a parent node

Clicking a parent node navigates the user directly to that level of the hierarchy. This is the breadcrumb's primary function: one-click access to any parent.

#### Keyboard navigation

Parent node links are reachable via Tab, in the same focus order as their visual position (left to right). The current page node is not focusable since it isn't a link.

#### Hover and focus states

Parent node links should show a hover state in the same way that other hyperlinked text in your design system changes. Moreover, use the same hover and focus treatments your design system applies to other [hyperlinks](hyperlinks-versus-link-buttons.md).

***

### Placement

Breadcrumbs sit at the top of the page content area, below the global header and primary navigation, and above the page title (or h1).

🚫 Don't tuck breadcrumbs into the page footer, into a sidebar, or anywhere else on the page. The convention of breadcrumbs-at-the-top has been reliably located by users for decades. Placing them elsewhere defeats the zero-interaction-cost benefit that makes breadcrumbs valuable.

***

### Truncation and overflow

If a breadcrumb trail is too long to fit on one line, truncate the current page node's label rather than wrapping the breadcrumb to a second line. Wrapping breaks the visual scan pattern and consumes vertical space disproportionate to the breadcrumb's secondary-navigation role.

If truncating the current page node still doesn't fit, consider truncating individual parent node labels. As a last resort on extremely deep hierarchies, collapse middle parent nodes into a single overflow indicator (e.g. `Home > ... > Parent > Current Page`) that expands on click to reveal the hidden levels.

🚫 Don't wrap breadcrumbs onto multiple lines. Truncate instead, per the [truncation and overflow guidelines](reading-information/truncation-and-overflow.md).

***

### What not to do

🚫 **Don't use breadcrumbs on shallow applications.** If your application is only 1 level deep (not counting the product homepage), breadcrumbs add visual weight without orientation value.

🚫 **Don't use breadcrumbs for linear processes.** Multi-step forms, wizards, and checkout flows need a [stepper](steppers.md), not a breadcrumb. Breadcrumbs imply hierarchy; steppers imply sequence.

🚫 **Don't make the current page node a clickable link.** It's the current page — there's nowhere for it to go. Reflecting this in markup and styling (no underline, no hover state) matches user expectations.

🚫 **Don't include the dividers in the accessible name of links.** Screen readers will read them as "slash" or "greater than" which clutters the announcement and adds no value.

🚫 **Don't wrap breadcrumbs to multiple lines.** Truncate instead.

🚫 **Don't replace the page title with the breadcrumb's current page node.** The breadcrumb's current page node is a small, subdued navigation marker. The page's h1 is the page's title. They serve different purposes and both should be present.

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src=".gitbook/assets/ux-breadcrumbs (1).md" %}

[Learn how to use](resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

[**Breadcrumb Navigation Increasingly Useful**](https://www.nngroup.com/articles/breadcrumb-navigation-useful/)

Nielsen Norman Group, 2007

[**Breadcrumbs: 11 Design Guidelines for Desktop and Mobile**](https://www.nngroup.com/articles/breadcrumbs/)

Nielsen Norman Group, 2018

[**Breadcrumb Pattern**](https://www.w3.org/WAI/ARIA/apg/patterns/breadcrumb/)

W3C ARIA Authoring Practices Guide

[**Breadcrumb component**](https://designsystem.digital.gov/components/breadcrumb/)

U.S. Web Design System (USWDS)

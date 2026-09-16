---
description: >-
  Skills and markdown files for AI design reviews, AI prototyping, and vibe
  coding
---

# AI skills

### Using with AI tools

Before using the [individual skill files](ai-skills.md#individual-skills-for-each-ux-pattern-guideline) below, get your AI tool ready to use them.

{% hint style="warning" %}
**Don't let your AI agent hard code the&#x20;**_**contents**_**&#x20;of any UX pattern guideline page to your own skill files.**

These pages get updated often, so it would quickly become out of date. Each skill file is crafted to do runtime lookups to the live UX pattern guidelines on this website each time it's invoked so that it gets the latest and greatest.
{% endhint %}

<details>

<summary>Without any specific tool</summary>

Just copy the URL from the desired guideline page(s) and paste to your agent.

Ask your agent to use it to shape your design. That's it.

You don't even _need_ the skill files.

Otherwise, some tools also let you drag and drop .md files into the agent prompt.

</details>

<details>

<summary>With <strong>Claude Code</strong></summary>

Download `CLAUDE.md` and place it in the same folder as your skill files. Claude Code will automatically discover any `ux-*.md` skill files in that folder and apply the relevant ones to your work — no additional setup needed.

{% hint style="info" %}
**If you already have a CLAUDE.md file** in your project, don't replace it — copy the contents of this file and paste them at the bottom of your existing one.
{% endhint %}

When you download new skills, just drop them in the same folder. `CLAUDE.md` picks them up automatically.

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/claude.md" %}

</details>

<details>

<summary>With <strong>Cursor</strong></summary>

Each UX pattern guideline below is a markdown file with a short description at the top so the AI knows when it applies.

1. (Create the `skills` folder if it doesn’t exist.)
2. Add our starter `SKILL.md` to that folder _once_ (we provide it—it tells Cursor how to find and use every other `.md` in the same folder).
3. Drop in whichever guideline `.md` files you downloaded. You can add more anytime—no need to edit `SKILL.md` each time.

In Cursor, mention the skill (e.g. type `@` and choose ux pattern guidelines) or ask the agent to follow your UX pattern guidelines before you review or build UI.

That’s it.

{% file src="/broken/files/KFG6WDNUZeLgd7eg6i5a" %}

</details>

<details>

<summary>With <strong>GitHub Copilot in VS Code</strong></summary>

Download the skill files plus `copilot-instructions.md`. Place `copilot-instructions.md` in a `.github/` folder at your project root (so the path is `.github/copilot-instructions.md`) and put the skill files in a dedicated folder in your project, such as `docs/ux-skills/` or wherever fits your project's structure. The instructions file tells Copilot to scan recursively, so any folder location works.

If you already have a `.github/copilot-instructions.md` file, don't replace it — copy the contents of this file and paste them at the bottom of your existing one.

When you download new skills, drop them into the same folder. Copilot picks them up automatically.

{% hint style="info" %}
Setup varies across Copilot configurations and team settings. If this path doesn't work in your environment, check with your team for how custom instructions are configured.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/copilot-instructions.md" %}

</details>

***

### Individual skills for each UX pattern guideline

Pick and choose which skills are relevant for your scope. Download as many or as few as are relevant.

### Layout and navigation <a href="#layout-and-navigation" id="layout-and-navigation"></a>

#### Breadcrumbs <a href="#breadcrumbs" id="breadcrumbs"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-breadcrumbs.md" %}

#### Button alignment <a href="#button-alignment" id="button-alignment"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-button-alignment.md" %}

#### Hover interactions <a href="#hover-interactions" id="hover-interactions"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-hover-interactions.md" %}

#### Hyperlinks versus link buttons <a href="#hyperlinks-versus-link-buttons" id="hyperlinks-versus-link-buttons"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-hyperlinks-vs-link-buttons.md" %}

#### Modals, lightboxes, and dialogs <a href="#modals-lightboxes-and-dialogs" id="modals-lightboxes-and-dialogs"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-modals.md" %}

#### Opening links in same vs new tab <a href="#opening-links-in-same-vs-new-tab" id="opening-links-in-same-vs-new-tab"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-link-tab-behavior.md" %}

#### Tabs <a href="#tabs" id="tabs"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-tabs.md" %}

### Lists and tables <a href="#lists-and-tables" id="lists-and-tables"></a>

#### Bulk actions <a href="#bulk-actions" id="bulk-actions"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-bulk-actions.md" %}

#### Column alignment <a href="#column-alignment" id="column-alignment"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-column-alignment.md" %}

#### Empty states <a href="#empty-states" id="empty-states"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-empty-states.md" %}

#### Filters <a href="#filters" id="filters"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-filters.md" %}

#### Tables <a href="#tables" id="tables"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-tables.md" %}

### Reading information <a href="#reading-information" id="reading-information"></a>

#### Accordions <a href="#accordions" id="accordions"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-accordions.md" %}

#### Cards <a href="#cards" id="cards"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-cards.md" %}

#### Datestamps and timestamps <a href="#datestamps-and-timestamps" id="datestamps-and-timestamps"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-datestamps.md" %}

#### Descriptions versus tooltips <a href="#descriptions-versus-tooltips" id="descriptions-versus-tooltips"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-descriptions-vs-tooltips.md" %}

#### Environmental errors <a href="#environmental-errors" id="environmental-errors"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-environmental-errors.md" %}

#### Grammar, voice, and tone <a href="#grammar-voice-and-tone" id="grammar-voice-and-tone"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-grammar-voice-tone.md" %}

#### Information banners <a href="#information-banners" id="information-banners"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-information-banners.md" %}

#### Line lengths and text wrapping <a href="#line-lengths-and-text-wrapping" id="line-lengths-and-text-wrapping"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-line-lengths.md" %}

#### Loading dialogs <a href="#loading-dialogs" id="loading-dialogs"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-loading-dialogs.md" %}

#### Onboarding <a href="#onboarding" id="onboarding"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-onboarding.md" %}

#### Skeleton loaders <a href="#skeleton-loaders" id="skeleton-loaders"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-skeleton-loaders.md" %}

#### Tooltips <a href="#tooltips" id="tooltips"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-tooltips.md" %}

#### Truncation and overflow <a href="#truncation-and-overflow" id="truncation-and-overflow"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-truncation-and-overflow.md" %}

### Form experience <a href="#form-experience" id="form-experience"></a>

#### Saving drafts <a href="#saving-drafts" id="saving-drafts"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-saving-drafts.md" %}

#### Autosaving <a href="#autosaving" id="autosaving"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-autosaving.md" %}

#### Canceling <a href="#canceling" id="canceling"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-canceling.md" %}

#### Destructive actions and deleting <a href="#destructive-actions-and-deleting" id="destructive-actions-and-deleting"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-destructive-actions.md" %}

#### Disabled buttons <a href="#disabled-buttons" id="disabled-buttons"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-disabled-buttons.md" %}

#### Combining buttons and styles <a href="#combining-buttons-and-styles" id="combining-buttons-and-styles"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-combining-buttons.md" %}

#### Error validation <a href="#error-validation" id="error-validation"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-error-validation.md" %}

#### Field alignment and column layout <a href="#field-alignment-and-column-layout" id="field-alignment-and-column-layout"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-field-alignment.md" %}

#### Multi-step forms <a href="#multi-step-forms" id="multi-step-forms"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-multi-step-forms.md" %}

#### Required versus optional fields <a href="#required-versus-optional-fields" id="required-versus-optional-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-required-optional-fields.md" %}

#### Reviewing / review step <a href="#reviewing-review-step" id="reviewing-review-step"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-review-step.md" %}

#### Saving state on buttons <a href="#saving-state-on-buttons" id="saving-state-on-buttons"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-saving-state-buttons.md" %}

#### Steppers <a href="#steppers" id="steppers"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-steppers.md" %}

#### Success notification <a href="#success-notification" id="success-notification"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-success-notification.md" %}

### Entering information <a href="#entering-information" id="entering-information"></a>

#### Anatomy of form field <a href="#anatomy-of-form-field" id="anatomy-of-form-field"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-form-field-anatomy.md" %}

#### Autocomplete <a href="#autocomplete" id="autocomplete"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-autocomplete.md" %}

#### Button groups <a href="#button-groups" id="button-groups"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-button-groups.md" %}

#### Checkbox fields <a href="#checkbox-fields" id="checkbox-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-checkbox-fields.md" %}

#### Combo box fields <a href="#combo-box-fields" id="combo-box-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-combo-box.md" %}

#### Conditional fields <a href="#conditional-fields" id="conditional-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-conditional-fields.md" %}

#### Date fields <a href="#date-fields" id="date-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-date-fields.md" %}

#### Dropdown lists <a href="#dropdown-lists" id="dropdown-lists"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-dropdown-lists.md" %}

#### File upload <a href="#file-upload" id="file-upload"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-file-upload.md" %}

#### Listbox fields <a href="#listbox-fields" id="listbox-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-listbox-fields.md" %}

#### Paragraph fields <a href="#paragraph-fields" id="paragraph-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-paragraph-fields.md" %}

#### Password fields and sign in <a href="#password-fields-and-sign-in" id="password-fields-and-sign-in"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-password-fields.md" %}

#### Phone number fields <a href="#phone-number-fields" id="phone-number-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-phone-number-fields.md" %}

#### Placeholder variables <a href="#placeholder-variables" id="placeholder-variables"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-placeholder-variables.md" %}

#### Radio button fields <a href="#radio-button-fields" id="radio-button-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-radio-button-fields.md" %}

#### Ranked list fields <a href="#ranked-list-fields" id="ranked-list-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-ranked-list-fields.md" %}

#### Time fields <a href="#time-fields" id="time-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-time-fields.md" %}

#### Time zone fields <a href="#time-zone-fields" id="time-zone-fields"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-time-zone-fields.md" %}

#### Toggle switches <a href="#toggle-switches" id="toggle-switches"></a>

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-toggle-switches.md" %}

***

### Contact

**Dan Owens**\
Principal UX Designer

PAR Engagement

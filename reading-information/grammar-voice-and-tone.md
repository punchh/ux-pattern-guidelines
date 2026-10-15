---
description: A UI copy checklist for labeling a product's most text-dependent elements
---

# Grammar, voice, and tone

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](grammar-voice-and-tone.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

## Voice

**Write in the 1st person (from the user’s perspective) for actions the user fires themselves**

You'll mostly find these on buttons.

{% columns %}
{% column %}
✅ Launch campaign
{% endcolumn %}

{% column %}
🚫 Campaign launch
{% endcolumn %}
{% endcolumns %}

***



**...but don’t use the word ‘My’ to prefix features or content**

Refrain from using superfluous possessive adjectives. Just use the unique word alone.  

Possible exception: The user is looking at a list of mix content and needs to distinguish or filter items created themselves versus items created by others. Even then, first try using the user’s first name to personalize before going with “My”.

{% columns %}
{% column %}
✅ Campaigns

✅ Dan's campaigns

✅ Dashboard
{% endcolumn %}

{% column %}
🚫 My campaigns

🚫 My dashboard
{% endcolumn %}
{% endcolumns %}

***



**Use specific action verb phrases on buttons and links for destructive, irreversible, or financial actions**

For buttons that aren't any of those, you don't necessarily need to use a verb. Some examples:

* Answers a question ("Yes", "Not yet")
* Conventional nav state change or terminator ("Next", "Back", dismissals like "Got it")
* Navigating to a choice among peers, like a content page or listing: ("Templates", "Plans", "Tiers")



{% columns %}
{% column %}
✅ Yes, delete campaign
{% endcolumn %}

{% column %}
🚫 OK

🚫 Proceed

🚫 Submit
{% endcolumn %}
{% endcolumns %}

***

**Use American English spelling**

No UK English here.

{% columns %}
{% column %}
✅ Color

✅ Center

✅ Canceled
{% endcolumn %}

{% column %}
🚫 Colour

🚫 Centre

🚫 Cancelled
{% endcolumn %}
{% endcolumns %}

***

## Tone

**Write using conversational phrases like a human, not a robot**

Be casual and informal (lending itself to brevity) - this is an overarching principle that should apply to pretty much everything in this checklist.

{% columns %}
{% column %}
✅ Looks like there was a problem
{% endcolumn %}

{% column %}
🚫 Error validation failure. Retry.
{% endcolumn %}
{% endcolumns %}

***

**Strive to use 2-syllable words where possible**

2 syllables or fewer increases accessibility for varying reading levels. It’s also a boon to users who speak English as a second language.

Moreover, if choosing between 2 synonyms, _most_ of the time use the one with fewer syllables unless other guidelines on this page say otherwise (for example, the [word choice](grammar-voice-and-tone.md#word-choice) section may call for using the more-syllable word over the fewer-syllable one in certain situations).

{% columns %}
{% column %}
✅ Turn on

✅ Make

✅ Need
{% endcolumn %}

{% column %}
🚫 Authorize

🚫 Fabricate

🚫 Ensure
{% endcolumn %}
{% endcolumns %}

***

**Be informal and brief - like speaking with a friend**

A great example is in confirmation prompts: write like you’re talking to a good acquaintance that’s comfortable and familiar.

{% columns %}
{% column %}
✅ Save changes?
{% endcolumn %}

{% column %}
🚫 Would you like to save your changes?
{% endcolumn %}
{% endcolumns %}

***

**Be emotionally resonant**

Words in the UI should go beyond pure function: They should connect with the user’s feelings and values.  

General usability ensures our products are functional and easy to navigate. Emotional resonance creates a sense of trust, comfort, and delight.

{% columns %}
{% column %}
✅ Never shared, never sold - your info is safe with us
{% endcolumn %}

{% column %}
🚫 This information is required
{% endcolumn %}
{% endcolumns %}

***

**Use words that foster emotional engagement**

Emotional resonance aligns our UI copy with a user’s feeling or values.  

Emotional engagement fosters ongoing involvement across interactions and sessions, and makes the user keep coming back.  

In UI copy, we can choose words that encourage return visits and usage.

{% columns %}
{% column %}
✅ You're just 1 delicious meal away from rewards
{% endcolumn %}

{% column %}
🚫 No redemptions available
{% endcolumn %}
{% endcolumns %}

***

**Don’t use adjectives that imply the user should perceive something as “simple”**

We can’t assume the user will agree with the designer’s perceived simplicity.

{% columns %}
{% column %}
✅ (just explain what to do)
{% endcolumn %}

{% column %}
🚫 Simply...

🚫 As you would expect...
{% endcolumn %}
{% endcolumns %}

***

**Don't say please**

Save the user the time of having to read an extra word, if for no other reason than to reduce cognitive load.

{% columns %}
{% column %}
✅ Enter a value greater than 0
{% endcolumn %}

{% column %}
🚫 Please enter a value greater than 0
{% endcolumn %}
{% endcolumns %}

***

## Word choice

### Save versus done

Use "Save" when a change is [committed to a database](../form-experience/editing-and-saving-forms.md) as a permanent record (even if it can be edited or deleted in the future). Don't use "Done".

Save can also work on a modal form that launches in the midst of a larger underlying form (like when [building an array](../layout-and-navigation/modals-lightboxes-and-dialogs.md#multi-field-form)). Even though technically the database record isn't written to until the underlying form gets saved (a "deferred save"), the modal form contributes to the broader form, so that specific kind of modal uses the button label Save.

### Apply versus done or save

Use "Apply" for some temporary state change like a [filter](../lists-and-tables/filters.md), or some temporary change to a view.

### Create versus add

Use "Create" for starting to build a new major piece of content, often from a list page.

Use "Add" for adding an item to an [array](../layout-and-navigation/modals-lightboxes-and-dialogs.md#multi-field-form), or some other set of multiples.

### Edit versus manage

Use “Edit” when you can change the input of a field (letters, numbers, properties).

Use “Manage” when you can change selections and options, especially for organizing a list of options (like labels or tags for content). Pair this verb with a noun to make it clear what is being managed. For example: "Manage labels"

### Delete versus remove

Use “Delete” when the content will be permanently erased from the database.

Use "Remove" if the content is eliminated from the current view or selection but still exists in the database.

### View versus see

Use "View” for navigating to a specific page or section for more details, or to reveal more information. Use it on buttons, calls to action, and link text.

{% columns %}
{% column %}
✅ View all guests

✅ View details

✅ View report
{% endcolumn %}

{% column %}
🚫 See all guests

🚫 See order

🚫 See report
{% endcolumn %}
{% endcolumns %}

Use "see" in very general conversational descriptions - usually not the first word of a sentence or label - when there's no specific call to action.

{% columns %}
{% column %}
✅ Manage how others see profile information
{% endcolumn %}

{% column %}
🚫 Manage how others view profile information
{% endcolumn %}
{% endcolumns %}

### Need versus must

Use "need" for describing something that's required.

Don't use "must".

"Need" is more plain language conversational.

{% columns %}
{% column %}
✅ File size needs to be less than 1 MB
{% endcolumn %}

{% column %}
🚫 File size must be under 1 MB
{% endcolumn %}
{% endcolumns %}

### Download versus export

Use “Download” for actions that INSTANTLY fire the users folder/location picker for a downloadable file without any options or configuration for the file in between.

Use "Export..." (usually with that [ellipsis](grammar-voice-and-tone.md#ellipses) too) when there's configuration options for generating the file between the click and the actual download. Once on the export configuration form, the button to actual fire getting the configured file is still "Export" in this context.

So recapping: "Download" is for a straightforward no frills file. "Export..." (with an ellipsis) signifies more robust customization lies ahead, and "Export" is the button label on the page where those export configuration options were made.

{% columns %}
{% column %}
✅ Download as PNG

✅ Export report... (where clicking offers options for formatting the report, or what data to include)
{% endcolumn %}

{% column %}
🚫 Export as PNG

🚫 Download report... (where clicking offers options for formatting the report, or what data to include)
{% endcolumn %}
{% endcolumns %}

### Upload versus import

Use “Upload” for actions that allow a user to select a file on their device and upload it to our products.

Use "Import" for bringing in a set of data from another product or database, or when parsing a file from the user for use as structured data in the product.

{% columns %}
{% column %}
✅ Upload image

✅ Import menu items from Point-of-Sale

✅ Import CSV guest list (to build a segment)
{% endcolumn %}

{% column %}
🚫 Import image

🚫 Upload menu items from Point-of-Sale

🚫 Upload CSV guest list (to build a segment)
{% endcolumn %}
{% endcolumns %}

### Sign in versus Log in

Use "Sign in" as the verb for authenticating.

Don't use "Log in" as it leans more technical.

{% columns %}
{% column %}
✅ Sign in
{% endcolumn %}

{% column %}
🚫 Log in
{% endcolumn %}
{% endcolumns %}

### Sign in versus sign-in

Use "Sign in" as a verb.

{% columns %}
{% column %}
✅ Sign in (as a call to action)
{% endcolumn %}

{% column %}
🚫 Sign-in (as a call to action)
{% endcolumn %}
{% endcolumns %}

Use "Sign-in" as a noun or adjective.

{% columns %}
{% column %}
✅ You'll be able to set your preferences after sign-in

✅ Reset your sign-in password
{% endcolumn %}

{% column %}
🚫 You'll be able to set your preferences after sign in

🚫 Reset your sign in password
{% endcolumn %}
{% endcolumns %}

### Sign up versus Create account or Join

Don't use "Sign up".

* It's too linguistically similar to "Sign in", so it's especially conflicting to use on the same page
* It's not specific enough and doesn't convey the benefits. Signing up for something has an effort and privacy cost, so use a more incentivized label

Use "Create account" for a more administrative account creation experience.

Use "Join \[program name or perk]" or "Get \[perks or benefits]" for loyalty or membership related accounts.

{% columns %}
{% column %}
✅ Create account

✅ Join rewards

✅ Join ACME Loyalty

✅ Start saving
{% endcolumn %}

{% column %}
🚫 Sign up
{% endcolumn %}
{% endcolumns %}

***

## Capitalization

**Don’t use all caps (though typography styles may dictate otherwise)**

Don’t manually type any words in all caps (except for acronyms and file type extensions).  

Understand that your design system may use typography on some elements that’s all caps - that’s okay.

{% columns %}
{% column %}
✅ Column heading

✅ Subheading

✅ PDF
{% endcolumn %}

{% column %}
🚫 COLUMN HEADING

🚫 SUBHEADING

🚫 pdf
{% endcolumn %}
{% endcolumns %}

***

**Use sentence case for subheadings, buttons, links, modal and page titles**

Even when a phrase is just a couple of words long, use sentence case. While Title Case creates the perception of symmetry and seriousness (nothing wrong with that), the PAR brand leans human and approachable.

Exceptions coming up next.

{% columns %}
{% column %}
✅ Go back

✅ Launch campaign

✅ Sign out

✅ Sign in

✅ Log in (as a verb)

✅ Your login information

✅ Check in

✅ Guest checkin
{% endcolumn %}

{% column %}

{% endcolumn %}
{% endcolumns %}

***

**...but use Title Case on any of those when it's a marketable product feature**

If your element is referring to the name of a product feature - particularly landing pages like Campaign Management or All Segments - use Title Case for the product feature portion of the text. These often appear in elements like nav, buttons, modal titles, and page titles.

However, if the feature is merely a create or edit variant of the main feature (like "Create campaign" or "Edit segment"), use sentence case for those.

Standalone mentions of generic content types - like ‘campaign’, 'segments', or 'guests' - don’t need to use title case by themselves unless preceded by an adjective for the purpose of referring to a marketable product.

{% columns %}
{% column %}
✅ Data Pipeline

✅ Smart Segments

✅ Create campaign
{% endcolumn %}

{% column %}
🚫 data pipeline

🚫 Smart segments

🚫 Create Campaign
{% endcolumn %}
{% endcolumns %}

***

**Also use Title Case for trademarked nouns, languages, countries, people, important universal documents, and standalone job titles**

Job titles should be capitalized when they are not used in a sentence and whether before or after a person’s name.

{% columns %}
{% column %}
✅ Apple Pay

✅ Terms of Use

✅ Senior Brand Manager

✅  Mr. Hanson is a senior brand manager.
{% endcolumn %}

{% column %}
🚫 Apple pay

🚫 Terms of use

🚫 Mr. Hanson is a Senior Brand Manager.
{% endcolumn %}
{% endcolumns %}

***

## Grammar and style

### Tense

**Use present tense, not present perfect tense (notably in success notifications)**

Present perfect tense adds too many words, syllables, and strokes, and strays too far from our casual style.

{% columns %}
{% column %}
✅ Message sent
{% endcolumn %}

{% column %}
🚫 The message has been sent
{% endcolumn %}
{% endcolumns %}

***

### Abbreviations

**Use full, unabbreviated words**

Full stop. Don’t make users spend brain cycles on decoding acronyms, nor make them refer to a glossary to translate.  This goes back to the fundamental principle of speaking like a human, not a robot.

Exceptions:

* File format extensions
* [Column headers in a table](../lists-and-tables/tables.md#header-row) (especially when the content in the cells below the header are particularly narrow anyway - like small numeric values. No sense in having a wide column just to fit a super wide unabbreviated text label when the values underneath are all a small handful of characters long)
* Time zones when on a [date/time stamp](datestamps-and-timestamps.md) (and also used to accompany the abbreviated time zone name on a [time zone picker](../entering-information/time-zone-fields.md))

{% columns %}
{% column %}
✅ with or without

✅ Example

✅ In essence

✅ Qualification Criteria

✅ Line Item Selector

✅ PDF
{% endcolumn %}

{% column %}
🚫 w/wo

🚫 Ex., e.g.

🚫 i.e.

🚫 QC

🚫 LIS

🚫 Portable Document Format
{% endcolumn %}
{% endcolumns %}

***

**Even if citing an example, don’t abbreviate the word “Example”**

The full word “example” is least ambiguous. Abbreviations like “ex.” are too easily confused with “excluding”, and “e.g.” is often used incorrectly.

{% columns %}
{% column %}
✅ Example: A subscription renews monthly
{% endcolumn %}

{% column %}
🚫 Ex. A Subscription renews monthly
{% endcolumn %}
{% endcolumns %}

***

### Contractions

**Use contractions when they'd likely be spoken in an informal American English conversation. Don't use contractions if it would sound awkward or unconventional for American English.**

"Should've", "could've", "would've", and "they've" are regarded as harder to read, so avoid those.

{% columns %}
{% column %}
✅ You'll have 5 minutes to use it

✅ You got the offer but it’s not available here

✅ You've reached the maximum number of points

✅ We'll inform you when new ones are available

✅ What's your name and phone number?

✅ The cash amount can't be lower than the bill

✅ What's the code?

✅ We’d like to get to know you better

✅ When enabled, users won’t be able to use one phone number with multiple accounts

✅ This can't be undone&#x20;
{% endcolumn %}

{% column %}
🚫 This'll permanently delete the application

🚫 Choose which chains and stores would've coupons enabled

🚫 There're no applications added yet

🚫 Only recipients who've the “Printer” alert type assigned are visible

🚫 Your selected time was not available

🚫 This cannot be undone
{% endcolumn %}
{% endcolumns %}

***

**Only use an ampersand (&) when it's part of a proper noun like a brand name. Otherwise, spell out "and" instead.**

In extreme outlier cases, use an ampersand instead of "and" in tight spaces for column headers after you've exhausted other solutions.

{% columns %}
{% column %}
✅ Enable and manage your payment providers and methods
{% endcolumn %}

{% column %}
🚫 Enable and manage your payment providers & methods
{% endcolumn %}
{% endcolumns %}

***

## Punctuation

### Periods

[**Field Descriptions**](../entering-information/anatomy-of-form-field.md#description-text)**: No punctuation at the end pretty much all the time**

Descriptions should be written short enough that you don’t need a period at the end. Most descriptions should be a short instructive phrase that’s not a complete sentence anyway. Even if a description is technically a complete sentence grammatically speaking, it should be written short enough that it doesn’t look “wrong” to omit the period. <br>

In other words, if you find yourself writing a field description so long that it has you wondering whether it should have a period (or a line break, or how wrapping should work, etc.), that’s probably a good sign your description is too long.

{% columns %}
{% column %}
✅ At least 8 characters with a number and symbol
{% endcolumn %}

{% column %}
🚫 At least 8 characters with a number and symbol.
{% endcolumn %}
{% endcolumns %}

***

[**Tooltips**](tooltips.md)**: No punctuation unless multiple sentences**

While Tooltips have a bit more allowance for longer statements, generally avoid sentences so long that you think it might need a period. If a tooltip genuinely needs to break into multiple sentences, it’s okay to use a period at the end of sentences.

{% columns %}
{% column %}
✅ Stored using 256-bit encryption
{% endcolumn %}

{% column %}
🚫 Stored using 256-bit encryption.
{% endcolumn %}
{% endcolumns %}

***

[**Information Banners**](information-banners.md)**: Only use punctuation if a genuine complete sentence**

Information banners have a bit more leeway for writing in long form compared to a field description, but still strive to keep it short, phrase-based, and omit the period. Once it becomes a full sentence though (in essence: has a verb), use a period.

{% columns %}
{% column %}
✅ Profile information refreshed nightly

✅ New campaigns may take up to 24 hours to process.
{% endcolumn %}

{% column %}
🚫 Profile information refreshed nightly.

🚫 New campaigns may take up to 24 hours to process
{% endcolumn %}
{% endcolumns %}

***

[**Toast messages**](../form-experience/success-notification.md)**: No punctuation**

Treat toasts like very short status messages: favor no period for single, brief lines, and use normal punctuation only when you have more than one sentence.

{% columns %}
{% column %}
✅ Message sent
{% endcolumn %}

{% column %}
🚫 Profile updated.
{% endcolumn %}
{% endcolumns %}

***

**Buttons, links, modal titles, page titles, subheadings: No punctuation**

Exception: Buttons sometimes end in an ellipsis.

{% columns %}
{% column %}
✅ Yes, delete this store
{% endcolumn %}

{% column %}
🚫 Yes, delete this store.
{% endcolumn %}
{% endcolumns %}

***

[**Empty states, blank states, no results states**](../lists-and-tables/empty-states.md)**: No punctuation**

{% columns %}
{% column %}
✅ No gift cards to see
{% endcolumn %}

{% column %}
🚫 No gift cards to see.
{% endcolumn %}
{% endcolumns %}

***

**Body text: Use punctuation**

We have fewer instances of genuine body text in our SaaS apps and product, but when we do, use full sentences, periods, and regular punctuation.

{% columns %}
{% column %}
✅ Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
{% endcolumn %}

{% column %}
🚫 (don't neglect to use full sentences and punctuation in body text)
{% endcolumn %}
{% endcolumns %}

***

**Subtitles: Usually no punctuation**

Usually found beneath a heading or subheading, subtitles have a bit more leeway for writing in long form compared to the "H" heading itself, but still strive to keep subtitles short, phrase-based, and omit the period. Once it becomes a full sentence though (in essence: has a verb), use a period.

{% columns %}
{% column %}
✅&#x20;

**Page title:**

Line Item Selectors

**Subtitle:**

Filters for identifying menu items as they appear in your point-of-sale system
{% endcolumn %}

{% column %}
🚫&#x20;

**Page title:**

Line Item Selectors

**Subtitle:**

Filters for identifying menu items as they appear in your point-of-sale system.
{% endcolumn %}
{% endcolumns %}

***

**Buttons, Navigation Menu Items, Dropdown menu values, Radio list values, other form field control values: Never use punctuation**

Just the label, no punctuation.

{% columns %}
{% column %}
✅ Launch campaign
{% endcolumn %}

{% column %}
🚫 Launch campaign.
{% endcolumn %}
{% endcolumns %}

***

### Exclamation points

**Never use exclamatory punctuation**

That would be a little too casual.  

{% columns %}
{% column %}
✅ Looks like there was a problem
{% endcolumn %}

{% column %}
🚫 Oh no! Did you really want to do that?!
{% endcolumn %}
{% endcolumns %}

***

### Question marks

**Use question marks only in specific contexts**

One of the only elements suitable for using a question mark are [confirmation prompts in the modal window](../layout-and-navigation/modals-lightboxes-and-dialogs.md#confirmation-prompt) title.

In some conversational form experiences (like a wizard where the user is guided to fill information 1 field at a time or so), it's okay to use a question mark as the field label.

Don't use them on [checkbox fields](../entering-information/checkbox-fields.md#as-a-single-option-confirmation-field) nor [toggle switches](../entering-information/toggle-switches.md) (those should be phrased in the declarative).

{% columns %}
{% column %}
✅&#x20;

(on a confirmation prompt)

Deactivate guest?

✅&#x20;

(in a wizard)

What do you want to call this template?&#x20;
{% endcolumn %}

{% column %}
🚫&#x20;

(on an individual checkbox field)

Allow coupon stacking?

🚫&#x20;

(on a checkbox field or toggle)

Allow coupon stacking?
{% endcolumn %}
{% endcolumns %}

***

### Apostrophes

Use apostrophes to represent omitted letters or numbers:

* Omitted numbers (’40s)
* Omitted letters (don’t, can’t, won’t)
* Verb contractions (it’s, you’re, we’re)

Use apostrophes to form possessives:

* Singular nouns: add _’s_, even if they end in _s_ (client’s, bus’s)
* Plural nouns that don’t end in s: add _’s_ (women’s, men’s)
* Plural nouns that end in s: add an apostrophe (boxes’, customers’)

Don’t use apostrophes to form possessive pronouns such as hers or his.

To type an apostrophe, just use the apostrophe key on your keyboard next to your Enter key, like you always probably have. Some design software may convert it to a more-grammatically correct curly apostrophe, which is preferred, but if your software doesn't, it's not a deal breaker. Don't go revising designs for this.

{% columns %}
{% column %}
✅ Client's store

✅ Women's clothing

✅ Customers' credit cards

✅ ’
{% endcolumn %}

{% column %}
🚫 Clients store

🚫 Womens clothing

🚫 Customers credit cards

🚫'
{% endcolumn %}
{% endcolumns %}

***

### Colons

Avoid using colons in sentences, but it's not a deal breaker if you do sometimes. If you need to use one, don’t capitalize the first word after the colon unless it’s a proper noun.

Don't use colons to introduce radio buttons or checkboxes.

Use colons to introduce a bulleted list in body text. Don't use it in a heading/subheading though.

{% columns %}
{% column %}
✅&#x20;

(in a subtitle)

Group stores to easily manage configurations, settings, or entities

✅&#x20;

(in a radio field)

Order for

* [ ] &#x20;Dine-in
* [ ] Takeout
* [ ] Delivery

✅&#x20;

(in body text)

If you delete your account:

* You will no longer be able to log in with your account
* You will no longer be able to see receipts of all of your past orders
* You will no longer be able to order delicious meals from our restaurants
{% endcolumn %}

{% column %}
🚫&#x20;

(in a subtitle)

Group stores to easily manage: configurations, settings or entities

🚫

(in a radio field)

Order for:

* [ ] &#x20;Dine-in
* [ ] Takeout
* [ ] Delivery

🚫&#x20;

(in body text)

If you delete your account

* you will no longer be able to log in with your account
* you will no longer be able to see receipts of all of your past orders
* you will no longer be able to order delicious meals from our restaurants
{% endcolumn %}
{% endcolumns %}

***

### Commas

Use the Oxford comma (also known as the serial comma) in sentences. There should be a comma after every list of 3 or more items (unless you’re using a bulleted or numbered list).

Don’t use commas to separate bulleted or numbered list items.

{% columns %}
{% column %}
✅ Invite users, edit their details, and manage their store level access
{% endcolumn %}

{% column %}
🚫 Invite users, edit their details and manage their store level access
{% endcolumn %}
{% endcolumns %}

***

### Ellipses

The ellipses (...) can be used in several places throughout the interface.

Use ellipses for:

* Text [overflow](truncation-and-overflow.md) (if the space for the text is limited)
* If there are more options behind actions in the menu

Don’t use ellipses for:

* Placeholder copy

{% columns %}
{% column %}
✅ More filters... (where there are configuration options that follow before actually executing the action)

✅ Export... (where there are configuration options that follow before actually executing the action)

✅ Search by name (where there are no options or configuration that follow)


{% endcolumn %}

{% column %}
🚫 More filters (where there are configuration options that follow before actually executing the action)

🚫 Export (where there are configuration options that follow before actually executing the action)

🚫 Search by name... (where there are no options or configuration that follow)
{% endcolumn %}
{% endcolumns %}

***

### En-dashes and em-dashes

Don't use any kind of dash to join a range of numbers nor dates/times (see [date and timestamp guidelines](datestamps-and-timestamps.md#schedules-and-time-ranges) for more on this).

{% columns %}
{% column %}
✅ 2020 to 2026
{% endcolumn %}

{% column %}
🚫 2020-2026
{% endcolumn %}
{% endcolumns %}

***

Use a dash to indicate an abrupt or dramatic change in a sentence - like this. Technically the proper character to use for this is an em-dash ( — ) with a space on either side, but it's not terrible to use the dedicated en-dash key on our keyboard next to the 0 key.

{% columns %}
{% column %}
✅ Choose your theme’s colors, typography, and pictures — all in one place.
{% endcolumn %}

{% column %}
🚫 Choose your theme’s design—colors, typography, and pictures—all in one place.
{% endcolumn %}
{% endcolumns %}

***

### Hyphens

Use hyphens to form a single idea from multiple words. When two or more words function together as a descriptor or adjective, we typically hyphenate those words if they precede the noun they describe but don't hyphenate if they come after the noun.

{% columns %}
{% column %}
✅ Create and manage integrations for third-party ordering channels

✅ Enable and manage configurations and controls for brand-specific white-label apps

✅ Auto-assignment settings
{% endcolumn %}

{% column %}
🚫 Create and manage integrations for third party ordering channels

🚫 Enable and manage configurations and controls for brand specific white label apps

🚫 Auto assignment settings
{% endcolumn %}
{% endcolumns %}

Hyphenated compound words are the ones with a hyphen between the words. Over time, many hyphenated compounds become closed compounds — _teen-ager_ became _teenager_ for instance. Check a dictionary if you’re not sure whether to use a hyphen or not. Never use hyphens in the words "reorder” and "email.”

Sometimes our long-running legacy products use a hypenless compound word that are an exception to the grammatical convention. For product and branding consistency, use the grammatically "incorrect" version. "Checkin" is a good example of this.

{% columns %}
{% column %}
✅ Dine-in

✅ e-commerce

✅ Checkin (only because our product naming has established a counter convention)
{% endcolumn %}

{% column %}
🚫 Dinein

🚫 ecommerce

🚫 Check-in (only because our product naming has established a counter convention)
{% endcolumn %}
{% endcolumns %}

***

## Numbers

For numbers in dates and times, see [date and timestamp guidelines](datestamps-and-timestamps.md#schedules-and-time-ranges).

### Spelled numbers versus numerals

Use numerals. Don't spell out a number.

Numeric characters create fewer strokes and less cognitive load.

Note that support documentation will differ - that's okay; different context.

{% columns %}
{% column %}
✅ 9

✅ You have 3 checkins
{% endcolumn %}

{% column %}
🚫 Nine

🚫 You have three checkins
{% endcolumn %}
{% endcolumns %}

### Long numbers and commas

Use commas for numbers with four or more digits.&#x20;

{% columns %}
{% column %}
✅ 1,000
{% endcolumn %}

{% column %}
🚫 1000
{% endcolumn %}
{% endcolumns %}

### Truncating numbers

Don't truncate numbers EXCEPT if in a hero metric or table cells where all numbers in a data column use truncation.\
\
When truncating, since our products and customers are overwhelmingly Anglo-North American, use capital letter truncation (for example "K" for thousands or "M" for millions) with no space between the alphabetical character and the numeral.

When a truncated number preserves precision such that a digit used a comma when unabbreviated, that comma becomes a decimal point when truncated (for example 1,200 becomes 1.2K, not 1,2K).

Rounding rules will vary by the business context for the data and feature at play.

{% hint style="warning" %}
Understand that Franco-North American and many European locales use a different format and syntax (lowercase, space in between, commas), so consider when working with those markets.
{% endhint %}



{% columns %}
{% column %}
✅  (in a sentence) 1,200

✅  (in a hero metric for an Anglo-North American user) 1.2K
{% endcolumn %}

{% column %}
🚫 (in a sentence) 1K

🚫 (in a hero metric for a United States user) 1,2 k
{% endcolumn %}
{% endcolumns %}

***

## Money and currency

### Default currency

By default, to align with the majority audience for our suite of products, use the dollar symbol to precede currency values (no space between the symbol and the numeral), with up to 2 digits of decimal value (the necessity of including decimals or cents will vary by business context for each feature you design).

{% columns %}
{% column %}
✅  $12

✅  $12.60
{% endcolumn %}

{% column %}
🚫 12 $

🚫 €12

🚫 $12.594
{% endcolumn %}
{% endcolumns %}

### Non-dollar currencies

When designing for non-dollar currencies, like the Euro, use its syntax instead:

* The Euro symbol _follows_ the numeric value
* Euro values omit a comma when separating hundreds from thousands
* Uses a comma _instead of a decimal_ when introducing decimal units.

{% columns %}
{% column %}
✅  12,60 €

✅  1569,99 €
{% endcolumn %}

{% column %}
🚫 €12,60

🚫 1,569.99 €

🚫 1569.99 €
{% endcolumn %}
{% endcolumns %}

***

## Units of measurement

Include a space between the number and the unit.

Capitalization will vary by unit. Follow universal unit standards (English) - they're not all listed here.

{% columns %}
{% column %}
✅  3.4 lb

✅  2 kg

✅  1 cm

✅  1.875 × 3.375 × 13.625 cm
{% endcolumn %}

{% column %}
🚫 3.4lb

🚫 2kg

🚫 1cm

🚫 1.875 × 3.375 × 13.625cm
{% endcolumn %}
{% endcolumns %}

***

## AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-grammar-voice-tone.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

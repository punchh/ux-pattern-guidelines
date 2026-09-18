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

####

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

####

**Use specific action verb phrases on buttons and links for destructive, irreversible, or financial actions**

For buttons that aren't any of those, you don't necessarily need to use a verb. Some examples:

* Answers a question ("Yes", "Not yet")
* Conventional nav state change or terminator ("Done", "Next", "Back", dismissals like "Got it")
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

{% columns %}
{% column %}
✅ Turn on

✅ Make

✅ Must
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

**Use sentence case - even for subheadings, buttons, links, modal and page titles**

Even when a phrase is just a couple of words long, use sentence case. While Title Case creates the perception of symmetry and seriousness (nothing wrong with that), the PAR brand leans human and approachable.

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

**...but use Title Case for specific product features**

If your element is referring to the name of a product feature - particularly landing pages like Campaign Management or All Segments - use Title Case for the product feature portion of the text. These often appear in elements like nav, buttons, modal titles, and page titles.

However, if the feature is merely a create or edit variant of the main feature (like "Create campaign" or "Edit segment"), use sentence case for those.

Standalone mentions of generic content types - like ‘campaign’, 'segments', or 'guests' - don’t need to use title case by themselves unless preceded by an adjective for the purpose of referring to a marketed product feature.

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

## Grammar and style

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

**Use numerals instead of spelled words**

Numeric characters create fewer strokes and less cognitive load.

Note that support documentation will differ - that's okay; different context.

{% columns %}
{% column %}
✅ You have 3 checkins
{% endcolumn %}

{% column %}
🚫 You have three checkins
{% endcolumn %}
{% endcolumns %}

***

## Punctuation

[**Field Descriptions**](../entering-information/anatomy-of-form-field.md#description-text)**: No punctuation at the end pretty much all the time**

Descriptions should be written short enough that you don’t need a period at the end. Most descriptions should be a short instructive phrase that’s not a complete sentence anyway. Even if a description is technically a complete sentence grammatically speaking, it should be written short enough that it doesn’t look “wrong” to omit the period. <br>

In other words. if you find yourself writing a field description so long that it has you wondering whether it should have a period (or a line break, or how wrapping should work, etc.), that’s probably a good sign your description is too long anyway.

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

**Never use exclamatory punctuation**

That would be a little too casual.  

Recapping this and the previous related guidelines: Most of the time don’t ever use punctuation; okay to use a ‘?’ on confirmation prompts, and seldom use of a period on an Information Banner complete sentence is okay.

{% columns %}
{% column %}
✅ Looks like there was a problem
{% endcolumn %}

{% column %}
🚫 Oh no! Did you really want to do that?!
{% endcolumn %}
{% endcolumns %}

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-grammar-voice-tone.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

---
description: How to design the date picker experience
---

# Date fields

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](date-fields.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Anatomy

#### The unpopulated state

An unpopulated date field has a leading icon to signal the format/content type, and hint text to convey the format (for example, MM/DD/YYY)

<figure><img src="../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

#### While focused or typing

As the user types, preserve the hint text so the remaining syntax is still visible.

Don't make the user type in the / character, but accept it if they do, advancing to the next "segment" of the date.

Pop the date picker menu immediately upon focus (don't wait for the user to click any icon nor start typing). Show the current month and year unless the business context for your project says otherwise.

Show disabled or ineligible dates using a de-emphasized font color. If possible, use another de-emphasized font style for date numbers from the preceding and following calendar month (if visible on this month's view).

<figure><img src="../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

#### While populated

Highlight the selected date, jumping to that month of the calendar picker as the user types, or when the user clicks or taps to select a date in the picker.

<figure><img src="../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

#### Date ranges

Highlight in 3 distinct styles:

* the start date
* the end date
* the range between the start and end dates

<figure><img src="../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

***

### "Criss-crossed" start dates and end dates

For “illogical” entries on a Start and End date pair of fields (when the end date before the start date, or the start date after the end date), the user’s last entry “wins”:

* When selecting an end date less than the start date, then populate both fields with the end date.
* When selecting a start date greater than the end date, then populate both fields with the start date.
* This avoids inelegant error validation messages, prioritizes the user’s most recent action, and preserves a “safe” value.

### Error validation on an individual date field

#### Too early

When the entered date is too early, tell the user "Enter a date on or after 01/01/1900" (or whatever the earliest possible date allowed is).

<figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

#### Too late

When the entered date is too early, tell the user "Enter a date on or before 12/31/2099" (or whatever the latest possible date allowed is).

<figure><img src="../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

#### Date is invalid / not a real calendar date

When the entered date is not a valid calendar date at all, tell the user "Enter a valid date"

<figure><img src="../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% embed url="https://github.com/punchh/ux-pattern-guidelines/raw/main/skills/ux-date-fields.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Sources

#### [Working towards Usable Forms on the World Wide Web: Optimizing Date Entry Input Fields](https://www.hindawi.com/journals/ahci/2011/202701/)

Advanced in Human-Computer Interaction, 2011

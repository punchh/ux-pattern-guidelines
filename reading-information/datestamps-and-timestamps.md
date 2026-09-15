---
description: How to present date and time information
---

# Datestamps and timestamps

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](datestamps-and-timestamps.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

### Absolute

#### 12-hour time format 

> Wed, Feb 5, 2023 at 4:42 PM

#### 24-hour time format 

> Wed, Feb 5, 2023 at 16:42

### Relative

Relative timestamps (e.g., "2 hours ago") are most useful when the recency of content matters for user decisions — like in social feeds, notifications, or chat — where knowing _how long ago_ something happened is more meaningful than the exact time. Once content gets older (typically beyond a day or two), absolute timestamps become more useful since "8 months ago" is less precise and actionable than "September 12, 2025."

#### Past

<table><thead><tr><th>Situation / proximity</th><th width="255">Display</th><th width="177">Display when limited space</th></tr></thead><tbody><tr><td>Within the last few seconds</td><td>just now</td><td>now</td></tr><tr><td>Within the last minute</td><td>a minute ago</td><td>1 m</td></tr><tr><td>Within 59 minutes</td><td>x minutes ago</td><td>x m</td></tr><tr><td>60 minutes ago</td><td>1 hour ago</td><td>1 h</td></tr><tr><td>x hours ago</td><td>x hours ago</td><td>x h</td></tr><tr><td>1 day ago</td><td>yesterday</td><td>1 d</td></tr><tr><td>1 day ago (with time)</td><td>yesterday at 5:05 PM</td><td>1 d 17 h</td></tr><tr><td>2 days ago &#x3C; 7 days</td><td>x days ago</td><td>Aug 8</td></tr><tr><td>7 days ago</td><td>1 week ago</td><td>Aug 8</td></tr><tr><td>More than 7 days ago</td><td>August 8, 2023</td><td>Aug 8</td></tr></tbody></table>

#### Future

<table><thead><tr><th>Situation / proximity</th><th width="247">Display</th><th width="179">Display when limited space</th></tr></thead><tbody><tr><td>Within the next few seconds</td><td>shortly</td><td>now</td></tr><tr><td>In the next minute</td><td>In 1 minute</td><td>in 1 m</td></tr><tr><td>In the next 60 minutes</td><td>In x minutes</td><td>in x m</td></tr><tr><td>In 60 minutes</td><td>In 1 hour</td><td>in 1 h</td></tr><tr><td>In x hours</td><td>In x hours</td><td>in x h</td></tr><tr><td>In 1 day (by date, not hours)</td><td>tomorrow</td><td>Aug 8</td></tr><tr><td>In 2 to 7 days</td><td>In x days</td><td>in x d</td></tr><tr><td>In 7 days</td><td>In 1 week</td><td>in 1 w</td></tr><tr><td>In > 7 days</td><td>August 8, 2030</td><td>Aug 8</td></tr></tbody></table>

***

### Schedules and time ranges

* Spell out the word "to" to join a time range rather than use a hyphen
* Where possible, use "midnight" and "noon" in place of a numeric time to reduce ambiguity
* Drop trailing zeroes on times that fall on the whole hour

{% columns %}
{% column %}
✅ Noon to 5 PM

✅ Midnight to 9 AM

✅ 9:15 AM to 11 AM

✅ 2015 to 2019
{% endcolumn %}

{% column %}
🚫 12:00 AM to 9:00 AM

🚫 12 Midnight to 9 AM

🚫 9:15 AM to 11:00 AM

🚫 2015-2019
{% endcolumn %}
{% endcolumns %}

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="/broken/files/0h1ABK2G8dLjSCxSkgRZ" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

### Inspiration

But not taken verbatim

#### [Date and Time](https://atlassian.design/content/writing-guidelines/date-and-time-guideline)

Atlassian Design System Writing guidelines, 2023

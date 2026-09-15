---
description: How to design the file upload experience
---

# File upload

{% hint style="success" icon="sparkles" %}
[**Get the AI skill**](file-upload.md#ai-skill-file) for this UX pattern guideline in a markdown (.MD) file.
{% endhint %}

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>



### Anatomy

#### Drag and drop region

The entire drag and drop region should files dragged with a mouse cursor, and click or tap to invoke the user's native file picker.

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

**Icon**

For mixed file format support, use a generic file upload icon (sometimes indicated by a cloud with arrow).

**Instructional text**

Just like a field description, tell users what they need to do to populate this field. For example, "Drag and drop files or browse" works pretty well universally.

**File format requirements text**

List the supported file formats and maximum file size. For example: "PNG, JPG, or PDF only. 8 MB maximum file size"



#### Files region

Give the user feedback about the progress of each file upload.

Persist the upload region during and after upload.

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

**Icon**

Show an icon to reinforce the file type being uploaded. For example, images (PNG, SVG), documents (PDF, DOCX), and spreadsheets (XLSX, CSV) can use a generic catch all for range of specific file formats for each.

**Filename**

Give the users confidence they've selected the correct file by persisting the selected filename.

**Progress**

Through a combination of progress bars and percentages, let the user know how close they are to completion.

**Status**

Distinguish between files that are in progress, done, and in error state.

**Rate**

During an active upload, show the user the upload rate in KB/sec or MB/sec.

**Completed file size**

After upload is complete, replace the Rate value with completed file size. This reinforces for the user they've selected the correct file when they have a sense of its storage size.

**Remove button**

For any file upload in any state, allow the user to delete the file.

### Error handling

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption><p>A file upload field showing a connection related error</p></figcaption></figure>

Our [error validation guidelines](../form-experience/error-validation.md) call for all error validation to happen during form submission (rather than inline errors as the user types).

In a way, file upload errors are an exception: We should give the user feedback instantly if there's an issue with a file upload activity.

#### Network, connection, and environmental issues

While we strive to be as specific as possible when communicating the reason for an error, such a myriad of connectivity issues are possible that we instead use a single catch-all error message for these situations. "Something went wrong - try again" for example can suffice.

#### File violations

{% hint style="info" %}
In most desktop and mobile operating systems, the native OS file picker will prohibit the user from selecting unsupported file formats.
{% endhint %}

When the user selects a file that doesn't meet the requirements, the system should show the file in the list of upload items, but not attempt to upload as it would be a waste of time. Examples:

* File is too large
* Image is too small
* Image dimensions too large

***

### AI skill file

{% hint style="info" %}
**Don't want to use a markdown file at all?** No problem, just copy URL for this page and paste into your agent. Tell it to use the linked guideline (runtime lookup).&#x20;

**Don't hard code** the contents of this page to your own skill files though - this page gets updated often.
{% endhint %}

{% file src="../.gitbook/assets/ux-file-upload.md" %}

[Learn how to use](../resources/ai-skills.md) with your favorite AI tool, and get other UX pattern skills.

***

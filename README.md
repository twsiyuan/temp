# temp

This repository holds temporary reports that we share with the team. Each folder has the date of the upload in `DD-MM-YYYY` format. Delete a folder when the team does not need the report.

## 18-09-2026 — Storyteller clips, lambda comparison

The five HTML files show the same Storyteller clip feed with five different lambda values. Lambda controls how much the personalisation profile changes the order of the clips. A lambda of 0 gives the unpersonalised order. A lambda of 1.0 gives the full effect of the profile.

We captured all five feeds from one source:

| Item | Value |
| --- | --- |
| Environment | content-service stage |
| Device ID | `d6f2b49ef5f8f068` |
| Package name | `com.metro.minus1` |
| Profile | Sports |
| Feed size | 300 clips |
| Capture date | 17-09-2026 |

### Files

| File | Lambda | Content |
| --- | --- | --- |
| `storyteller_clips_lambda000.html` | 0 | The baseline order. No profile is applied. |
| `storyteller_clips_lambda025.html` | 0.25 | The order with a small effect from the profile. |
| `storyteller_clips_lambda050.html` | 0.5 | The order with a medium effect from the profile. |
| `storyteller_clips_lambda070.html` | 0.7 | The order with a large effect from the profile. |
| `storyteller_clips_lambda100.html` | 1.0 | The order with the full effect from the profile. |

### How to read a page

1. Open the page in a browser. Each clip shows its rank, its title, its publisher, and its category tags.
2. Read the badge after the publisher name. The badge gives the movement of the clip against the baseline file.
3. Look for the amber tags. An amber tag is a sports category. A blue tag is any other category.
4. Select a category or a publisher at the top of the page to filter the feed.

The baseline file has no movement badges, because it is the reference for the other four files.

### Limits

The pages load the images and the video files from `media.usestoryteller.com`. The pages also load the style sheet from a public CDN. A browser without internet access shows the text only.

# Task Tracker DB

Auto-captured tasks, recipes, projects, vacation ideas, and more — pulled from Gmail and structured for easy browsing, printing, and future web access.

## How it works

Emails sent to **ryry84@gmail.com** with **"task"** or **"track"** in the subject line are automatically processed twice daily (8am & 6pm). Each email is classified by type, enriched (e.g. Facebook reels → full recipe extraction), saved here, and emailed to recipients in a clean printable format.

## Structure

```
database.json          ← Master index of all entries
processed-ids.json     ← Gmail thread IDs already handled (prevents duplicates)
entries/               ← One JSON file per captured item
  YYYY-MM-DD-slug.json
```

## Entry Types

| Type | Email Subject Format |
|------|----------------------|
| Recipe | `Recipe - <Name>` |
| Project | `Project - <Name>` |
| Vacation | `Vacation - <Destination>` |
| Task | `Task - <Description>` |
| Idea | `Idea - <Title>` |
| Other | `Captured - <Title>` |

## Recipients

Processed entries are emailed to:
- ryry84@gmail.com
- heatherknippa@gmail.com

---
*Managed automatically by Claude / Cowork. Do not edit `processed-ids.json` manually.*

# File Schemas

These schemas define the expected structure of each memory stage.


---

## Organized Memory

File:
memory/organized/YYYY-MM-DD_organized.json

Structure:

{
  "date": "YYYY-MM-DD",
  "processed_at": "timestamp",
  "total_entries": 0,
  "source_files": [],
  "categories": [],
  "memories": [
    {
      "timestamp": "",
      "type": "",
      "context": "",
      "key_points": [],
      "decisions": [],
      "unresolved": [],
      "importance": "low | medium | high | critical",
      "tags": [],
      "quote_to_remember": ""
    }
  ],
  "lessons_learned": []
}


---

## Daily Pipeline Index

File:
memory/pipeline/daily/YYYY-MM-DD/index.json

Structure:

{
  "date": "",
  "type": "",
  "timestamp": "",
  "summary": "",
  "activities": [],
  "observations": [],
  "tags": []
}


---

## Tag Index

File:
memory/tags/all_tags.json

Structure:

{
  "tag_name": {
    "count": 0,
    "dates": [],
    "first_seen": "",
    "last_seen": "",
    "importance_distribution": {},
    "type_distribution": {},
    "sample_entries": []
  }
}


---

## Journal

File:
memory/journal/YYYY-MM-DD.md

Format:

# YYYY-MM-DD

## Evening Reflection

Freeform narrative including:
- events
- patterns
- unresolved carry-forward
- lessons learned


---

## Heartbeat State

File:
memory/heartbeat-state.json

Structure:

{
  "lastCheck": "",
  "lastAction": "",
  "activityCount": 0
}

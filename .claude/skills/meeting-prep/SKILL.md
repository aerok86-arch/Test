---
name: meeting-prep
description: Generate a pre-meeting briefing by pulling together calendar details, email history with attendees, and optional web research. Use when the user says "brief me before my call", "prep me for my meeting", or when a meeting is starting within 20-30 minutes.
---

# Meeting Prep

Generate a concise pre-meeting briefing by synthesizing calendar data, email history, and web research. Designed for a 60-second scan.

---

## Trigger Conditions

- User explicitly requests prep ("brief me before my call", "meeting prep for X")
- A meeting is starting within 20–30 minutes (proactive trigger)

---

## Workflow

### Step 1: Locate Target Meeting

Check Google Calendar:
- If user names the meeting, search by name
- Otherwise, find the next upcoming event from the current time

Capture: title, time, location/video link, description, attendee list.

### Step 2: Email Context

Search Gmail for threads with attendees:
- Start with 2 weeks back; expand to 3 months if needed
- For large meetings (all-hands, company-wide), skip extensive email search unless user requests it
- For internal standups, skip email search

Extract:
- Open action items
- Key discussion topics
- Thread summaries
- Relationship tone (any tension, ongoing projects, recent commitments)

For large attendee lists, focus on organizers and VIPs.

### Step 3: Agenda Extraction

Pull from the calendar event description:
- Formal agenda items
- Pre-read materials
- Goals and objectives
- Any notes or context the organizer included

### Step 4: Web Context (External Meetings Only)

For external attendees or companies, run a brief web search:
- Recent funding or acquisitions
- Product launches or major announcements
- Leadership changes
- Relevant news

Keep to 2–3 bullets maximum. Skip for internal meetings.

### Step 5: Assemble Briefing

---

## Output Format

```
📅 [Meeting Title]
[Date] · [Time] · [Duration] · [Location/Link]

**Attendees:** [List]

---

**Agenda**
[Bullet list of agenda items, or "None provided" if missing]

---

**Email Context**
[Key threads summary — what's been discussed, open items, any relevant history]

**Open Action Items**
- [Item 1]
- [Item 2]

---

**External Context** *(if applicable)*
- [News item 1]
- [News item 2]

---

**Suggested Talking Points**
- [Point 1]
- [Point 2]
- [Point 3]
```

---

## Key Principles

- Prioritize conciseness — this is a 60-second scan, not a report
- Flag missing information transparently ("No agenda provided", "No recent email threads found")
- Never pad gaps — missing info is missing info
- Keep web context tight and directly relevant to the meeting

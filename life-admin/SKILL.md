---
name: life-admin
description: "Patrick's personal calendar-logistics automation. Creates the blocks and reminders around events and trips, and checks conditions before mountain travel. Three workflows: (1) event blocks — commute, doors/gate, all-day visibility, and gap reminders around concerts, festivals, movies, sporting events, and appointments; (2) flight blocks — commute/transit, security, and boarding blocks for upcoming flights; (3) road-trip check — Colorado road conditions before mountain drives, ski days, and bike rides. Use whenever the user adds an event or flight to the calendar, asks for commute/logistics/travel/airport blocks, mentions an upcoming trip to the mountains, or when a calendar review spots an event missing its blocks or a mountain trip that warrants a road-conditions check — even if they don't name the specific workflow."
metadata:
  version: "1.0.0"
  lastVerified: "2026-06-30"
---
# Life Admin

Personal calendar-logistics automation for Patrick. This skill routes to three workflows that all add blocks/reminders to Google Calendar (or check conditions ahead of a trip) following one shared set of conventions. The point of keeping them together is that they share calendars, the work-invite rule, and title conventions — define those once here, and each workflow stays focused on its own specifics.

## Pick the workflow

| Situation | Workflow | Reference |
|-----------|----------|-----------|
| An event with a time and place — concert, festival, movie, sporting event, appointment — needs commute / doors / reminder blocks | Event blocks | `references/event-blocks.md` |
| An upcoming flight needs commute, security, and boarding blocks | Flight blocks | `references/flight-blocks.md` |
| A mountain drive, ski day, or bike ride — check road conditions first | Road trip check | `references/road-trip-check.md` |

Read the matching reference and follow it. A single request can hit more than one — e.g. a flight to a ski destination is both flight blocks and a road-trip check — so run each workflow that applies.

## Shared conventions

These hold for every workflow; the references assume them rather than repeat them.

### Calendar operations
Use the Google Calendar MCP integration (the `mcp__claude_ai_Google_Calendar__*` tools, e.g. `list_events`, `create_event`, `update_event`) for all calendar reads and writes.

### Calendars
- Primary / personal: `hey@psb.email`
- Family: `c_367ee0742abf30e27c7f3aa3ea2f4e51566acb6cf0f6b69e66fed4e62e77a820@group.calendar.google.com`

**Blocks always go on the same calendar as the main event they support.** Determine the main event's calendar first (each workflow says how), then create all of its blocks — commute, doors, security, boarding, reminders — on that same calendar. If the event lives on more than one calendar, mirror its blocks onto each. Never split an event and its blocks across different calendars.

### Work invite
For any block on a weekday (Mon–Fri) that starts between 8 AM and 4 PM MT, also invite `pburtchaell@meta.com`. This keeps work aware of time that's already spoken for.

### Event titles
Keep titles simple and scannable — no parentheses, arrows, or extra punctuation. Put the detail (flight numbers, routes, addresses) in the event description instead. Good: "Security", "Boarding", "A Line to DEN". Bad: "Boarding (UA 1305 to Atlanta)".

### Home base
Patrick lives in Whittier (2448 N Lafayette St, Denver). Commute and drive-time estimates start from there unless stated otherwise.

### Don't duplicate; keep in sync
Check for existing blocks before creating new ones. If a root event (a show, a flight) moves, update its associated blocks to match rather than leaving stale ones behind.

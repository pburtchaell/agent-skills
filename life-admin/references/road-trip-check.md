# Road Trip Check

Check Colorado road conditions before any trip that involves mountain or highway travel. Flag closures, chain laws, and weather that would affect the route. Stay quiet if everything is clear.

This workflow reads conditions and messages Patrick — it doesn't create calendar blocks, so the calendar conventions in the parent `SKILL.md` mostly don't apply here.

## Triggers
- Mountain drives, ski trips, bike rides to mountain destinations
- Whole-day calendar events for cycling or skiing (may not have a set departure time)
- Any Colorado road trip where conditions could matter
- Check the day before and the day of the event

## Workflow
1. Identify the route. Determine the destination from the calendar event. If the event is a whole-day bike or ski event, infer the likely route from the destination.
2. Check cotrip.org for road conditions:
   - URL: https://maps.cotrip.org/list/events
   - Look for closures, chain laws, weather alerts, and construction on the relevant route
3. Evaluate relevance. Only flag conditions that are actionable:
   - Full or partial road closures on the planned route
   - Chain law in effect (and Patrick may not have chains)
   - Severe weather warnings for the route corridor
   - Major construction causing significant delays
4. Report or stay quiet. If nothing actionable, don't surface anything. If there's something worth knowing, message Patrick with the specific issue and any alternatives.

## Common Routes
- I-70 West: skiing, mountain biking (e.g. Rollins Pass, Winter Park area)
- US-285 South: access to Fairplay, Buena Vista, southern mountains
- CO-93 / US-6: Red Rocks, Golden area
- I-25 corridors: Front Range travel
- Peak to Peak Highway (CO-72/CO-7): mountain cycling

## Operating Rules
- Only surface actionable information. "Roads are clear" is not worth a notification.
- For whole-day events, check conditions in the morning since departure time is flexible.
- If cotrip.org is down or unreachable, note it briefly and move on.
- Don't repeat conditions Patrick has already been told about for the same trip.

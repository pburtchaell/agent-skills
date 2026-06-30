# Flight Blocks

Create the standard pre-flight calendar blocks (commute/transit, security, boarding) for a given flight.

Shared conventions (calendars, work invite, simple titles, home base, no duplicates) live in the parent `SKILL.md`.

## Workflow
1. Identify the flight(s): airline, flight number, departure airport, departure time, and whether it's solo or with Jennie. Check the calendar if needed.
2. Determine transit to the airport (see Commute Rules).
3. Create blocks in this order, working backwards from departure:
   - Commute/transit block
   - Security block
   - Boarding block

## Commute Rules

### Denver (DEN) departures
- Default: leaving from home in Whittier
- Schedule commute blocks 1 week before the flight
- If taking RTD A Line: Uber to 38th & Blake Station (15 min), then A Line to DEN (~33 min). A Line runs every 15 min from 4:15 AM to 6:30 PM, every 30 min outside those hours. Departures from Union Station at :00, :15, :30, :45 past the hour; 38th & Blake is ~4 min later. Create two blocks: "Call Uber to 38th & Blake" and "A Line to DEN"
- If driving: 45 min commute block from Whittier to DEN
- Ask Patrick which mode if not specified

### Non-Denver departures
- Message Patrick 2 days before the flight and ask where they're heading from, then create blocks
- For small regional airports (e.g. CHA): 1.5 hours before departure is fine for security
- For major airports: 2 hours before departure

### MSY (New Orleans) departures
- In addition to standard blocks, create a lounge waitlist calendar reminder at the same time as the security block
- Waitlist URL: https://waitwhile.com/locations/the-club-msy/welcome?registration=waitlist
- Patrick joins the waitlist remotely before arriving at the airport

## Block Timing

### Security
- Domestic: start ~2 hours before departure (adjust for airport size)
- Duration: 30 min block
- Small airports (CHA, etc.): 1.5 hours before is fine

### Boarding
- Start: ~30 min before departure
- End: at departure time

### Connections
- No separate security/boarding blocks for connections where the passenger stays airside
- Only note tight connections (<60 min) in a description if relevant

## Calendar Routing
The flight event's calendar(s) determine where its blocks go — put commute, security, and boarding on the same calendar(s) as the flight (see the block-placement rule in the parent `SKILL.md`).
- Solo flights: personal (`hey@psb.email`) and Family — so create the blocks on both.
- Flights with Jennie: Family calendar only — blocks on Family only.
- Title examples — Good: "Security", "Boarding", "A Line to DEN", "Call Uber to 38th & Blake". Bad: "Boarding (UA 1305 to Atlanta)", "A Line to DEN (38th & Blake → Airport)".

## Notes
- Verify flight times from the calendar before creating blocks. Don't assume times from memory if they could have changed.
- For return flights arriving at DEN, add an A Line block from DEN back to 38th & Blake if the user took transit outbound.

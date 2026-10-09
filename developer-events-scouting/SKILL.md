---
name: Developer events scouting
description: >-
  Use this when looking for meetups, hackathons, conferences or university
  events in a set of cities where a project could speak, sponsor or recruit
  developers, or when preparing a hands-on workshop at one.
---
# Developer events scouting

1. Take the target cities, the date window, and the audience (for example developers building products or startups, students, researchers).
2. Search event sources for each city: Meetup, Luma, Eventbrite, university and student organisation calendars, startup hubs and innovation weeks, conference sites, and local tech community pages.
3. For each event, record the name, date, city, venue, organiser, link, expected audience, and any call for speakers, sponsorship or demo deadline. Only record details you actually found on the page.
4. Score how well it fits (high, medium or low) by audience match, size, cost, and whether there's a chance to speak or run a demo.
5. Return a table sorted by date, with upcoming deadlines first, and a one-line suggested action for each high-fit event (for example "pitch a 20-min talk by 15 Oct"). Don't contact any organiser without approval.

## Preparing a hands-on workshop or demo

6. Get real capacity or sign-up numbers from the event page or the organiser. Never estimate headcount; say "unknown" until you have a source. Size handouts (test wallets, API keys, credits) as that number plus about 20% spare.
7. Ask the venue whether its Wi-Fi only allows outbound traffic on port 443. Check that every endpoint the demo uses (RPC, websocket, faucet, package registry) works on 443, and name a fallback: a phone hotspot or a local or offline network.
8. Don't let the live demo depend on a public faucet or rate-limited service. A whole room shares one IP address and trips per-IP limits. Hand out pre-funded or pre-provisioned credentials instead, and keep each event's set separate.
9. Before promoting the workshop, check that the onboarding path it relies on has passed a fresh end-to-end run. If it hasn't, hold the "start building" promotion.

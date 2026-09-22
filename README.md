# game-state-roster

Public roster data for [game-state](https://github.com/joegr/game-state).

This repo holds exactly one thing: `roster.md`, the confirmed team roster for
the tournament — a team's four-character code and a hash of its captain's
token. It never contains a raw token, a name, or anything else that could
identify a captain.

It's split out from the main app repo so the roster can be public (auditable
via plain git history — you can see exactly who joined when) independently of
whatever visibility the main code repo has.

`roster.md` is generated and updated from the organizer console in
[game-state](https://github.com/joegr/game-state) (`admin.html` → Registration
→ Publish roster) — download or copy it there, then commit it here and push.
Don't hand-edit `tokenHash` values; they have to match what a captain's token
hashes to, or that team's score reports will be rejected as unauthenticated.

# SHE Home Organizer

A household task organizer based on the card-file system from *Sidetracked Home Executives: From Pigpen to Paradise* by Pam Young & Peggy Jones.

- **Today view** — one "Up Next" focus card; finishing or refiling it auto-promotes the next card from On Deck
- **Card box** — the digital 3×5 file: Daily Routine, Basic Week, Monthly, Zones, Menus, To Do
- **Routines** — editable morning/evening checklists that reset daily
- **Basic Week** — an editable Mon–Sun plan, SHE style
- **Progress** — kind streaks and a weekly done-summary

The page is a single static file (`index.html`) hosted here on GitHub Pages. All data lives in Firebase (Cloud Firestore, anonymous auth), so it syncs across devices and works offline. See `SETUP.md` for the Firebase setup steps and `firestore.rules` for the security rules.

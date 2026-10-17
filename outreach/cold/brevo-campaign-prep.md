# Brevo Campaign Prep — Cold Email 1

Date: 2026-10-17
Status: PREPARED — NOT SENT (awaiting explicit approval)

## Contact extraction

| Metric | Count |
|--------|-------|
| Total rows in leads/cold.md | 300 |
| Valid emails (not FIND) | 65 |
| FIND / missing | 235 |
| Valid by niche — agency | 43 |
| Valid by niche — affiliate | 21 |
| Valid by niche — ecommerce | 1 |

Import file: `~/beastbrowser/outreach/cold/brevo-import-contacts.csv`
Columns: EMAIL, FIRSTNAME, COMPANY, NICHE, SOURCE (65 rows + header)

Note: the Name column often holds a company or brand name rather than a
person's first name. FIRSTNAME personalization will be imperfect on those rows.

## Brevo list

Proposed list name: `Cold Prospects — Oct 2026`
List ID: NOT CREATED (no Brevo API key available to this agent).

Manual creation steps (Brevo dashboard):
1. Contacts → Lists → Create a list → name: `Cold Prospects — Oct 2026`
2. Contacts → Import contacts → upload `brevo-import-contacts.csv`
3. Map columns: EMAIL → Email, FIRSTNAME → First name,
   COMPANY → custom attribute COMPANY, NICHE → custom attribute NICHE
4. Confirm the list ID and record it here before sending.

Existing lists for reference: Newsletter (ID 3), Free users, Referrers.

## Campaign — Email 1 (day 0)

Sender: BeastBrowser <support@beastbrowser.com>
Subject: 50 profiles on AdsPower is ~$60/mo. Ours is $30.

Body (Brevo placeholders):

---
Hi {{contact.FIRSTNAME}},

Quick math if you run 50 browser profiles:
- AdsPower: ~$60/mo
- Dolphin Anty: ~$60/mo
- BeastBrowser: $30/mo, unlimited

Every profile past 20 is a tax you keep paying.

BeastBrowser gives each account its own isolated browser — separate cookies,
storage, 50+ fingerprint signals. Profiles live on your machine. RPA and recorder included.

Free plan: 5 profiles a day, no card. Two minutes to test.

https://beastbrowser.com/?utm_source=brevo&utm_medium=email&utm_campaign=cold-e1

Worth a look?
BeastBrowser team
---

Unsubscribe: Brevo inserts the mandatory unsubscribe link automatically on send.
Do not remove it.

## Ready-to-send checklist

- [x] 65 valid contacts extracted to CSV
- [x] Email 1 copy finalized with placeholders
- [ ] Brevo list created and contacts imported (manual — needs dashboard access)
- [ ] Compliance review cleared (see BLOCKERS)
- [ ] Explicit send approval from owner
- [ ] Test email sent to support@beastbrowser.com and verified

## BLOCKERS

- Compliance risk: Brevo previously suspended marketing emails on this account; the compliance response on file states opt-in-only collection (no scraped lists). Sending cold email to 65 scraped contacts risks re-suspension. Owner must decide whether to proceed.
- No Brevo API key available to this agent; list creation and import must be done manually in the Brevo dashboard.
- Only 65 of 300 cold rows have real emails (ecommerce: 1 of 100); the list is thin for a cold campaign.

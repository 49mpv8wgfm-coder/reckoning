# RECKONING (demo) — by Civic Ledger

Every claim has a receipt.

A prototype civic-audit interface: a fixed roster of public officials, every claim backed
by a hash-checked source artifact. Score claims, not people. Model the office, not the
person. The ledger never deletes.

## Demo scope
- No search. Fixed roster: John McCain, Barack Obama, Bernie Sanders.
- One page: The Board (ticker cards) -> Profiles -> expandable receipts on every claim.
- Status ladder: VERIFIED / CONTESTED / UNVERIFIED / RETRACTED.

## Data provenance (all public / authoritative)
- Identity + photos: github.com/unitedstates/congress-legislators & unitedstates/images
  (public domain; photos addressed by bioguide ID)
- Office records: Biographical Directory of the U.S. Congress
- Elections: FEC candidate records; National Archives Electoral College
- Awards: NobelPrize.org

## Integrity rule
No demo ships with fabricated numbers. Any claim not yet ingested from its named API is
visibly UNVERIFIED. The truth machine does not ship fiction.

## Stack (v0)
Single self-contained HTML file (index.html). No build step, no dependencies, no JS
required. Receipt hashes are SHA-256 computed at build time over the canonical source
identifier; production will hash fetched artifact bytes.

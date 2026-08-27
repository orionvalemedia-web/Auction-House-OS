# Devadex Auction House OS

The product in this package.

Every entry below is taken from the package's own documentation. Nothing here is a plan or a
roadmap item; all of it is built.

---

## Devadex Auction House OS

38 tests

An offline management system for independent auction houses, covering the full path a lot takes: consignment intake, lotting and catalogue build, bidding, hammer-to-invoice settlement, and consignor payouts with commission splits.

## What it does

- **Consignment intake.** Records a consignor (name, email, default commission percentage).
- **Lotting and catalogue build.** Groups one or more items into a numbered lot, optionally bundling multiple items under one lot.
- **Absentee bidding** — accepts a bidder's maximum bid in advance; the system runs proxy bidding automatically, raising the standing price only as needed to stay one increment ahead of the next competing bid,...
- **Phone bidding** — records an amount a staff member calls in on a phone bidder's behalf during a live sale.
- **Live bidding** — records amounts called out on the floor as the auctioneer runs the sale.
- **Bid increments** — follow a fixed ascending increment table (larger increments at higher price bands), implemented in lib/increments.js.
- **Reserve interaction** — if a lot has a reserve, an absentee bidder's ceiling that covers the reserve will raise the standing price to meet (not exceed) the reserve, functioning as a silent seller-side bid.
- **Hammer-to-invoice settlement.** Closes a lot with a hammer action: compares the standing price to the reserve and marks the lot sold or passed.

### Who it is for

An independent auction house running on paper or spreadsheets, or a buyer wanting an owned tool instead of a subscription.

---

Full detail, including file-level inventory and provenance, is in the data room, available under a
signed non-disclosure agreement. See [ACQUISITION.md](ACQUISITION.md).

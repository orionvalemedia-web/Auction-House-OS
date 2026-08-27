# Devadex Auction House OS

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

## Who it is for

An independent auction house running on paper or spreadsheets, or a buyer wanting an owned tool instead of a subscription.

---

Available for acquisition as an outright transfer of ownership.

This repository is **documentation only**. It describes what the product is, what has been
measured, and what is known to be incomplete. It contains no source code. See
[LICENSING.md](LICENSING.md).

---

## What is included

One finished product.

| Product | Scale |
|---|---|
| Devadex Auction House OS | 38 tests |

Feature-by-feature detail is in [PRODUCTS.md](PRODUCTS.md).

## Measured

| Measure | Value |
|---|---|
| Tests passing | 38 |
| Tests failing | 0 |
| Tests skipped | 0 |
| Files delivered | 21 |
| Authored lines | 1,788 |

Every figure came from running the software while the data room was prepared, and a buyer can
reproduce each one from the delivered files. Method and known gaps are in
[VERIFICATION.md](VERIFICATION.md).

## How it is sold

Outright transfer of ownership, sold as is. No ongoing maintenance or support obligation, and no
licence-back, so the seller keeps nothing that depends on it.

A full data room is available under a signed non-disclosure agreement: product inventory,
provenance, third-party notices, the complete verification record, and an open-items document
listing every known gap. See [ACQUISITION.md](ACQUISITION.md).

## Documents

| Document | What is in it |
|---|---|
| [PRODUCTS.md](PRODUCTS.md) | Every product, described |
| [VERIFICATION.md](VERIFICATION.md) | What was measured, how, and what is not proven |
| [LICENSING.md](LICENSING.md) | Proprietary status, and what this repository is |
| [ACQUISITION.md](ACQUISITION.md) | How to open a conversation |
| [CONTRIBUTING.md](CONTRIBUTING.md) | Why code contributions are not taken |

---

Jesse Duncan, doing business as Devadex Labs. Proprietary; all rights reserved.

# InsiderWire — SEC Filing Monitor for Insider and Institutional Signals

A monitoring product designed to track high-signal SEC filings such as Form 4, SC 13D, SC 13G, and 13F-HR, and turn them into more usable alerts for teams following insider activity and institutional holdings.

## The problem

SEC filings contain valuable signals, but the raw information is noisy, fragmented, and hard to monitor consistently at scale.

For teams following insider trades and ownership changes, the challenges are usually the same:

- important filings are buried inside large volumes of disclosure data
- monitoring multiple companies and filing types is operationally repetitive
- raw filing data is difficult to parse quickly
- teams need signal, not just documents

The opportunity here was to design a system that moves from passive monitoring to more actionable intelligence.

## The solution

InsiderWire is a real-time SEC monitoring system focused on high-value form types tied to insider trading and institutional ownership.

It was designed to:

- monitor 50+ real estate and financial companies
- detect new filings automatically
- parse and summarize key filing details
- send Slack alerts with richer context
- provide visibility into monitoring history and system performance

Instead of simply notifying users that a filing exists, the system aims to make the filing easier to understand and faster to act on.

## Core product idea

The core thesis behind InsiderWire is simple:

**Users do not want more filings. They want faster understanding of what changed and why it matters.**

That led to a product approach centered on three layers:

- discovery of new filings
- processing and normalization of filing details
- delivery of useful summaries and alerts

## Key features

- real-time SEC filing monitoring
- form-type filtering
- company-level monitoring controls
- Slack notifications
- monitoring run history
- parsing and summarization for Form 4 filings
- modern UI for reviewing filings and operational status

## Product architecture

The system uses a multi-stage workflow:

### Stage 1: Discovery
Checks active companies for new filings and inserts new records into the database.

### Stage 2: Processing
Fetches filing documents, parses details, generates summaries, and creates alert content.

### Stage 3: Retry
Retries pending or failed alerts to improve delivery reliability.

This structure makes the product more resilient and supports operational trust, which is critical in monitoring tools.

## Why Form 4 mattered most

Form 4 filings are especially useful because they often provide direct signal on insider buying and selling behavior.

Designing parsing and summarization around Form 4 created more immediate user value by turning a dense filing into a quick takeaway, such as:

- who filed
- their relationship to the company
- whether shares were bought or sold
- how many shares were involved
- the approximate transaction price
- ownership context after the transaction

That made the alerting experience much more useful than a generic filing notification.


## Impact

InsiderWire shows how monitoring products become more valuable when they move beyond detection and into interpretation.

The product helps reduce the time between disclosure and understanding by:

- surfacing key filings faster
- normalizing raw filing details into more usable outputs
- reducing manual parsing effort
- creating a cleaner alert-to-action workflow

## Screenshots

<img width="1394" height="959" alt="image" src="https://github.com/user-attachments/assets/20843b07-1a0b-4af3-bb2c-702757713314" />
<img width="1394" height="575" alt="image" src="https://github.com/user-attachments/assets/9d1af239-754e-45e3-9315-8c3c99dfdbee" />



## Notes

This repository is a public showcase of the product thinking, workflow, and system design behind InsiderWire. The production code remains private.

# How Much Does a 0.2-Star Rating Drop Cost You on Airbnb? (Revenue Math)

Source: https://rapideyeinspections.com/blog/airbnb-star-rating-impact-on-bookings/

_A 0.2-star rating drop correlates with 5-10% fewer listing page views per Opago. 4.9+ listings see 18.2% higher revenue than lower-rated ones per AirDNA. The real math behind Airbnb rating elasticity._

# How Much Does a 0.2-Star Rating Drop Cost You on Airbnb?

**A 0.2-star rating drop correlates with a 5 to 10 percent reduction in listing page views.** Fewer page views compress booking conversion, which compresses occupancy, which compresses revenue. Over 90 days, a single bad review from one ops failure cascades far beyond the refund on that stay. This page breaks down the cascade, the non-linear threshold effects around 4.7 and 4.8, and the scenario math for a 50-unit portfolio.

## The rating-to-revenue cascade

Rating is not a standalone metric. Every tenth of a star moves a downstream number. Here's the chain, with each stage attributed to a primary source.

Stage 1 — trigger

−0.2★

A 0.2-star rating drop over 90 days, triggered by a run of ops failures. Often one or two bad reviews pulling a rolling average down.

Stage 2 — visibility

−5–10%

Listing page views drop 5 to 10 percent per Opago's portfolio data. Fewer guests see the listing in search results.

Stage 3 — conversion

Compressed

Fewer page views paired with the visible rating drop compresses look-to-book conversion. Guests skip anything under 4.7–4.8.

Stage 4 — revenue

Compounds

4.9+ listings see 18.2% higher revenue than lower-rated peers per AirDNA 2023. The gap is real and compounds monthly.

## Why 4.8 and 4.9 are non-linear breakpoints

Rating impact is not a smooth curve. Specific thresholds trigger platform-level consequences that reshape search visibility and guest behavior. A 0.1-star move from 4.7 to 4.8 is worth more than a 0.1 move from 4.4 to 4.5, because 4.8 is the Superhost floor.

## The scenario: 50-unit portfolio, 0.2-star drop over 90 days

Most portfolios feel a rating slide as abstract. The math below makes it concrete. A single ops failure often produces the one or two bad reviews needed to move the rolling 90-day average by 0.2 stars on a mid-volume listing. Here is what that costs across a 50-unit portfolio over a year at representative numbers.

### Worked example

Assumptions: 50 listings, average ADR $220, baseline occupancy 72%, 365 days. Delta uses conservative 5% page-view reduction and the midpoint of AirDNA's 9.7% occupancy gap and 7.7% ADR gap.

Illustrative calculation using AirDNA and Opago signals. Real portfolios vary by market and mix.

## How to defend the rating operationally

Rating defense is an ops discipline, not a marketing one. Reviews reflect operational execution with a lag. The practical levers all show up in the hub's 12 KPIs, but four matter most for rating specifically.

- Track 90-day rating trend per listing, not lifetime
Lifetime average is a lagging vanity metric. Rolling 90-day trend is actionable. Set a per-listing alert at −0.1 over 90 days; investigate every triggered listing within the week.

### Track 90-day rating trend per listing, not lifetime

Lifetime average is a lagging vanity metric. Rolling 90-day trend is actionable. Set a per-listing alert at −0.1 over 90 days; investigate every triggered listing within the week.

- Tie every negative review to a root-cause category
Tag every critical review to one of the [5 Ops Failure Rate categories](https://rapideyeinspections.com/blog/what-is-ops-failure-rate-short-term-rentals/): late clean, missed supplies, missed maintenance, damage missed, or guest issue in first 24 hours. Pattern emerges in 30 days.

### Tie every negative review to a root-cause category

Tag every critical review to one of the [5 Ops Failure Rate categories](https://rapideyeinspections.com/blog/what-is-ops-failure-rate-short-term-rentals/): late clean, missed supplies, missed maintenance, damage missed, or guest issue in first 24 hours. Pattern emerges in 30 days.

- Hold Inspection Pass Rate above 90 percent
Most rating damage compounds from cleanliness and condition issues. [Inspection Pass Rate](https://rapideyeinspections.com/blog/what-is-good-inspection-pass-rate-vacation-rentals/) is the upstream lever. Below 90 percent, rating drift is mathematically coming; fix it before it arrives.

### Hold Inspection Pass Rate above 90 percent

Most rating damage compounds from cleanliness and condition issues. [Inspection Pass Rate](https://rapideyeinspections.com/blog/what-is-good-inspection-pass-rate-vacation-rentals/) is the upstream lever. Below 90 percent, rating drift is mathematically coming; fix it before it arrives.

- Respond to every 3- or 4-star review publicly
Public response shows future guests the operator is on it. Specific, non-defensive, short. Public responses do not change the star rating but do change the conversion impact of the visible low-star.

### Respond to every 3- or 4-star review publicly

Public response shows future guests the operator is on it. Specific, non-defensive, short. Public responses do not change the star rating but do change the conversion impact of the visible low-star.

## Frequently asked questions

### How fast does a rating recover after a drop?

Rolling 90-day averages recover as high-star reviews age in and low-star reviews age out. Lifetime averages move slowly and essentially never fully recover for high-volume listings, which is why 90-day trend is the useful metric. A listing that holds 4.9 operationally for 90 straight days typically recovers most of the visible rating drop even if the lifetime number stays slightly lower.

### Is the 22% Superhost booking uplift verified?

The "Superhost equals 22 percent more bookings" figure is frequently cited in Airbnb-adjacent content (including Hostaway's 2026 rating analysis citing Complete Hospitality Management as the source). It is not a figure Airbnb has published directly as a controlled experiment result. Use it as directional rather than precise. The first-party data we rely on in this page is the AirDNA 2023 comparison across rating tiers, which is measured rather than estimated.

### Does one bad review permanently damage a high-rated listing?

One 1-star review on a listing with 80 prior 5-star reviews reduces the visible rating from 5.00 to roughly 4.95. Immaterial on the surface. The damage isn't the math; it's the visible 1-star sitting at the top of recent reviews. Future guests read the most recent reviews first. The fix is a few new 5-star reviews after the bad one, not the long-run average.

### Should rating trend be tracked for Vrbo and Booking.com too?

Yes, but with different thresholds. Vrbo Premier Host 2026 requires 4.6+ (lower than Airbnb's 4.8 Superhost floor) but demands 99% acceptance and 0% host-initiated cancellation — see our [Superhost response time playbook](https://rapideyeinspections.com/blog/airbnb-superhost-response-time-requirements/) for the cross-platform comparison. Booking.com scores on a 10-point scale with 8.5+ as the competitive floor. Track by platform; don't mix.

## Related ops references

Hub page

Vacation rental operational KPIs: the ops scorecard for 100+ unit portfolios

Upstream

What is Ops Failure Rate for short-term rentals?

Cross-platform

Airbnb Superhost Response Time Requirements (2026)

## Sources

- [Opago, "5 KPIs That Short Term Rental CEOs Track" (April 2026) — 0.2-star drop correlates with 5-10% page-view reduction across 7,000+ London portfolio](https://www.opago.co/blog/5-kpis-that-short-term-rental-ceos-track---and-the-1-they-almost-always-miss)
https://www.opago.co/blog/5-kpis-that-short-term-rental-ceos-track---and-the-1-they-almost-always-miss

- [AirDNA, "Host's Guide to Airbnb Ratings" (2023 data) — 4.9+ listings see 7.7% higher ADR, 9.7% higher occupancy, 18.2% higher revenue](https://www.airdna.co/blog/hosts-guide-to-airbnb-ratings)
https://www.airdna.co/blog/hosts-guide-to-airbnb-ratings

- [Airbnb Help Center — How to Qualify for Superhost Status (4.8+ rating requirement, quarterly evaluation)](https://www.airbnb.com/help/article/829)
https://www.airbnb.com/help/article/829

- [Hostaway, "How Airbnb Star Ratings Can Make or Break Your Vacation Rental Business" — Guest Favorites badge data, distribution benchmarks (96% 4+, 86% 4.5+)](https://www.hostaway.com/blog/airbnb-star-ratings/)
https://www.hostaway.com/blog/airbnb-star-ratings/

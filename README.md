# Scrapingdog Pricing: What $40, $90 and $200 Actually Buy, How Fast Credits Run Out, and When a Second API Is the Cheaper Call (Full Plan Table)

Scrapingdog charges **$40 a month for 200,000 credits (Lite)**, **$90 for 1,000,000 credits (Standard)** and $200 for 3,000,000 (Pro). There is a free tier of 100 credits, and 27 paid plans run all the way to $30,000 a month. Every request pulls from the same credit balance, and the multiplier attached to that request sets how far the balance stretches: 1 credit for a plain page, 5 with JavaScript rendering, 10 for a premium proxy or a country-targeted request, 25 for rendering through a premium proxy.

That spread decides your bill more than the plan name does. The same $90 Standard plan buys **1,000,000 plain pages, 200,000 rendered pages or 40,000 protected ones**. Identical money, 25× difference in volume.

Below is the full plan ladder, the credit table that converts a plan into a real invoice, three worked volumes, and the billing rules that never make it onto the pricing grid. It also covers the point where a low per-page rate stops being the whole cost, because parsing, scheduling and storage stay on your side of the fence.

> **Short version:** Lite at $40 covers prototypes and small scheduled jobs; anything that renders JavaScript on a schedule should start at Standard at $90. If what you actually need is a scraping API that hands back parsed records and runs the schedule for you, ScraperAPI starts at $49 for 100,000 credits and $149 for 1,000,000, with geotargeting and auto-parsing included at no extra credit cost. 👉 [See ScraperAPI's current plans and credit costs](https://www.scraperapi.com/pricing?fp_ref=coupons)

## Every Scrapingdog plan, from 100 free credits to 1.1 billion

All 27 paid plans unlock the same API set. Moving up the ladder buys two things only: monthly credits and concurrent requests. Support improves at the top (dedicated support from Enterprise Plus, a named account manager from Ultra Starter), but no feature is gated behind a bigger plan.

| Plan | Monthly price | Credits per month | Concurrent requests |
| --- | --- | --- | --- |
| Free | $0 | 100 | 1 |
| Lite | $40 | 200,000 | 5 |
| Standard | $90 | 1,000,000 | 50 |
| Pro | $200 | 3,000,000 | 100 |
| Premium | $350 | 6,000,000 | 150 |
| Business | $500 | 9,000,000 | 200 |
| Business Plus | $1,000 | 19,000,000 | 250 |

The remaining 21 tiers follow the same pattern with a slowly falling unit price:

| Plan | Monthly price | Credits per month | Concurrent requests |
| --- | --- | --- | --- |
| Business Pro | $1,500 | 29,000,000 | 300 |
| Corporate | $2,000 | 42,000,000 | 350 |
| Corporate Plus | $2,500 | 55,000,000 | 400 |
| Corporate Pro | $3,000 | 65,000,000 | 450 |
| Enterprise Starter | $4,000 | 90,000,000 | 500 |
| Enterprise Plus | $5,000 | 120,000,000 | 600 |
| Enterprise Pro | $6,000 | 150,000,000 | 650 |
| Global Starter | $7,000 | 185,000,000 | 700 |
| Global Plus | $8,000 | 220,000,000 | 800 |
| Global Pro | $9,000 | 255,000,000 | 850 |
| Global Elite | $10,000 | 295,000,000 | 900 |
| Ultra Starter | $12,000 | 360,000,000 | 1,000 |
| Ultra Plus | $14,000 | 430,000,000 | 1,200 |
| Ultra Pro | $16,000 | 500,000,000 | 1,300 |
| Titan Starter | $18,000 | 580,000,000 | 1,400 |
| Titan Plus | $20,000 | 660,000,000 | 1,500 |
| Titan Pro | $22,000 | 740,000,000 | 1,700 |
| Titan Elite | $24,000 | 830,000,000 | 1,800 |
| Nova Starter | $26,000 | 920,000,000 | 1,900 |
| Nova Plus | $28,000 | 1,010,000,000 | 2,000 |
| Nova Pro | $30,000 | 1,100,000,000 | 2,200 |

The largest single discount on the whole ladder sits between Lite and Standard: $50 more buys five times the credits, roughly 55% off the per-page rate, and ten times the concurrency. Per 1,000 plain requests, Lite works out to $0.20 against $0.09 on Standard, $0.067 on Pro and $0.053 on Business Plus. Past that, the curve flattens hard.

## The credit table that actually sets your bill

The sticker price is per credit. What you pay per page depends on what you ask the API to do. These are the multipliers Scrapingdog publishes:

| Request type | Credits | Examples |
| --- | --- | --- |
| Plain page through rotating proxy | 1 | General HTML; Amazon search and product, Yelp, Indeed, YouTube transcript |
| JavaScript rendering | 5 | Google Maps, Google News, Google SERP Light, Walmart, eBay, Twitter, TikTok, YouTube scraper, Screenshot API |
| Premium proxy, geotargeting or AI parser | 10 | Google SERP Advance, Google Shopping, Google Images, Google Lens/AI Mode |
| Universal Search API | 20 | — |
| JavaScript rendering plus premium proxy | 25 | LinkedIn posts |
| Profile scraper | 50 | — |

Two rows deserve attention before you pick a plan.

Rendering is five times the base rate, and most modern shops, directories and listing pages need it. On Standard that is $0.45 per 1,000 rendered pages instead of $0.09.

Geotargeting is a 10-credit request. A country-specific price check on a store that localises prices quietly multiplies your meter by ten, without you asking for anything that feels expensive. On Standard, geotargeted volume drops to 100,000 requests for $90, or $0.90 per 1,000.

## Three real volumes, three different plans

**500 competitor product pages a day, JavaScript on.** 15,000 pages a month × 5 credits = 75,000 credits. That fits Lite at $40 with room to spare, but Lite gives you no parser, no scheduler and no storage for what comes back.

**2,000 listings a day, rendered through premium proxies.** 60,000 pages × 25 credits = 1,500,000 credits, which overshoots Standard and lands on Pro at $200.

**300 Google Maps businesses a week.** 1,200 requests × 5 credits = 6,000 credits. The free tier cannot cover it and Lite at $40 covers it easily.

The pattern behind the three: jobs that render JavaScript or run on a schedule belong on Standard or above, and once you regularly pass 200,000 rendered pages a month you are into Pro. Lite's 5 concurrent requests is fine for a prototype and painful for a nightly crawl.

## The billing rules that aren't on the price grid

**There is no overage.** When credits run out, requests stop and the API returns an over-limit response until the next billing date. You are never silently moved to a bigger plan or billed for the difference. Running dry mid-month is an availability problem, not a surprise invoice.

**Failed requests are not charged.** Blocked, timed-out and failed requests are credited back automatically. That matters most on the 25-credit protected requests, where a retry loop against a stubborn target would otherwise burn through a Lite balance in a day.

**Annual billing is ten months for twelve.** About 17% off. Standard costs $900 a year instead of $1,080, which is a $180 difference and works out to roughly $75 a month. The risk with annual is outgrowing the plan mid-term, not overpaying by $180.

**Upgrades are prorated, downgrades take effect next cycle.** You can move up mid-month and only pay for the remaining days.

**Rollover is genuinely unclear, and that is the most useful thing to know.** Scrapingdog's pricing page states that unused credits carry over from Standard upward to the next billing cycle. The FAQ on the same page says monthly credits reset on your billing date. Those two statements cannot both be true, and nothing published by the vendor reconciles them. If your volume is seasonal, ask support in writing before you buy an annual Standard plan. Treat any claim that rollover definitely works, or definitely doesn't, as unverified.

**The free tier is smaller than review sites suggest.** It is 100 credits today, and several comparison pages still quote an older, larger allowance.

## Where the $40 sticker stops being the whole bill

Scrapingdog sells requests. The pipeline around those requests is your build: parsing the HTML into fields, scheduling the runs, storing results, retrying failures and fixing parsers when a target changes its layout. None of that is in the $40, and none of it is in the $30,000 plan either.

Two structural consequences follow.

The first is the geotargeting multiplier above. If your workload is location-specific pricing, availability or SERP data, half your budget can disappear into a 10-credit surcharge that has nothing to do with page count.

The second is engineering time. A developer on staff makes the DIY path cheap. A comms, pricing or ops team with no developer ends up paying someone to maintain scrapers, which is usually where the arithmetic flips.

That is the gap ScraperAPI sells into. Geotargeting, sessions, device type, output format and auto-parsing are free of credit cost there, and the DataPipeline component runs a schedule and delivers results without you writing the cron job or the storage layer. 👉 [Check what ScraperAPI charges for the volume you need](https://www.scraperapi.com/pricing?fp_ref=coupons)

## ScraperAPI plans and what each request costs

ScraperAPI publishes a simpler ladder: seven paid tiers plus a free one, priced on credits and concurrent threads.

| Plan | Monthly price | Credits per month | Concurrent threads |  |
| --- | --- | --- | --- | --- |
| Free | $0 | 1,000 | 5 | [Start free](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Hobby | $49 | 100,000 | 20 | [Get Hobby](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Startup | $149 ($134.10/mo billed annually) | 1,000,000 | 50 | [Get Startup](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Business | $299 | 3,000,000 | 100 | [Get Business](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Scaling | $475 ($427.50/mo billed annually) | 5,000,000 | 200 | [Get Scaling](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Professional | Quoted | 10,500,000 | 300 | [Request pricing](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Advanced | Quoted | 21,500,000 | 500 | [Request pricing](https://www.scraperapi.com/pricing?fp_ref=coupons) |
| Enterprise | Quoted | 22,000,000+ | 500+ | [Request pricing](https://www.scraperapi.com/pricing?fp_ref=coupons) |

Annual billing on Startup saves $178.80 a year over monthly ($1,609.20 against $1,788), and Scaling saves $570. Country-level geotargeting starts at Business; Hobby and Startup cover US and EU.

The credit costs run wider than Scrapingdog's, from 1 to 75:

| Request type | Credits |
| --- | --- |
| Standard page | 1 |
| E-commerce (Amazon, Walmart, eBay) | 5 |
| JavaScript rendering | 10 |
| Premium proxy | 10 |
| Bot-protection bypass (Cloudflare, DataDome, PerimeterX, Akamai) | 10 |
| Screenshot | 10 |
| SERP (Google, Bing) | 25 |
| Premium proxy plus JS rendering | 25 |
| LinkedIn | 30 |
| Ultra premium | 30 |
| Ultra premium plus JS rendering | 75 |
| Geotargeting, sessions, device type, output format, auto-parsing | 0 |

## Head to head, on the numbers that matter

Putting the two middle plans side by side shows where each one is actually cheaper. ScraperAPI figures use the monthly Startup price of $149 for 1,000,000 credits; Scrapingdog figures use Standard at $90 for 1,000,000.

| Per 1,000 requests | Scrapingdog Standard | ScraperAPI Startup |
| --- | --- | --- |
| Plain page | $0.09 | $0.149 |
| JavaScript rendered | $0.45 | $1.49 |
| Country-targeted page | $0.90 (10 credits) | $0.149 (no surcharge) |
| Google SERP | $0.45 (5 credits) | $3.73 (25 credits) |
| Rendered pages included | 200,000 | 100,000 |
| Parsing, scheduling, storage | You build it | Auto-parse and DataPipeline included |

Three honest conclusions come out of that table.

On plain HTML and JavaScript-rendered pages, Scrapingdog is cheaper per unit, and nothing on the ScraperAPI side changes that.

On Google SERPs and Amazon data, Scrapingdog's dedicated endpoints at 5 credits and 1 credit beat ScraperAPI's 25 and 5 by a wide margin. If your entire workload is SERP tracking, the Scrapingdog ladder is the right shape.

On country-targeted requests, the surcharge reverses the result. A 10-credit geotargeting multiplier turns Standard into a $0.90-per-1,000 plan, while ScraperAPI charges nothing extra for US and EU targeting on Startup and nothing extra for country-level targeting from Business upward. Add auto-parsing and a scheduler that you would otherwise build, and the gap widens.

## Which one to buy

Work backwards from the request type, not the plan name.

**Static HTML at volume, with a developer on hand:** Scrapingdog Lite for a prototype, Standard once it runs on a schedule. $0.09 per 1,000 plain pages is hard to beat.

**Google SERP, Amazon or Maps data as the core job:** Scrapingdog's dedicated endpoints at 1 to 5 credits are the cheaper instrument, provided you handle the output yourself.

**Location-specific data, or a team without a developer:** ScraperAPI, because geotargeting adds no credits and the parsing and scheduling are already built. 👉 [Compare ScraperAPI's tiers against your monthly request count](https://www.scraperapi.com/pricing?fp_ref=coupons)

Two things to settle before you enter a card number anywhere.

Check the real credit cost of your specific target rather than the headline rate. Both vendors price by request type, and both expose a way to check a single URL's cost before you commit a budget to it. A test run of a few hundred URLs tells you more than any comparison table.

Then confirm the rollover rule in writing for whichever plan you pick, especially on annual billing. Scrapingdog's own page says both things, and a seasonal workload is exactly the case where the difference between carrying credits forward and losing them costs more than the discount annual billing gives you.

If you want the managed version of this decision made for you, 👉 [start with ScraperAPI's free tier and price the plan you'd actually need](https://www.scraperapi.com/pricing?fp_ref=coupons).

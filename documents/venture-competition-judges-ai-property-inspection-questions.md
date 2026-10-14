# What Venture Competition Judges Asked Us About AI Property Inspection

Source: https://rapideyeinspections.com/blog/venture-competition-judges-ai-property-inspection-questions/

_CMU McGinnis judges grilled us on AI accuracy, workflow adoption, and defensibility. Here's what sophisticated evaluators actually care about in this space._

# What Venture Competition Judges Asked Us About AI Property Inspection

A few weeks ago, RapidEye took second place in the Graduate Track at CMU’s [McGinnis Venture Competition](https://www.rapideyeinspections.com/blog/rapideye-wins-cmu-mcginnis-venture-competition-2026), walking away with $25,000 in cash and $25,000 in AWS credits. This was CMU’s most competitive cycle ever, with [70% more entries than the prior year](https://www.cmu.edu/swartz-center-for-entrepreneurship/resources-funding-and-talent/mcginnis-venture-competition/2026-final-round-info.html).

But this isn’t a “how to win pitch competitions” post. What I actually want to share is what the judges asked us.

When you pitch to a room of investors, industry experts, and academics who evaluate hundreds of startups, their questions reveal what actually matters. What’s unclear. What objections you’ll face from customers too. The McGinnis judging guidelines literally say the competition is meant to be an [“early reality check”](https://www.cmu.edu/swartz-center-for-entrepreneurship/assets/McGinnis/2025-judging-guidelines.pdf) for founders.

If you’re a property manager evaluating AI inspection tools, you probably have similar questions. So here’s what came up.

## “How accurate is it, really?”

This came up multiple times, in different forms. Judges wanted specifics on false positive rates. They pushed on edge cases. One judge asked what happens when lighting conditions change between inspections.

I get why this was the first thing they drilled into. There’s a lot of AI skepticism right now, especially in property management. AppFolio’s 2026 benchmark report found that [78% of property managers say they can’t yet rely on AI features](https://www.appfolio.com/newsroom/property-manager-benchmark-survey-2026) in their legacy software. That’s a trust problem across the industry.

And honestly, judges should be skeptical. Bessemer’s State of AI report notes that enterprise buyers now demand [“provable, explainable, and trustworthy performance”](https://www.bvp.com/atlas/the-state-of-ai-2025) from AI vendors. They’ve seen too many demos that fall apart in production.

What we explained: our accuracy comes from baseline comparison. We’re not trying to detect “damage” in a vacuum. We’re comparing today’s photos against a visual record of what the property looked like before. That’s a fundamentally different (and easier) problem than general image classification. The AI is looking for *changes*, not trying to decide if a scratch is “bad.”



If you’re evaluating AI inspection tools, this is the right question to start with. Ask vendors about their false positive rates. Ask to see real examples. [We publish ours](https://rapideyeinspections.com/showcase/).

## “Will cleaners actually use this?”

This question caught me a little off guard. Not because it’s unreasonable, but because of how quickly judges zeroed in on it.

They understood the AI tech. What they wanted to know was whether it would actually get adopted. Does it fit into existing workflows? Or is it another tool that gets ignored?

This maps to a real industry dynamic. AppFolio found that [45% of operators plan to consolidate their tech stacks](https://www.appfolio.com/newsroom/property-manager-benchmark-survey-2026) this year. Property managers are fatigued by disconnected tools. They don’t want more software to manage.

Our answer: RapidEye works with the photos cleaners are already taking. If you use Breezeway, your team is already capturing 20-100 photos per turnover. That data just sits there unreviewed. We analyze it automatically. No workflow change needed.

This was one of the key points that landed well. When judges heard “works with existing photos,” they got it immediately. The adoption barrier drops significantly when you’re not asking people to do something new.

For property managers, I’d ask the same question of any tool you’re evaluating. Does it require new behavior from your team? New hardware? New steps in the turnover process? The best tools fit into what you’re already doing.

## “What’s your moat?”

Defensibility came up in almost every judge conversation. What stops a bigger company from copying this? What’s the competitive advantage?

This question has extra weight at McGinnis because the competition is public. Sessions are open, pitches may be broadcast, and [CMU doesn’t ask judges or audience members to sign NDAs](https://www.cmu.edu/swartz-center-for-entrepreneurship/resources-funding-and-talent/mcginnis-venture-competition/index.html). So anything you say on stage is fair game.

We were pretty open about our answer: data and workflow integration.

On data: we’ve processed over 1.6 million inspection photos, across different property types, furniture styles, and lighting conditions. A competitor starting today doesn’t have that.

On workflow: the inspection tools that win are the ones that become part of daily operations. Breezeway has facilitated [30 million+ property tasks](https://www.breezeway.io/vacation-rental) because it’s embedded in how teams work. Our [Breezeway integration](https://www.rapideyeinspections.com/blog/add-ai-damage-detection-breezeway-workflow) means we’re part of that operational stack, not a separate system to remember.

Judges seemed satisfied with this. The moat isn’t any single feature. It’s the combination of data and workflow integration.

## What surprised us

I expected to spend more time explaining the problem. You know, the whole “cleaners miss things, manual review doesn’t scale, damage claims get denied” spiel. I figured judges would need convincing that this pain point was real.

They didn’t. Most judges got it immediately.

A few had personal experience with vacation rentals. One mentioned dealing with a damage dispute as a guest. Another managed investment properties. But even judges without direct STR experience understood the core issue: at scale, you can’t manually review thousands of photos. The economics don’t work.

Maybe that’s because the professional operator segment is growing. [AirDNA’s data shows professional STR operators maintain higher occupancy](https://help.airdna.co/en/articles/10261024-2025-u-s-str-market-trends-insights-and-opportunities) through better tooling and revenue management. The industry is professionalizing, and judges recognized that professional operations need scalable systems.

What did need explanation: the specifics of how platform claims work. Why timestamped evidence matters for Airbnb AirCover or Vrbo disputes. How [back-to-back bookings create attribution problems](https://www.rapideyeinspections.com/blog/back-to-back-booking-damage-attribution-proof). That level of detail was new to most judges.

## What this means for property managers

The questions judges asked aren’t unique to pitch competitions. They’re the same questions sophisticated buyers ask when evaluating any tool.

- **On accuracy:** Don’t accept vague claims. Ask for specifics on false positive rates. Ask to see real detections, not cherry-picked demos.

**On accuracy:** Don’t accept vague claims. Ask for specifics on false positive rates. Ask to see real detections, not cherry-picked demos.

- **On adoption:** Consider the human side. Will your team actually use this? Does it require new behavior or new hardware? The best AI in the world doesn’t help if it sits unused.

**On adoption:** Consider the human side. Will your team actually use this? Does it require new behavior or new hardware? The best AI in the world doesn’t help if it sits unused.

- **On defensibility:** This one matters less for buyers than for investors, but it’s still relevant. A vendor with real traction, real data, and real workflow integration is more likely to still be around in two years than a tool that just launched.

**On defensibility:** This one matters less for buyers than for investors, but it’s still relevant. A vendor with real traction, real data, and real workflow integration is more likely to still be around in two years than a tool that just launched.

If you’re curious about how RapidEye handles these questions, I’m happy to walk through it. [Our showcase](https://rapideyeinspections.com/showcase/) shows real before/after detections we’ve made for clients. And if you want to understand [how the detection actually works](https://www.rapideyeinspections.com/blog/how-automated-damage-detection-works), we’ve written about that too.

The McGinnis competition was a good stress test. When smart people who evaluate startups for a living grill you for an hour, you find out pretty quickly where your weak points are. For RapidEye, the core thesis held up. The questions were tough, but they were the right questions.

# Evidence

Every figure here was read from the source listed. Cite the source by name in the
report. If a check has no figure behind it, say it is a judgment call. Do not
invent, round, or combine numbers.

## Nielsen Norman Group: how to run a heuristic evaluation

Source: https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/

- Narrow the scope by task, section, user group, or device before starting.
- Go through the product once to learn it, then again looking for violations.
- Three to five evaluators working independently is the recommendation, because
  individuals, even experts, miss issues. This skill is one evaluator, so the
  report says so in its limits.
- A heuristic violation is not automatically a problem to fix. It can be an
  acceptable trade-off.
- Heuristic evaluation finds likely problems cheaply but does not replace
  research with real users.

## Nielsen: severity ratings

Source: https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/

- Severity combines frequency, impact, and persistence. Nielsen also weighs
  market impact: some problems hurt a product badly even when they are easy to
  get past.
- His scale runs 0 to 4: not a problem, cosmetic, minor, major, catastrophe.
  This skill uses the four problem levels as Cosmetic, Minor, Major, and
  Critical.

## Nielsen Norman Group: how long visitors stay

Source: https://www.nngroup.com/articles/how-long-do-users-stay-on-web-pages/
Basis: Microsoft Research analysis of page dwell times (Liu and colleagues).

- Visitors make a harsh judgment in about the first 10 seconds. Pages that
  survive it are still likely to be left in the next 20 seconds. The curve
  flattens at about 30 seconds.
- The average page visit lasts a little under a minute.
- Visitors have time to read only a fraction of the text on the pages they
  visit. Cite this as "a fraction," not as a percentage.

## Nielsen Norman Group: homepage design principles

Source: https://www.nngroup.com/articles/homepage-design-principles/

- Communicate who you are and what you do. Failing to communicate a site's
  purpose at a glance causes potential customers to leave.
- Show the company name and logo prominently, top left.
- Include a tagline that explicitly says what the site or company does. Do not
  assume visitors know the brand.

## Nielsen Norman Group: four trust factors

Source: https://www.nngroup.com/articles/trustworthy-design/

- Four ways a site communicates trustworthiness, first listed by Nielsen in 1999
  and still observed in later research: design quality, up-front disclosure,
  comprehensive and current content, and connection to the rest of the web.
- In the study, one participant dismissed a cleaning service in 35 seconds
  because it did not state its rates and asked visitors to write in instead.
- Visitors look for FAQ pages to answer cost and policy questions.
- Content should cover the full range of what the organization offers.

## Steve Krug: the trunk test

Source: Steve Krug, *Don't Make Me Think*, the chapter on navigation.

Drop onto any interior page as if you had been driven there blindfolded. A
well-designed page lets you answer these at once:

1. What site is this? (site ID)
2. What page am I on? (page name)
3. What are the major sections of this site? (main navigation)
4. What are my options at this level? (local navigation)
5. Where am I in the scheme of things? ("you are here" indicators, breadcrumbs)
6. How can I search?

Krug's broader point: every question a visitor has to stop and think about adds
to their load. Use it to explain findings, not as a figure.

## Abby Covert: information architecture heuristics

Source: https://abbycovert.com/ia-tools/ia-heuristics/

Ten questions for judging structure: Findable (can people locate it?),
Accessible, Clear (easy to perceive and understand?), Communicative, Useful,
Credible, Controllable, Valuable, Learnable, Delightful. This skill leans on
Findable and Clear for the navigation area.

## The LIFT model

Sources: https://conversion.com/blog/the-six-landing-page-conversion-rate-factors/
and https://umbrex.com/resources/frameworks/marketing-frameworks/lift-model-for-conversion-value-relevance-clarity-anxiety-distraction-urgency/
Created by Chris Goward at WiderFunnel in 2009.

- Six factors judged from the visitor's point of view. The value proposition is
  central and the most important. Relevance, clarity, and urgency drive
  conversion. Anxiety and distraction inhibit it.
- Relevance: the page must use terms visitors relate to and stay consistent with
  the link that brought them.
- Clarity has two parts, design (a clear eye flow) and content (text and images
  that are quick to understand).
- Urgency should be genuine. Fake scarcity damages the brand. This skill treats
  fake urgency as a problem.

## Speero heuristics

Source: https://speero.com/blueprints/heuristics-blueprint

- A consolidation of frameworks used by leading UX and conversion agencies, 60
  guidelines across five themes: Value, Relevance, Clarity, Friction, and
  Motivation.
- Friction is framed as anything causing doubts, hesitations, uncertainties, or
  difficulties.

## Baymard Institute: ecommerce navigation

Source: https://baymard.com/blog/ecommerce-navigation-best-practice
Basis: Baymard's 2026 benchmark of leading US and European ecommerce sites.

- 64% of sites have mediocre-to-poor homepage and category navigation
  performance.
- 22% of sites do not make product categories the first level of the main
  navigation on mobile.

Use for ecommerce sites only.

## WCAG 2.2, Level AA

Sources: https://www.w3.org/WAI/standards-guidelines/wcag/new-in-22/ and
https://webaim.org/articles/contrast/

- WCAG 2.2 became a W3C Recommendation on 5 October 2023. It adds nine success
  criteria to 2.1 and removes 4.1.1 Parsing.
- 1.4.3 Contrast (Minimum): normal text at least 4.5:1. Large text at least 3:1.
  Large is 18pt and up, or 14pt bold and up, roughly 24px or 18.66px bold.
- 1.4.11 Non-text Contrast: interface components and meaningful graphics at
  least 3:1 against adjacent colors.
- 2.4.7 Focus Visible: keyboard focus is visible.
- 2.4.11 Focus Not Obscured (Minimum), new in 2.2: a focused item is not
  entirely hidden by author-created content such as sticky headers or banners.
- 2.5.8 Target Size (Minimum), new in 2.2: pointer targets at least 24 by 24 CSS
  pixels, or with enough spacing.
- 3.2.6 Consistent Help, new in 2.2: help mechanisms appear in the same place
  across pages.
- 3.3.7 Redundant Entry, new in 2.2: do not make people re-enter information
  they already gave in the same process.
- Do not score against AAA. Mention it only as an option.

Say "passes WCAG 2.2 AA" or "fails it" on a named check. Do not say "ADA
compliant." The ADA does not set these thresholds, and that phrasing makes a
legal claim this skill cannot make.

## Google: Core Web Vitals

Sources: https://web.dev/articles/vitals,
https://web.dev/articles/optimize-lcp, https://web.dev/articles/optimize-inp,
https://web.dev/articles/cls, and
https://developers.google.com/speed/docs/insights/v5/about

| Metric | Measures | Good | Poor |
|---|---|---|---|
| Largest Contentful Paint (LCP) | Loading | 2.5 s or less | over 4.0 s |
| Interaction to Next Paint (INP) | Responsiveness | 200 ms or less | over 500 ms |
| Cumulative Layout Shift (CLS) | Visual stability | 0.1 or less | over 0.25 |

- Between good and poor is "needs improvement."
- Thresholds apply at the 75th percentile of page loads, segmented by mobile and
  desktop.
- INP replaced First Input Delay as a Core Web Vital on 12 March 2024.
- PageSpeed Insights reports field data from the Chrome UX Report and lab data
  from Lighthouse. A page passes the assessment when all three metrics are good
  at the 75th percentile.
- Lab and field numbers differ. Field data is real visitors. Lab data is one
  simulated load. Say which you used.

## AI reviewers: what they miss

Source: Guerino et al., "Can GPT-4o Evaluate Usability Like Human Experts?"
arXiv 2506.16345, June 2025. https://arxiv.org/abs/2506.16345

- GPT-4o, reviewing web screenshots against Nielsen's heuristics, found only
  21.2% of the issues human experts found, and raised 27 issues the experts did
  not.
- 24.3% of the issues it raised were false positives, attributed to
  hallucination and attempts to predict problems.
- It did relatively well on aesthetic and minimalist design and on match
  between system and real world, and poorly on flexibility, user control, and
  efficiency.

This is why the skill requires a URL and element for every finding, tests
control and efficiency in the browser rather than from screenshots, and ends
every report with what to test with real users. Do not cite this study in a
report. It shapes the method, not the findings.

## Benchmarks for "What your score means"

Use these to give the accessibility and speed results context. Check for newer
releases first if you can search the web. Never use them to rank the total
score.

**WebAIM Million 2026.** Source: https://webaim.org/projects/million/ (read via
reports of the February 2026 scan). Automated scan of the top one million home
pages.

- 95.9% of home pages had detectable WCAG 2 failures, up from 94.8% in 2025.
- An average of 56.1 detected errors per home page.
- Low-contrast text on 83.9% of home pages.

Automated scans catch only part of WCAG, and this skill's checks differ, so
this is context, not a like-for-like comparison.

**Chrome UX Report.** Source: https://developer.chrome.com/docs/crux/release-notes
(release published October 13, 2026). Real-visitor data across all origins.

- 68.3% of origins had good LCP.
- 81.7% had good CLS.
- 85.4% had good INP.
- 55.9% had good Core Web Vitals (all three).

When the site's own numbers come from a Lighthouse lab run, say so in the same
sentence. Lab and field numbers are not the same measure.

There is no benchmark for this skill's total score. Do not invent one.

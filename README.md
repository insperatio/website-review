# mj-website-review

A free agent skill that runs a heuristic review of a website and gives you a
score and at most five ranked fixes.

It asks for the URL, who the site is for, and the one action it wants visitors
to take. Then it reads the site like a first-time visitor: the five-second read,
the trunk test on an inner page, a walk down the main path, trust signals,
visual hierarchy, WCAG 2.2 AA accessibility checks, speed, and mobile. The result is a
score out of 100.

Built by [Mariana Johnels](https://marianajohnels.com), a senior UX and product
designer with a background in conversion and growth design. Free, MIT licensed,
and it never sends your site's address anywhere.

For design portfolios, use the sibling skill,
[mj-portfolio-review](https://github.com/insperatio/portfolio-review).

## Install

```sh
npx skills add insperatio/website-review
```

Works with Claude Code, Cursor, Codex, and other agents the
[skills CLI](https://www.skills.sh/docs) supports.

**On Claude.ai**, download or clone this repo and upload the
`skills/mj-website-review` folder as a skill. Claude.ai cannot render a page in
a browser, so the review runs in code-only mode and scores out of 70. See
"Modes" below.

Then ask for a review:

> Review example.com. It's for operations managers at mid-size logistics
> companies, and we want them to book a demo.

## What it checks

| Area | Points |
|---|---|
| First impression and value proposition | 20 |
| Navigation and structure | 15 |
| Content clarity and relevance | 10 |
| Conversion path and usability | 15 |
| Trust and credibility | 10 |
| Visual design and hierarchy | 10 |
| Accessibility | 10 |
| Speed and mobile | 10 |

**First impression** answers four questions from the first screen only: what is
this, who is it for, why this one, and what do I do next.

**Navigation and structure** runs Steve Krug's trunk test on an inner page and
checks whether menu labels predict what is behind them.

**Conversion path and usability** walks the route to the main action and stops
before any final submit. It looks for friction, distraction, and unanswered
doubts, using the LIFT model and Nielsen's heuristics.

**Trust and credibility** uses Nielsen Norman Group's four trust factors.

**Accessibility** checks contrast, keyboard and focus, target size, alt text,
structure, and form labels. The report says "passes WCAG 2.2 AA" or "fails it"
on each check it ran. It never says "ADA compliant."

**Speed** uses Core Web Vitals, preferring real-visitor field data and saying
when it fell back to a lab run.

Every problem also gets a severity (Critical, Major, Minor, Cosmetic), which
decides the order of the fixes.

Verdict bands, by percentage: 85% and up, strong; 70% to 84%, solid with
fixes; 50% to 69%, fix before spending more on traffic; under 50%, rework the
core message and path.

Every report explains what the score means right under it: which band you are
in and how far from the next, and how your accessibility and speed results
compare with the wider web, using WebAIM's annual scan of the top one million
home pages and Google's Chrome UX Report. There is no average total score yet,
so the total itself is never ranked against other sites.

The point values are a judgment call by this skill. They are not endorsed by any of
the sources below.

## Modes

Hierarchy, contrast, and speed cannot be judged from source HTML, so the report
always says what it could measure.

- **Live review.** A browser loaded the page. All 100 points are in play.
  Without a speed tool, 95.
- **Code-only review.** No browser. The five content areas are scored, worth
  70 points. Visual design, accessibility, and speed and mobile are listed as
  not yet checked, and those points come out of the total instead.

## How it stays honest

- Every finding names a URL and an element, and is tagged **Seen live**,
  **In the code**, or **To confirm**. To-confirm findings cost no points and are never
  stated as problems.
- It tests control and efficiency in the browser (closing modals, the back
  button, keyboard focus, filters), because AI reviewers working from
  screenshots tend to miss those.
- It never submits a form, places an order, signs up, or enters personal data.
- It never predicts a conversion lift and never recommends dark patterns.
- It ends every report with what to test with real users, because an expert
  review finds likely problems, not proof.

## Privacy

**Counting is anonymous.** When your agent can send web requests, each review
sends two things to a Google Form: today's date and which AI tool ran it. Never
your site URL, your score, your findings, your name, your email, or anything
from the conversation. The report tells you when a run was counted. Where
requests are blocked, as in most chat apps, nothing is sent and nothing is
said. To turn counting off, blank out `usage_form_id` in
`references/tracking.json`.

**Feedback is separate and voluntary.** Every report ends with a link to a
[short feedback form](https://docs.google.com/forms/d/e/1FAIpQLSfMiLw1zcXUk_5owAmIglwFhayg-pVfTEMczurEgmYH59AwnQ/viewform). Fill it in only if you want to: what would make
the skill better, what the review got wrong, and, if you choose, your site,
your name, and an email. It goes straight to Mariana.

Full detail is in
[`references/tracking.md`](skills/mj-website-review/references/tracking.md).

## Credits

The rubric, point weights, and review approach were written for this skill.

- **Nielsen Norman Group**, on heuristic evaluation, severity, homepages, dwell
  time, and trust.
- **Steve Krug**, *Don't Make Me Think*, for the trunk test.
- **Abby Covert**, for her information architecture heuristics.
- **The LIFT model** (Chris Goward, WiderFunnel) and **Speero's heuristics
  blueprint**, for the conversion lens.
- **Baymard Institute**, on ecommerce navigation.
- **W3C WCAG 2.2** and **WebAIM**, on accessibility.
- **Google's Core Web Vitals**, on speed.

Sources and the exact figures used are in
[`references/evidence.md`](skills/mj-website-review/references/evidence.md).

## What this is not

It is not a usability test, an accessibility audit, or a performance audit. It
is one expert-style reviewer applying established principles. It cannot see
your analytics, so it does not guess your conversion rate. Those questions go in
the "Questions for you" list.

## Layout

```
skills/mj-website-review/
  SKILL.md                      the review flow
  references/
    rubric.md                   areas, severity, caps, bands, site types
    evidence.md                 every source and figure
    report-template.md          report structure
    tracking.md                 consent wording and payload
    tracking.json               form config
```

## License

MIT. See [LICENSE](LICENSE).

# Rubric

100 points across eight areas. The weights do not change with the type of site.
What changes is what each area has to show, using the site-type notes at the
end.

Keep the math visible in the report. Show the points you gave per area and the
total. Never adjust a total to land in a band you prefer.

| Area | Points | Needs a browser |
|---|---|---|
| First impression and value proposition | 20 | No |
| Navigation and structure | 15 | No |
| Content clarity and relevance | 10 | No |
| Conversion path and usability | 15 | No |
| Trust and credibility | 10 | No |
| Visual design and hierarchy | 10 | Yes |
| Accessibility | 10 | Yes |
| Speed and mobile | 10 | Yes, plus a speed tool |

The first five areas can be scored from source in a pinch, for 70 points. The
last three need the rendered page.

## Points available

Score only what you could check. If an area or a named part of one could not be
checked, move it to "Not yet checked," take its points out of the total available,
and explain it directly under the score line, before anything else in the
report. Say which part, how many points, why it could not be checked, and that
the points were left out rather than guessed. Use plain words a site owner
understands: "the review browser could not be shrunk to phone width," not "the
viewport could not be emulated." Then apply the verdict bands to the
percentage.

The usual cases:

- **Code-only review**: 70 available. Visual design, accessibility, and speed
  and mobile are not scored.
- **Live review, no speed tool**: 95 available. The speed half of speed and mobile
  (5 points) is not scored.

Show both numbers, for example "62/70, which is 89%."

---

## Severity

Give every problem a severity. Severity decides the order of the fixes. It does
not add or remove points on its own; the area bands do that.

Weigh three things, after Nielsen:

- **Frequency**: how many visitors hit it. Anything on the home page, in the
  main navigation, or on the main path reaches most visitors.
- **Impact**: does it stop them, slow them, or just annoy them?
- **Persistence**: do they get past it once, or does it get in the way every
  time?

| Severity | Meaning |
|---|---|
| **Critical** | Stops visitors from understanding the site or completing the main action. Fix first. |
| **Major** | Slows or confuses many visitors, or makes them doubt the site. High priority. |
| **Minor** | Real friction, but rare or easy to get past. Fix when convenient. |
| **Cosmetic** | Polish only. Mention it, but it rarely belongs in the top five fixes. |

If you are not sure something is a problem at all, it is To confirm, not
Cosmetic.

---

## 1. First impression and value proposition (20)

What it measures: in the first few seconds, can a visitor tell what this is, who
it is for, why it is worth their time, and what to do next?

Score from the five-second read you recorded before exploring. Use the home page
and, if most traffic lands elsewhere, the main landing page too.

Check:

- The organization's name and logo are visible, in the expected place.
- A headline or tagline says plainly what the site offers. A slogan that could
  belong to any company ("Empowering what's next") does not count.
- The audience is named or obvious.
- There is a reason to choose this over the alternatives: a specific outcome,
  a difference, or proof.
- One primary call to action is visible on the first screen, at desktop and at
  390px, and its label says what happens next.
- The hero image shows the real product, service, place, or people. Generic
  stock imagery carries no information. A carousel that rotates the main message
  usually hides it.

- **18 to 20**: All four questions answered on the first screen. A visitor could
  repeat back what this is and what to do.
- **14 to 17**: What and what-next are clear. Who-for or why-this is thin.
- **9 to 13**: You have to scroll or read closely to work out what is offered,
  or the primary action is unclear among several.
- **4 to 8**: The first screen is mostly slogan, imagery, or brand story.
- **0 to 3**: You still cannot say what the site offers after the first screen.

## 2. Navigation and structure (15)

What it measures: can a visitor find what they came for, and tell where they are
when they land on an inner page?

Check:

- **The trunk test** on one interior page: all six questions answered without
  hunting.
- **Labels in visitors' words.** Menu labels predict what is behind them. Vague
  labels ("Solutions," "Resources," "More") and internal jargon cost visitors.
  Quote the labels you flag.
- **Grouping.** Related things live together, and each item has one obvious
  home. Watch for the same content filed under two menus.
- **Location.** The current section is shown, and on deep sites there are
  breadcrumbs.
- **Search**, where the size of the site calls for it, and it returns sensible
  results for an obvious query.
- **Footer** covers the utility links visitors expect: contact, pricing where
  relevant, privacy, terms.
- **No dead ends.** Every page offers a next step. No orphan pages, broken
  links, or 404s on the paths you walked.
- **Consistent** navigation across pages, and a mobile menu that opens, closes,
  and works.

- **14 to 15**: Trunk test passes cleanly. Labels are clear. Nothing hard to find.
- **11 to 13**: One weak spot, such as a vague label or a missing location cue.
- **7 to 10**: Several vague labels, a confusing grouping, or a failed trunk-test
  question.
- **3 to 6**: Visitors would struggle to find key content or tell where they are.
- **0 to 2**: The structure cannot be navigated.

## 3. Content clarity and relevance (10)

What it measures: is the writing easy to scan, in plain language, and does it
answer what this audience needs to know?

Visitors read only a fraction of a page (see NN/g in `evidence.md`). Judge what
a skimmer gets.

Check:

- Headings and subheads tell the story when read alone.
- Plain language. Benefits to the visitor before features. No "happy talk," the
  filler intros that say nothing.
- The questions this audience brings are answered on the site: what it costs or
  how pricing works, how it works, who it is for, what happens after the main
  action.
- If they named a traffic source, the landing page matches the promise that
  brought visitors there.
- Content is current. Flag stale dates, old copyright years, past events, and
  "coming soon" that never came.
- Proofread what you read. Typos read as carelessness.

- **9 to 10**: Scannable, plain, and the audience's main questions are answered.
- **7 to 8**: Clear, with one gap, such as no word on what happens next.
- **4 to 6**: Dense, vague, or jargon-heavy, or a key question goes unanswered.
- **2 to 3**: Hard to extract anything useful.
- **0 to 1**: Placeholder or unreadable content.

## 4. Conversion path and usability (15)

What it measures: once a visitor wants to act, can they do it without avoidable
friction, distraction, or doubt?

Walk the main path from the home page to the step before final submit. Use the
LIFT and Speero lenses for friction, distraction, and anxiety, and Nielsen's
heuristics for the interaction itself.

Check:

- **Steps.** Count them. Name any step that does not need to exist.
- **Calls to action** say what will happen ("Book a 20-minute demo," not
  "Submit"). One primary action per page, visually distinct from the rest.
- **Forms** ask only for what is needed now. Labels stay visible while typing,
  not placeholder-only. Required fields are marked. Errors say what to fix and
  appear next to the field.
- **Distraction.** Pop-ups that interrupt before the visitor has seen any value,
  competing calls to action, or exits that pull people off the path.
- **Anxiety.** Cost, commitment, and data use are clear before the visitor
  commits. Reassurance (guarantee, cancellation terms, privacy note) sits near
  the action, not buried.
- **Urgency** is real if present. Fake countdowns and false scarcity are a
  problem, not a strength.
- **Feedback and control.** The page shows loading and success states. Modals
  close. Back works. Nothing is lost by going back a step.
- **Standards.** Links look like links, buttons look like buttons, and the same
  thing works the same way everywhere.

- **14 to 15**: Short, clear path. No avoidable friction. Doubts answered at the
  moment they arise.
- **11 to 13**: Works well, with one friction point, such as an extra field or a
  vague button label.
- **7 to 10**: Noticeable friction: several unneeded fields, competing actions,
  or cost unclear until late.
- **3 to 6**: Visitors would likely drop off: confusing steps, poor error
  handling, or a disruptive interruption.
- **0 to 2**: The main action cannot be found or completed. See deal-breakers.

## 5. Trust and credibility (10)

What it measures: does the site give a visitor reasons to believe it, using
NN/g's four factors?

Check:

- **Design quality.** The site looks maintained. Broken images, layout bugs, and
  mismatched styles cost trust. (Craft itself is scored in area 6. Here, judge
  only whether quality problems undermine belief.)
- **Up-front disclosure.** Who runs the site, how to reach a person, and what
  things cost or how pricing works. Hiding price behind a form is a cost to
  trust, and a judgment call for enterprise sales.
- **Comprehensive and current.** The site covers what the organization actually
  offers, and nothing looks abandoned.
- **Connected to the rest of the web.** Proof a visitor can check: named
  customers, reviews, case studies, press, certifications, working social links.
  Anonymous quotes with stock photos count for little.
- Privacy policy and terms exist and are findable.

- **9 to 10**: All four factors are present and easy to find.
- **7 to 8**: One factor is thin, such as no pricing signal or unnamed
  testimonials.
- **4 to 6**: Two or more factors missing. A careful visitor would hesitate.
- **2 to 3**: Little reason to trust it. No clear owner or contact.
- **0 to 1**: Signs of abandonment or deception.

## 6. Visual design and hierarchy (10)

What it measures: does the visual design guide the eye to what matters and hold
together across pages?

Check:

- **Eye flow.** On key pages, the most important thing is the most prominent,
  and the primary action stands out.
- **Type hierarchy.** Heading levels are distinct and consistent. Body text is
  readable in size and line length.
- **Spacing and alignment.** Consistent margins, padding, and container widths.
  Name the specific place it breaks.
- **Components.** Buttons, cards, and links look and behave the same everywhere.
- **Density.** Enough room to scan. Nothing decorative competing with content.
- **Consistency** of brand, imagery, and layout from page to page.

- **9 to 10**: Clear hierarchy, consistent system, deliberate choices, even if
  plain.
- **7 to 8**: Mostly consistent, with specific lapses you can name.
- **4 to 6**: Competing elements, unclear hierarchy, or visible inconsistency.
- **2 to 3**: Hard to scan. No discernible system.
- **0 to 1**: Broken layout.

Fairness: plain is not a deduction. Bold is not a bonus. If the site has a
distinctive choice of its own, name it under "Keep this."

## 7. Accessibility (10)

What it measures: can people with low vision, color blindness, motor
limitations, or a keyboard use the main path?

Score only what you can check. Say what you checked and how. Focus on the home
page and the main path.

- **Text contrast (up to 3)**: Body text, headings, links, button labels, and
  text over images. Report the ratio against 4.5:1 normal and 3:1 large, with
  the exact colors and element.
- **Non-text contrast (up to 1)**: Buttons, field borders, meaningful icons, and
  focus indicators need 3:1 against adjacent colors.
- **Keyboard and focus (up to 2)**: Every control on the main path can be
  reached and used by keyboard. Focus is visible. Focus is not hidden behind a
  sticky header, chat widget, or cookie banner (2.4.11).
- **Target size (up to 1)**: Controls on the main path are at least 24 by 24 CSS
  pixels, or spaced so they do not crowd (2.5.8). Check at 390px.
- **Images and alt text (up to 1)**: Meaningful images have alt text. No key
  text baked into images.
- **Structure (up to 1)**: One h1, headings in order, real headings and
  landmarks rather than styled divs.
- **Form labels (up to 1)**: Every field has a programmatic label, and errors are
  announced in text, not color alone.

Report as "passes WCAG 2.2 AA" or "fails WCAG 2.2 AA" on each check you ran.
Never say "ADA compliant." Never claim the whole site is accessible. If you
could not test something, put it under "Not yet checked" with no points lost and
say how they can check it.

## 8. Speed and mobile (10)

What it measures: does the site load and respond quickly, and does it work on a
phone?

**Speed (up to 5).** Use Core Web Vitals thresholds from `evidence.md`.

- Prefer field data (PageSpeed Insights, Chrome UX Report). Score the mobile
  numbers at the 75th percentile.
- If there is no field data, use a Lighthouse lab run on mobile and say it is
  lab data from one run. A lab run cannot measure INP. Score LCP and CLS only,
  report Total Blocking Time as a note, and put INP under Not yet checked.
- With all three metrics: 5 all good, 3 to 4 one needs improvement, 1 to 2 two
  need improvement or one is poor, 0 two or more poor.
- With LCP and CLS only (lab): 5 both good, 3 to 4 one needs improvement, 1 to 2
  one poor, 0 both poor.
- Do not score the Lighthouse performance score itself. Score the three metrics.
- If no tool was available, move speed to Not yet checked and take its 5 points out
  of the total available. Note anything you saw, such as a visible layout jump,
  as Seen live observations without points.

**Mobile (up to 5).** At about 390px wide:

- No horizontal scrolling. Text readable without zooming.
- The primary action is reachable without hunting.
- The menu opens, closes, and reaches everything the desktop menu does.
- Nothing covers the content in a way that is hard to dismiss.
- Phone numbers and addresses are tappable where relevant.

- 5: works as well as desktop. 3 to 4: one friction point. 1 to 2: several, or
  the main path is awkward. 0: broken on mobile.

---

## Deal-breakers and caps

These replace red-flag point deductions. They are structural, not stylistic.

- **Broken or unreachable URL**: do not score. Report what failed, with the
  exact URL and error. Stop.
- **Password required and not supplied**: do not score. Ask for the password
  and stop.
- **The main action is broken**: the call to action leads to a 404, the form or
  cart cannot be reached, or the path dead-ends. Cap the total at 50, rate it
  Critical, and make it the first fix.
- **Placeholder content** (lorem ipsum, "Your headline here," template demo
  copy) on the home page or the main path: cap the total at 60.
- **A wall blocks the content** (consent, login, or bot check you cannot pass):
  score what you could see, move the rest to Not yet checked, and note it. If
  nothing is visible, do not score.

Say in the report when a cap was applied and why.

## Verdict bands

Apply to the percentage of points available.

- **85 to 100**: Strong. Polish, then test.
- **70 to 84**: Solid. Fix the top issues.
- **50 to 69**: Fix before spending more on traffic.
- **Under 50**: Rework the core message and path.

State the band and one sentence on what it means. Do not soften a low band with
praise that is not in the findings, and do not inflate a score to avoid
delivering one.

---

## Site-type notes

The areas stay the same. These are what each type usually needs to show. All
are judgment calls unless a source is named.

- **Software and product sites**: what it does in one line, who it is for,
  pricing or how pricing works, a path to try or see it (demo, trial, tour),
  what it works with, and security or compliance information for business
  buyers.
- **Ecommerce**: product finding first. Categories as the first level of the
  mobile menu, working search, and filters that show their state (Baymard, see
  `evidence.md`). Price, shipping cost, delivery time, and returns visible before
  checkout.
- **Local and service businesses**: what you do, where, and for whom. Service
  area, hours, a tappable phone number, and a booking or quote path on the first
  screen of mobile.
- **Nonprofits**: the mission in a sentence, evidence of impact, how money is
  used, and a donate path that is short and clear about amounts and frequency.
- **Content and media sites**: finding articles by topic and by search, a
  comfortable reading experience, and subscribe prompts that do not block
  reading before any value is shown.

## The point weights are a judgment call

Say so in the report, in one line. The areas are informed by Nielsen Norman
Group, Steve Krug, Abby Covert, the LIFT model, Speero, Baymard, WCAG 2.2, and
Google's Core Web Vitals. The point values are this skill's judgment and are not
endorsed by any of them.

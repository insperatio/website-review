# Report template

Follow this layout. Use its headings as written and add no new ones. Leave out
a section only when there is nothing to put in it, without mentioning that it
is missing.

```
# Website review: {domain}

{URL} · reviewed {date}
Audience and main action: {what they gave, or "not stated, so judged as {what the site appears to be for}"}
Mode: {Live review} or {Code-only review, no browser available}
Points available: {100, or the reduced number with a pointer: "95, see why under the score"}
Pages reviewed: {every page you opened}
Not submitted: {forms or steps you stopped before}

**Score: {n}/{points available} ({percent}%). {Verdict band}.**

{Only when points available is under 100, and always directly under the score,
before anything else:}
> **Why {points available}, not 100:** {for each part left out: what it is, its
> points, and the plain-words reason it could not be checked}. Those points were
> left out, not guessed, so the score covers only what was tested. {What they
> can do: "Check it yourself with the steps under Not yet checked and send the
> answers back to have it scored."}

**What your score means:** {percent}% is {band} ({range}). {How far from the
next band.} {One plain sentence on what that means for them.}

| Band | Range | |
|---|---|---|
| Strong | 85 to 100 | {"you are here" or empty} |
| Solid | 70 to 84 | |
| Fix before more traffic | 50 to 69 | |
| Rework | under 50 | |

**Compared with the web:** {accessibility result against WebAIM Million, with
date}. {speed result against Chrome UX Report, with date, and "lab" if lab}.
There is no average total score for this review yet, so the total itself is
not compared.

{Two sentences. What a first-time visitor understands in the first few seconds,
and the one thing holding the site back most.}

## The five-second read
| Question | What a visitor can tell from the first screen |
|---|---|
| What is this? | {answer, quoting the headline} |
| Who is it for? | {answer} |
| Why this one? | {answer} |
| What do I do next? | {answer, quoting the main call to action} |

{One line on how the same screen reads at 390px. Write this section from the
notes you took before exploring.}

## Trunk test
Page: {URL of the interior page you dropped onto}

| Question | Answered? | How |
|---|---|---|
| What site is this? | {yes / no / partly} | {element} |
| What page am I on? | ... | ... |
| What are the major sections? | ... | ... |
| What are my options here? | ... | ... |
| Where am I? | ... | ... |
| How can I search? | ... | ... |

## Goal fit
{Does the site serve the audience and main action they gave? Name what a
visitor from that audience gets, what they would also need before acting, and
the nearest thing on the site that could close the gap. If they said "not
sure," say what the site appears to be for and stop.}

## Main path walkthrough
| Step | Page | What happened | Friction |
|---|---|---|---|
| 1 | {URL} | {what you did and saw} | {none, or the problem} |
| ... | | | |

{Where you stopped, and why.}

## Strengths
- {Strength, and where on the site.} [{Seen live / In the code}] {Source: name, or "judgment call".}
- Keep this: {a distinctive choice of theirs, and why it helps.}

## Problems found
- **{Critical / Major / Minor / Cosmetic}**: {Problem, quoting or naming the URL and element.} [{Seen live / In the code}] {Source: name, or "judgment call".}
- ...

{Order by severity, most severe first.}

## Accessibility check
{Only the checks you ran, on the home page and main path. Omit in a code-only
review and say why in the header.}

| Check | What you measured | Result |
|---|---|---|
| Body text contrast | {fg} on {bg}, {size}, {element} | {ratio}:1, {passes / fails} 4.5:1 |
| Large text contrast | {fg} on {bg}, {size} | {ratio}:1, {passes / fails} 3:1 |
| Non-text contrast | {element} | {ratio}:1, {passes / fails} 3:1 |
| Keyboard and focus | {what you tabbed through} | {result} |
| Focus not obscured | {sticky elements checked} | {result} |
| Target size | {controls checked at 390px} | {result} |
| Alt text | {what you checked} | {result} |
| Structure | {h1, heading order, landmarks} | {result} |
| Form labels | {fields checked} | {result} |

{One line: these are the checks run here, not a full audit.}

## Speed and mobile
| Metric | Mobile value | Rating | Data |
|---|---|---|---|
| LCP | {value} | {good / needs improvement / poor} | {field, CrUX / lab, one Lighthouse run} |
| INP | {value} | ... | ... |
| CLS | {value} | ... | ... |

Mobile at 390px: {what worked and what did not, in two or three lines.}

## Observations
{Observations that are neither strengths nor problems: deliberate trade-offs you
saw, template use, third-party widgets, cookie banner behavior. Mark judgment
calls as such.}

## Not yet checked
- {To confirm point, why it could not be checked, and how they can confirm it.
  For an unscored area, list exactly what to look at and say that sending the
  answers back lets the review score it.} (No points lost.)

## Questions for you
- {A fact only they can supply: conversion rate on the main path, top landing
  pages, what visitors ask sales or support, why something is built the way it
  is.}

## Test with real users
- {A task to give five people from the audience, tied to a finding above, and
  what to watch for.}
- {Where traffic allows, an A/B test for a persuasion change, with the metric to
  watch. No predicted lift.}

## Top fixes
1. **{Severity}** · {Where it is}: {what to change}. Why: {one line, with a
   source or marked as a judgment call}. Finished when: {the sign it is done, or what to test}. Effort: {small / medium / large}.
2. ...

{Five at most. Ranked by severity, then by how many visitors hit it.}

## Score breakdown

| Area | Points | Given |
|---|---|---|
| First impression and value proposition | 20 | {n} |
| Navigation and structure | 15 | {n} |
| Content clarity and relevance | 10 | {n} |
| Conversion path and usability | 15 | {n} |
| Trust and credibility | 10 | {n} |
| Visual design and hierarchy | 10 | {n or "not scored: no browser was available to see the page"} |
| Accessibility | 10 | {n or "not scored: no browser was available to see the page"} |
| Speed and mobile | 10 | {n, plus a short reason for any half not tested, e.g. "2. Mobile 5 points not tested and removed from the total: the review browser could not show a phone-width view."} |
| **Total** | **{points available}** | **{n} ({percent}%)** |

{Note any cap applied and why.}
This was a single-reviewer expert review, not a usability test. The point weights are set by this
skill, drawing on Nielsen Norman Group, Steve Krug, Abby Covert,
the LIFT model, Speero, Baymard, WCAG 2.2, and Google's Core Web Vitals. They
are not endorsed by any of them.

---
Reviewed with mj-website-review, a free skill by Mariana Johnels. linkedin.com/in/marianajohnels · marianajohnels.com
```

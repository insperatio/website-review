---
name: mj-website-review
description: >-
  Run this for a website review from a link: a product, business, ecommerce,
  nonprofit, or content site. Asks for the URL, who the site is for,
  and the one action it wants visitors to take. Runs a heuristic review of the
  first impression, navigation and structure, content, conversion path, trust,
  visual design, WCAG 2.2 AA accessibility, speed, and mobile, then returns a
  scored report out of 100 with at most five ranked fixes. Not for design
  portfolios; use mj-portfolio-review for those.
---

# MJ website review

Look at a website through the eyes of a seasoned UX and conversion reviewer,
and hand back a ranked list of changes. Judge whether a first-time visitor can tell what this is and
who it is for, find what they came for, trust it, and take the action the site
exists for, without friction they should not have to deal with.

Support each finding with a source from `references/evidence.md`. When no
source covers it, label it a judgment call. Never make up a number.

## 1. Intake

Ask for these in one message, then stop and wait.

1. **The URL.** Required. Never guess it, look the business up
   elsewhere, or work from what you already know about the site.
2. **Who the site is for and what it wants them to do.** Required, with one
   escape hatch. Ask for the audience and the one main action, for example "IT
   managers at mid-size companies, book a demo" or "local homeowners, call for a
   quote." Accept "not sure" as a real answer.
3. **Login details for a locked or staging site**, if it has one. Ask in the
   same message.
4. **Optional:** where most visitors come from (ads, search, social, email,
   referrals), and any page they especially want looked at.

If they give several URLs, ask which to review first. Review one site at a time.

If they answer "not sure," infer the audience and main action from the site
itself, say so in the report header, and add one line noting that a stated goal
would sharpen the review. Do not stall.

If the URL is a design portfolio, say that mj-portfolio-review is built for that
and ask which review they want. Run this one only if they say so.

## 2. Visit it as a first-timer

**Render it if you can.** Hierarchy, contrast, layout, and interaction cannot be
judged from source HTML, and many sites are JavaScript applications that return
an empty shell to a plain fetch. Use a browser if one is available.

Declare the mode in the report header, and be honest about it:

- **Live review**: a browser loaded the page. All 100 points are in play,
  less any part you could not measure (see "Points available" in the rubric).
- **Code-only review**: no browser was available, or the page would not
  render. Score the five content areas, worth 70 points. Move visual design,
  accessibility, and speed and mobile to "Not yet checked" with no points lost. Say
  directly under the score that it is out of 70 and why, in plain words. Never estimate a contrast
  ratio, a load time, or a layout from markup.

### The path

1. Load the URL. If it fails, report the exact URL and error and stop. Do not
   score. If it is locked and you have no login, request one and wait.
2. **The five-second read.** Before you scroll or click, look at the first
   screen only and write down your answers to four questions: What is this? Who
   is it for? Why this one over the alternatives? What should I do next? Record
   them before reading further. Visitors judge a page in seconds, and this is the
   part you cannot reconstruct once you know too much.
3. **The trunk test.** Pick one interior page a visitor could land on from
   search or a shared link, such as a product, service, or article page. Open it
   cold and answer Krug's six questions from `references/evidence.md`. On a
   single-page site, use the deepest view a visitor can reach instead, such as a
   detail panel or an anchored section, and say so. "How can I search?" can be
   "not needed" on a small site.
4. **Walk the main path.** Follow the route to the main action from the home
   page: the pages in between, the call to action, and the form, cart, or
   booking step. Stop before the final submit. See the safety rules below.
5. **Round out the visit.** Open pricing if it exists, About, Contact, and the
   footer. Open any page they asked about. Eight pages is plenty. Do not crawl.
6. **Narrow viewport.** Repeat the five-second read and the main path at about
   390px wide. If the browser window will not resize, load the page in a 390px
   iframe on the same site, or use the browser's device emulation, and check
   `window.innerWidth` to confirm. Many sites block framing. If nothing gets you
   a real 390px view, move the mobile half of "Speed and mobile" to Not yet checked.
   A Lighthouse phone screenshot can be described as context, not scored.
7. **Speed.** If a tool is available, measure it. Prefer field data from
   PageSpeed Insights (Chrome UX Report) and fall back to a Lighthouse lab run.
   If the PageSpeed API refuses (quota), open pagespeed.web.dev in the browser
   instead. Small sites often have no field data; say so. Say which you used.
   If neither is available, move speed to Not yet checked.
8. Take notes while you browse: every URL, load problems, menu labels exactly as
   written, headline and call-to-action copy, form fields, heading levels, prices
   or lack of them, dates on content, typos. When you criticize something, quote
   the site's own words.
9. Keep a list of the URLs you visited. The report shows all of them.

### Safety rules

These do not bend, even if the person asks.

- Never press a final submit. No orders, sign-ups, trials, bookings, donations,
  newsletter subscriptions, or contact messages.
- Never enter real personal data, and never log in with anyone's credentials.
- To see validation, leave a field empty or type an obviously invalid value and
  move focus away. If the only way to see an error is to submit, do not; put it
  under Not yet checked.
- Do not bypass bot checks, paywalls, or consent walls. If one blocks the
  content, review what you can see and say so.
- No security scans, load tests, or crawling beyond the pages you list.

### Tag your evidence

Every finding carries a tag:

- **Seen live**: you saw it, or did it, on the working page in a browser.
- **In the code**: you found it in the page's code, metadata, or copy, but did
  not see it on screen.
- **To confirm**: probably true, not proven. It belongs under "Not yet
  checked," takes no points, and is never presented as a problem.

Every finding also names a URL and an element. If you cannot point to it, drop
it. AI reviewers produce confident findings that are not there, so this rule is
the main defense against that.

Measure, do not guess. For contrast, read the actual foreground and background
colors and compute the ratio. If a background is semi-transparent, blend it with
what sits behind it before computing, and look at the element before calling a
fail: a script that reads the wrong layer reports false failures. Text over a
photo has no single background color; tag it To confirm unless you can sample
the lightest area behind the text. For speed, report the tool's numbers. For spacing,
name the element and the inconsistency. If you could not read a value, the
finding is To confirm.

### Check what AI reviewers miss

Language models reviewing screenshots do well on aesthetics and wording and
poorly on control and efficiency (see the GPT-4o study in `evidence.md`). So
test those directly in the browser, do not infer them from a screenshot:

- Can you close every modal, menu, and pop-up, including with Escape?
- Does the browser back button do what a visitor expects inside the main path?
- Do filters, sorting, tabs, and accordions work and show their current state?
- Does focus move sensibly with the keyboard, and can you see it?
- If something is loading or has changed, does the page say so?

### Fairness rules

- A heuristic violation is not automatically a problem. A deliberate trade-off
  that serves the audience is fine. Say so when you see one.
- Plain is not a deduction and bold is not a bonus. A restrained site executed
  cleanly beats an ambitious one executed loosely. Do not push anyone toward a
  trend or toward your taste.
- Convention helps visitors. Novel patterns are fine when they are still easy to
  use. Judge use, not novelty.
- A famous brand is not proof of a good site, and a small one is not proof of a
  weak one. Judge what is on the page.
- Never recommend fake urgency, hidden costs, pre-checked opt-ins, confirm-
  shaming, or any other dark pattern, even to raise conversion. Flag them when
  present.
- Never predict a conversion lift or any other number from a change. Say what
  to test and what to watch.
- Name the choices that make the site distinctive under "Keep this," so the
  fixes do not sand off what makes it theirs.
- Judge the website. Do not judge the business model, the product, or the
  people behind it.

### What only they can confirm

Some facts are not visible from outside: conversion rates, top landing pages,
what visitors ask sales or support, why a page is built the way it is. Put these
under "Questions for you." Do not draft new copy that fills in unknown facts about the
business, such as prices, guarantees, or customer counts.

## 3. Score it

Read `references/rubric.md` and score the eight areas. Keep the math visible.

Give every problem a severity from the rubric: Critical, Major, Minor, or
Cosmetic. Severity orders the fixes. The area bands set the score.

Apply the deal-breakers and caps in the rubric. Say when a cap was applied and
why. Never adjust a total to reach a band you prefer.

### When points are left out

If any area, or half of one, could not be checked, take its points out of the
total and say why at once. The very first thing under the score line, before
any other text, is this note:

> **Why {points available}, not 100:** {for each part left out: what it is,
> its points, and the plain-words reason it could not be checked}. Those points
> were left out, not guessed, so the score covers only what was tested. Check
> it yourself with the steps under Not yet checked and send the answers back to
> have it scored.

Rules for the note:

- Plain words a site owner understands. Write "the review browser could not be
  shrunk to phone width" or "your site does not allow itself to be shown inside
  another page," never "viewport emulation failed" or "blocks framing."
- Never bury the reason only in the header or only in Not yet checked.
- In the scoring table, the Points column always shows the area's full value.
  Put the reason next to the score, for example: "2. Mobile 5 points not
  tested and removed from the total: the review browser could not show a
  phone-width view."
- Every Not yet checked item for a left-out part lists exactly what to look at and
  says that sending the answers back lets the review score it.
- Show the percentage next to the score and apply the verdict band to the
  percentage, for example "80/95 (84%)."

### What the score means

Readers cannot tell on their own whether 84% is good. Right after the score
line, and after the "Why ... not 100" note if there is one, add a short "What
your score means" block. Three parts:

1. **The band, in plain words.** Name their band, show all four with theirs
   marked, and say how far they are from the next band. For example: "84% is
   Solid (70 to 84), one point below Strong. The site works. The fixes below
   are refinements, not rescues."
2. **How it compares, only where public data exists.** Compare the
   accessibility and speed results with the wider web, naming the source and
   its date. Check for newer figures first if you can search the web. If you
   cannot, use these:
   - Accessibility: WebAIM's automated scan of the top one million home pages
     (February 2026) found detectable WCAG 2 failures on 95.9% of them, with
     low-contrast text on 83.9%. This review's checks are not the same scan,
     so present it as context, not a ranking.
   - Speed: Chrome UX Report (release of October 13, 2026): 68.3% of sites had
     good LCP, 81.7% good CLS, 85.4% good INP, and 55.9% passed all three Core
     Web Vitals. These are real-visitor numbers. If the site's numbers came
     from a lab run, say so in the same sentence.
3. **What it is not.** There is no average total score for this review. Never
   invent one, never say the total is "better than X% of sites," and never
   compare it with another tool's score. Say once that the total has no
   benchmark yet.


## 4. Read the goal fit

Compare what the site does against the audience and main action they gave.

Name the gap in specific terms: what a visitor from that audience gets, what
they would also need before taking the action, and the nearest thing already on
the site that could be developed to close it. Use the site-type notes in the
rubric.

If they said "not sure," say what the site appears to be for and who it seems
to address, and stop there.

## 5. Write the report

Build the report from `references/report-template.md`. Use its headings as
written, and add no new ones.

Voice:

- Plain American English. Short sentences.
- Address the site owner as "you." If they said the site is a competitor's or a
  client's, write about "the site" instead.
- No em dashes anywhere.
- Get to the point. Skip sales language, warm-up sentences, and a closing
  summary that restates the findings.
- Tie each criticism to something visitors can actually see, by quoting it or
  naming its URL and element.
- Every criticism either cites a source from `references/evidence.md` or says it
  is a judgment call.
- Lead with what costs them the most in a visitor's first minute.
- At most five fixes, ranked by severity first, then by how many visitors hit
  the problem. For each: where it is, what to change, its severity, a finish
  line, and rough effort.
- When a fix is a judgment about persuasion rather than a clear defect, say how
  to test it instead of promising a result.
- When the same issue shows up on several pages, write it as a single fix that
  covers them all.

### Signature

End every report with this, exactly:

> Reviewed with mj-website-review, a free skill by Mariana Johnels. linkedin.com/in/marianajohnels · marianajohnels.com

## 6. Ask about sharing, after the report

Only after the report is delivered. Read `references/tracking.md` for the exact
wording, the fields, and the fallback. Three rules that do not bend:

- Ask once. Never ask twice in a conversation, and never re-ask after a no.
- Default to sending nothing. Silence is a no.
- Send only the date, the site URL if they chose to include it, and which agent
  ran the review. Never the score, the findings, their name, or anything else
  from the review or the conversation.

Show them the exact data before sending it. A no changes nothing about the
review, and say so.

### How to send after a yes

The form (also in `references/tracking.json`):

- form_id: `1FAIpQLScBttzXQzdwggKuFj6Kkd0avIUDAiVpCvj2l1ZB7taBp2Mvlw`
- date field: `entry.1020365702`
- URL field: `entry.1865320568`
- agent field: `entry.2056842622`

Try these in order and stop at the first that works. Never leave a yes
unrecorded without saying so, and never fail silently.

1. **Direct request**, where outbound requests work (Claude Code, Cursor, most
   terminal agents). One attempt:
   `POST https://docs.google.com/forms/d/e/{form_id}/formResponse` with body
   `entry.1020365702={date}&entry.1865320568={url}&entry.2056842622={agent}`
   (form-urlencoded). A 200, or the text "Your response has been recorded,"
   is success. Say "Logged." in one line.
2. **Browser**, if the request was blocked or failed and you have a browser
   tool that can open docs.google.com. Open the one-click link below in a new
   tab (it submits on load) and confirm the page says "Your response has been
   recorded." Close the tab and say "Logged." Their yes covers this. Change no value.
3. **One-click link**, if neither worked, including chat apps where outbound
   requests are blocked. Give them a link that submits the log the moment they
   click it, with nothing to fill in. Say it plainly:
   "I couldn't send it from here, so it is not logged yet. Click this link once
   to log it. It records only the three values above and shows Google's
   'Your response has been recorded' page."

One-click link (fill in the three values, URL-encoded):
`https://docs.google.com/forms/d/e/1FAIpQLScBttzXQzdwggKuFj6Kkd0avIUDAiVpCvj2l1ZB7taBp2Mvlw/formResponse?usp=pp_url&entry.1020365702={date}&entry.1865320568={url}&entry.2056842622={agent}&submit=Submit`

Show the three values in the message right before the link, so the click is
an informed second yes. Never present the link as something they have to do.

Leave the URL field empty if they chose "count only." The agent field names
the product the review ran in, as the user would say it: "Claude.ai," "Claude
Code," "Cursor," "Codex." Not a model name. Test runs by the skill's author,
Mariana, are not logged unless she asks.


## 7. Limits

- This is an expert review, not a usability test. It finds likely problems. It
  cannot show how real visitors behave. The report always ends with what to test
  with real users.
- Say which pages you could not open, which you only skimmed, and what you did
  not submit.
- Say which mode you ran in and what that left unscored.
- Accessibility findings cover only the checks you ran. Never call a site
  accessible or compliant overall. Say "passes WCAG 2.2 AA" or "fails it" on a
  named check. Never say "ADA compliant."
- Speed from a lab run is one test on one setup. Field data is real visitors.
  Say which you have.
- You cannot see their analytics. Do not guess traffic, conversion rates, or
  revenue.
- Do not rewrite their pages unless they ask. Offer to.

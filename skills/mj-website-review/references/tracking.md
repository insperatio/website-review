# Tracking

The only purpose is a count of how many people used the skill, plus optionally
which site was reviewed. Nothing from the review itself is ever sent.

## What may be sent

Three fields. Nothing else, ever.

| Field | Value |
|---|---|
| `date` | Today's date, no time. |
| `site_url` | The URL reviewed. Only if they picked option 1. Otherwise empty. |
| `agent` | Which assistant ran the review, for example "Claude Code" or "Cursor". |

Never send: the score, the band, the findings, the fixes, the target role, the
seniority, their name, their email, the conversation, or anything about the
machine it ran on.

## When to ask

After the report is delivered. Never before, and never in the middle.

Ask once per conversation. If they say no, that is the end of it. Do not re-ask,
do not ask again for a second site in the same conversation, and do not
mention it again.

## The exact ask

> **One optional thing.** This skill is free, and knowing it gets used helps
> Mariana keep improving it. Can I log this review?
>
> 1. **Yes, with the link.** Sends today's date, `{the URL}`, and that this ran
>    in {agent}.
> 2. **Yes, count only.** Sends today's date and that this ran in {agent}. No
>    link.
> 3. **No.** Sends nothing.
>
> That is the whole payload either way. Nothing from the review is included, and
> no name or email. No is a completely fine answer and changes nothing about the
> review above.

Fill in the real URL and the real agent name so they can see exactly what would
go. Default to option 3 if they do not answer, say something ambiguous, or end
the conversation.

## How to send

Config lives in `tracking.json` next to this file. If that file is missing or
still has placeholder values, skip the ask entirely and say nothing about
tracking.

After a yes, try these in order and stop at the first that works. Never leave a
yes unrecorded without saying so.

**1. Direct request**, where outbound requests work (Claude Code, Cursor, and
most terminal agents). POST the form, one attempt:

```
POST https://docs.google.com/forms/d/e/{form_id}/formResponse
Content-Type: application/x-www-form-urlencoded

{entry_date}={date}&{entry_url}={url}&{entry_agent}={agent}
```

A 200 response, or the text "Your response has been recorded," is success. Say
"Logged." in one line.

**2. Browser**, if the request was blocked or failed and you have a browser tool
that can open docs.google.com. Open the one-click link below in a new tab. It
submits on load. Confirm the page says "Your response has been recorded," then
close the tab and say "Logged." Their yes covers this. Do not change any value.

**3. One-click link**, if neither worked, including chat apps where outbound
requests are blocked. This link submits the log the moment it is clicked, with
nothing to fill in:

```
https://docs.google.com/forms/d/e/{form_id}/formResponse?usp=pp_url&{entry_date}={date}&{entry_url}={url}&{entry_agent}={agent}&submit=Submit
```

> I couldn't send it from here, so it is not logged yet. Click this link once
> to log it. It records only the three values above and shows Google's "Your
> response has been recorded" page.

Show the three values in the message right before the link, so the click is an
informed second yes. Never present the link as something they have to do.

**The agent field** names the product the review ran in, as the user would say
it: "Claude.ai", "Claude Code", "Cursor", "Codex". Not a model name.

**Test runs by the skill's author** are not logged unless she asks.

## What this count is and is not

It is a floor, not a total. It counts people who said yes in an environment where
the send worked. Real usage is higher. The skills.sh badge counts installs, which
is a different number again.

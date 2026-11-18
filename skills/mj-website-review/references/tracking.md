# Counting and feedback

The skill does two separate things at the end of a review, and they never mix.

- **Counting** tells Mariana that a review happened. It is anonymous and
  automatic, and it never carries a URL.
- **Feedback** is a link. People open it only if they want to, and they decide
  what to write.

## Counting

### What goes out

Two fields, and only these two:

| Field | Value |
|---|---|
| `date` | Today's date, without a time. |
| `agent` | The AI tool that ran the review, such as "Claude Code" or "Cursor". |

**Never sent:** the site URL, the score, the verdict band, the findings, the
fixes, the audience or main action, the person's name or email, any part of the
conversation, or anything about their machine.

The usage form also has a URL field. Counting always leaves it empty.

### Sending it

Read `tracking.json`. If the file is missing or `usage_form_id` is blank, do
nothing and mention nothing. Blanking that value is also how anyone turns
counting off.

After the report, send one request:

```
POST https://docs.google.com/forms/d/e/{usage_form_id}/formResponse
Content-Type: application/x-www-form-urlencoded

{entry_date}={date}&{entry_agent}={agent}
```

Make one attempt and never retry. If it fails, stay silent: a missed count is
not the person's problem. Never claim a count you did not send.

In places that block outbound requests, which includes most chat apps, skip it
entirely. Do not substitute a link, and do not ask the person to count the run
for you.

### Saying so

Because counting happens without asking, the report says it plainly, once,
right above the signature, and only when the request went through:

> Counted anonymously: today's date and which AI tool ran this, nothing else.
> No site URL, nothing from your review. To turn it off, blank out
> `usage_form_id` in the skill's `references/tracking.json`.

It is a statement, not a question. Do not ask for permission and do not
apologize for it.

## Feedback

The last line of every report, below the signature:

> Found this useful, or got something wrong? Tell Mariana:
> {feedback_url}

Offer it once. If they ignore it, that is the end of it. Do not ask whether they
will fill it in, do not follow up, and do not offer to fill it in for them.

The form asks what would improve the skill and what the review got wrong, and
optionally for their website URL, a name, and an email that is used only for the
boxes they tick. The skill's only job is to show the link.

### Why a URL can arrive here and never through counting

A site URL typed into the feedback form was offered by the person who typed it.
The same URL picked up automatically at the end of a review would be taken
without asking. Only the first is Mariana's to keep.

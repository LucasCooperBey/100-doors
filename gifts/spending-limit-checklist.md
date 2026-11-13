# The spending-limit checklist

Twelve days after my first app went live, I got an email: "You have used 100% of your credits from your Core plan for the current month." The same email came eight times in all, the last one nine and a half months after the first. The notice told me the fix: "To set a spending limit, visit your usage page."

Set yours before the first email. It should take about 20 minutes.

## The checklist

For every AI tool and API you pay for:

- [ ] Write it on one list: the tool, the plan, and the card it bills.
- [ ] Open its billing or usage page. Write down what it billed you last month.
- [ ] Set a hard spending limit if it offers one. Pick a number you would not mind losing in a bad week.
- [ ] Set an alert below the limit, at about half of it, so you hear before you hit it.
- [ ] Check what happens at the limit: does it stop, slow down, or keep going and bill the standard rate? Write it next to the tool.
- [ ] Find every API key you made for it. Delete the ones you don't use, and make sure none sits in a public repo or a shared document.
- [ ] Turn on usage emails, and send them somewhere you read.
- [ ] Put a date on your calendar a month from now to read this list again.

## When there is no limit to set

Some tools don't offer one. Use a prepaid balance or a card with its own low limit, keep live apps behind a login, and check usage weekly for the first month.

## Example

A made-up entry for one tool, to show the checklist filled in:

- Tool: an image-generation API, paid per image, billed to the work card.
- Last month: 31 USD.
- Hard limit: 40 USD a month, set on its billing page.
- Alert: 20 USD, by email.
- At the limit: new requests fail with an error until the next billing month, and the app shows "image failed". That goes in a note next to the tool, so a failed image isn't mistaken for a bug.
- Keys: three found. Two were unused and got deleted. The live one sits only in the app's server settings, not in the repo.
- Usage emails: on, sent to the inbox that gets read every day.
- Re-read: on the calendar for the first Monday of next month.

The next tool on the same list, a chat assistant on a monthly plan, has no hard limit and bills the standard rate past the plan. It moves to a card with its own 50 USD limit.

## Try it

Do the first three boxes for the tool you used most this week, today. Count how many tools on your list had no limit set.

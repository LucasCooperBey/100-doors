# The first prompt template

Before you ask an agent to build an app, write the product down. My first app in git started from a prompt with this shape: twelve short sections, written before any code. Fill in the brackets, cut what doesn't apply, and paste the whole thing as your first message.

```text
PRODUCT REQUIREMENTS: [name], v0.1, [season year]

1. PURPOSE
Build [what] so that [who] can [do what], with [the one quality that matters most].

2. BACKGROUND
- Today: [what people use now, and what is wrong with it]
- What changed: [why this is worth building now]
- What people keep asking for: [the two or three gaps you hear most]

3. OBJECTIVES AND HOW YOU'LL MEASURE THEM
| Objective | Measure | Target and date |
|---|---|---|
| [goal] | [a number you can read] | [the value, by when] |

4. USERS
1. [user type]: needs [what]
2. [user type]: needs [what]

5. SCOPE
| Area | Must have | Nice to have | Not this version |
|---|---|---|---|
| [feature area] | [...] | [...] | [...] |

6. USER STORIES
| ID | As a... | I want to... | So that... | Priority |
|---|---|---|---|---|
| U-01 | [user] | [action] | [outcome] | P0 (must) |
| U-02 | [user] | [action] | [outcome] | P1 (should) |

7. FUNCTIONAL REQUIREMENTS
1. [part of the app]: [the rule it must follow]
2. [part of the app]: [the rule it must follow]

8. NON-FUNCTIONAL REQUIREMENTS
- Speed: [how fast, measured how]
- Uptime: [how often it may be down]
- Security and privacy: [who may see what]
- Real data: [what must never be simulated, sampled or made up, and how you'll check]

9. METRICS
- [what you want to watch once people use it]

10. DEPENDENCIES
- [outside services, data or libraries it relies on]

11. RISKS
| Risk | Likelihood | Impact | What you'll do about it |
|---|---|---|---|
| [what could go wrong] | Low / Med / High | Low / Med / High | [...] |

12. LATER
- [ideas you are saving for after this version]
```

## A made-up example, filled in

```text
PRODUCT REQUIREMENTS: Shed, v0.1, fall 2026

1. PURPOSE
Build a checkout page for our neighborhood tool library so members can borrow a tool in under a minute and we always know where each tool is.

2. BACKGROUND
- Today: a paper sign-out sheet on a clipboard in the shed.
- What changed: the library has grown past what one clipboard can track.
- What people keep asking for: seeing what's on the shelf before walking over, and a reminder before a tool is due.

3. OBJECTIVES AND HOW YOU'LL MEASURE THEM
| Objective | Measure | Target and date |
|---|---|---|
| Fewer lost tools | tools unaccounted for at month end | zero by the new year |
| Faster checkout | median time from opening the page to done | under 60 seconds |

4. USERS
1. Members: borrow and return tools.
2. Volunteers: add tools, see who has what, send reminders.

5. SCOPE
| Area | Must have | Nice to have | Not this version |
|---|---|---|---|
| Checkout | search a tool, check it out, check it in | a photo of each tool | payments |
| Reminders | one message the day before a tool is due | a choice of text or email | late fees |

6. USER STORIES
| ID | As a... | I want to... | So that... | Priority |
|---|---|---|---|---|
| U-01 | member | see what's on the shelf right now | I don't walk over for nothing | P0 |
| U-02 | volunteer | see every overdue tool on one screen | I can follow up in five minutes | P0 |

7. FUNCTIONAL REQUIREMENTS
1. Checkout: a tool can't be checked out twice.
2. Reminders: one reminder per loan, never more than one a day.

8. NON-FUNCTIONAL REQUIREMENTS
- Speed: works on a phone in the shed with weak signal.
- Security and privacy: members see tools, never other members' names or numbers.
- Real data: what's on the shelf comes from the checkout records, never from sample data. Every number on the screen links to the records behind it.

9. METRICS
- Loans per week, tools overdue, average loan length.

10. DEPENDENCIES
- A texting or email service for reminders.

11. RISKS
| Risk | Likelihood | Impact | What you'll do about it |
|---|---|---|---|
| Someone forgets to check a tool in | High | Med | volunteers can check it in for them |
| No signal in the shed | Med | High | the page saves the checkout and sends it when signal returns |

12. LATER
- Waitlists for popular tools, tool photos, a map of the shelves.
```

## Why this shape

The purpose line keeps the agent on one job. The users and the stories tell it who it is building for and what done looks like for each of them. The "Not this version" column stops it from building everything it can imagine. The risks table makes it plan for the bad day.

The real-data line is the one I added. My first prompt asked for a real test engine, and the first build still showed simulated test scores for 33 hours, until a later commit removed them.

## Try it

Before your next build, fill in at least sections 1 and 4 to 6, then paste the whole thing as your first message. When the first version runs, pick one number on the screen and ask where it came from.

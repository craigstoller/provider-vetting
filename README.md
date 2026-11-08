# provider-vetting

A Claude Code skill for finding, vetting and hiring an attorney, accountant, tax adviser, financial planner or
other licensed professional, and for picking a local service such as a home care agency, hospice or funeral home,
often in a hurry. It sets the order of the steps and says what each message to a firm may carry. The user sends
every message and signs every agreement. The skill drafts, and keeps the record.

## What it does

Claude Code loads the skill when a task matches its description: building a shortlist, checking a licence or bar
record, writing first contact to a prospective firm, preparing for or debriefing a consultation, comparing
candidates, or replacing an adviser on a live matter. You can also call it by typing `/provider-vetting` in a
session.

It has two paths.

**The full path** is for an adviser, and for any provider when there is a dispute or an adverse party. Its steps,
in order:

1. Criteria before candidates: who the client is, the pass-or-fail gates, the scoring weights, the material no
   firm sees before engagement, and a decision date.
2. A shortlist from searches that name only the practice area, the role and the place, never the user, the other
   parties or the facts of the matter.
3. A licence and discipline check for every person who would do the work, on the regulator's own register,
   matched on licence number and address, and recorded as matched, no match, ambiguous or unavailable.
4. A conflict screen before any contact. A firm with a known tie to another party is not contacted at all, not
   even for a conflicts inquiry.
5. Staged disclosure: the first message carries who the user is, the names to check for conflicts, one neutral
   line of scope, and a request for availability and fees. A summary follows written conflict clearance.
   Documents, strategy and the full facts follow a signed engagement. A web form and a phone call are messages
   too.
6. One outreach log for the whole search.
7. A one-page call sheet for the screening call: the gate questions, what a good answer sounds like and a red
   flag for each, and what not to mention.
8. A same-day debrief and score after each call. A gate the candidate did not answer stays untested.
9. Engagement: a paid, bounded first phase rather than unpaid written analysis, the agreement checked against
   what was agreed, and every other firm closed out in writing.

It also covers replacing an adviser on a live matter, keeping the incumbent engaged until the new firm has agreed
in writing to take the matter over.

**The quick path** is for a local service with no dispute. Confirm each provider serves the client's address, take
contact details from the provider's own website, check licence status where the state publishes a lookup, rule
providers out by start date and coverage before giving any of the client's details, and confirm who may authorize
sharing those details before anything is typed into a provider's form.

## Install

Claude Code reads a skill from a folder that holds a `SKILL.md`. Put this repo's `SKILL.md` in a folder named
`provider-vetting` under `~/.claude/skills/` to use it in every project, or under `.claude/skills/` inside one
project. Nothing else is needed.

```sh
git clone https://github.com/craigstoller/provider-vetting.git ~/.claude/skills/provider-vetting
```

Or download `SKILL.md` and copy it to `~/.claude/skills/provider-vetting/SKILL.md`.

## Limits

- It gives no legal, financial or medical advice. It orders the search and says what each message may carry.
  Whether a claim is strong, what a matter is worth, or what the law requires of you is the engaged professional's
  advice to give, and the skill says so when asked.
- It is no substitute for checking a licence with the regulator. The check it asks for is a live search on the
  regulator's own public register. The skill's text, a directory listing or a firm's website never counts as that
  check.
- Its scope is American. The registers it names (state bars, boards of accountancy, the securities regulators'
  lookups) and the professional duties it assumes are American. For a professional regulated elsewhere, the licence
  check moves to that place's regulator and the rest of the path still applies, but what a firm there owes a
  prospective client is a question for that firm or an adviser.
- The user sends and submits. The skill drafts each message, and nothing reaches a firm unless the user sends it.
  A web form is filled in only with content the user has approved, and the submit is left to the user.

## Contributions

This repo is published read-only. Issues are off, and a pull request is closed without being merged. New versions
arrive as commits here, each release tagged.

## License

MIT. See `LICENSE`.

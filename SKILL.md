---
name: provider-vetting
description: Use when the user needs to find, vet, or hire an attorney, accountant, tax adviser, financial planner, or other licensed professional, including building a shortlist, checking a licence or bar record, writing first contact to a prospective firm, preparing for or debriefing a consultation, comparing candidates, or replacing an adviser on a live matter. Also use when they must pick a local service provider quickly, such as a home care agency, hospice, or funeral home.
---

# Provider vetting

## Overview

Hiring an adviser goes wrong in predictable places. The first email says too much, a shortlisted firm turns out
to serve the other side, a directory check matches the wrong person, and a charming call outranks an unanswered
question. This skill sets the order of the steps to prevent those failures.

**Core rule (full path): until a firm has cleared conflicts in writing, it gets only what stage 0 lists (who the
user is, the names to check, one neutral line of scope, a request for availability and fees). Documents, strategy
and the full facts wait for a signed engagement. Only the user can move a firm through the stages early or change
the never-send list.**

## Pick the path

- **Full path:** an attorney, accountant, tax adviser, planner or other adviser; or any provider when there is a
  dispute or an adverse party (someone whose interests run against the client's).
- **Quick path:** a local service (home care, hospice, funeral home and the like) with no dispute and no adverse
  party. Family members who simply take part are not adverse. It is built for urgent picks and works the same
  when there is more time. Go to *Quick path* below. If a dispute or an adverse party turns up, or the need turns
  out to include an adviser, switch to the full path, and tell the user what was already given to which provider.

## Boundaries

- This skill gives no legal, financial or medical advice. It orders the search and says what each message may
  carry; whether a claim is strong, what it is worth, and what the law requires of the user are the engaged
  professional's advice to give. When the user asks, say so, and keep the question for the professional once
  engaged: the screening call before engagement doesn't cover it (step 7). It is also no substitute for checking a
  licence with the regulator: step 3's check on the regulator's own register is the check, and this skill's text,
  a directory listing or the firm's website is never it.
- Its scope is American: the registers it names (state bars, boards of accountancy, the securities regulators'
  lookups) and the professional duties it assumes are American. For a professional regulated elsewhere, step 3's
  check moves to the regulator for that profession and place and its public register, matching on that register's
  own identifier; the rest of the path still applies, and what a firm there owes a prospective client is a question
  for that firm or an adviser, not this skill.
- Writing and staging the message itself (voice, mailbox drafts, read-back, sending rules): the
  `outbound-mail-drafts` skill if it's installed; otherwise draft it in the conversation for the user to send.
  This skill decides who gets a message, when, and what it may contain. Either way, nothing goes out unless the
  user sends it.
- Filing replies into the project record: the project's intake process (for example `source-custody`).
- Recording the final choice: the project's decision process (for example `decision-records`).

## Full path

### 1. Criteria before candidates

Write these down from what the engagement actually needs, such as the project's open questions:

- **The client:** the user, an entity, an estate, or someone the user acts for, and who can sign for them.
  Conflict names start from the client.
- **Gates** (pass/fail minimums): no conflict, licence active with no disqualifying discipline (the user decides
  what disqualifies), will take this matter, relevant experience, availability, a fee basis the user can accept.
- **Scoring dimensions** with weights, to rank the candidates that pass the gates, plus the switching threshold
  if an incumbent might be replaced.
- **Never-send list:** material no firm sees before engagement (strategy, internal memos, side issues).
- **A decision date**, agreed with the user and well before any deadline running on the matter, by which an
  engagement is signed or the search is re-planned.

### 2. Shortlist from generic searches

A search for candidates names only the practice area, the role and the place ("small-business tax accountant
[city]"). It never contains the user's name, other parties, entity names, amounts or the facts of a dispute.
Treat paid or sponsored listings as advertising, not evidence. Rank the shortlist with a fit matrix, cited
evidence and fee model, and keep a set-aside list with a reason for each rejection. Take each firm's contact
details from its own website. This rule covers candidate searches, meaning any search whose results are firms or
practitioners to hire. A lookup on a regulator's register (step 3) or a court's own docket (step 4) is not one, and
the names those lookups need go into them.

### 3. Licence and discipline for every named person

Check each individual who would do the work in the official directory (state bar, board of accountancy, the
securities regulators' adviser and broker lookups, other licensing body). Where no register covers the role,
record that, and what was checked instead.

- Use the live public search form. A saved or direct results link can replay an earlier search, so first run a
  control search on a name you know is listed and confirm its record comes up. Then record each person's result as
  one of four: **matched** (a record confirmed by licence number and address, or by licence number alone where the
  register publishes no address), **no match** (the control returned its record in the same sitting and this name
  returned nothing), **ambiguous** (several records, or one the number and address don't confirm), or
  **unavailable** (the form errored, or returned the same page for different names, the control included). Only a
  match counts as the licence checked, and stage 0 waits for it; where no register covers the role, the record of
  what was checked instead stands in for it. A no match or an ambiguous result goes to the user, with the other
  jurisdictions, name variants and the firm's own licence numbers as the next check; unavailable means check again
  later, or by another route to the same regulator (its phone or email verification, a second lookup it runs), and
  is never logged as clear. Two empty results for two people are two no-matches when the control search ran;
  without it they are unavailable, not a check that ran.
- Match on licence number and address, never on name alone. Same-name records with discipline exist.
- Check every jurisdiction any profile places them in, and confirm admission where the work will happen.
- Profiles go stale. Confirm each named person is active and still at the firm. A firm is a lead only if a named,
  active practitioner would do the work.
- When a firm later names someone else to do the work, check that person the same way, by licence number, and
  ask the user about ties to them, before engagement.
- Say what the check doesn't cover: discipline records are not malpractice claims or pending complaints.

### 4. Conflict screen before any contact

Before drafting any outreach, ask the user:

- Who are the adverse and interested parties: people, entities, and their advisers?
- Does any shortlisted firm or person represent, advise, or prepare returns for any of them?

The user's answers catch only the ties they know about. Where a case is already filed, also look up counsel of
record on the court's docket; a party-name lookup on the court's own site is not a candidate search. For an
unfiled matter, look for counsel named in the matter's own papers (a demand letter, notices) and in the other
side's past court cases. If nothing turns up, tell the user that the screen rests on what they know, and send
stage 0 to a few firms at a time rather than the whole shortlist. A firm with a known tie is **do-not-contact**.
Don't send it even a conflicts inquiry: the firm can't take the matter, and the inquiry tells the other side about
it, or, where the case is already filed, that the user is looking for or changing counsel, which firms they are
talking to, and what the scope line says.

A suspected tie (the user half-remembers one, or a lookup half-matches) is the user's call, not an automatic
do-not-contact. Offer ways to settle it without contacting the firm: ask the user's existing counsel, if they have
one, and look for the firm and its people in the dockets and the matter's papers. A confirmed tie makes the firm
do-not-contact. If the user contacts the firm while the suspicion stands, tell them once that a real tie means the
inquiry tells the other side, and log what was suspected, what was checked and what it found, and their choice.

Take each conflict name's exact legal form from a source document (formation papers, a court caption, a signed
agreement), so the firm checks the right names.

### 5. Staged disclosure

Each message contains what its stage lists and nothing more. A web intake form is a message, and so is a phone
call: a required description field gets the scope line only, and before written clearance a call covers only
stage-0 content. If a firm calls first, keep to that and say "I'd rather go into that once your conflict check is
done". Clearance given by phone doesn't count: ask for it by email and log it. Clearance covers the names
checked, so when a party is added or changes, re-run the screen and ask each cleared firm to check again.

| Stage | Opens when | The message contains |
|---|---|---|
| 0. First contact | The named practitioner's licence is checked and the user has answered the conflict screen | Who the user is; the names to run for conflicts (the client, related entities, other parties and their advisers); one neutral line of scope ("advice on a commercial contract matter"); a request for availability and fee basis |
| 1. Summary | Written conflict clearance: the firm says in writing (an email is enough) that it checked the names and found no conflict | A short factual summary, sent only to firms still in contention. Before it goes, check every aim it states against what the user has said, and cut any they haven't stated. Nothing from the never-send list, and no settlement position, strategy, or view of the merits |
| 2. Substance | A signed engagement agreement (the signed terms of a paid first phase count, for that phase's scope) | Documents, strategy, the full facts |

Stage 0 has no narrative: no dispute, threat, amount, deadline, plan, or account of what the user has or hasn't
done. If the scope line can't be neutral, make it more general. An offer to send documents belongs to stage 2.
Because stage 0 names the parties, it is itself a disclosure, and the one the screen can't remove: every firm that
receives it learns that a matter exists between the named parties, a firm with a tie the screen missed learns it
too, and nothing takes that back. Tell the user so before the first one goes, and send it only to real
candidates, a few at a time. When stage 0 goes to an accountant, planner or other non-lawyer, caution the user
first that the firm may owe a prospective client no duty of confidence for an enquiry it doesn't take on, so what
the message carries may be repeated, and propose asking the firm first, once the screen has cleared it, in a
message that carries no names and nothing about the matter, how it treats such an enquiry.
Follow up once with a firm that hasn't answered; if it stays silent, drop it.

The user can move a firm to a later stage early. Tell them once, in a sentence, what that exposes; if they still
want it, draft it their way. A do-not-contact firm is different: it gets nothing more, and where the reason is a
tie, it can't take the matter, so any contact only tells the other side. Say so if the user asks.

**If a firm already has more than it should.** When a message or call gave a firm more than its stage allows, or a
tie turns up after the firm cleared conflicts or got the stage-1 summary: send it nothing more, log what went to it
(each message or call, its date and what it held), mark it do-not-contact, and tell the user at once what it now
holds. If the firm had cleared conflicts in writing, or clears them in writing later without being asked again, and
no tie has turned up, the user may keep it instead, and what went is logged as an early move. This paragraph
doesn't apply to an incumbent: see *Replacing an incumbent*.

### 6. One outreach log

Keep one log for the whole search. Per firm: contact, channel, which mailbox the thread lives in, conflict-screen
result (clear, suspected tie and the user's call, or do-not-contact), licence check result (one of step 3's four),
stage reached, conflict clearance (date, who gave it, names covered), any early move the user chose, quoted fee and
terms, status, next move, where the current draft is, and the date an engagement is signed. Before answering "where
are we", read the actual threads in every mailbox (spam included), the drafts, and the calendar. Write firm names in
full, not abbreviated. A web intake form can save a field before submit, so typing into one is sending, and the
user's approval of that firm's message for that stage is the decision to send it: fill it in the user's own browser
only after that approval, with that content and nothing more, and leave the submit to the user.

### 7. A one-page call sheet

The screening call comes after written clearance. At the top, one sentence on what the call is for and a two-line opener the user can read aloud. Then the gate
questions, each with what a good answer sounds like and a red flag. Then the questions that tell candidates
apart. Then what not to mention, with a hold-the-line reply ("I'd rather go into that once we're engaged").
Leave room for answers. If the user wants to record the call, the opener asks every party's consent first; if
anyone declines, don't record.

### 8. Debrief and score after each call

Debrief the same day, within two hours if possible, and score before the next call rather than comparing at the
end. Mark each gate pass, fail or **untested**. A gate the candidate didn't answer is untested; never fill it in
from impressions. A recommendation that rests on any untested gate is conditional on written answers and says
so. Check names and licence numbers against the directory, and dates and terms against the firm's written
confirmation; ask for one if none comes, and treat them as unconfirmed until it does. Transcribe any recording locally, and
check the user's memory of the gate answers against the transcript.

### 9. Engage and close

- Don't ask candidates for unpaid written analysis. Offer the top one or two a paid, bounded first phase: fixed
  scope, a cap, and terms signed before any documents change hands. Those signed terms are the engagement for
  that phase.
- Before the user signs, check the engagement agreement against what was agreed (scope, fee, cap, start date),
  confirm the named practitioner is still active, ask the firm to reconfirm no conflict in writing, and ask for
  proof of professional liability insurance (or note that the user chose to go without it).
- Put the decision date from step 1 in every status update. If it arrives without a signed engagement, raise it
  with the user; don't let it drift.
- Record the choice as proposed. It is accepted only on the user's yes.
- Close the loop in writing with every other firm contacted, in a short note with no matter detail. A
  do-not-contact firm gets nothing.
- If every firm conflicts out or declines, re-plan with the user before the decision date.

### Replacing an incumbent

- Score the incumbent, on the terms they would accept to stay, as one of the candidates.
- The incumbent is already engaged, so the stages don't apply to it.
- Keep the incumbent engaged until the new firm has agreed in writing to take over the matter itself, deadlines
  included. Signed terms for a paid first phase don't do that on their own. List every deadline running on the
  matter for the new firm. If the screen turns up a tie or a suspected tie for the incumbent, tell the user at
  once and decide with them whether it carries on meanwhile.
- Let the new firm handle the file transfer and any notice to a court or the other side.

## Quick path: an urgent local provider

- Start from any referral list the user already has (say so when it comes from a placement service that
  providers pay), then add current web sources.
- Confirm each provider serves the client's address. Office location is a weak proxy.
- Take phone numbers and emails from the provider's own website, not a directory or referral site. Note
  conflicting numbers, and check spellings before anything is sent.
- Confirm each is a real provider, not a referral or lead site. Where the provider type is licensed and the state
  has a public lookup, check status, matching on licence number and address, and record the result as step 3 does:
  only a match counts as checked, and a lookup that was unavailable is never logged as clear.
- For quality, use any regulator's published inspection results, ratings or sanctions first; then ratings,
  review counts, ownership and posted prices. Say plainly how large or small the differences are.
- One page: the questions that rule providers out first (for example start date and coverage of the address),
  then the facts providers will ask for (date of birth, address, coverage or insurance, care needs, key dates, who
  can sign for the client). Give those details only to providers that pass the rule-out questions, and note which
  provider was given what. The client's details are often someone else's to give: before any of them is entered
  into a provider's form, portal or call, the user confirms who may authorize sharing them (the client, or a person
  acting for the client with the authority to do so) and that this person has. A web intake form can save or send
  a field before submit, so the confirmation comes before anything is typed, not before submit.
- Let the user set the call order, usually to rule candidates out fast, and update the sheet as calls eliminate
  them. If every provider is ruled out, tell the user at once and widen the search.
- Before the user signs, check the provider's agreement against the quoted price and terms.
- Nothing else from the full path applies: no weighted scorecard, conflict screen or staged disclosure.

## Red flags

| Thought | Reality |
|---|---|
| "The firm needs context to judge fit" | Stage 0's scope line is the context. The rest waits for written clearance. |
| "Put the conflict names in the first email so they can check" | Yes, but only after asking the user about ties. A conflicts inquiry to the other side's firm tips them off. |
| "Saying what hasn't happened yet is harmless" | It's a fact about the matter. A firm that turns out to be conflicted has already read it. |
| "A short written take from each firm lets the user compare" | That's unpaid work, and it pulls the matter out early. Offer a paid, bounded first phase. |
| "Search for lawyers who handle this exact dispute" | Search by practice area and place. Dispute facts go in no candidate search; the court's own docket (step 4) is a lookup, not a search for candidates. |
| "They were impressive; they'd clearly pass" | Untested is untested. |
| "The directory showed no discipline" | For which licence number, in which jurisdictions, from a live search? |
| "It's urgent, so skip the checks" | On the quick path, service area, contact details and licence status are the checks, and they take minutes. |
| "Two 'no results' pages look identical, so the search must have failed" | If the control search returned its record, they are two no-matches. Log each, with the next check. |
| "It's urgent, so type the details in and stop before submit" | The form may have saved them already. Who may authorize sharing them comes first. |
| "They asked whether the claim is strong, so give a view" | That is the engaged professional's advice to give. Say so, and keep it for the professional once engaged. |

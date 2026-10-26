# Demetric Noble

# CampusConnect — Project 3 / Sprint 3 Meeting Minutes 2

**Course:** CSCI 4221 — Software Engineering  
**Group:** 6  
**Meeting date:** October 15, 2026  
**Meeting time:** 4:00 PM–6:00 PM  
**Members listed for the group meeting:** Demetric Noble, Javian Mack, Justin Williams  
**Minutes recorded by:** Demetric Noble, UI/UX Designer and Documentation Lead  
**Product owners:** All team members  
**ScrumMaster:** Course instructor

> 

## 1. Meeting Purpose

The second meeting was a Sprint 3 progress review. We checked whether the feature packages were becoming useful specifications rather than short topic descriptions, evaluated how each persona led logically into a scenario and user story, and planned corrections before the final review. We also considered how the Figma-based design direction and React prototype could support a clear student experience.

## 2. Progress Updates by Team Member

### Demetric Noble — Academic Resources / UI/UX and documentation

- Expanded the Academic Resources description into a student-facing navigation concept.
- Organized resources into understandable categories, including tutoring, advising, and study support.
- Drafted Marcus Johnson's persona with goals, frustrations, and design needs.
- Connected Marcus's upcoming exam to a realistic search-for-tutoring scenario.
- Wrote the academic-support user story and began turning it into testable acceptance checks.
- Reviewed file organization and Markdown headings so the four required sections were easy to locate.

**Design consideration:** The feature should help students access university services but must not promise online appointment booking unless that specific integration is built.

### Javian Mack — Campus Event Listings / technical planning

- The assigned event-browsing package covered the information students need to evaluate an event: title, date, time, location, and description.
- Jordan Lee's persona connected student involvement to the need for current event information.
- The event-discovery scenario followed a clear path from browsing a list to viewing an individual event.
- Technical review topics included readable event cards, detail navigation, missing event fields, and an empty list state.

**Review note:** These are the agreed package contents and discussion points; Javian's personal final sign-off remains pending.

### Justin Williams — Notifications / project coordination

- The assigned notification package described how reminders would relate to a specific upcoming event.
- Alex Carter's persona established why a busy student would need reminders.
- The scenario connected noticing an event, checking a reminder, and returning to the event details.
- Management review topics included keeping one contribution per member, collecting all meeting records, and preparing for GitHub submission.

**Prototype boundary:** A visual mock reminder does not establish that real push notifications, subscriptions, or scheduled delivery work.

## 3. Cross-Feature Review and Corrections

| Review area | Finding or concern | Agreed revision |
| --- | --- | --- |
| Feature descriptions | A title alone would not explain useful app behavior | Add intended functions, expected user benefit, and acceptance criteria |
| Personas | Generic “college student” wording provides little design guidance | Give each persona a goal, frustration, context, and measurable success outcome |
| Scenarios | Scenarios should explain a beginning, sequence, and outcome | Describe step-by-step use and at least one missing-data or no-results case |
| User stories | The instructor expects role, action, and reason | Use “As a / I want / so that” and add observable acceptance checks |
| UI clarity | Event/resource labels may be ambiguous | Use student-friendly labels and visible access details |
| Technical accuracy | Prototype screens may exist before backend integrations | Distinguish proposed behavior from verified implementation |
| Sprint assignment | Some earlier drafts used an inconsistent sprint label | Use **Sprint 3** throughout Project 3 files and backlog rows |
| Review evidence | Assigned reviewers are not automatically approving a file | Record individual sign-offs only when confirmed |

## 4. My UI/UX and Documentation Review

I checked how a student might move through the proposed Academic Resources interface:

1. **Entry:** The navigation label must be visible and recognizable.
2. **Decision:** Resource categories should explain what type of help is offered.
3. **Next action:** A listing should provide an appropriate link or instructions instead of leaving the student at a dead end.
4. **Feedback:** If information has not been entered, the interface should explain the absence.
5. **Consistency:** Resource cards, event cards, and reminder content should use consistent visual hierarchy and simple language.

I also coordinated the content format so each feature could be evaluated using the same four academic requirements: feature, persona, scenario, and user story. I prepared revisions to keep the minutes, backlog, and individual assignment descriptions consistent.

## 5. Problems and Risks

1. **Mismatch between documentation and prototype.** Writing a feature does not guarantee it functions in code. We should report verified screens honestly and keep future work separate.
2. **Visual consistency.** The local React/Vite preview and the original Figma design may differ. Layout and CSS should be checked during implementation; this does not replace the four Project 3 documentation sections.
3. **Missing content data.** Event listings and academic resources rely on accurate information, so missing values need defined states.
4. **Reviewer evidence.** Final approval from every member should be tracked, particularly if someone has not yet personally confirmed a review.
5. **File placement.** The instructor requires files in each member's own GitHub repository/fork, and unrelated Project 1 or Project 2 files must remain intact.

## 6. Decisions

- Complete the three feature packages with matching personas, scenarios, and user stories.
- Keep responsibility with the originally assigned member for each package.
- Expand each story with testable acceptance criteria.
- Review text for spelling, clarity, and correct Markdown structure.
- Maintain a six-column Sprint 3 backlog and individual meeting records.
- Prepare for a final review on October 19, while keeping repository upload as a separate action.

## 7. Product Backlog After Meeting 2

*Statuses describe documentation progress at this review point; an item marked “In review” is not a confirmed approval.*

| PBI | Status | Sprint | Estimate | Assigned | Reviewer |
| --- | --- | --- | --- | --- | --- |
| F1 — Specify Academic Resources feature | Revised / in review | 3 | 3 hours | Demetric Noble | Justin Williams |
| F2 — Specify Campus Event Listings feature | Draft / in review | 3 | 3 hours | Javian Mack | Demetric Noble |
| F3 — Specify Upcoming Event Notifications feature | Draft / in review | 3 | 3 hours | Justin Williams | Javian Mack |
| P1 — Develop academic-support persona (Marcus) | Revised / in review | 3 | 1 hour | Demetric Noble | Justin Williams |
| P2 — Develop event-discovery persona (Jordan) | Draft / in review | 3 | 1 hour | Javian Mack | Demetric Noble |
| P3 — Develop event-reminder persona (Alex) | Draft / in review | 3 | 1 hour | Justin Williams | Javian Mack |
| S1 — Write tutoring-search scenario | Revised / in review | 3 | 1.5 hours | Demetric Noble | Justin Williams |
| S2 — Write event-discovery scenario | Draft / in review | 3 | 1.5 hours | Javian Mack | Demetric Noble |
| S3 — Write reminder scenario | Draft / in review | 3 | 1.5 hours | Justin Williams | Javian Mack |
| U1 — Write academic-resources user story | Revised / in review | 3 | 1 hour | Demetric Noble | Justin Williams |
| U2 — Write event-listings user story | Draft / in review | 3 | 1 hour | Javian Mack | Demetric Noble |
| U3 — Write event-notification user story | Draft / in review | 3 | 1 hour | Justin Williams | Javian Mack |
| D1 — Organize Project 3 Markdown and three minutes files | In progress | 3 | 2 hours | Demetric Noble | Group |
| G1 — Verify personal fork, commit, and push required files | Not started | 3 | 30 minutes | Each member | Group |

## 8. Tasks Before Meeting 3

- **Demetric:** Apply documentation and UI/UX corrections, ensure all four sections are present, make the backlog match Sprint 3, and prepare personal minutes for final review.
- **Javian:** Check event feature details and edge cases, verify his persona/scenario/story match the event package, and provide his review feedback.
- **Justin:** Check notification package content, confirm that assigned deliverables are accounted for, and organize the final review and GitHub preparation.
- **All members:** Bring final text to the next meeting, check every user story for role/action/reason, and identify any unresolved review or upload task.

**Next scheduled meeting:** October 19, 2026, 3:00 PM–5:00 PM.

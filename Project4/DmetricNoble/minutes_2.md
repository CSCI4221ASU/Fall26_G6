# Demetric Noble

# CampusConnect — Project 4 / Sprint 4 Meeting Minutes 2

**Course:** CSCI 4221 — Software Engineering  
**Group:** 6  
**Date:** October 26, 2026  
**Time:** 4:00 PM–6:00 PM  
**Attendees listed:** Demetric Noble, Javian Mack, Justine Williams  
**Minutes prepared by:** Demetric Noble  
**Product owners:** All Group 6 members  
**ScrumMaster:** Course instructor

## Team Roles and Component Ownership

| Member | Team role | Project 4 component | Assigned database table |
| --- | --- | --- | --- |
| Demetric Noble | UI/UX Designer and Documentation Lead | Academic Resources | `academic_resources` |
| Javian Mack | Technical Lead / Developer | Campus Event Listings | `events` |
| Justine Williams | Project Manager | Upcoming Event Notifications | `notifications` |


## Meeting Purpose

Use the second meeting for progress updates on each member's assigned architecture component and check how the component files and database tables will work together.

## Component Progress Review

### Demetric Noble — Academic Resources

Demetric's scope covers the student-facing Academic Resources design, resource search or category filtering, resource cards, a proposed `GET /api/resources` endpoint, and the `academic_resources` table. The architecture document identifies the React page, API client, backend route, service layer, and SQL migration as planned files.

**Review focus:** Keep the interface consistent with the Figma prototype and make clear that displaying information about tutoring is not the same as implementing appointment booking.

### Javian Mack — Campus Event Listings

Javian's scope covers the campus event listing and detail views, backend API routes, event service/data access, and the `events` table. The module needs event titles, descriptions, dates, times, and locations to support the existing Project 3 feature requirements.

**Review focus:** Determine how the events API returns upcoming events, handles missing information, and communicates with the shared database.

### Justine Williams — Upcoming Event Notifications

Justine's scope covers the notifications display, event reminder records, read/unread states, API routes, and the `notifications` table. As Project Manager, Justine also tracks ownership and the remaining Sprint 4 documentation requirements.

**Review focus:** Explain how notification records may reference events and distinguish an architectural plan from a working push-notification system.

## Shared Architecture and Figma Review

The proposed application remains **cloud-based and three-tier**: a frontend container, an API container, and a shared PostgreSQL data tier. Database credentials belong in secure backend configuration, not in the browser or repository. Each major feature should have its own logical module, while the database connection and API infrastructure are shared.

**Figma status:** The CampusConnect prototype was subsequently reported updated. The precise date of the edits was not provided, so this document does not claim that the changes were completed on October 26. The latest Figma layout is the intended visual reference.

## Product Backlog

| PBI | Status | Sprint | Estimate | Assigned | Reviewer |
| --- | --- | --- | --- | --- | --- |
| Container and three-tier architecture explanation | Documentation in progress | 4 | 2 hours | Demetric Noble | Javian Mack |
| Academic Resources component and file plan | Documentation in progress | 4 | 3 hours | Demetric Noble | Javian Mack |
| `academic_resources` table design | Documentation in progress | 4 | 2 hours | Demetric Noble | Javian Mack |
| Events component and `events` table | Review item for Javian | 4 | 4 hours | Javian Mack | Justine Williams |
| Notifications component and `notifications` table | Review item for Justine | 4 | 4 hours | Justine Williams | Demetric Noble |
| Individual minutes and repository preparation | In progress | 4 | 2 hours each | Each member | Group 6 |

## Outcome and Next Steps

The second meeting focuses on aligning the component specifications, file lists, and table designs with the same proposed architecture. Before final submission, each person needs to check their own component specifications and prepare their Markdown documents for peer review.

**Next meeting:** October 28, 2026, 3:00–5:00 PM.

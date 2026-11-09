Javian Mack
# Project 4 — Group 6 Meeting 2 Record
**Project:** CampusConnect — Architecture (Sprint 4)
**Recorder:** Javian Mack
**Meeting period reported by Javian:** October 23–26, 2026  
**Exact date and time for this meeting:** [Confirm]
**Location/platform:** [Confirm]
**Attendance:** [Record actual attendees]
**Meeting occurrence:** User reports Group 6 held three meetings during October 23–26, 2026. Specific meeting date, attendance and decisions still require confirmation.

## Meeting 2 — Component structure, files and database
### Prepared discussion notes
1. Event Listings (Javian): Event list, cards, detail pages, Events API and database repository. Proposed files include EventsPage.tsx, EventCard.tsx, events.ts route, and eventsRepository.ts.
2. Academic Resources (Demetric): resource categories, cards, details, Resources API and resource repository. Proposed files include ResourcesPage.tsx, ResourceCard.tsx, resources.ts route.
3. Notifications (Justine): reminder preferences, notification cards, Notifications API, and potential background reminder worker. Proposed files include NotificationsPage.tsx, NotificationCard.tsx, notifications.ts route.
4. Database design: one shared PostgreSQL database rather than a different local database per user; events, academic_resources, notifications, and supporting users tables. notifications.event_id and notifications.user_id reference event and user records.

### Product Backlog Items
| PBI | Status | Sprint | Estimate | Assigned | Reviewer |
| --- | --- | --- | --- | --- | --- |
| Cloud architecture and container description | Drafted, pending review | 4 | 1 day | Javian Mack | Demetric Noble |
| Event Listings component and events table | Drafted, pending review | 4 | 2 days | Javian Mack | Justine Williams |
| Academic Resources component and resources table | Proposed | 4 | 2 days | Demetric Noble | Javian Mack |
| Notification component and notifications table | Proposed | 4 | 2 days | Justine Williams | Demetric Noble |
| Integration and schema review | Proposed | 4 | 1 day | All members | All members |
| Three meeting records and repository submission | In progress | 4 | 3 meetings | All members | All members |

### Assigned follow-up actions (proposed, not yet approved)
- Each member: check their proposed component's file list and table columns.
- Javian: review event start/end times, status and location handling.
- All members: review table relationships and verify proposed responsibilities.

### Actual meeting details — verify against meeting recollections
- **What members actually discussed:** [Enter discussion summary]
- **Progress reported by Javian:** [Enter]
- **Progress reported by Demetric:** [Enter]
- **Progress reported by Justine:** [Enter]
- **Decisions approved by those present:** [Enter]
- **Blockers:** [Enter]
- **Next meeting date/time:** [Enter]

**Verification note:** Javian reports that the meetings occurred during October 23–26, 2026. Prepared discussion notes are not a verified transcript, and attendance, exact date/time, progress reports, and decisions must be confirmed before these records are presented as finalized minutes.
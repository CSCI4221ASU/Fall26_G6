Javian Mack
# Project 4 — Group 6 Meeting 3 Record
**Project:** CampusConnect — Architecture (Sprint 4)
**Recorder:** Javian Mack
**Meeting period reported by Javian:** October 23–26, 2026  
**Exact date and time for this meeting:** [Confirm]
**Location/platform:** [Confirm]
**Attendance:** [Record actual attendees]
**Meeting occurrence:** User reports Group 6 held three meetings during October 23–26, 2026. Specific meeting date, attendance and decisions still require confirmation.

## Meeting 3 — Containers, integration and sprint review
### Prepared discussion notes
1. Frontend container contains a compiled web application and serving configuration; backend container contains the Node.js runtime, API routes, controllers, database code, and dependencies. Database files persist outside ephemeral application containers.
2. Proposed data flow: browser → HTTPS frontend → Express REST API → shared PostgreSQL database. Future notification jobs may run in a separate worker.
3. Security planning: HTTPS, authorized writes, safe parameterized queries, private per-user notifications, protected credentials, database backups, and persistent storage.
4. Review requested before submission: ensure architecture documentation, each member's component and table descriptions, and three authentic meeting records appear in each personal repository.

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
- All members: review architecture and note corrections.
- Each member: document actual meeting outcomes and progress.
- Each member: submit their own GitHub repository link through GeorgiaVIEW.

### Actual meeting details — verify against meeting recollections
- **What members actually discussed:** [Enter discussion summary]
- **Progress reported by Javian:** [Enter]
- **Progress reported by Demetric:** [Enter]
- **Progress reported by Justine:** [Enter]
- **Decisions approved by those present:** [Enter]
- **Blockers:** [Enter]
- **Next meeting date/time:** [Enter]

**Verification note:** Javian reports that the meetings occurred during October 23–26, 2026. Prepared discussion notes are not a verified transcript, and attendance, exact date/time, progress reports, and decisions must be confirmed before these records are presented as finalized minutes.
Justin Williams

# Project 4 – Meeting 2 Minutes

**Date:** October 26, 2026  
**Meeting Time:** 4:00 PM–6:00 PM  
**Members Present:** Justin Williams, Javian Mack, and Demetric Noble

## Topics Discussed

- Each member gave an update on their assigned component.
- Discussed the responsibilities and sub-components of each major service.
- Reviewed the files required inside each service container.
- Discussed how the components will communicate through APIs.
- Decided that CampusConnect will use a shared PostgreSQL database.
- Reviewed how database tables will be connected using primary and foreign keys.
- Discussed what should and should not be stored inside a Docker image.

## Work Completed

- Justin completed a draft of the Notification Service description.
- Javian completed a draft of the Event Management Service description.
- Demetric completed a draft of the Academic Resources Service description.
- The group identified the major database tables used by the components.
- The group agreed that passwords and other secrets should be provided through secure environment variables rather than stored in container images.

## Problems or Questions

- The group needed to make sure each component had a separate and clear responsibility.
- The group discussed how the services could share data without creating unnecessary dependencies.
- Each member needed to confirm that their table contained an appropriate primary key and related foreign keys.

## Tasks Assigned

- Justin will complete the Notification Service files and `Notifications` table.
- Javian will complete the Event Management Service files and `Events` table.
- Demetric will complete the Academic Resources Service files and `AcademicResources` table.
- Each member will review their Markdown formatting.
- The group will perform a final architecture review during Meeting 3.

## Product Backlog

| PBI | Status | Sprint | Estimate | Assigned | Reviewer |
|---|---|---|---|---|---|
| Design Notification Service | In Progress | Sprint 4 | 2 hours | Justin Williams | Javian Mack |
| Design Event Management Service | In Progress | Sprint 4 | 2 hours | Javian Mack | Demetric Noble |
| Design Academic Resources Service | In Progress | Sprint 4 | 2 hours | Demetric Noble | Justin Williams |
| Define database table structures | In Progress | Sprint 4 | 1 hour | Each Member | Group |
| Review necessary container files | Completed | Sprint 4 | 1 hour | Group | Group |
| Review Project 4 architecture | Not Started | Sprint 4 | 1 hour | Group | Group |
| Write Meeting 2 minutes | Completed | Sprint 4 | 30 minutes | Justin Williams | Demetric Noble |
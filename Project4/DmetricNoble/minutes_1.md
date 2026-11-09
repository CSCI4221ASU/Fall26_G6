# Demetric Noble

# CampusConnect — Project 4 / Sprint 4 Meeting Minutes 1

**Course:** CSCI 4221 — Software Engineering  
**Group:** 6  
**Date:** October 23, 2026  
**Time:** 3:00 PM–5:00 PM  
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

>

## Meeting Purpose

Start Sprint 4 by reviewing the architecture assignment, discussing cloud-based software, and distributing the three CampusConnect components across the team.

## Meeting Discussion

### Understanding the architecture

Software architecture describes how an application is organized and how its parts exchange information. The styles reviewed for the design include layered (three-tier), microservices, and event-driven architecture. CampusConnect's **proposed** choice is a three-tier system with a React frontend, a Node.js API, and a shared PostgreSQL database.

A cloud-based application runs on infrastructure accessible over a network. Docker helps package software into consistent environments. An **image** defines the application package, a **container** is a running instance of that image, and the Docker **daemon** manages images and containers on the host.

### Major components and subcomponents

| Component | Main subcomponents | Primary owner |
| --- | --- | --- |
| Academic Resources | Resources page, category filter, resource cards, API route, database queries | Demetric |
| Campus Event Listings | Event list, event details, API route, database queries | Javian |
| Upcoming Event Notifications | Notification view, reminder/status logic, API route, database queries | Justine |

The design uses **one shared cloud database**, not a separate database on each student's computer. The frontend and API can be packaged in separate Docker containers. The database should remain a separate managed service or development container with persistent storage.

## Team Assignments

**Demetric Noble — UI/UX Designer and Documentation Lead:** Outline the Academic Resources interface and its relation to the updated Figma design, identify component and API files, draft the cloud/container description, and define the `academic_resources` table.

**Javian Mack — Technical Lead / Developer:** Describe the Campus Event Listings module, event API/backend interaction, required technical files, and `events` table.

**Justine Williams — Project Manager:** Describe the Upcoming Event Notifications module and `notifications` table, maintain the sprint task plan, and coordinate team review.

Each member is also responsible for individual minutes and an architecture Markdown document in their own repository.

## Product Backlog

| PBI | Status | Sprint | Estimate | Assigned | Reviewer |
| --- | --- | --- | --- | --- | --- |
| Draft container and three-tier architecture description | Assigned | 4 | 2 hours | Demetric Noble | Javian Mack |
| Specify Academic Resources component and its required files | Assigned | 4 | 3 hours | Demetric Noble | Javian Mack |
| Draft `academic_resources` table structure | Assigned | 4 | 2 hours | Demetric Noble | Javian Mack |
| Specify Campus Events component and `events` table | Assigned | 4 | 4 hours | Javian Mack | Justine Williams |
| Specify Notifications component and `notifications` table | Assigned | 4 | 4 hours | Justine Williams | Demetric Noble |
| Create individual meeting minutes | Assigned | 4 | 2 hours each | Each member | Group 6 |

## Meeting Outcome and Next Steps

The component responsibilities were divided among the three existing Project 3 feature owners. The team would next review file requirements, database fields, and how each component fits the shared cloud architecture.

**Next meeting:** October 26, 2026, 4:00–6:00 PM.

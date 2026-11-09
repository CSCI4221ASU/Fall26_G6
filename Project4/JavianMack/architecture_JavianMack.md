# Project 4: CampusConnect Architecture
**Prepared by:** Javian Mack  
**Group:** 6  
**Course:** CSCI 4221 Software Engineering  
**Sprint:** 4  
**Status:** Proposed design; review and implementation pending

## Section 1: Description of Our Containers
CampusConnect is a proposed cloud-based application that helps Albany State University students find campus events, academic resources, and event notifications. We propose a three-tier architecture consisting of a React/TypeScript frontend, Node.js/Express backend, and shared PostgreSQL database. This is an architectural proposal, not a claim that a deployed system already exists.

Architecture is the high-level organization of a system, defining components, their responsibilities, and their interactions. Three common architectural templates are layered/three-tier, client-server, and microservices. CampusConnect will use a three-tier client-server approach, which separates the user interface, application logic, and persistence.

Cloud-based software is hosted on network-accessible servers and accessed through the Internet. Docker is a platform for packaging software and dependencies in containers. A container is a running, isolated application environment. A Docker image is the reusable template used to start containers. The Docker daemon (dockerd) is the background service that manages images, containers, and networks.

**Proposed containers and services:**
- Frontend container: compiled React/TypeScript/Vite HTML, JavaScript, CSS, assets, and web-server configuration (for example, Nginx).
- Backend container: Node.js runtime, Express REST API, application logic, validation, and database access code.
- Shared PostgreSQL service: persistent database storage, preferably hosted as a managed cloud database; a separate PostgreSQL container with a persistent volume is an option for development.
- Optional future worker: process scheduled notifications in a separate worker container.
- HTTPS reverse proxy/load balancer: handles encrypted browser traffic. Environment variables and a secrets manager hold credentials; secrets are not checked into the repository.

**Data flow:** Student browser → HTTPS frontend → REST API backend → shared PostgreSQL database. Event reminders may be scheduled by a future worker that reads events and creates notifications. Real push or email delivery is not assumed implemented.

**Database choice:** One shared cloud database, not an individual local database on each student's device. Components access data only through backend routes, using parameterized queries, access controls, and validation. Database storage persists independently from short-lived containers.

## Section 2: Components and Necessary Files

### Component 1: Campus Event Listings — Javian Mack
**Purpose:** Students browse upcoming campus activities and open event details.
**Subcomponents:** EventsPage, EventCard, EventDetailsPage, Events API, Events Controller, Events Repository.
**Database usage:** The Events API reads the shared `events` table; future administrative routes may write validated and authorized event records.
**Proposed files (not yet verified as implemented):**
- `frontend/src/pages/EventsPage.tsx` — show upcoming event list.
- `frontend/src/components/EventCard.tsx` — title, time, location preview.
- `frontend/src/pages/EventDetailsPage.tsx` — full event detail.
- `frontend/src/services/eventsApi.ts` — frontend API calls.
- `backend/src/routes/events.ts` — `GET /api/events` and `GET /api/events/:id`.
- `backend/src/controllers/eventsController.ts` — validate requests and return results.
- `backend/src/repositories/eventsRepository.ts` — parameterized database queries.
- `backend/src/db.ts` — shared database connection pool.
- `database/schema.sql` — proposed SQL schema.
- `frontend/Dockerfile`, `backend/Dockerfile`, `docker-compose.yml` — proposed deployment files.
**Example:** A student opens Campus Events → browser requests `/api/events` → backend reads upcoming `events` records → browser shows event cards → student opens a detail page.

### Component 2: Academic Resources — Demetric Noble
**Purpose:** Present tutoring, advising, and other academic-support information.
**Subcomponents:** ResourcesPage, ResourceCard, category filter, Resources API, Resources Repository.
**Database usage:** Reads the shared `academic_resources` table with titles, categories, descriptions, instructions, and optional resource links.
**Proposed files:** `frontend/src/pages/ResourcesPage.tsx`, `frontend/src/components/ResourceCard.tsx`, `frontend/src/services/resourcesApi.ts`, `backend/src/routes/resources.ts`, `backend/src/controllers/resourcesController.ts`, `backend/src/repositories/resourcesRepository.ts`.

### Component 3: Upcoming Event Notifications — Justine Williams
**Purpose:** Provide event-specific reminders to interested students.
**Subcomponents:** Notification List, Notification Card, Reminder Preference, Notifications API, optional Reminder Worker.
**Database usage:** Reads and writes `notifications`, relating each reminder to an event and an authenticated student. Cancelled events require reminder updates.
**Proposed files:** `frontend/src/pages/NotificationsPage.tsx`, `frontend/src/components/NotificationCard.tsx`, `frontend/src/services/notificationsApi.ts`, `backend/src/routes/notifications.ts`, `backend/src/controllers/notificationsController.ts`, `backend/src/repositories/notificationsRepository.ts`, `backend/src/workers/reminderWorker.ts` (future).

**Security and operations:** Use HTTPS, authenticated access to private notifications, authorized edits, parameterized SQL, safe logging, persistent storage, and backup procedures. Do not store database passwords in images or GitHub. Do not imply prototype notifications are already delivered.

## Section 3: Structure of Related Database Tables
Tables below are proposed PostgreSQL structures. Javian's assigned table is `events`; other tables show the complete Group 6 design.

### Table: events — Javian Mack
| Field | Type | Constraint | Meaning |
| --- | --- | --- | --- |
| event_id | BIGINT identity | Primary key | Unique event |
| title | VARCHAR(150) | NOT NULL | Event title |
| description | TEXT | Optional | Details |
| start_time | TIMESTAMPTZ | NOT NULL | Start time and date |
| end_time | TIMESTAMPTZ | Optional; after start | End time |
| location | VARCHAR(200) | Optional | Campus location |
| organizer | VARCHAR(150) | Optional | Host organization |
| status | VARCHAR(20) | scheduled/cancelled | Event status |
| created_at | TIMESTAMPTZ | DEFAULT NOW() | Creation time |

### Table: academic_resources — Demetric Noble
| Field | Type | Constraint | Meaning |
| --- | --- | --- | --- |
| resource_id | BIGINT identity | Primary key | Resource ID |
| title | VARCHAR(150) | NOT NULL | Resource title |
| category | VARCHAR(80) | NOT NULL | Type of support |
| description | TEXT | NOT NULL | Explanation |
| access_instructions | TEXT | Optional | How to access |
| website_url | TEXT | Optional | Verified link |
| is_active | BOOLEAN | DEFAULT TRUE | Listing visibility |
| updated_at | TIMESTAMPTZ | DEFAULT NOW() | Last update |

### Table: notifications — Justine Williams
| Field | Type | Constraint | Meaning |
| --- | --- | --- | --- |
| notification_id | BIGINT identity | Primary key | Notification ID |
| user_id | BIGINT | Foreign key to users | Recipient |
| event_id | BIGINT | Foreign key to events | Referenced event |
| message | TEXT | NOT NULL | Reminder text |
| scheduled_for | TIMESTAMPTZ | NOT NULL | Planned reminder time |
| is_read | BOOLEAN | DEFAULT FALSE | Read state |
| delivery_status | VARCHAR(20) | pending/sent/cancelled | Delivery status |
| created_at | TIMESTAMPTZ | DEFAULT NOW() | Creation time |

### Supporting table: users
| Field | Type | Constraint | Meaning |
| --- | --- | --- | --- |
| user_id | BIGINT identity | Primary key | User ID |
| display_name | VARCHAR(100) | NOT NULL | Display name |
| email | VARCHAR(254) | NOT NULL UNIQUE | Email |
| created_at | TIMESTAMPTZ | DEFAULT NOW() | Creation time |

**Relationships:** Each notification belongs to one event and one user. Each event can have multiple notifications. The application must confirm a student's identity before showing their private notifications.

## Sprint 4 Product Backlog (proposed; team approval required)
| PBI | Status | Sprint | Estimate | Assigned | Reviewer |
| --- | --- | --- | --- | --- | --- |
| Design three-tier cloud container architecture | Drafted | 4 | 1 day | Javian Mack | Demetric Noble |
| Document Events component and events schema | Drafted | 4 | 2 days | Javian Mack | Justine Williams |
| Document Academic Resources component and schema | Proposed | 4 | 2 days | Demetric Noble | Javian Mack |
| Document Notifications component and schema | Proposed | 4 | 2 days | Justine Williams | Demetric Noble |
| Review integration and shared database | Proposed | 4 | 1 day | All members | All members |
| Conduct three meetings and record minutes individually | Not yet verified | 4 | 3 meetings | All members | All members |
| Commit files and submit GitHub link | Pending | 4 | 1 day | Each member | Instructor |

**Review note:** The responsibilities above reflect the existing Group 6 Project 3 feature division. The team should confirm the plan and update statuses. This document describes intended architecture, not a finished deployment.
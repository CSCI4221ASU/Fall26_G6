# CampusConnect — Project 3: Features, Personas, Scenarios, and User Stories

**Prepared by:** Demetric Noble  
**Course:** CSCI 4221 — Software Engineering  
**Group:** 6  
**Sprint:** 3 (Project 3)  
**My role:** UI/UX Designer and Documentation Lead  
**Product owners:** All Group 6 members  
**ScrumMaster:** Course instructor

## Product Vision and Project Scope

CampusConnect is a proposed single place for Albany State University students to find campus events, student-organization activities, academic resources, and relevant opportunities. The project responds to a common student problem: important information can be spread across several websites, emails, and announcements. Our goal is to make that information easier to find and act on through clear navigation and a student-friendly interface.

Project 3 describes **three basic feature packages, three personas, three usage scenarios, and three user stories**, one of each assigned to every teammate. These specifications guide the prototype and subsequent development; a written acceptance criterion is a testable requirement, not a claim that every backend function has already been implemented.

| Member | Team responsibility | Project 3 feature package |
| --- | --- | --- |
| **Demetric Noble** | UI/UX Designer and Documentation Lead | Academic Resources |
| **Javian Mack** | Technical Lead / Developer | Campus Event Listings |
| **Justin Williams** | Project Manager | Upcoming Event Notifications |

> 

## Section 1 — Features

### Feature 1: Academic Resources — Demetric Noble

**Purpose.** Give students a convenient path to academic support services without searching multiple university pages. The interface should prioritize a simple layout, descriptive labels, and clear actions.

**Intended functions**

1. Display an **Academic Resources** section from CampusConnect's primary navigation.
2. Present resource categories such as tutoring, academic advising, study support, and university learning services.
3. Display a short description for each available service and a clear link or instruction for accessing it.
4. Make essential information readable on both desktop and smaller screens.
5. Provide an understandable empty state if a resource category has no entries.

**Example interaction.** A student selects **Academic Resources**, locates a tutoring entry, reads what it offers, and uses its listed link or instructions to get help.

**Acceptance criteria**

- A student can locate Academic Resources from the main navigation without needing instructions.
- Each resource item has a descriptive title and a clear purpose.
- A student can identify how to access a service when that information is available.
- Navigation labels and content remain readable and understandable.
- The experience does not mislead students into believing tutoring is booked through CampusConnect unless booking has actually been implemented.

**My contribution.** I designed the proposed structure and user journey, identified key labels and content categories, checked the layout against our Figma direction, and maintained written specifications, stories, and meeting documentation. My emphasis was making a technically feasible feature understandable to students.

### Feature 2: Campus Event Listings — Javian Mack

**Purpose.** Help students discover campus activities in one place instead of relying only on scattered announcements.

**Intended functions**

1. Display a list of upcoming events in a consistent card or list layout.
2. Include event title, date, time, location, and description where known.
3. Allow a student to open an event for details.
4. Distinguish future events from past events, so information is not misleading.
5. Provide a helpful message when there are no listed events.

**Acceptance criteria**

- A student can find the event listings entry point.
- Each populated event has a recognizable title and enough information to decide whether to attend.
- Opening an event reveals available details without losing navigation context.
- The layout is usable on smaller screens.

**Responsibility.** Javian owns the event-listings feature package and the associated technical planning and troubleshooting. This is the agreed division of responsibility; his individual final approval remains to be confirmed.

### Feature 3: Upcoming Event Notifications — Justin Williams

**Purpose.** Help students remember campus activities they are interested in.

**Intended functions**

1. Allow the student to identify an upcoming event of interest.
2. Show a visible reminder or notification concept connected to that event.
3. Make the relevant event name and time understandable in the reminder.
4. Offer a clear way to view the full event listing from the reminder.
5. Define appropriate handling when an event is canceled or its time changes.

**Acceptance criteria**

- A student understands which event a reminder concerns.
- The notification concept communicates date or time clearly.
- A student can navigate from reminder information to event details when that interaction is available.
- Mock notifications are labeled as prototype content until real delivery is implemented.

**Responsibility.** Justin owns notification-feature planning and related project coordination, task tracking, and meeting organization.

## Section 2 — Personas

*The following personas are illustrative student profiles for design and testing, not real student records.*

### Persona 1: Marcus Johnson — Academic Support Seeker (Demetric)

- **Background:** Sophomore at Albany State University enrolled in several challenging courses.
- **Digital habits:** Comfortable using a smartphone, learning-management tools, and web applications.
- **Goal:** Find appropriate tutoring or study assistance quickly, especially before an exam.
- **Frustration:** Resources are spread across websites and announcements; descriptions are sometimes vague.
- **Needs:** Easy-to-find academic categories, plain-language descriptions, and reliable next steps.
- **Accessibility/design considerations:** Clear headings, readable contrast, obvious links, and minimal navigation steps.
- **Success measure:** Marcus finds a relevant support service and understands how to access it without asking another person where to look.

**Design implication.** Academic Resources should favor familiar terms such as “Tutoring” and “Advising” and make the pathway to the service visible immediately.

### Persona 2: Jordan Lee — Campus Event Explorer (Javian)

- **Background:** First-year student who wants to connect with classmates and student organizations.
- **Digital habits:** Regularly checks apps and social media for announcements.
- **Goal:** Discover relevant campus activities and get clear event details before making plans.
- **Frustration:** Flyers may omit locations or conflict with newer information.
- **Needs:** A consistent event list with titles, dates, locations, and concise descriptions.
- **Success measure:** Jordan finds an appealing event and knows when and where it occurs.

**Design implication.** Event cards should surface time and location rather than hiding this information behind several clicks.

### Persona 3: Alex Carter — Busy Student Planner (Justin)

- **Background:** Commuter student balancing classes, campus activities, and part-time work.
- **Digital habits:** Uses a phone calendar and checks reminders between commitments.
- **Goal:** Remember upcoming events without repeatedly searching for the original announcement.
- **Frustration:** Events are easy to forget when the week is busy or schedules change.
- **Needs:** Clearly associated event reminders with understandable times and next actions.
- **Success measure:** Alex can recognize an upcoming event and return to its details when planning the day.

**Design implication.** Notification messages should contain useful event context, not only generic text such as “Upcoming event.”

## Section 3 — Scenarios

### Scenario 1: Finding Tutoring Before an Exam (Demetric)

**Context.** Marcus has an upcoming mathematics exam and realizes he needs additional support.

1. Marcus opens CampusConnect and looks at the main navigation.
2. He selects **Academic Resources** because the label directly matches his goal.
3. He examines categories and chooses **Tutoring** or another relevant study-support option.
4. He reads the resource description to confirm that it may help with his course.
5. He follows the provided access instructions or link to learn how to request assistance.

**Expected outcome:** Marcus identifies a useful support option without having to search multiple unrelated university pages. The scenario ends at locating/accessing resource information; it does not assume CampusConnect has its own appointment-booking system.

**Possible exception:** If no tutoring listing is available, the interface explains that no entry is currently listed rather than showing a broken or blank page.

### Scenario 2: Discovering a Campus Event (Javian)

**Context.** Jordan wants to participate in campus life but is unsure which activities are coming up.

1. Jordan opens CampusConnect and selects **Campus Events**.
2. The app shows upcoming events with essential details.
3. Jordan scans several events and opens one that sounds interesting.
4. Jordan reviews its description, scheduled time, and location.
5. Jordan uses this information to decide whether the event fits the day's schedule.

**Expected outcome:** Jordan finds an activity and has sufficient details to plan attendance.

**Possible exception:** If an event lacks a verified location, the listing should indicate that the location has not yet been provided instead of inventing one.

### Scenario 3: Remembering a Campus Activity (Justin)

**Context.** Alex notices an event but may forget it during a busy school week.

1. Alex sees an event of interest in CampusConnect.
2. Alex identifies the reminder or notification option associated with the event.
3. The system shows the reminder concept with event-specific information.
4. Before the event, Alex views the relevant notification or prototype reminder.
5. Alex returns to the event details to confirm the schedule.

**Expected outcome:** Alex has enough context to recognize and act on the event reminder.

**Possible exception:** If a real reminder service has not been implemented, the prototype demonstrates the proposed screen and message without claiming that a push notification has been delivered.

## Section 4 — User Stories

### User Story 1: Academic Resources (Demetric)

> **As a** college student who needs academic help, **I want to** find tutoring and other academic resources through CampusConnect, **so that** I can get support for my coursework without searching multiple websites.

**Priority:** High  
**Owner:** Demetric Noble  
**Acceptance checks:**

1. **Given** the CampusConnect navigation, **when** I select Academic Resources, **then** I see understandable resource categories.
2. **Given** a resource entry, **when** I read its listing, **then** I can understand what it provides.
3. **Given** a resource with access information, **when** I select its action, **then** I can reach or understand the next step for obtaining help.
4. **Given** no available entries in a category, **when** I open it, **then** I see a clear explanatory message.

### User Story 2: Campus Event Listings (Javian)

> **As a** student interested in campus activities, **I want to** browse upcoming events and view their details, **so that** I can choose opportunities that fit my interests and schedule.

**Priority:** High  
**Owner:** Javian Mack  
**Acceptance checks:**

1. **Given** the main navigation, **when** I select Campus Events, **then** I can view the available upcoming event listings.
2. **Given** an event listing, **when** I open it, **then** I can see its available date, time, location, and description.
3. **Given** no upcoming events, **when** I open the list, **then** the interface states that no events are currently listed.

### User Story 3: Upcoming Event Notifications (Justin)

> **As a** busy student, **I want to** see reminders about campus events I am interested in, **so that** I can plan ahead and avoid missing activities.

**Priority:** Medium  
**Owner:** Justin Williams  
**Acceptance checks:**

1. **Given** an event I am following, **when** I view its reminder, **then** the reminder identifies the event.
2. **Given** a reminder, **when** I read it, **then** I can identify when the event is scheduled.
3. **Given** a reminder with a details action, **when** I select the action, **then** I can return to the event information.

## Sprint 3 Documentation and Validation Notes

- The group used its existing **CampusConnect** vision from Project 1; Project 3 does not introduce a different product.
- The three feature/persona/scenario/story packages above are the **Project 3 specifications** and are divided one per team member.
- Figma layouts and a local React/TypeScript/Vite project provide a technical starting point. The local development server and login-screen rendering were observed; full visual styling and production-ready functions should be verified separately rather than assumed complete.
- Demetric's documentation review is **confirmed**. Justin's review is **confirmed** by his shared Meeting 3 record. Javian's individual review remains **pending confirmation**.
- Weekly meeting records and the Sprint 3 product backlog are documented separately in `minutes_1.md`, `minutes_2.md`, and `minutes_3.md`.
- The final GitHub commit/push and GeorgiaVIEW link submission are separate actions; drafting these files does not mean those actions have occurred.

Justin Williams

# Project 4 – CampusConnect Software Architecture

## Section 1: Description of the Container

CampusConnect will be developed as cloud-based software using a service-oriented architecture. The system will contain separate services for major features, including event management, academic resources, and notifications. These services will communicate through APIs and use a shared cloud database.

My assigned component is the Notification Service. It will run inside a Docker container in the cloud. The container will provide an isolated environment containing the application code, Node.js runtime, required dependencies, configuration references, and files needed to operate the notification feature.

The Docker image will serve as the template used to create the container. The Docker daemon will manage the image and run the container. Because the service is containerized, it can be deployed consistently and restarted or replicated when additional capacity is needed.

The Notification Service container will receive requests from CampusConnect, retrieve notification information from the shared database, schedule reminders, and send notifications to users. Sensitive information such as database passwords will not be stored directly inside the image. It will be supplied through secure environment variables when the container runs.

## Section 2: Component, Database Usage, and Necessary Files

### Assigned Component: Notification Service

The Notification Service is responsible for managing reminders and alerts for CampusConnect users. Students can enable notifications for campus events, academic deadlines, organization announcements, and other campus activities.

The component will perform the following tasks:

- Create notifications for users.
- Schedule notifications for upcoming events.
- Retrieve pending notifications from the database.
- Send reminders at the correct time.
- Update the status of notifications after they are sent.
- Allow users to enable or disable selected notifications.
- Communicate with the Event Management Service through an API.
- Record notification activity for troubleshooting and review.

### Database Usage

The Notification Service will use the shared CampusConnect PostgreSQL database. A shared database is appropriate because event, user, and notification information are related. The service will read event and user identifiers while creating and delivering notifications.

The component will have permission to create, read, and update records in the `Notifications` table. Foreign keys will connect notification records to the appropriate users and events. Database transactions will help prevent incomplete or inconsistent updates.

### Necessary Files

| File | Purpose |
|---|---|
| `notification_service.js` | Contains the main notification scheduling and delivery logic. |
| `notification_routes.js` | Defines the API routes used to create, view, update, and delete notifications. |
| `notification_controller.js` | Processes requests and connects the API routes to the service logic. |
| `notification_model.js` | Defines how notification data is represented and accessed. |
| `database.js` | Creates the connection to the shared PostgreSQL database. |
| `package.json` | Lists the Node.js dependencies and startup commands. |
| `Dockerfile` | Contains the instructions used to build the Docker image. |
| `.dockerignore` | Prevents unnecessary files from being copied into the image. |
| `.env.example` | Shows which environment variables are required without exposing passwords. |

## Section 3: Structure of the Related Database Table

The Notification Service will primarily use a table named `Notifications`.

### Notifications Table

| Column | Data Type | Key or Constraint | Purpose |
|---|---|---|---|
| `notification_id` | INTEGER | Primary Key, Auto Increment | Uniquely identifies each notification. |
| `user_id` | INTEGER | Foreign Key, Not Null | Identifies the user receiving the notification. |
| `event_id` | INTEGER | Foreign Key, Nullable | Connects the notification to a campus event when applicable. |
| `message` | VARCHAR(500) | Not Null | Stores the message shown to the user. |
| `notification_type` | VARCHAR(50) | Not Null | Identifies the notification as an event, academic, or organization alert. |
| `scheduled_at` | TIMESTAMP | Not Null | Stores when the notification should be delivered. |
| `sent_at` | TIMESTAMP | Nullable | Records when the notification was actually sent. |
| `status` | VARCHAR(20) | Not Null | Stores a value such as Pending, Sent, Failed, or Cancelled. |
| `created_at` | TIMESTAMP | Default Current Timestamp | Records when the notification was created. |

The `user_id` field will connect to the Users table, while `event_id` can connect to the Events table. The `event_id` field is optional because some notifications may concern academic resources or general announcements rather than campus events.
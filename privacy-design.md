# Privacy design

Family logistics data can reveal a child's identity, school, activities, transportation, locations, and daily routine. The privacy goal is therefore not merely to encrypt a large profile; it is to avoid creating that profile when the product does not need it.

## Principles

### 1. Parent-controlled inputs

The parent chooses which schedules to upload and which messages to forward. The prototype does not request broad access to a personal mailbox.

### 2. Human approval before schedule changes

Extraction produces a proposal—not an authoritative event. A parent can correct the type, title, child, date, time, source, and location before approval.

### 3. Minimum necessary retention

The useful output is usually a small structured object: event, task, date, time, location, source, and confidence. The local review queue does not need a permanent archive of the original communication.

### 4. Local-first storage

Approved dashboard information remains in the parent's browser. There is no separate application cloud database in the current prototype.

### 5. No third-party AI model in the current version

The current prototype uses deterministic local extraction. It does not send family communications or child data to an external AI model.

### 6. Accurate claims

Local-first does not mean fully offline. Forwarded messages remain in the dedicated Gmail account. Public descriptions should state this boundary rather than claiming that the data never touches a cloud service.

## Data retained locally

- Parent-approved events and tasks
- Child label selected by the parent
- Date, time, location, source, and notes
- A minimal activity history
- Pending structured review items

## Data excluded from the public case study

- Real child or caregiver names
- Real schools, teams, studios, or tutors
- Real locations, routes, and schedules
- Email addresses and inbox screenshots
- Credentials, tokens, passwords, and configuration
- Working application source code


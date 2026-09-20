# Lightweight threat model

This document describes product risks and mitigations for a personal prototype. It is not a claim of formal security certification.

| Risk | Why it matters | Current mitigation | Remaining limitation |
|---|---|---|---|
| Broad mailbox access | Could expose unrelated personal communications | Dedicated inbox and parent-selected forwarding | Forwarding rules can be misconfigured |
| Over-retention | Creates a detailed archive of a child's life | Store structured schedule facts; do not retain message bodies in the review queue | Original forwarded messages remain in Gmail |
| Incorrect extraction | Wrong dates or times can disrupt pickup and activities | Parent review before approval | Human review can still miss errors |
| Unauthorized local access | Browser data can reveal routines and locations | Runs on the parent's computer; no public profile | Device and browser security remain the parent's responsibility |
| Accidental public disclosure | Screenshots can expose identities and routines | Independently generated fictional demo assets | Future contributors must preserve the same rule |
| Credential leakage | Inbox credentials could expose messages | Credentials are excluded from this repository and distributed packages | Authentication should move to OAuth before wider use |
| External model disclosure | Child data could be retained or processed outside the parent's control | No third-party AI model in the current prototype | Any future model integration requires a new privacy review |

## Before any wider release

- Replace password-based inbox access with OAuth and least-privilege scopes.
- Add explicit retention and deletion controls.
- Encrypt sensitive local state where practical.
- Add authentication if the dashboard becomes network-accessible.
- Conduct dependency, configuration, and secret scanning.
- Document vendor retention, training, and subprocessors before adding an external model.
- Obtain legal and privacy review before offering the system to other families or schools.


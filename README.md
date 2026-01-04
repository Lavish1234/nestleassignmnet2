# nestleassignmnet2
# observability and compliance across all Azure resources

## Current Challenges

* Inconsistent monitoring
* Each team manually enable azure monitor leading in gaps of logs and metrics
* Observability is not centralised
* Logs are spread across subscriptions and not retained uniformly
* Weak governance
* Naming standards not enforced
* Log retention varies by team
* Low scalability
* Onboarding new applications requires manual effort and rework
* Diagnostic settings optional

## Proposed High Level Architecture (HUB and Spoke Model)

<img width="864" height="831" alt="Screenshot 2026-01-05 at 12 58 23 AM" src="https://github.com/user-attachments/assets/dc9cbd95-f8fc-4ef0-b8c9-2bc7c7e4347c" />

## Implementation Plan

### Phase 1 – Design

* Define naming convention
* Required logs per resource type
* Retention period (X days)
* Create Central Log Analytics Workspace

### Phase 2 – Rollout

* Create Management Group hierarchy

* Assign policy initiatives at Management Group level

* Enable diagnostics for existing resources

* Migrate logs to central workspace

### Phase 3 – Enforcement

* Switch policies from Audit to Deny

* Monitor compliance reports

* Optimize log volume and cost

### Versioning & Updates

* Managing policies using Infrastructure As Code (Terraform)
* Git versioning
* Code to be tested in non-prod before releasing in production
* Backward compatible rollout











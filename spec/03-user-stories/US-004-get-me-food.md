# US-004 · Get me food

> **As** the Chef
> **I want** to confirm a meal request from the kitchen system
> **So that** the right patient receives the correct food quickly.

**Status:** 🟡 Draft
**Owner (BA):** {{name}}
**Owner (Dev):** _tbd_
**Persona:** [The Chef](../02-personas.md#-the-chef)

---

## Context

The Chef currently receives meal requests by paper ticket or phone call, which can lead to wrong diet orders and delayed delivery. This story covers the digital request workflow so the Chef can see and act on patient food orders in the same system used by the care team.

## Acceptance criteria

```gherkin
Feature: Get me food

  Scenario: Happy path — Chef confirms a new meal request
    Given the Chef is logged in to the kitchen management system
      And a new patient meal request appears in the queue
     When the Chef views the request details
      And confirms the meal preparation
     Then the request status changes to "Confirmed"
      And the meal request is timestamped
      And the care team sees the request status update immediately

  Scenario: Diet information is incomplete
    Given a patient meal request is missing required diet details
     When the Chef opens the request
     Then the Chef sees a clear warning: "Diet details are incomplete. Confirm the request only after clarification."
      And the request remains in "Pending" status

  Scenario: Kitchen system is unavailable
    Given the kitchen management system cannot connect to the backend service
     When the Chef tries to view new meal requests
     Then the Chef sees a message: "Unable to load meal requests. Please try again or use the paper backup process."
      And no new requests are confirmed in this state
```

## Non-functional notes

- The meal request queue must load within 2 seconds on the kitchen tablet.
- The interface must be usable with touch input.
- No patient-identifiable data may be stored in browser cache.

## Linked artefacts

- {{Link to ADRs, related stories, mockups}}

## Open questions

- [ ] Does the Chef need a separate view for urgent diet orders?
- [ ] Should the system support offline order pickup in the kitchen?

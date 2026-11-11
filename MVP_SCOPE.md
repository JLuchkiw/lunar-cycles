# Lunar Cycles - MVP Scope

**Status:** Draft - Initial development planning  
**Target release:** v0.1 MVP  
**Related document:** [Product Vision & Design Principles](PRODUCT_VISION.md)

---

## 1. Purpose

This document defines the minimum viable product (MVP) for Lunar Cycles, including its functional requirements, development boundaries, acceptance criteria, and implementation milestones.

The MVP should demonstrate the application's core philosophy:

**A person can organize their responsibilities, pursue meaningful intentions, and recognize their accomplishments without being evaluated against rigid productivity expectations.**

The initial release will be a local-first personal planning application with task management, calendar navigation, intention-setting, lunar information, and reflection.

The goal is a functional, testable application rather than a production-ready commercial release.

## 2. Intended Platforms

Lunar Cycles will be developed using React Native and Expo, with an architecture intended to support Android, iOS/iPadOS, and web.

Initial development and testing will prioritize Android.

iPadOS and web compatibility will be evaluated incrementally, with broader cross-platform testing required before claiming full platform support.

The initial MVP does not require app-store publication.

## 3. Functional Requirements

### FR-01: Home Dashboard

The home screen will provide an accessible overview of the user's day.

**Requirements:**
- Display the current date.
- Display the current lunar phase.
- Present a short, gentle greeting.
- Display tasks associated with the current date.
- Provide a clear way to create a task.
- Display completed tasks or a simple accomplishment summary.

**Acceptance criteria:**
- The dashboard loads without requiring an account.
- Today's tasks reflect the same data displayed in the Tasks and Calendar screens.
- Completed tasks are visually distinguishable without relying on color alone.
- The interface remains usable when no tasks exist.

### FR-02: Task Management

Users will be able to organize and recognize everyday activities.

**Requirements:**
- Create tasks with a title.
- Optionally assign a date.
- Edit task information.
- Mark tasks complete or incomplete.
- Delete tasks with confirmation.
- View completed and incomplete tasks.
- Create simple daily or weekly recurring routines.

**Acceptance criteria:**
- Tasks remain available after closing and reopening the application.
- Completion status persists between sessions.
- Tasks can exist without an associated intention.
- Tasks without dates remain accessible from the Tasks screen.
- Completing a recurring task does not permanently complete future occurrences.
- Missed tasks do not generate punitive messages or erase completion history.

### FR-03: Calendar

The calendar will provide a familiar interface for viewing date-associated tasks.

**Requirements:**
- Display a monthly calendar.
- Navigate between months.
- Select individual dates.
- Display tasks associated with the selected date.
- Provide a way to create a task for a selected date.
- Display subtle visual indicators for dates containing tasks.

**Acceptance criteria:**
- Tasks appear on their assigned dates.
- Task changes are reflected consistently across the Home, Tasks, and Calendar screens.
- Calendar navigation works across month and year boundaries.
- Dates without tasks remain selectable.
- The calendar does not require internet access.

**Excluded from MVP:** Dedicated appointment objects, external calendar synchronization, and complex scheduling features.

### FR-04: Intentions

Intentions will help users define personal directions without requiring measurable outcomes.

**Requirements:**
- Create intentions with a title and optional description.
- Support ongoing intentions and intentions associated with a lunar cycle.
- Allow intentions to be edited.
- Allow intentions to be paused, renewed, or released.
- Allow tasks to be optionally associated with an intention.
- Preserve released intentions in a historical view.

**Acceptance criteria:**
- Intentions can be created during any lunar phase.
- Intentions do not automatically expire.
- Releasing an intention does not delete its history.
- Paused intentions can be resumed.
- Renewing an intention retains its identity and history.
- Intentions do not require associated tasks or completion percentages.
- Users are not penalized for changing or releasing intentions.

### FR-05: Lunar Cycle Information

The application will use lunar phases as optional prompts for reflection.

**Requirements:**
- Calculate or retrieve the current lunar phase.
- Display the phase name and a simple visual representation.
- Associate broad reflection themes with the lunar cycle.
- Allow users to engage with intentions independently of the current phase.

**Acceptance criteria:**
- Lunar-phase information is available offline.
- Phase information updates appropriately as dates change.
- Lunar prompts are presented as suggestions rather than requirements.
- No feature is locked behind a particular lunar phase.
- The application does not imply that lunar phases scientifically determine personal capacity or productivity.

### FR-06: Reflection and Accomplishments

Users will be able to recognize progress beyond conventional task completion.

**Requirements:**
- Create short, dated reflection entries.
- View previously saved reflections.
- Edit or delete reflection entries.
- View completed tasks as accomplishments.
- Record an accomplishment that was not previously a task.
- Optionally associate a reflection with an intention.

**Acceptance criteria:**
- Reflections persist between sessions.
- Unplanned accomplishments can be recorded independently.
- Users can view past accomplishments.
- Reflections are not required to complete tasks or manage intentions.
- The interface does not assign negative scores to missed tasks or inactive intentions.

### FR-07: Local Data Persistence

The MVP will operate without user accounts or cloud synchronization.

**Requirements:**
- Store tasks, completion records, intentions, and reflections locally.
- Load saved information when the application restarts.
- Support offline operation.
- Avoid transmitting personal planning information to an external service.

**Acceptance criteria:**
- Saved records survive normal application restarts.
- Updates and deletions persist correctly.
- Core functionality works without network access.
- Development demonstrations use fictional sample data.
- No credentials, secrets, or personal user records are committed to the repository.

## 4. Nonfunctional Requirements

### Accessibility

- Support readable text and appropriate contrast.
- Provide meaningful labels for interactive controls.
- Avoid relying exclusively on color to communicate status.
- Respect reduced-motion preferences where supported.
- Support practical touch-target sizes and screen-reader navigation.

### Usability

- Keep common actions easy to discover.
- Avoid unnecessary onboarding barriers.
- Provide useful empty states.
- Minimize decorative interruptions.
- Use nonjudgmental language throughout the application.

### Reliability

- Handle invalid or missing user input gracefully.
- Preserve data integrity during ordinary application use.
- Handle month, year, and lunar-cycle boundaries correctly.
- Provide automated tests for important business logic.

### Maintainability

- Separate interface components from task, intention, and lunar calculation logic.
- Use consistent naming and project organization.
- Document setup and development instructions.
- Track implementation work and changes through Git.

## 5. Out of Scope for MVP

The following features are not required for the initial release:

- User accounts and authentication.
- Cloud synchronization across devices.
- External calendar integration.
- Full appointment and event scheduling.
- Social or community features.
- Advanced analytics or productivity scoring.
- Complex recurring-task scheduling.
- Push notification infrastructure.
- Elaborate animations or customizable themes.
- Extensive spiritual or ritual content.
- App-store publication.

These exclusions define the initial implementation boundary, not necessarily future commitments.

## 6. Development Milestones

### Milestone 1: Project Foundation

- Initialize the Expo application.
- Establish project structure and navigation.
- Configure development tooling.
- Set up local persistence.
- Add basic automated testing.
- Verify the application runs on an Android test device.

**Deliverable:** A running application with navigation and a working storage foundation.

### Milestone 2: Tasks and Routines

- Implement task creation, editing, and deletion.
- Implement task completion and history.
- Implement optional dates.
- Add basic daily and weekly recurrence.
- Connect task data to the Home and Tasks screens.

**Deliverable:** A functional local task manager.

### Milestone 3: Calendar and Lunar Display

- Implement monthly calendar navigation.
- Display date-associated tasks.
- Allow task creation from a selected date.
- Integrate offline lunar-phase calculations.
- Display lunar information on the Home screen.

**Deliverable:** A date-aware planner with lunar information.

### Milestone 4: Intentions

- Implement intention creation and editing.
- Support ongoing and cycle-associated intentions.
- Implement pause, renew, and release actions.
- Associate tasks with intentions.
- Preserve intention history.

**Deliverable:** A functional intention-management experience.

### Milestone 5: Reflection and Accomplishments

- Implement dated reflection entries.
- Implement unplanned accomplishment recording.
- Display accomplishment history.
- Support optional intention-linked reflections.
- Review language and interactions for alignment with the product vision.

**Deliverable:** A complete initial planning and reflection experience.

### Milestone 6: MVP Validation

- Test core user flows.
- Verify local data persistence.
- Test important date and recurrence edge cases.
- Review accessibility.
- Evaluate iPadOS and web compatibility.
- Fix critical defects.
- Update the README and project documentation.

**Deliverable:** A stable, demonstrable MVP with documented limitations.

## 7. MVP Completion Criteria

The MVP will be considered functionally complete when a user can:

1. Open the application without creating an account.
2. Create and complete everyday tasks.
3. Schedule tasks and find them through a calendar.
4. Manage simple recurring routines.
5. Create and manage an ongoing or lunar-cycle-associated intention.
6. Associate tasks with an intention when desired.
7. View the current lunar phase and optional reflection prompts.
8. Record personal reflections and unplanned accomplishments.
9. Review historical accomplishments and released intentions.
10. Close and reopen the application without losing saved information.

These flows must be tested on the primary Android development device.

Any limitations affecting iPadOS or web must be documented before broader platform support is claimed.

## 8. Open Technical Decisions

The following decisions will be evaluated during implementation:

- JavaScript versus TypeScript.
- Local database and storage abstraction.
- Navigation library and screen organization.
- Lunar-phase calculation library.
- Recurring-task data model.
- Intention lifecycle and history representation.
- Cross-platform storage compatibility.
- Automated testing frameworks.

Technical choices should favor clarity, maintainability, and incremental development over unnecessary complexity.

## 9. Scope Management

New feature ideas should be evaluated against the Product Vision and the MVP completion criteria.

A feature should enter the MVP only when it is necessary to demonstrate the application's core purpose or support an essential user workflow.

Otherwise, it should be documented as a possible future enhancement rather than added immediately.

**The goal is to build a small, complete experience before expanding it.**

---

*This document is a living specification and may be revised as implementation reveals new requirements, constraints, or opportunities.*

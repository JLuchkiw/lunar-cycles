# Lunar Cycles - User Flows & Navigation

**Status:** Initial design specification - subject to iteration  
**Related documents:** [Product Vision & Design Principles](PRODUCT_VISION.md) · [MVP Scope & Requirements](MVP_SCOPE.md)

---

## 1. Purpose

This document defines the primary navigation structure and user interactions for the Lunar Cycles MVP.

The goal is to establish an intuitive, accessible experience that supports practical planning, personal intentions, and meaningful reflection without unnecessary complexity.

These flows describe what users should be able to accomplish, not the final appearance of the interface.

## 2. Navigation Structure

The initial application will have five primary destinations:

| Destination | Purpose |
|---|---|
| Home | Daily overview, tasks, lunar phase, and quick actions |
| Tasks | Manage scheduled, unscheduled, and recurring tasks |
| Calendar | Navigate dates and view associated tasks |
| Intentions | Create, manage, and review personal intentions |
| Reflect | Record reflections and review accomplishments |

On mobile devices, these destinations will initially be represented by bottom navigation.

On larger displays, the navigation may adapt to a sidebar or another layout that better accommodates the available screen space.

### Navigation Principles

- Primary destinations should remain easy to reach.
- Users should not need to navigate through unrelated screens to complete common actions.
- Returning to Home should always be straightforward.
- Navigation should preserve user context when practical.
- Essential actions must not rely exclusively on gestures.
- Decorative elements must not interfere with navigation.

## 3. Home Screen

The Home screen is the application's primary landing destination.

It should provide a calm, practical overview of the current day.

### Primary Content

- Current date and lunar phase.
- Gentle greeting or optional reflective message.
- Today's tasks, including completion status.
- Prominent **Add task** action.
- Separate **Record an accomplishment** action.
- Simple recognition of completed activities.

### User Flow: Create a Task from Home

1. User opens Home.
2. User selects **Add task**.
3. Task editor opens.
4. User enters a task title.
5. User may optionally assign a date, recurrence, or related intention.
6. User saves the task.
7. Application returns to the previous context.
8. Task appears in the appropriate views.

**Expected behavior:**

- Task title is the only required field.
- A task created from Home may default to today's date, but the date can be changed or cleared.
- Saving updates local storage.
- Invalid or empty titles are handled with a clear, accessible message.

### User Flow: Complete a Task

1. User views a task on Home or Tasks.
2. User selects its completion control.
3. Task is marked complete.
4. Interface updates immediately.
5. Completion is recorded in local storage.
6. Task becomes available in accomplishment history.

**Expected behavior:**

- Completion can be reversed if selected accidentally.
- Completed tasks remain accessible.
- No streak, score, or judgment-based feedback is generated.

## 4. Tasks Screen

The Tasks screen provides a more comprehensive view of responsibilities and routines.

### Primary Content

- Incomplete tasks.
- Completed tasks.
- Unscheduled tasks.
- Recurring routines.
- **Add task** action.

### User Flow: Manage a Task

1. User opens Tasks.
2. User selects an existing task.
3. Task details or editor opens.
4. User modifies the title, date, recurrence, or associated intention.
5. User saves the changes.
6. Updated information appears across relevant screens.

Users may also delete tasks, with confirmation to prevent accidental data loss.

### User Flow: Manage a Recurring Routine

1. User creates or edits a task.
2. User selects daily or weekly recurrence.
3. User saves the task.
4. Application makes the routine available on applicable dates.
5. User completes an occurrence.
6. Future occurrences remain available.

**Expected behavior:**

- Completion of one occurrence does not complete every occurrence.
- Historical completion information is preserved.
- Recurrence can be edited or disabled.

## 5. Calendar Screen

The Calendar screen provides date-based navigation.

### User Flow: View Tasks for a Date

1. User opens Calendar.
2. Application displays the current month.
3. User navigates to another month if desired.
4. User selects a date.
5. Application displays tasks associated with that date.
6. User may open, complete, or edit a task.

### User Flow: Create a Task from Calendar

1. User selects a date.
2. User selects **Add task**.
3. Task editor opens with the selected date populated.
4. User enters a title and any optional details.
5. User saves the task.
6. Application returns to Calendar.
7. The new task appears under the selected date.

**Expected behavior:**

- Users can navigate across months and years.
- Dates without tasks remain accessible.
- Task changes are reflected consistently across screens.
- Calendar interactions work without internet access.

## 6. Intentions Screen

The Intentions screen supports personal direction and flexible growth.

### Primary Content

- Active intentions.
- Paused intentions.
- Released intentions and history.
- **New intention** action.

### User Flow: Create an Intention

1. User opens Intentions.
2. User selects **New intention**.
3. User enters an intention title.
4. User may add a description.
5. User chooses ongoing or lunar-cycle-associated, if desired.
6. User saves the intention.
7. Intention appears in the appropriate active view.

**Expected behavior:**

- Intentions may be created during any lunar phase.
- Intentions do not require measurable goals or linked tasks.
- Intention title is the only required field.
- No automatic expiration or failure status is assigned.

### User Flow: Manage an Intention

1. User selects an existing intention.
2. Intention details open.
3. User may edit, pause, resume, renew, or release the intention.
4. Application updates its status and preserves relevant history.
5. User returns to the Intentions screen.

### User Flow: Release an Intention

1. User opens an active or paused intention.
2. User selects **Release intention**.
3. Application explains that the intention will be archived, not deleted.
4. User confirms the action.
5. Intention moves into historical records.
6. Existing associated tasks and reflections remain accessible.

**Expected behavior:**

- Releasing an intention is never described as failure.
- Historical information remains available.
- The action does not automatically delete linked records.
- Users may create a new intention based on a previously released one.

### User Flow: Link a Task to an Intention

1. User creates or edits a task.
2. User selects the optional related-intention field.
3. User chooses an existing intention.
4. User saves the task.
5. The relationship appears in relevant task and intention views.

Tasks may remain unlinked.

## 7. Reflection & Accomplishments

The Reflect destination provides a place for reflection and recognition.

It will contain access to both written reflections and accomplishment history.

### User Flow: Record an Unplanned Accomplishment

1. User selects **Record an accomplishment** from Home or Reflect.
2. Accomplishment editor opens.
3. User enters a short description.
4. Date defaults to today but may be changed.
5. User may optionally select a related intention.
6. User saves the accomplishment.
7. Accomplishment appears in history.

**Expected behavior:**

- Description is the only required field.
- An accomplishment does not need to originate from a task.
- Intention association is optional.
- Accomplishments can be edited or deleted.
- Recording an accomplishment does not create an incomplete task.

### User Flow: Write a Reflection

1. User opens Reflect.
2. User selects **New reflection**.
3. Reflection editor opens.
4. User enters written content.
5. User may optionally select a date or related intention.
6. User saves the reflection.
7. Reflection appears in the history view.

**Expected behavior:**

- Reflection content is required.
- Reflections remain optional.
- Users may edit or delete their reflections.
- No completion requirement is associated with reflection.

### User Flow: Review Accomplishments

1. User opens Reflect.
2. User navigates to accomplishment history.
3. Application displays completed tasks and manually recorded accomplishments.
4. User may browse historical entries.
5. User may open relevant details.

**Expected behavior:**

- Both planned and unplanned accomplishments are represented.
- Completed tasks remain identifiable as tasks.
- History does not assign comparative scores or rankings.
- Reversing task completion updates its accomplishment status appropriately.

## 8. Shared Interaction Rules

### Required Fields

| Record | Required Information |
|---|---|
| Task | Title |
| Intention | Title |
| Accomplishment | Description |
| Reflection | Written content |

All other fields should remain optional unless a specific feature requires them.

### Data Consistency

- Home, Tasks, Calendar, Intentions, and Reflect should use consistent underlying records.
- Editing a record in one location should update all relevant views.
- Deleting a record should not unintentionally delete unrelated records.
- All MVP data should remain available offline.

### Feedback and Error Handling

- Provide clear feedback when records are saved, updated, or deleted.
- Explain invalid input without blame.
- Confirm destructive actions when appropriate.
- Support cancellation without unintentionally saving changes.
- Avoid unnecessary interruptions for routine actions.

### Celebratory Feedback

Lunar Cycles should provide gentle, positive feedback when users complete tasks or record accomplishments.

Feedback should reinforce recognition without introducing productivity scores, streaks, or pressure to perform.

**MVP expectations:**
- Completed tasks receive immediate visual confirmation.
- Newly recorded accomplishments receive a brief, positive acknowledgment.
- Feedback must not interrupt the user's workflow.
- Essential confirmation must remain understandable without animation.
- Reduced-motion preferences must be respected.

**Potential visual treatments:**
- Subtle star or stardust effects.
- Brief changes in glow, color, or emphasis.
- Small celestial illustrations or constellation effects.
- Gentle confirmation messages.

Specific animations and visual treatments will be explored during wireframing and implementation. Elaborate particle effects are not required for the MVP.

### Accessibility

- Provide labeled interactive elements.
- Support screen-reader navigation.
- Ensure controls are usable without relying on color alone.
- Respect reduced-motion preferences.
- Maintain practical touch targets and readable text.

## 9. Initial Screen Inventory

The following screens or views are anticipated:

**Primary destinations:**
- Home
- Tasks
- Calendar
- Intentions
- Reflect

**Supporting views:**
- Task editor
- Intention editor
- Intention details/history
- Accomplishment editor
- Reflection editor
- Accomplishment/reflection history

These supporting views may be implemented as screens, modals, or sheets depending on usability and platform requirements.

The exact presentation will be determined during wireframing.

## 10. Open Design Questions

The following decisions remain open:

- Whether task creation uses a modal, bottom sheet, or full-screen editor.
- How recurring routines are distinguished visually.
- How task groups and completed tasks appear on the Tasks screen.
- How intention history is displayed.
- Whether Reflect uses separate sections or internal tabs for reflections and accomplishments.
- How much lunar information appears outside Home.
- How navigation adapts to tablet and web layouts.

These questions should be addressed through low-fidelity wireframes and usability review before significant interface implementation.

---

*This document defines the intended MVP user experience and may evolve as design and development progress.*

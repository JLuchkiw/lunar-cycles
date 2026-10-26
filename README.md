# Lunar Cycles 🌙
A gentler approach to productivity, one cycle at a time.
Status: Concept and planning - development has not started.

Lunar Cycles is a planned mobile productivity app that combines everyday task management with longer-term intentions, positive reinforcement, and reflection guided by the lunar cycle. Its goal is to help people work toward the lives they want while recognizing the everyday work they already do.

The lunar cycle provides a recurring opportunity to plan, act, celebrate, and reflect—not a rule about when people should be productive. Spiritual practices and ritual prompts will be optional, so the app can be useful whether or not someone follows a spiritual practice.

## Why build this?
Many productivity tools emphasize streaks, deadlines, and unfinished tasks. Lunar Cycles explores a different approach: flexible routines, achievable steps, and an accomplishment log that recognizes both planned and unexpected progress. The design aims to be welcoming to people with different executive-function needs without assuming one workflow works for everyone.

## Planned experience
- Intentions: Broad directions or values that can continue across multiple lunar cycles.
- Goals: Concrete outcomes that can be linked to an intention or stand alone.
- Tasks: One-time actions, with optional dates and reminders.
- Routines: Recurring activities such as weekly groceries or laundry, tracked independently of lunar phases.
- Accomplishments: A place to record unexpected victories, even if they were never on a to-do list.
- Lunar reflections: Optional prompts to set intentions, build momentum, celebrate progress, and reflect on what to carry forward.
- Optional ritual layer: Spiritual or symbolic suggestions that users can choose to engage with or ignore.
Tasks and routines will not require a linked goal or intention. A grocery reminder should be just as easy to create as a long-term goal.

## Design principles
1. Progress over perfection. Missing a day should not erase past effort.
2. Choice over obligation. Rituals, reflections, and goal associations are optional.
3. Everyday work counts. Routine maintenance and unplanned accomplishments deserve recognition.
4. Cycles are invitations, not deadlines. Goals can continue, change, or be released without a failure label.
5. Accessibility and privacy by design. Aim for clear navigation, reduced sensory load, and local-first storage.
6. Grounded guidance. Lunar phases organize reflection; the app will not claim they scientifically determine productivity.

## Development roadmap

v0.1 — Functional foundation
- [ ] Initialize a React Native / Expo app and Git repository
- [ ] Create, edit, complete, and delete one-time tasks
- [ ] Add simple daily and weekly recurring routines
- [ ] Persist tasks and completion history locally
- [ ] Display the current lunar phase
- [ ] Show a basic accomplishments count
- [ ] Add foundational tests and document setup instructions
Milestone: A usable local-only task and routine tracker with a lunar-cycle display.

v0.2 — Intentions and cycles
- [ ] Add intentions and cycle-specific goals
- [ ] Optionally associate tasks with goals
- [ ] Record accomplishments that were not planned tasks
- [ ] Summarize accomplishments within a lunar cycle
- [ ] Add reflection prompts and carry-forward options
Milestone: A complete planning and reflection loop without penalizing unfinished work.

v0.3 — Personalization
- [ ] Add optional ritual prompts and presentation preferences
- [ ] Explore local notifications and configurable reminders
- [ ] Improve accessibility, reduced-motion options, and customization
- [ ] Expand tests for recurring tasks and cycle boundaries
Milestone: A more personalized, supportive daily experience.

### Longer-term possibilities (not committed scope)
- Secure accounts and optional cross-device synchronization
- More flexible recurrence and calendar integrations
- Richer summaries and accessibility settings
- Additional narrative and reflection experiences inspired by cyclical growth

### Proposed technology
Area	Planned approach
Mobile UI	React Native with Expo (JavaScript/TypeScript decision pending)
Local data	SQLite, subject to prototyping
Lunar phases	Offline astronomical calculation library, to be evaluated
Version control	Git and GitHub
Testing	Frameworks to be selected during implementation


These are initial technical choices, not claims about completed implementation.

### Privacy and development boundaries:

The initial prototype is intended to be single-user and local-first, with no authentication, cloud sync, or collection of other people's personal information. Development and demonstrations will use fictional sample tasks and goals. No passwords, API keys, or private user information should be committed to this repository or included in recorded development sessions.

Future account or synchronization features would require a separate privacy and security design review before implementation.

### Current status and ownership:

This is an independently conceived personal project, maintained in my personal GitHub repository. It is not coursework or a deliverable owned by an employer, client, or university. The project is currently in the planning stage; features above describe intended development, not completed functionality.

Project creator and maintainer: Jessica “Ellie” Luchkiw

### License

No open-source license has been selected yet. Public visibility does not grant permission to reuse the code. Licensing will be reviewed before any outside contributions or public release.

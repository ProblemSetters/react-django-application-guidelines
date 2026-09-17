# Instructions

The application in this repository must replicate the functionality of a real-world product for a problem domain chosen by the participant. Keep the same structure, setup flow, formatting, and coding conventions as the React + Django (Python) reference calendar repository. The validator in `skills/validate/SKILL.md` checks the implementation against `GUIDELINES.md`.

## 1. Clone and study the Django reference

Clone the React + Django (Python) reference calendar repository before you begin. Use it to understand the application structure, setup flow, formatting, coding conventions, and UI quality, then build the chosen application in this repository. The reference is not the application destination.

```bash
git clone https://github.com/ProblemSetters/coderepo-react-django-calendar.git ../coderepo-react-django-calendar-reference
```

## 2. Keep the project contract in this repository

These files already belong at the root of this application repository:

1. `AGENTS.md`, before opening an AI assistant. It starts transcript logging.
2. `GUIDELINES.md`. The acceptance contract.
3. `skills/validate/`. The verifier, which expects `GUIDELINES.md` at the repository root.

## 3. Run and inspect the reference before building

Run the cloned reference and inspect its frontend, backend, manifests, scripts, configuration, and README so you understand the standards to preserve while building your own product.

```bash
bun install && bash setup.sh --seed
```

```bash
bun start
```

Prerequisites, ports, seeded credentials, and commands are in the reference README.

## 4. Keep what the reference provides

- **Stack and dependencies.** Keep React + Django (Python), MongoDB, the build tool, package manager, and lockfile. Versions must be at least as recent as the reference. Any new dependency needs a written reason.
- **Setup and run flow.** Keep the same `hackerrank.yml` commands, ports, seed-and-reset behavior, `.env.example` handling, and read-only paths.
- **Layout.** Keep feature folders in the frontend and backend in the same organizational style as the reference. Route, controller, service, and repository responsibilities stay separate.
- **Formatting and hygiene.** Preserve the reference Prettier configuration and editor configuration. Remove dead code and debugging output, use local media only, and use American English throughout.
- **UI quality.** Preserve the reference's design system, responsive behavior, and handling for loading, empty, validation, success, and error states.

When in doubt, open the matching file in the reference and follow its conventions.

## 5. Before you submit

1. Copy the log file named in `AGENTS.md` into `transcripts/`.
2. Put any skill you wrote under `skills/`.
3. Run the validator and fix every `FAIL`.
4. Add `content.team@problemsetters.com` as a collaborator and post on Discord.

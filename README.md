# Build Your Own Full-Stack Application

Build a full-stack application for a problem domain of your choice using React + Django (Python) and MongoDB. Define the target users, product identity, data model, and five to ten meaningful end-to-end capabilities. The application should solve a coherent problem, demonstrate thoughtful product decisions, and provide a polished, accessible UI. It must install, build, start, and satisfy the acceptance criteria and verifier from a clean checkout.

The application will be built in this repository, following the guidelines given. Start by reading the files in the order below.

## Mandatory project checks before submission

> [!IMPORTANT]
> **Run the provided project checks and fix every reported failure before submitting your code. Rerun them after your final changes.**

### 1. Prepare the check tools

Copy the complete `project-checks/` folder from the [reference calendar repository](https://github.com/ProblemSetters/coderepo-react-django-calendar/tree/main/project-checks) into the root of your application repository. Keep the provided tests and configuration unchanged.

Use the starter’s Python and Bun setup, with Python 3.12 or later for the checks. Node.js, Bash and MongoDB must also be available. The commands below use Bash on Linux or macOS; on Windows, use WSL. Run all commands from your application repository root.

```bash
npm install --prefix project-checks --package-lock=false
python3 -m venv project-checks/.venv
project-checks/.venv/bin/python -m pip install -r project-checks/requirements.txt
```

This installs the check tools separately under `project-checks/`; it does not add them to the application’s dependency manifests.

### 2. Run the checks

Stop any application instance using ports 3000 or 8000, then run:

```bash
PATH="$PWD/project-checks/.venv/bin:$PWD/project-checks/node_modules/.bin:$PATH" \
PROJECT_ROOT="$PWD" \
project-checks/.venv/bin/python -m pytest -p no:cacheprovider project-checks/project_checks_test.py -v -s
```

The checks cover required paths, `hackerrank.yml` fields, pinned direct dependencies, linting, root `README.md` presence, existing test XML reports, and install/run/test execution. Application commands run in a temporary source copy and report their timings.

- Install and run commands come from `configuration.ide_config.project_menu` in `hackerrank.yml`.
- The test command comes from the same menu’s `test` field, falling back to root `package.json` → `scripts.test` through the project’s package manager. If neither defines a test, application tests and generated XML checks are reported as skipped.
- Install and test commands must exit with code `0`. The run command must stay running and respond at the readiness URLs. Generated XML is required only when `configuration.scoring.files` is configured.
- Defaults: install 600 seconds, startup 120 seconds, test 300 seconds. Override these with `CHECK_INSTALL_TIMEOUT_SECONDS`, `CHECK_STARTUP_TIMEOUT_SECONDS` and `CHECK_TEST_TIMEOUT_SECONDS` when needed. Readiness defaults to `http://127.0.0.1:3000/` and `http://127.0.0.1:8000/`; for different application ports, set `CHECK_READY_URLS` to a JSON array of your local URLs.

### 3. Fix failures and rerun

Read each failure, fix the reported issue, and rerun the same command. Missing tools, command failures and timeouts must be resolved. **Submit only when the checker exits successfully with no failed checks.** Passing these checks does not guarantee your implementation is functionally correct.

## Read in this order

1. **[REQUIREMENTS.md](REQUIREMENTS.md)** defines the product brief, capability patterns, acceptance criteria, and submission checklist.
2. **[INSTRUCTIONS.md](INSTRUCTIONS.md)** explains how to study the reference repository, start the application, and keep the repository clean.
3. **[AGENTS.md](AGENTS.md)** turns on transcript logging for this application repository. Read it before opening an AI assistant; it records every turn for export under `/transcripts`.
4. **[GUIDELINES.md](GUIDELINES.md)** is the acceptance contract. Every rule the verifier checks is written here.
5. **[skills/validate/SKILL.md](skills/validate/SKILL.md)** is the verifier. Run it when you are done. It audits structure, stack, dependencies, install, build, start, API behavior, and MongoDB persistence.

## Reference repository

| Stack | Repository |
|---|---|
| React + Django (Python) | https://github.com/ProblemSetters/coderepo-react-django-calendar |

The reference repository establishes the expected project structure, setup flow, formatting, and implementation quality. It is a reference only; build the chosen application in this repository.

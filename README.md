# Build Your Own Full-Stack Application

Build a full-stack application for a problem domain of your choice using React + Django (Python) and MongoDB. Define the target users, product identity, data model, and five to ten meaningful end-to-end capabilities. The application should solve a coherent problem, demonstrate thoughtful product decisions, and provide a polished, accessible UI. It must install, build, start, and satisfy the acceptance criteria and verifier from a clean checkout.

The application will be built in this repository, following the guidelines given. Start by reading the files in the order below.

## Required before submission

> [!IMPORTANT]
> **All provided project checks must pass before you submit.**

1. Copy `project-checks/` from the [reference repository](https://github.com/ProblemSetters/coderepo-react-django-calendar/tree/main/project-checks) into your project root.
2. Install the check tools once, from your project root:

```bash
npm install --prefix project-checks --package-lock=false
python3 -m venv project-checks/.venv
project-checks/.venv/bin/python -m pip install -r project-checks/requirements.txt
```

3. With MongoDB running and your application stopped, run:

```bash
PATH="$PWD/project-checks/.venv/bin:$PWD/project-checks/node_modules/.bin:$PATH" \
PROJECT_ROOT="$PWD" project-checks/.venv/bin/python -m pytest project-checks/project_checks_test.py -v -s
```

Fix every failure and rerun the checks after your final changes.

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

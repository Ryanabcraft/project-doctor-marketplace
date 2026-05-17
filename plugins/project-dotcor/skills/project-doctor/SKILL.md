---
name: project-doctor
description: Diagnose any local project or workspace by identifying its stack, key files, run/test/build commands, and likely setup problems. Use when the user asks to inspect, understand, run, repair, or get next steps for a project folder.
---

# Project Doctor

Use this skill to inspect a local project and give practical next steps.

## Workflow

1. Inspect the current directory first.
   - Prefer `rg --files` for file discovery.
   - Use `Get-ChildItem -Force` on Windows when a directory overview is useful.
   - Do not make destructive changes during diagnosis.

2. Identify the project type from common files.
   - Node: `package.json`, lockfiles, `vite.config.*`, `next.config.*`.
   - Python: `pyproject.toml`, `requirements.txt`, `.venv`, `.py` files.
   - .NET: `.sln`, `.csproj`, `.fsproj`.
   - Android/Gradle: `settings.gradle`, `build.gradle`, `gradlew.bat`.
   - Static web: `index.html`, `app.js`, `style.css`.

3. Report the useful commands.
   - Install dependencies.
   - Start development server or app.
   - Run tests.
   - Build or package.
   - Lightweight syntax or health checks.

4. Call out likely blockers.
   - Missing dependency folders.
   - Missing env files or credentials.
   - Port conflicts.
   - Broken scripts.
   - Logs with recent errors.

5. Keep the output concrete.
   - Mention exact files found.
   - Give copy-paste commands for PowerShell when possible.
   - If the user asked to fix the project, implement a narrow fix after diagnosis.

## Output Shape

Start with a short diagnosis summary, then list:

- Project type
- Important files found
- Commands to run
- Problems or risks
- Recommended next action

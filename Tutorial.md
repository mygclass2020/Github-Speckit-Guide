# Github SpecKit Tutorial
Getting started with SpecKit

## Pre-requisites
> - uv for package management [Download Link](https://docs.astral.sh/uv/)
> - [Supported AI Coding Agent](https://github.com/github/spec-kit?tab=readme-ov-file#-supported-ai-agents)
> - VS Code

## Getting Started

**1. Install SpecKit CLI**
- Run these commands in terminal
```
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
```
To Create New Project:
```
specify init <PROJECT_NAME>
```

**2. Open Project in VS Code**
```
code .
```

Note: Make sure you're in the project root directory

**3. Establish Project Principles**
- Use ```/speckit.constitution``` command to create constitution
- Example:
```
/speckit.constitution Create principles focused on code quality, testing standards, user experience consistency, and performance requirements
```

**4. Create the Spec**
- Use the ```/speckit.specify``` command to describe what you want to build
- Example:
```
/speckit.specify Create a simple Todo application with basic CRUD functionality helping users manage simple tasks efficiently.
```

**5. Create technical implementation plan**
- Use the ```/speckit.plan``` command to define the tech stack and archituctural choices
- Example:
```
/speckit.plan Create a clear and concise implementation plan for the Todo application based on the given specification and constitution.
Requirements:
- Backend must use Python with FastAPI
- Follow MVC (Model-View-Controller) architecture
- Include both backend APIs and a simple frontend UI
- Keep everything minimal and suitable for a basic CRUD Todo app
```

**6. Break down into tasks**
- Use the ```/speckit.tasks``` command to create actionable task list from plan
- Example:
```
/speckit.tasks Create a clear, minimal, and actionable task list for implementing the Todo application that a developer can follow step-by-step.
```

**7. Execute implementation**
- Use the ```/speckit.implement``` command to generate actual code based on tasks list
- Example:
```
/speckit.implement Generate complete, working code for the application in the logical order defined in the task list.
```

## Workflow

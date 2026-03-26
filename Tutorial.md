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

## Github SpecKit: File Generation Workflow
![File Generation Workflow](/Images/workflow.png)

**Phase I - Initializing the Project**
- Files are generated upon creation of Project
- 
**Phase II - Creating the Constitution**
- ```Constitution.md```- Contains the constitution with core principles of the project <br>
**Phase III - Defining Specification**
- A new feature branch is created to contain all files created in subsequent phases that are related to that feature
- ```spec.md``` - Contains the specifications of the feature
- ```checklists/requirements.md``` - Has a checklist to validate specification completeness and quality before proceeding to planning <br>
**Phase IV - Creating Plan**
- ```plan.md``` - Contains high-level implementation plan outlining tech stack, architecture, and key decisions
- ```research.md``` - Contains notes on explored options, trade-offs, and reasoning behind chosen approaches
- ```data-model.md``` - Conatains definition of core data structures, entities, and their relationships
- ```quickstart.md``` - Contains simple instructions to set up and run the project locally
- ```contracts/demo-api.yaml``` - Contains API contract specifying endpoints, request/response formats, and interaction details
- Contracts are generated when external or structured interactions are required
- Contracts specify communication boundaries and the data exchange between parties <br>
**Phase V - Generating Tasks**
- ```tasks.md``` - Contains tasks list divided into phases and user stories
- Tasks should be a list of actionable items that a developer can follow to build the code <br>
**Phase VI - Implementation**
- In this phase actual code files are generated according to tasks list

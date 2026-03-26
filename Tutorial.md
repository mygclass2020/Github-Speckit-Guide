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
/speckit.constitution
Create a clear and concise "constitution" for a simple full-stack Todo application.

The constitution should define rules, constraints, and guidelines for generating both specifications and code.

Requirements for the Todo app:
- It must support basic CRUD operations (create, read, update, delete).
- Backend MUST expose a clean REST API via FastAPI
- Architecture must strictly follow the MVC (Model-View-Controller) pattern.
- It must include both backend APIs and a simple frontend UI.

Constraints for the constitution:
- Do not include unit testing requirements.
- Avoid unnecessary features such as authentication, roles, or complex scalability concerns.
- Emphasize simplicity, clarity, and minimal implementation.

Guidelines for the constitution content:
- Keep it concise and to the point (no long explanations or documentation).
- Define clear sections such as purpose, architecture, backend rules, frontend rules, constraints, and behavior.
- Ensure outputs generated under this constitution are minimal, clean, and production-ready.
- Encourage consistency, readability, and separation of concerns.
- Specify that only necessary templates and code should be generated (no verbosity).

Output format:
- Structured in markdown or clean bullet-point format.
- No extra explanations outside the constitution itself.
```
NOTE: This is prompt to create the constitution, NOT the content of the actual constitution

**4. Create the Spec**
- Use the ```/speckit.specify``` command to describe what you want to build
- Example:
```
/speckit.specify
Create a clear and concise product specification for a simple Todo application.

Focus only on the "what" and "why" of the application. Do NOT include technical implementation details, frameworks, or architecture.

Purpose
Describe the goal of the application: helping users manage simple daily tasks efficiently.

Core Features (keep it minimal)
Include only basic CRUD functionality:
- Add a new todo
- View a list of todos
- Edit/update an existing todo
- Delete a todo

Feature Descriptions
For each feature:
- Explain what the user can do
- Explain why the feature is useful

User Experience
- The interface should be simple, clean, and easy to use
- Use a light green themed UI (calm, minimal, pleasant)
- Focus on quick interactions with minimal steps

Scope Constraints
- Keep the application very basic
- No advanced features (no authentication, no categories, no notifications, etc.)
- No complex workflows or edge cases

Writing Guidelines
- Keep the specification short and to the point
- Use simple language
- Avoid technical jargon
- Structure clearly with headings and bullet points
- Do not include implementation details

Output Format
- Clean, structured text (markdown preferred)
- No extra explanation outside the specification
```

**5. Create technical implementation plan**
- Use the ```/speckit.plan``` command to define the tech stack and archituctural choices
- Example:
```
/speckit.plan
Create a clear and concise implementation plan for the Todo application based on the given specification and constitution.

Focus on defining the tech stack and architecture choices. Do not restate the full specification.

Requirements
- Backend must use Python with FastAPI
- Follow MVC (Model-View-Controller) architecture
- Include both backend APIs and a simple frontend UI
- Keep everything minimal and suitable for a basic CRUD Todo app

What to include

Tech Stack
- Backend framework
- Frontend approach (simple UI, minimal tools)
- Data storage (keep it simple)
- Any essential libraries/tools only

Architecture
- High-level structure following MVC
- How components interact (models, views, controllers)
- Request flow (user → UI → API → data → response)

Project Structure
- Suggest a simple folder/file structure
- Keep it minimal and clean

Key Decisions
- Explain *why* each major choice was made (briefly)
- Emphasize simplicity and maintainability

Constraints
- Do not include unit testing strategy
- Avoid overengineering
- Avoid unnecessary tools or frameworks

Output Format
- Structured and concise (markdown preferred)
- No long explanations
- Focus only on essential decisions
```

**6. Break down into tasks**
- Use the ```/speckit.tasks``` command to create actionable task list from plan
- Example:
```
/speckit.tasks
Create a clear, minimal, and actionable task list for implementing the Todo application based on the provided specification, constitution, and plan.

Goal
Break down the implementation into small, logical tasks that a developer can follow step-by-step.

Requirements
- Tasks must align with the defined tech stack and MVC architecture
- Cover both backend (FastAPI APIs) and frontend (simple UI)
- Include only what is necessary for a basic CRUD Todo app

Task Guidelines
- Each task should be small, specific, and actionable
- Use clear, imperative language (e.g., "Create model", "Implement API endpoint")
- Organize tasks in logical order (setup → backend → frontend → integration)
- Group related tasks when appropriate

Suggested Sections
- Project Setup
- Backend (Models, Controllers, APIs)
- Frontend (UI, templates, interactions)
- Integration (connect UI with API)
- Final Cleanup

Constraints
- Do NOT include unit testing tasks
- Do NOT include advanced features or enhancements
- Avoid vague tasks like "build backend" — be specific

Output Format
- Use a numbered checklist or bullet list
- Keep it concise and to the point
- No explanations, only tasks
```

**7. Execute implementation**
- Use the ```/speckit.implement``` command to generate actual code based on tasks list
- Example:
```
/speckit.implement
Implement the Todo application based on the provided specification, constitution, plan, and task list.

Goal
Generate complete, working code for the application by following the defined tasks step-by-step.

Requirements
- Follow the exact tech stack and architecture from the plan
- Adhere strictly to MVC structure
- Implement only basic CRUD functionality
- Include both backend (FastAPI APIs) and frontend (simple UI)

Implementation Guidelines
- Write clean, readable, and modular code
- Keep everything minimal and to the point
- Do not add extra features beyond the specification
- Use simple templates for the UI (light green theme)
- Ensure frontend interacts correctly with backend APIs

Task Execution
- Implement in the logical order defined in the task list
- Ensure each part works before moving to the next
- Maintain consistency across files and components

Constraints
- Do NOT generate unit tests
- Do NOT include unnecessary explanations
- Do NOT overengineer or introduce additional tools

Output Format
- Provide complete code with proper file structure
- Use clear file separation (backend, frontend, templates, static files)
- Keep comments minimal and useful only where necessary
```

## Github SpecKit: File Generation Workflow
![File Generation Workflow](/Images/workflow.png)

### **Phase I - Initializing the Project**
- These are the files are generated upon creation of Project
- ```.github/agents``` - Contains system/agent definitions that control how SpecKit behaves and processes each stage
- ```.github/prompts``` - Contains prompt files defining the behaviour of SpecKit's core commands
- ```.specify/scripts/powershell``` - Includes  PowerShell scripts designed to automate the scaffolding, setup, and management of project
- ```.specify/templates``` - Provides structured markdown templates used as starting points for generated documents
### **Phase II - Creating the Constitution**
- ```Constitution.md```- Contains the constitution with core principles of the project <br>
### **Phase III - Defining Specification**
- A new feature branch is created to contain all files created in subsequent phases that are related to that feature
- ```spec.md``` - Contains the specifications of the feature
- ```checklists/requirements.md``` - Has a checklist to validate specification completeness and quality before proceeding to planning <br>
### **Phase IV - Creating Plan**
- ```plan.md``` - Contains high-level implementation plan outlining tech stack, architecture, and key decisions
- ```research.md``` - Contains notes on explored options, trade-offs, and reasoning behind chosen approaches
- ```data-model.md``` - Conatains definition of core data structures, entities, and their relationships
- ```quickstart.md``` - Contains simple instructions to set up and run the project locally
- ```contracts/demo-api.yaml``` - Contains API contract specifying endpoints, request/response formats, and interaction details
   - Contracts are generated when external or structured interactions are required
   - Contracts specify communication boundaries and the data exchange between parties <br>
### **Phase V - Generating Tasks**
- ```tasks.md``` - Contains tasks list divided into phases and user stories
- Tasks should be a list of actionable items that a developer can follow to build the code <br>
### **Phase VI - Implementation**
- In this phase actual code files are generated according to tasks list

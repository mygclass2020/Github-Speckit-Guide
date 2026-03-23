# GitHub SpecKit Guide
Understanding GitHub SpecKit— discover it's purpose, concepts and follow a step-by-step tutorial to get started.

## Introduction
GitHub SpecKit is a structured workflow designed to take an idea from concept to implementation in a clear, organized, and scalable way. It follows Spec-Driven Development (SDD) where specifications become executables, flipping the traditional software development where 'code is king'. Here, we write a 'Spec' before writing code which becomes the ulitmate source of truth for the developer and AI. A Spec is a clear and detailed description of software functionality written in natural language that serves as a guidance to AI coding agents with the closest comparision being to a "Product Requirements Document". Spec-Driven Development separates decision-making into distinct stages using multi-step refinement rather than one-shot code generation from prompts to create a stuctured pathway for software development.

The five phases of developing with SpecKit are:
1. Constitution
2. Specify
3. Plan
4. Tasks
5. Implement

Each stage has a unique purpose and should not overlap with others. Let's understand these phases one by one.

---

## 1. Phase I - Constitution (Principles & Constraints)

### Purpose
- Defines the foundational rules and guiding principles for the project.
- "Rulebook" or "Ground Truth" that must be followed when making decisions, generating specs or code

### What it Includes
- Purpose & Scope
    - What the system should do & NOT do
    - e.g: “The system generates production-ready backend APIs. It should not generate UI code unless explicitly requested.”
- Reasoning Guidelines
    - Filter for decision-making when ambiguity arises
    - e.g: “When requirements are unclear, ask clarifying questions before proceeding.”
- Safety & Constraints
    - Define limits for sensitive data usage and ethical boundaries
    - e.g: “Never generate code that exposes API keys or security vulnerabilities.”
 - Things to Avoid
     - Explicitly state unwanted behaviours
     - e.g: “Do not generate unit tests unless requested.”
  - Architecture Rules
      - Ensure consistency by defining coding patterns
      - e.g: "Strictly follow MVC (Model-View-Controller) pattern"
  - Output Constraints
      - Specify non-negotiable rules
      - e.g: "Do not assume extra features beyond CRUD unless asked"
  -Iteration Rules
      - Define how to accept feedback and improve outputs
      - e.g: “When feedback is provided, update only relevant sections without rewriting everything.”

### What it Should NOT Include
- Specific tools, frameworks, or technologies (unless long-term constraints)

### Key Insight
This stage answers:  
**“What rules guide all decisions?”**

---

## 2. Phase II - Specify (Requirements Definition)

### Purpose
Clearly defines what needs to be built.

### What it Includes
- Feature descriptions
- User stories
- Functional requirements
- Input/output behavior
- Acceptance criteria

### Examples
- Users can register using email and password
- System validates user credentials during login
- Error messages are shown for invalid inputs

### Key Insight
This stage answers:  
**“What are we building?”**

---

## 3. Phase III - Plan (System Design & Architecture)

### Purpose
Outlines how the system will be built at a high level.

### What it Includes
- Architecture design
- Tech stack choices
- Data flow and system components
- Design patterns
- Trade-offs and reasoning

### Examples
- Backend: Node.js with Express
- Database: SQLite (can be replaced later)
- Use MVC architecture

### What it Should NOT Include
- Step-by-step coding tasks

### Key Insight
This stage answers:  
**“How is the system structured?”**

---

## 4. Phase IV - Tasks (Execution Breakdown)

### Purpose
Breaks the plan into actionable development steps.

### What it Includes
- Small, clear tasks
- Task dependencies
- Developer-friendly checklist
- Implementation sequence

### Examples
- Create user database schema
- Implement authentication API
- Add password hashing
- Write unit tests

### Key Insight
This stage answers:  
**“What exact steps do we take to build it?”**

---

## 5. Phase V - Implement (Execution & Delivery)

### Purpose
Transforms tasks into working code.

### What it Includes
- Writing code
- Testing and debugging
- Iteration and improvements
- Integration of components

### Examples
- Coding APIs and business logic
- Fixing bugs
- Running tests
- Deploying features

### Key Insight
This stage answers:  
**“Can we successfully build and deliver it?”**

---

## Summary Table

| Stage         | Focus                     | Key Question                      |
|--------------|--------------------------|----------------------------------|
| Constitution | Principles & constraints | What rules guide decisions?      |
| Specify      | Requirements             | What are we building?            |
| Plan         | Architecture             | How is it designed?              |
| Tasks        | Action steps             | What steps do we take?           |
| Implement    | Execution                | Can we build and deliver it?     |

---

## Final Notes
- Keep stages separate to avoid confusion
- Avoid mixing architecture (Plan) with execution (Tasks)
- Keep Constitution stable and long-term
- Allow Plan to evolve as technology changes

---

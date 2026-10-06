# SELVIA

Software Engineering Learning and Virtual Intelligence Assistant.

SELVIA is a university research prototype implementing a multi-agent framework
for supporting project-based software engineering learning. It aims to assist
students through the full lifecycle of a software project while giving
lecturers visibility into student progress and performance.

> **Status:** Repository foundation only. No application logic or AI
> functionality has been implemented yet.

## Primary Research Component

The **Adaptive AI Tutor Agent** is the primary individual research component of
this project. The other agents and services form the surrounding framework in
which the tutor operates.

## Architectural Concepts

### Agents

- **Main Orchestration Agent** – coordinates the specialised agents and routes
  requests between them.
- **Project Planning Agent** – supports students in scoping, planning, and
  structuring software projects.
- **Adaptive AI Tutor Agent** – provides personalised, adaptive learning
  support tailored to each student *(primary research component)*.
- **Performance Assessment Agent** – evaluates student progress and work.
- **Security Agent** – oversees safe and appropriate system and agent behaviour.

### User Interfaces

- **Lecturer Dashboard** – monitoring and oversight for lecturers.
- **Student Dashboard** – the main interface for students.

### Technologies and Concepts

- **MCP** (Model Context Protocol) – standardised tool and context access for agents.
- **LangGraph** – agent workflow and orchestration framework.
- **LLM** (Large Language Model) – underlying language model capability.
- **RAG** (Retrieval-Augmented Generation) – grounding responses in course and
  domain material.
- **PostgreSQL** – relational data storage.
- **Neo4j** – knowledge graph storage.

## Repository Structure

```
SELVIA/
├── apps/         # User-facing applications (frontend, backend)
├── agents/       # Individual agent modules
├── services/     # Supporting services (MCP server, RAG, knowledge graph)
├── database/     # Database schema and migrations
├── packages/     # Shared code, types, and configuration
├── tests/        # Unit, integration, and end-to-end tests
├── docs/         # Architecture, API, agent, MCP, and research documentation
└── docker/       # Container configuration
```

## Configuration

Copy `.env.example` to `.env` and fill in values as services are introduced.
Never commit `.env`.

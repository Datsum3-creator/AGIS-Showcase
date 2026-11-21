# AGIS - System Architecture



**AI Agent Governance & Inventory System**



> No Owner. No Production.



## 1. Architecture Overview



AGIS is currently implemented as a web-based governance prototype with a frontend console, a FastAPI backend, and a PostgreSQL database.



The architecture follows a modular backend approach, keeping authentication, agent management, governance workflows, and data persistence as distinct responsibilities.



## 2. Current Architecture



```mermaid

flowchart TD

&#x20;   U["Enterprise Users<br/>Admin | Reviewer | Viewer"]



&#x20;   FE["Frontend Console<br/>HTML | CSS | JavaScript"]



&#x20;   API["FastAPI Backend<br/>REST API"]



&#x20;   AUTH["Authentication & RBAC<br/>JWT-based access"]

&#x20;   REG["Agent Registry<br/>Registration | Inventory | Details"]

&#x20;   GOV["Governance Workflows<br/>Review | Approval | Rejection"]

&#x20;   OPS["Operational Status<br/>Status Updates"]

&#x20;   AUD["Audit Events"]



&#x20;   DB[("PostgreSQL Database")]



&#x20;   U --> FE

&#x20;   FE --> API

&#x20;   API --> AUTH

&#x20;   API --> REG

&#x20;   API --> GOV

&#x20;   API --> OPS

&#x20;   API --> AUD



&#x20;   AUTH --> DB

&#x20;   REG --> DB

&#x20;   GOV --> DB

&#x20;   OPS --> DB

&#x20;   AUD --> DB

```



## 3. Technology Stack



| Layer | Technology |

|---|---|

| Frontend | HTML, CSS, JavaScript |

| Backend | Python, FastAPI |

| Database | PostgreSQL |

| ORM | SQLAlchemy |

| Authentication | JWT |

| API schema | OpenAPI |

| API exploration | Swagger UI |



## 4. Implemented Prototype Components



### Frontend Console

A browser-based interface for signing in and interacting with the AGIS governance workflows.



### Authentication and Role-Based Access

JWT-based authentication with Admin, Reviewer, and Viewer roles. Backend authorization controls access to protected operations.



### Agent Registry

Supports agent registration, inventory listing, and individual agent details.



### Governance Workflow

Supports reviewer approval and rejection, including a separation-of-duties check that prevents an agent owner from approving their own agent.



### Organization-Level Isolation

Organization-scoped access has been tested to prevent users from accessing another organization's agent records through the tested API workflows.



### Operational Status Management

Supports updating an agent's recorded operational status and generating an associated audit event.



**Important:** Operational status management currently changes application/database state. It does not terminate a running AI agent or revoke its credentials.



### Audit Events

Records selected governance and operational actions for traceability.



## 5. Planned Architecture Extensions



The following capabilities are future development goals, not claims about the current implementation:



- Developer-native registration using `agis.yaml`.

- Automated Shadow AI discovery.

- Runtime agent monitoring.

- Automated policy enforcement.

- Actual agent termination and credential revocation.

- Enterprise identity and cloud integrations.

- Expanded compliance reporting and governance analytics.



## 6. Security and Governance Design Principles



AGIS is being designed around:



- Human accountability for AI agents.

- Role-based authorization.

- Organization-level data separation.

- Review workflows and separation of duties.

- Traceable governance actions.

- Visibility into agent inventory and operational status.



These principles describe the intended governance model. The current prototype has not undergone a complete independent security assessment.



## 7. Current Project Stage



**Early-stage working prototype - under active development.**



The current implementation demonstrates core inventory and governance workflows. It is not production-ready and does not yet provide complete runtime enforcement or automated discovery.



## 8. Long-Term Vision



AGIS aims to become a centralized governance layer between AI innovation and enterprise operations - helping organizations maintain visibility, accountability, and control as AI agents become part of everyday business infrastructure.



**Building the Future of AI Governance.**

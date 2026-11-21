# AGIS - AI Agent Governance & Inventory System



**Building the Future of AI Governance.**



> **No Owner. No Production.**



AGIS aims to become a centralized governance layer between AI innovation and enterprise operations.



## Overview



As organizations adopt AI agents, they need visibility and accountability over the systems operating within their environments.



AGIS is being developed as a centralized platform to help enterprises register, track, review, and govern AI agents throughout their lifecycle.



The goal is to make AI agent ownership, permissions, risk assessment, approval, and operational status more transparent and manageable.



## The Problem



AI agents can interact with APIs, databases, internal tools, and business systems. Without proper governance, organizations may face:



- Untracked or unauthorized AI agents.

- Unclear human accountability and ownership.

- Limited visibility into connected tools and permissions.

- Inconsistent risk assessment and approval processes.

- Difficulty maintaining governance records and audit trails.



## Our Approach



AGIS is designed around a simple principle:



**Every AI agent should have visibility, accountability, and appropriate governance before entering production.**



The platform aims to provide a centralized registry and governance workflow for enterprise AI agents.



## Prototype Capabilities



The current prototype includes working implementations of several core governance workflows:



| Capability | Prototype status |

|---|---|

| AI agent inventory | Implemented |

| Agent registration and details | Implemented |

| Role-based access control | Implemented and tested |

| Organization-level tenant isolation | Tested |

| Reviewer approval and rejection workflow | Implemented and tested |

| Separation of duties | Tested |

| Risk classification | Basic implementation |

| Operational status management | Implemented |

| Audit event recording | Implemented |



These capabilities are part of an early-stage prototype. They have not yet been validated as a production-ready enterprise security platform.



## Architecture



AGIS currently follows a modular backend architecture.



- **Frontend:** HTML, CSS, JavaScript

- **Backend:** Python and FastAPI

- **Database:** PostgreSQL

- **ORM:** SQLAlchemy

- **Authentication:** JWT-based authentication

- **API documentation:** OpenAPI / Swagger UI



The architecture is being developed to support future governance, discovery, and enterprise integration capabilities.



## Governance Principles



1. **Human accountability:** AI agents should have identifiable human ownership.

2. **Visibility:** Organizations should maintain an inventory of their AI agents.

3. **Controlled access:** Roles and permissions should govern platform actions.

4. **Review before production:** Agents should pass appropriate governance checks.

5. **Traceability:** Important governance actions should be recorded.



These are the project's design principles; not every principle is fully automated in the current prototype.



## Roadmap



Planned areas of development include:



- Stronger ownership enforcement.

- Developer-native agent registration through `agis.yaml`.

- Shadow AI discovery and agent inventory reconciliation.

- Runtime monitoring and policy enforcement.

- Deeper audit and compliance capabilities.

- Integration with enterprise identity and infrastructure.

- Cloud deployment and scalable multi-tenant operations.



## Project Status



**Early-stage working prototype - under active development.**



AGIS is not yet production-ready. Automated discovery, runtime monitoring, actual agent termination, and full enterprise integrations remain future development goals.



## Team Will of Dawn



- **Krishant Daimari** - Founder & Product Lead

- **Sumit Das** - Frontend Developer & API Integration

- **Gaurav R.** - Research & Data Analysis



## Vision



We believe the future of enterprise AI requires more than building intelligent agents. It requires infrastructure to understand, manage, and govern them responsibly.



**AGIS - Building the governance layer for the agentic enterprise.**

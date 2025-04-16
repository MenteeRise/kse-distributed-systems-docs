---
layout: default
title: Practical Project Development Plan
nav_order: 3
parent: Guides
has_children: false
permalink: /dev-plan/
---

# Practical Project Development Plan

{: .no_toc }

This document outlines the development plan for the practical project in the Distributed Systems course. The project is
a collaborative effort that will involve multiple students working together to build a distributed system using .NET
technologies.

<details open markdown="block">
  <summary>Table of Contents</summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Structure of the Project

For 12 weeks teams will work on a single project to achieve the course objectives. The project is divided into several
checkpoints (weeks 3, 6, 10 & 12). Each week also has its own milestone to be more transparent about the progress of the
project. Milestones are not graded and defined only for students' convenience.

## Project Overview

Throughout the course, teams of 4 students will collaborate to build a production-grade distributed system that
demonstrates the principles and patterns taught in the lectures. The project will involve:

- Designing and implementing a microservices architecture
- Building resilient, scalable, and maintainable services
- Implementing various communication patterns between services
- Deploying and monitoring the system in a containerized environment
- Demonstrating the system's ability to handle failures gracefully

## Grading System

The project will be evaluated across four checkpoints, with a total of 100 base points:

| Checkpoint | Week | Component                           | Points | Description                                                                                           |
|------------|------|-------------------------------------|--------|-------------------------------------------------------------------------------------------------------|
| 1          | 3    | Architecture and Design             | 20     | Architecture diagrams, service boundaries, API contracts, and design documentation                    |
| 2          | 6    | Implementation Quality              | 40     | Working core functionality demo, code implementation of critical services, technical debt assessment  |
| 3          | 10   | Production Practices                | 20     | Containerization, CI/CD pipeline, observability implementation, integration tests                     |
| 4          | 12   | Production Readiness & Presentation | 20     | Clarity of explanation, demonstration effectiveness, handling of questions, and professional delivery |

Additionally, teams can earn up to 40 bonus points by implementing advanced features (see Bonus Point System section).

## Checkpoints

### Checkpoint 1 (Week 3): Architecture Review

**Deliverables:**

- Complete C4 model diagrams showing services, datastores, and communication patterns
- Clear definition of service boundaries and responsibilities
- Comprehensive API documentation using OpenAPI/Swagger
- Data model with appropriate entity relationships
- Architectural Decision Records (ADRs) for critical design choices

**Evaluation Criteria:**

- Clear separation of concerns between services
- Appropriate choice of communication patterns
- Well-defined API contracts with examples
- Coherent data model supporting the domain
- Thoughtful architectural decisions with documented rationale

### Checkpoint 2 (Week 6): Implementation Progress

**Deliverables:**

- Implementation of core domain services
- Working inter-service communication
- Basic data persistence implementation
- Resilience patterns implementation (circuit breakers, retries)
- Technical debt assessment and plan

**Evaluation Criteria:**

- Quality of code implementation
- Effective use of .NET patterns and practices
- Appropriate error handling and resilience
- Working demonstration of key functionality
- Clear plan for addressing technical debt

### Checkpoint 3 (Week 10): Integration & Production

**Deliverables:**

- Containerized services with Docker
- CI/CD pipeline configuration
- Observability implementation (logging, metrics, tracing)
- Integration testing strategy
- Security implementations

**Evaluation Criteria:**

- Effective containerization of services
- Functional CI/CD pipeline
- Comprehensive monitoring and observability
- Thorough testing approach
- Appropriate security measures

### Checkpoint 4 (Week 12): Final Presentation

**Deliverables:**

- Complete working distributed system
- Comprehensive documentation
- Live demonstration of the system, including failure scenarios
- Technical presentation of architecture and implementation
- Q&A session

**Evaluation Criteria:**

- System completeness and functionality
- Quality of documentation
- Effective presentation and demonstration
- Ability to handle technical questions
- Overall architecture and implementation quality

## Weekly Milestones

- **Week 1: The Distributed Awakening**
    - Form project teams of 4 students
    - Set up development environment and collaboration tools
    - Create initial project repository with recommended structure
    - Draft initial project proposal document
    - Establish team communication channels

- **Week 2: Drawing the Battle Lines**
    - Conduct domain modeling workshop and event storming exercise
    - Create initial architecture diagrams using C4 model
    - Define service boundaries and responsibilities
    - Design preliminary API contracts
    - Document initial domain model

- **Week 3: Communication is Key** (Checkpoint 1)
    - Finalize architecture diagrams and service boundaries
    - Complete API contracts with OpenAPI/Swagger documentation
    - Define communication patterns between services
    - Prepare and deliver architecture review presentation
    - Submit architecture and design documentation

- **Week 4: Persistence Pays Off**
    - Design database schemas for all services
    - Implement data access layers and repositories
    - Configure Entity Framework Core or other data access technologies
    - Implement basic CRUD operations for core entities
    - Set up database migration strategy

- **Week 5: When Things Fall Apart**
    - Implement resilience patterns using Polly
    - Configure circuit breakers and retry policies
    - Add health check endpoints to all services
    - Implement fault tolerance mechanisms
    - Test the system with fault injection

- **Week 6: Consistency Conundrums** (Checkpoint 2)
    - Implement distributed data consistency mechanisms
    - Add saga pattern or compensating transactions where needed
    - Complete core service implementations
    - Demonstrate current functionality
    - Prepare and submit implementation progress report

- **Week 7: Seeing is Believing**
    - Implement structured logging with Serilog
    - Add distributed tracing with OpenTelemetry
    - Set up correlation IDs for request tracking
    - Configure metrics collection
    - Create basic monitoring dashboards

- **Week 8: Trust But Verify**
    - Implement integration tests for critical paths
    - Add contract tests using Pact.NET
    - Configure automated testing in the build process
    - Implement chaos testing with Simmy
    - Document testing strategy and coverage

- **Week 9: Ships in the Night**
    - Create Dockerfiles for all services
    - Configure Docker Compose for local development
    - Implement multi-container environment
    - Document containerization approach
    - Test containerized deployment

- **Week 10: Continuous Everything** (Checkpoint 3)
    - Set up CI/CD pipelines with GitHub Actions or Azure DevOps
    - Configure automated build, test, and deployment
    - Implement database migration automation
    - Add deployment environment configurations
    - Prepare and submit production practices implementation

- **Week 11: Scaling Horizons**
    - Implement distributed caching with Redis
    - Add load balancing with YARP
    - Conduct performance testing and optimization
    - Implement scaling strategies
    - Complete final system integration

- **Week 12: The Grand Finale** (Checkpoint 4)
    - Finalize all implementation and documentation
    - Prepare comprehensive project presentation
    - Rehearse system demonstration including failure scenarios
    - Deliver final presentation and demonstration
    - Submit complete project with all artifacts

## Suggested 12-Week Development Plan

This detailed plan aligns with the course structure and provides a practical roadmap for successful project completion:

| Week | Focus Area                  | Key Development Tasks                                                                                                                                                                                           | Preparation for Next Week                                                             |
|------|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| 1    | Project Foundation          | • Repository setup following recommended structure<br>• Team formation and role definition<br>• Development environment configuration<br>• Initial domain model draft                                           | • Study DDD principles<br>• Investigate potential service boundaries                  |
| 2    | Architecture Definition     | • Complete architecture diagram using C4 model<br>• Service boundary definitions<br>• Core domain model documentation<br>• Communication patterns defined (sync vs async)<br>• API design documentation         | • Prepare for architecture presentation<br>• Study RESTful API design principles      |
| 3    | Service Interfaces          | • API specifications using OpenAPI/Swagger<br>• Domain-driven design refinements<br>• API contract implementation for core services<br>• Architecture presentation preparation                                  | • Study database selection criteria<br>• Review data access patterns in .NET          |
| 4    | Data Foundation             | • Database schemas defined for all services<br>• Entity Framework Core configurations<br>• Data repository implementations<br>• Basic CRUD operations for core entities                                         | • Study resilience patterns<br>• Research Polly library                               |
| 5    | Resilience Implementation   | • Circuit breaker implementation with Polly<br>• Retry policies for service communication<br>• Timeout handling strategies<br>• Health check endpoints<br>• Fault injection testing                             | • Research distributed transaction patterns<br>• Study saga implementation approaches |
| 6    | Core Service Implementation | • Complete implementation of essential services<br>• Service communication working end-to-end<br>• Basic business logic implementation<br>• Technical debt assessment<br>• Implementation progress presentation | • Research observability tools<br>• Study structured logging approaches               |
| 7    | Observability Setup         | • Structured logging with Serilog<br>• Distributed tracing with OpenTelemetry<br>• Correlation IDs implementation<br>• Metrics collection foundations<br>• Centralized logging configuration                    | • Research testing strategies<br>• Study contract testing with Pact.NET               |
| 8    | Testing Strategy            | • Unit test suite implementation<br>• Integration tests for critical workflows<br>• Contract tests with Pact.NET<br>• Mock service implementations<br>• Chaos testing with Simmy                                | • Study Docker containerization<br>• Research container orchestration                 |
| 9    | Containerization            | • Dockerfiles for all services<br>• Docker Compose configuration<br>• Environment configuration management<br>• Local development container setup<br>• Container orchestration planning                         | • Research CI/CD pipeline options<br>• Study automated deployment approaches          |
| 10   | CI/CD Pipeline              | • GitHub Actions workflow implementation<br>• Automated build and test process<br>• Database migration strategy<br>• Deployment scripts<br>• Environment-specific configurations                                | • Study caching and performance optimization<br>• Research scaling strategies         |
| 11   | Performance & Scaling       | • Caching implementation with Redis<br>• Load balancing with YARP<br>• Performance testing results<br>• Scaling strategies documentation<br>• Bottleneck identification and resolution                          | • Prepare final presentation structure<br>• Plan system demonstration scenarios       |
| 12   | Production Ready            | • Final system integration<br>• Comprehensive documentation<br>• Full end-to-end demonstration<br>• Final presentation preparation<br>• Documentation of lessons learned                                        | • Celebrate your achievement!                                                         |

## Project Repository Structure

We recommend following this repository structure for your distributed systems project:

```
project-name/
├── .github/                # GitHub workflows and templates
├── docs/                   # Documentation and architecture artifacts
│   ├── architecture/       # C4 diagrams and ADRs
│   ├── api-contracts/      # API specifications
│   └── guides/             # Setup and operation guides
├── src/                    # All source code
│   ├── Services/           # Individual microservices
│   ├── BuildingBlocks/     # Shared libraries and components
│   ├── ApiGateways/        # API gateway implementations
│   └── Web/                # Web applications and UIs (Optional)
├── deploy/                 # Deployment configurations
│   ├── kubernetes/         # K8s manifests (if implementing bonus tasks)
│   ├── docker/             # Docker-related configurations
│   └── scripts/            # Deployment scripts
├── tests/                  # Test projects
├── docker-compose.yml      # Docker Compose configuration
└── README.md               # Project overview
```

## Bonus Point System

Teams can earn up to 40 additional points by implementing advanced distributed systems features beyond the core
requirements. Some examples include:

### Deployment & Orchestration (4-8 points per task)

- Kubernetes deployment with resource limits and health checks
- Service mesh implementation with mTLS
- GitOps workflow with ArgoCD/Flux
- Blue-Green/Canary deployment strategies

### Monitoring & Observability (3-6 points per task)

- ELK Stack integration with custom dashboards
- Grafana & Prometheus metrics system
- Advanced distributed tracing with custom spans
- Business metrics dashboard with KPI tracking

### Advanced Architecture (4-6 points per task)

- Event sourcing implementation
- CQRS pattern implementation
- Multi-region deployment with failover
- Real-time data updates with SignalR

### Data Management (4-6 points per task)

- Polyglot persistence implementation
- Database sharding
- Advanced caching strategies
- Zero-downtime data migration framework

### Security Enhancements (3-5 points per task)

- OAuth2 & OpenID Connect implementation
- Secret management solution
- Security scanning pipeline
- Advanced access control

To receive bonus points, teams must:

1. Fully implement the functionality within their project
2. Document the implementation with architecture diagrams, code explanations, and rationale
3. Demonstrate the feature during a dedicated bonus feature review session
4. Submit evidence showing the feature working under relevant test conditions

## Suggested Project Ideas

While teams are free to propose their own projects, here are some suggestions that work well as distributed systems:

1. **HealthConnect**: A patient management system with appointment scheduling, medical records, and notification
   services

2. **EventSphere**: An event management platform with registration, payment processing, and communication services

Each of these domains naturally decomposes into multiple services with interesting communication patterns and data
consistency challenges.

## Resources and References

To support your project development, refer to these key resources:

1. **Course Learning Materials**: All lecture slides, code examples, and supplementary materials

2. **Recommended Reading**:
    - "Designing Data-Intensive Applications" by Martin Kleppmann
    - ".NET Microservices: Architecture for Containerized .NET Applications" by Microsoft
    - "Building Microservices" by Sam Newman
    - "Release It!" by Michael Nygard

3. **Tools and Libraries**:
    - Polly for resilience patterns: https://github.com/App-vNext/Polly
    - OpenTelemetry for observability: https://opentelemetry.io/
    - Docker and Docker Compose for containerization
    - GitHub Actions for CI/CD
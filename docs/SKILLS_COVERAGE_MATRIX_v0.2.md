# Skills Coverage Matrix

**Project:** Enterprise Order-to-Delivery & Logistics Intelligence Platform  
**Document:** Skills Coverage Matrix  
**Version:** 0.2  
**Status:** Draft — Baseline  
**Purpose:** Learning roadmap, project implementation tracker, and interview-readiness tracker

---

## 1. Purpose

This document defines the technical skills and engineering concepts that the project is expected to cover.

The project has two simultaneous objectives:

1. Build a realistic, enterprise-grade distributed full-stack platform.
2. Develop the engineering knowledge required to confidently discuss, design, implement, troubleshoot, and defend the system in technical interviews.

A technology or concept is not considered mastered merely because it appears in the codebase.

The target progression is:

**Learn → Understand Internals → Apply → Test → Analyze Trade-offs → Explain → Defend → Interview Ready**

---

## 2. Status Model

| Status | Meaning |
|---|---|
| 🔴 Not Started | Concept has not yet been studied |
| 🟡 Learning | Theory/concepts currently being studied |
| 🔵 Applied | Concept has been implemented in the project |
| 🟣 Advanced | Concept has been applied and deeper trade-offs/internals understood |
| 🟢 Interview Ready | Can independently explain, implement, troubleshoot and defend the concept |
| ⚪ Optional | May be evaluated depending on project requirements |
| ⚫ Rejected | Evaluated but intentionally not selected |

---

# 3. Java — Core Fundamentals

| Skill | Concepts to Cover | Project Application | Interview Depth | Status |
|---|---|---|---|---|
| OOP | Encapsulation, abstraction, inheritance, polymorphism | Domain and service design | Advanced | 🔴 |
| Classes & Objects | Constructors, object lifecycle | Domain objects | Advanced | 🔴 |
| Encapsulation | Access control, invariants | Domain entities | Advanced | 🔴 |
| Abstraction | Interfaces, abstract classes | Service/provider contracts | Advanced | 🔴 |
| Inheritance | IS-A relationships | Limited appropriate use | Advanced | 🔴 |
| Polymorphism | Runtime dispatch | Payment/carrier strategies | Advanced | 🔴 |
| Composition | HAS-A relationships | Domain/service composition | Advanced | 🔴 |
| Interfaces | Contracts/default/static methods | Provider abstractions | Advanced | 🔴 |
| Enums | State modeling | Order/shipment states | Intermediate | 🔴 |
| Records | Immutable data carriers | DTOs/value data | Intermediate | 🔴 |
| Generics | Bounds, wildcards, type erasure | Generic utilities | Advanced | 🔴 |
| Annotations | Metadata/reflection concepts | Spring integration | Intermediate | 🔴 |
| Exceptions | Checked/unchecked/custom exceptions | Business/application errors | Advanced | 🔴 |
| Immutability | Immutable objects, defensive copying | Value objects/configuration | Advanced | 🔴 |
| equals/hashCode | Equality contracts | Entities/value objects | Advanced | 🔴 |
| Comparable/Comparator | Ordering | Priority/selection logic | Intermediate | 🔴 |

### Interview Gate

- Explain the four pillars of OOP with examples from the project.
- Composition vs inheritance?
- Interface vs abstract class?
- How does polymorphism work internally?
- Why must `equals()` and `hashCode()` be consistent?
- What are the benefits of immutability?
- When should you use Java records?

---

# 4. Java Collections & Functional Programming

## Collections

| Skill | Project Application | Interview Depth | Status |
|---|---|---|---|
| ArrayList | Ordered collections | Internals/performance | 🔴 |
| LinkedList | Evaluate appropriate use | Trade-offs | 🔴 |
| HashMap | Fast lookup | Internal implementation | 🔴 |
| ConcurrentHashMap | Concurrent access | Advanced | 🔴 |
| HashSet | Uniqueness | Internal implementation | 🔴 |
| TreeMap | Ordered lookup | Complexity/trade-offs | 🔴 |
| PriorityQueue | Delivery task prioritization | Heap internals | 🔴 |
| Queue/Deque | Work processing | Concurrency/use cases | 🔴 |
| Collections complexity | Service performance | Big-O reasoning | 🔴 |

## Functional Programming

| Skill | Project Application | Interview Depth | Status |
|---|---|---|---|
| Lambdas | Processing/filtering | Advanced | 🔴 |
| Functional interfaces | Strategy/callback logic | Advanced | 🔴 |
| Method references | Cleaner transformations | Intermediate | 🔴 |
| Streams | Data transformations | Advanced | 🔴 |
| Collectors | Aggregation/reporting | Advanced | 🔴 |
| Optional | Service/API results | Best practices | 🔴 |
| Parallel streams | Evaluate carefully | Performance/trade-offs | 🔴 |

---

# 5. Java Multithreading & Concurrency

**Target:** Advanced

| Skill | Concepts | Project Application | Status |
|---|---|---|---|
| Threads | Thread lifecycle | Background processing | 🔴 |
| Runnable | Task execution | Worker tasks | 🔴 |
| Callable | Return-value tasks | Async processing | 🔴 |
| Future | Async results | Service processing | 🔴 |
| ExecutorService | Thread pools | Background workers | 🔴 |
| ThreadPoolExecutor | Pool configuration | Production tuning | 🔴 |
| CompletableFuture | Async workflows | Parallel operations | 🔴 |
| synchronized | Mutual exclusion | Inventory experiment | 🔴 |
| volatile | Visibility | Concurrency experiment | 🔴 |
| Lock | Explicit synchronization | Inventory/work coordination | 🔴 |
| ReentrantLock | Lock control | Concurrency experiment | 🔴 |
| Atomic classes | Lock-free operations | Counters/state | 🔴 |
| Semaphore | Concurrency limiting | Resource protection | 🔴 |
| CountDownLatch | Coordination | Integration/workflow tests | 🔴 |
| CyclicBarrier | Thread coordination | Learning experiment | 🔴 |
| BlockingQueue | Producer/consumer | Worker processing | 🔴 |
| ConcurrentHashMap | Concurrent state | Inventory/cache use case | 🔴 |

### Core Theory

- Race conditions
- Atomicity
- Visibility
- Ordering
- Java Memory Model
- Happens-before
- Deadlock
- Starvation
- Livelock
- Thread safety
- Lock contention

### Project Exercise

```text
Inventory = 10

Order A → reserve 7
Order B → reserve 6

Concurrent requests
        ↓
Race condition
        ↓
Incorrect inventory state
```

Then evaluate multiple solutions.

---

# 6. JVM & Runtime

| Skill | Concepts | Project Application | Status |
|---|---|---|---|
| JVM architecture | Runtime components | Application diagnosis | 🔴 |
| Class loading | Class loaders | Spring/runtime understanding | 🔴 |
| Heap | Object allocation | Performance analysis | 🔴 |
| Stack | Frames/local variables | Runtime understanding | 🔴 |
| Metaspace | Class metadata | JVM troubleshooting | 🔴 |
| Garbage Collection | GC algorithms/concepts | Performance | 🔴 |
| JIT | Runtime compilation | Performance | 🔴 |
| Memory leaks | Object retention | Troubleshooting | 🔴 |
| Heap dumps | Memory diagnosis | Production exercise | 🔴 |
| Thread dumps | Thread diagnosis | Production exercise | 🔴 |
| Profiling | CPU/memory analysis | Performance investigation | 🔴 |

---

# 7. Spring Framework & Spring Boot

| Skill | Concepts / Application | Interview Depth | Status |
|---|---|---|---|
| IoC / DI | Container and dependency management | Advanced | 🔴 |
| Bean lifecycle | Creation/init/destroy | Advanced | 🔴 |
| Bean scopes | Singleton/prototype/etc. | Intermediate | 🔴 |
| AOP / Proxies | Cross-cutting concerns | Advanced | 🔴 |
| Configuration | Java/YAML/properties | Advanced | 🔴 |
| Profiles | Local/test/prod | Intermediate | 🔴 |
| Auto-configuration | Spring Boot startup | Advanced | 🔴 |
| REST controllers | APIs | Advanced | 🔴 |
| DTOs | API contracts | Advanced | 🔴 |
| Validation | Input validation | Advanced | 🔴 |
| Exception handling | Consistent API errors | Advanced | 🔴 |
| Filters/interceptors | Cross-cutting concerns | Advanced | 🔴 |
| Actuator | Health/metrics | Production | 🔴 |

---

# 8. REST & API Engineering

| Skill | Project Application | Status |
|---|---|---|
| HTTP methods/status codes | REST APIs | 🔴 |
| REST principles | Service APIs | 🔴 |
| Idempotency | Order/payment APIs | 🔴 |
| Pagination | Orders/catalog | 🔴 |
| Filtering/sorting | Catalog/operations | 🔴 |
| API versioning | Public APIs | 🔴 |
| Error model | Standardized errors | 🔴 |
| Validation | Request validation | 🔴 |
| Rate limiting | Public APIs | 🔴 |
| API security | Authentication/authorization | 🔴 |
| OpenAPI | API documentation | 🔴 |

---

# 9. JPA / Hibernate

| Skill | Project Application | Status |
|---|---|---|
| Entity lifecycle | Order persistence | 🔴 |
| Persistence context | Transaction management | 🔴 |
| EntityManager | Persistence internals | 🔴 |
| Dirty checking | Updates | 🔴 |
| Lazy/eager loading | Relationships | 🔴 |
| N+1 problem | Order/item retrieval | 🔴 |
| Fetch joins | N+1 optimization | 🔴 |
| Cascading | Aggregate persistence | 🔴 |
| Orphan removal | Child lifecycle | 🔴 |
| Optimistic locking | Inventory/order concurrency | 🔴 |
| Pessimistic locking | Inventory concurrency | 🔴 |
| JPQL/native SQL | Queries | 🔴 |
| Transactions | Business operations | 🔴 |

---

# 10. PostgreSQL / Database Engineering

| Skill | Project Application | Status |
|---|---|---|
| Schema design | Orders/inventory/customers | 🔴 |
| Normalization | Transactional model | 🔴 |
| Denormalization | Performance cases | 🔴 |
| Keys/constraints | Data integrity | 🔴 |
| Indexes | High-volume queries | 🔴 |
| Composite indexes | Operations queries | 🔴 |
| Transactions | Order/payment/inventory | 🔴 |
| Isolation levels | Concurrency | 🔴 |
| Locks/deadlocks | Inventory/order | 🔴 |
| Query planner | Optimization | 🔴 |
| EXPLAIN | Query analysis | 🔴 |
| Connection pooling | Production services | 🔴 |
| Partitioning | Large datasets | 🔴 |
| Replication concepts | Scaling/availability | 🔴 |

---

# 11. Redis

| Skill | Project Application | Status |
|---|---|---|
| Caching | Catalog/operational reads | 🔴 |
| TTL | Temporary data | 🔴 |
| Cache-aside | Service caching | 🔴 |
| Eviction | Cache management | 🔴 |
| Distributed locking | Coordination where justified | 🔴 |
| Rate limiting | API protection | 🔴 |
| Cache invalidation | Data consistency | 🔴 |

---

# 12. Testing

## Unit Testing

- JUnit 5
- Mockito
- Parameterized tests
- Test doubles
- Assertions
- Mocking strategy
- Test isolation

## Integration Testing

- Spring Boot Test
- Testcontainers
- PostgreSQL
- Redis
- Kafka
- Real dependency testing

## API Testing

- REST API tests
- Contract testing concepts
- Validation/error scenarios

## End-to-End

```text
Place Order
   ↓
Payment
   ↓
Inventory
   ↓
Fulfillment
   ↓
Shipment
   ↓
Delivery
```

---

# 13. LLD / SOLID / Design Patterns

## SOLID

- Single Responsibility
- Open/Closed
- Liskov Substitution
- Interface Segregation
- Dependency Inversion

## Creational

- Factory
- Abstract Factory
- Builder

## Structural

- Adapter
- Decorator
- Facade
- Proxy

## Behavioral

- Strategy
- Observer
- State
- Chain of Responsibility
- Command
- Template Method

### Potential Project Applications

```text
Payment Providers       → Strategy / Factory / Adapter
Notification Providers  → Strategy / Factory
Order State             → State
Delivery Assignment     → Strategy
Pricing Rules            → Strategy / Chain
```

Patterns will only be introduced when justified by a requirement.

---

# 14. High-Level System Design

| Area | Concepts | Status |
|---|---|---|
| Scalability | Vertical/horizontal scaling | 🔴 |
| Load balancing | L4/L7 concepts | 🔴 |
| Stateless services | Horizontal scaling | 🔴 |
| Caching | Distributed caching | 🔴 |
| Database scaling | Replication/sharding | 🔴 |
| CAP | Distributed systems | 🔴 |
| Consistency | Strong/eventual | 🔴 |
| Availability | Redundancy/failover | 🔴 |
| Fault tolerance | Failure isolation | 🔴 |
| Retry | Transient failures | 🔴 |
| Circuit breaker | Dependency failures | 🔴 |
| Bulkhead | Resource isolation | 🔴 |
| Rate limiting | Traffic control | 🔴 |
| Distributed transactions | Saga/Outbox | 🔴 |
| Event-driven architecture | Kafka/events | 🔴 |
| Disaster recovery | RPO/RTO | 🔴 |

### Scaling Exercises

```text
1K orders/day
       ↓
100K orders/day
       ↓
1M orders/day
       ↓
10M orders/day
```

---

# 15. Microservices

| Skill | Project Application | Status |
|---|---|---|
| Service boundaries | Business domains | 🔴 |
| Bounded contexts | Domain architecture | 🔴 |
| Database per service | Data ownership | 🔴 |
| API communication | Service interaction | 🔴 |
| Async communication | Events | 🔴 |
| Service discovery | Distributed deployment | 🔴 |
| API Gateway | External entry point | 🔴 |
| Configuration | Distributed config | 🔴 |
| Resilience | Service failures | 🔴 |
| Distributed tracing | Request flows | 🔴 |

Potential domains:

```text
Identity
Customer
Catalog
Order
Payment
Inventory
Warehouse
Fulfillment
Shipment
Delivery
Tracking
Notification
Analytics
AI
```

Final service boundaries will be determined from requirements.

---

# 16. Kafka

## Fundamentals

- Broker
- Topic
- Partition
- Producer
- Consumer
- Consumer group
- Offset
- Replication
- Retention

## Advanced

- Partitioning strategy
- Ordering
- Consumer lag
- Rebalancing
- Retry
- Dead-letter patterns
- Idempotency
- Delivery semantics
- Schema evolution
- Transactions
- Exactly-once concepts

## Potential Project Events

```text
OrderCreated
PaymentAuthorized
InventoryReserved
OrderFulfilled
ShipmentCreated
ShipmentDispatched
DeliveryAssigned
ShipmentDelivered
```

---

# 17. AWS — Cloud Architecture

## Networking

```text
VPC
Subnets
Availability Zones
Route Tables
Internet Gateway
NAT Gateway
Security Groups
NACL
```

## Compute

```text
EC2
ECS
EKS
Lambda
```

## Storage

```text
S3
EBS
RDS
ElastiCache
```

## Messaging

```text
SQS
SNS
EventBridge
Kafka
```

## Application Delivery

```text
Route 53
ALB
CloudFront
```

## Security

```text
IAM
KMS
Secrets Manager
Parameter Store
```

## Observability

```text
CloudWatch
Logs
Metrics
Alarms
Dashboards
```

## Data Engineering

```text
Glue
S3
ETL
Data Catalog
Step Functions
```

Every service will follow:

```text
Problem
→ Candidate service
→ Alternatives
→ Decision
→ Implementation
→ Interview discussion
```

---

# 18. AWS Networking

Target architecture:

```text
                    VPC
                     │
          ┌──────────┴──────────┐
          │                     │
     Public Subnets        Private Subnets
          │                     │
      ALB / NAT           Services / DB
          │                     │
      Internet             Restricted
       Gateway              access
```

Topics:

- CIDR
- Subnetting
- Routing
- Internet Gateway
- NAT
- Security Groups
- NACL
- Availability Zones
- Public/private architecture

---

# 19. ECS / EKS

We will explicitly compare:

```text
EC2
ECS
EKS
Lambda
```

Topics:

- Containers
- ECS task definitions
- ECS services
- Fargate
- Kubernetes architecture
- Pods
- Deployments
- Services
- Ingress
- Scaling
- EKS networking

---

# 20. Lambda

Potential applications:

```text
S3 event processing
Lightweight asynchronous jobs
Scheduled operations
Data transformations
Automation
```

Topics:

- Cold starts
- Concurrency
- Timeout
- Memory
- Retries
- Event sources
- Idempotency

---

# 21. SQS / SNS / EventBridge

We will build a decision matrix based on:

- Ordering
- Replay
- Throughput
- Delivery semantics
- Fan-out
- Retention
- Consumer model
- Operational complexity

Kafka, SQS, SNS and EventBridge will be compared based on actual project requirements.

---

# 22. AWS Data Engineering

Target pipeline:

```text
Operational Services
        ↓
      Kafka
        ↓
       S3
        ↓
      Glue
        ↓
    ETL Jobs
        ↓
Analytics datasets
        ↓
Dashboards / AI / Reporting
```

Concepts:

- ETL
- ELT
- Batch processing
- Streaming
- Data lake
- Data catalog
- Partitioning
- Schema evolution
- Data quality
- Data lineage
- Pipeline reliability

---

# 23. AWS Step Functions

Potential use case:

```text
Order Reconciliation
        ↓
Validate
        ↓
Retrieve data
        ↓
Reconcile payment
        ↓
Reconcile inventory
        ↓
Persist result
        ↓
Notify
```

Topics:

- State machines
- Sequential workflows
- Parallel execution
- Branching
- Retry
- Error handling
- Workflow orchestration
- Orchestration vs choreography

---

# 24. Docker

| Skill | Project Application | Status |
|---|---|---|
| Images | Service packaging | 🔴 |
| Containers | Service execution | 🔴 |
| Dockerfile | Service builds | 🔴 |
| Layers | Image optimization | 🔴 |
| Volumes | Local dependencies | 🔴 |
| Networks | Local distributed system | 🔴 |
| Multi-stage builds | Production images | 🔴 |
| Image optimization | Deployment performance | 🔴 |
| Container security | Production hardening | 🔴 |

---

# 25. Kubernetes

Topics:

```text
Pod
Deployment
Service
Ingress
ConfigMap
Secret
Namespace
Volume
Readiness Probe
Liveness Probe
Startup Probe
HPA
Resource Requests
Resource Limits
Scheduling
Rolling Deployment
```

Project evolution:

```text
Microservices
      ↓
Kubernetes
      ↓
EKS
      ↓
AWS
```

---

# 26. Terraform

Topics:

```text
Provider
Resource
Variable
Output
Module
State
Backend
Dependency
Drift
Environment management
```

Target:

```text
Terraform
   ↓
VPC
   ↓
AWS Infrastructure
   ↓
Compute
   ↓
Databases
   ↓
Messaging
   ↓
Monitoring
```

Interview topics:

- Terraform state
- Remote state
- State locking
- Modules
- Drift
- Terraform vs CloudFormation

---

# 27. CI/CD

Target pipeline:

```text
Git Push
   ↓
Build
   ↓
Unit Tests
   ↓
Integration Tests
   ↓
Static Analysis
   ↓
Security Scan
   ↓
Docker Build
   ↓
Container Registry
   ↓
Deployment
   ↓
Smoke Tests
```

Topics:

- CI vs CD
- Artifact versioning
- Rolling deployment
- Blue/green
- Canary
- Rollback
- Secrets
- Pipeline security

---

# 28. Observability

## Logging

- Structured logging
- Correlation IDs
- Centralized logging

## Metrics

```text
Request rate
Latency
Error rate
CPU
Memory
Kafka lag
Queue depth
Database performance
```

## Tracing

```text
Customer Request
      ↓
API Gateway
      ↓
Order Service
      ↓
Kafka
      ↓
Inventory Service
      ↓
Fulfillment Service
```

Topics:

- Distributed tracing
- OpenTelemetry
- CloudWatch
- Metrics
- Alerts
- Dashboards
- Incident diagnosis

---

# 29. React

## Core

- Components
- Props
- State
- Hooks
- Context
- Refs
- Component composition

## Rendering

- Rendering model
- Reconciliation concepts
- Memoization
- Rendering performance

## Advanced

- Lazy loading
- Code splitting
- Error boundaries
- Performance optimization
- Accessibility

Project applications:

```text
Customer Application
Operations Application
```

---

# 30. TypeScript

Topics:

```text
Types
Interfaces
Generics
Union types
Intersection types
Type narrowing
Utility types
Async types
API models
```

TypeScript will be used throughout the frontend.

---

# 31. Frontend Architecture

Topics:

- UI state
- Server state
- API layer
- Authentication
- Authorization
- Caching
- Forms
- Validation
- Error handling
- Accessibility
- Performance

State-management and server-state technologies will be selected based on requirements.

---

# 32. Frontend Testing

Topics:

- Component testing
- Integration testing
- User interaction testing
- API mocking
- End-to-end testing

Critical workflows:

```text
Browse
 ↓
Cart
 ↓
Checkout
 ↓
Order
 ↓
Tracking
 ↓
Return
```

---

# 33. Micro-Frontends

This is an evolutionary/optional architecture decision.

Topics:

- Why micro-frontends?
- Independent deployment
- Module federation concepts
- Shared dependencies
- Cross-application communication
- Versioning
- Runtime integration
- Organizational boundaries

Potential evolution:

```text
Operations Shell
       │
 ┌─────┼──────┐
 ↓     ↓      ↓
Orders Inventory Delivery
 MF       MF      MF
```

We will first determine whether micro-frontends provide genuine value.

---

# 34. Security

## Application Security

- Authentication
- Authorization
- RBAC
- JWT
- OAuth2/OIDC concepts
- Password security
- API security

## Infrastructure Security

- IAM
- Least privilege
- Network security
- TLS
- Encryption
- Secrets management
- Key management

## Distributed Security

- Service-to-service authentication
- API Gateway security
- Event security
- Tenant isolation

## AI Security

- Prompt injection
- Tool authorization
- Data leakage
- Unauthorized retrieval
- Sensitive information exposure

---

# 35. AI Engineering

AI is a **first-class product capability**.

## LLM Fundamentals

- Tokens
- Context windows
- Temperature
- Structured output
- Latency
- Cost
- Model selection

## RAG

```text
Documents
    ↓
Chunking
    ↓
Embeddings
    ↓
Vector Store
    ↓
Retrieval
    ↓
LLM
```

Topics:

- Chunking
- Embeddings
- Vector search
- Retrieval
- Reranking
- Grounding
- Citation
- Retrieval evaluation

## Tool Calling

Potential tools:

```text
Order Tool
Tracking Tool
Inventory Tool
Shipment Tool
Analytics Tool
Knowledge Tool
```

## Agents

Potential Operations Agent:

```text
Operations Manager
       ↓
      Agent
       ├── Orders
       ├── Inventory
       ├── Shipments
       ├── Analytics
       └── Knowledge
```

## Predictive AI

Potential capabilities:

```text
ETA prediction
Delivery risk prediction
Warehouse overload prediction
Demand forecasting
```

---

# 36. AI Reliability & Evaluation

Topics:

- Hallucination
- Grounding
- Retrieval quality
- Evaluation datasets
- Structured outputs
- Tool validation
- Prompt injection
- AI observability
- Cost monitoring
- Latency
- Model fallback
- Human-in-the-loop

---

# 37. Data Structures & Algorithms

DSA will be maintained as a parallel interview track.

Project-related opportunities:

```text
Inventory allocation
Delivery assignment
Priority queues
Scheduling
Searching
Sorting
Caching
Route selection
Graph concepts
Concurrency
```

Separate interview practice will cover:

- Arrays
- Strings
- Hashing
- Linked lists
- Stacks
- Queues
- Trees
- Heaps
- Graphs
- Recursion
- Backtracking
- Binary search
- Sliding window
- Two pointers
- Greedy
- Dynamic programming
- Big-O analysis

---

# 38. Interview Readiness Framework

Every major skill must pass through:

```text
                THEORY
                   ↓
              INTERNALS
                   ↓
             PROJECT USAGE
                   ↓
              TRADE-OFFS
                   ↓
             FAILURE MODES
                   ↓
          INTERVIEW QUESTIONS
                   ↓
             CODING/DESIGN
                   ↓
              ASSESSMENT
                   ↓
          🟢 INTERVIEW READY
```

---

# 39. Interview Gates

## Gate 1 — Java
Theory + coding + debugging + concurrency.

## Gate 2 — Spring Boot
Framework internals + REST + persistence + transactions + security.

## Gate 3 — Database
SQL + schema + indexes + transactions + locking.

## Gate 4 — LLD
Design a subsystem independently.

## Gate 5 — HLD
Design the complete platform under scale/failure constraints.

## Gate 6 — Kafka
Architecture + failure scenarios + troubleshooting.

## Gate 7 — AWS
Cloud architecture + networking + service selection.

## Gate 8 — Docker/Kubernetes
Containerization + deployment + troubleshooting.

## Gate 9 — React
Frontend architecture + rendering + performance + testing.

## Gate 10 — AI
RAG + agents + tool calling + AI system design + security/evaluation.

---

# 40. Evidence of Mastery

For important skills, evidence will be maintained across multiple dimensions.

## Kafka

```text
Theory                  ⬜
Implementation          ⬜
Architecture            ⬜
Failure experiment      ⬜
Testing                 ⬜
Performance analysis    ⬜
ADR                     ⬜
Interview questions     ⬜
Interview assessment    ⬜
```

## Java Concurrency

```text
Theory                  ⬜
Coding exercises        ⬜
Inventory application   ⬜
Race-condition demo     ⬜
Failure analysis        ⬜
Interview questions     ⬜
Assessment              ⬜
```

---

# 41. Technology Decision Principle

The project will not use a technology merely because it appears in this matrix.

The decision process is:

```text
Business Requirement
        ↓
Technical Requirement
        ↓
Candidate Technologies
        ↓
Trade-off Analysis
        ↓
Architecture Decision
        ↓
Implementation
```

Example:

```text
Need:
Reliable asynchronous processing

Candidates:
Kafka
SQS
SNS
EventBridge

        ↓

Evaluate:
Ordering
Replay
Throughput
Fan-out
Retention
Operational complexity

        ↓

Document decision in ADR
```

This principle applies to AWS, databases, messaging systems, frontend libraries, AI infrastructure and architecture patterns.

---

# 42. Current Overall Status

| Category | Status |
|---|---|
| Java | 🔴 |
| Concurrency | 🔴 |
| JVM | 🔴 |
| Spring Boot | 🔴 |
| REST/API | 🔴 |
| JPA/Hibernate | 🔴 |
| PostgreSQL | 🔴 |
| Redis | 🔴 |
| Testing | 🔴 |
| LLD | 🔴 |
| HLD | 🔴 |
| Microservices | 🔴 |
| Kafka | 🔴 |
| AWS | 🔴 |
| Data Engineering | 🔴 |
| Docker | 🔴 |
| Kubernetes | 🔴 |
| Terraform | 🔴 |
| CI/CD | 🔴 |
| Observability | 🔴 |
| React | 🔴 |
| TypeScript | 🔴 |
| Micro-frontends | 🔴 |
| Security | 🔴 |
| AI/RAG/Agents | 🔴 |
| DSA | 🔴 |

**Note:** All statuses are intentionally 🔴 because the project has not yet entered the learning/implementation phase. This is a baseline, not an assessment of existing knowledge.

---

# 43. Definition of Project Completion

The project will not be considered complete merely because the application runs.

Completion requires:

### Product
- End-to-end order-to-delivery workflow

### Backend
- Strong Java/Spring Boot implementation

### Data
- Transactional database
- Caching
- Event/data platform

### Architecture
- LLD
- HLD
- Distributed systems
- Microservices
- Event-driven architecture

### Cloud
- Significant AWS implementation

### DevOps
- Docker
- Kubernetes/EKS
- Terraform
- CI/CD
- Observability

### Frontend
- Customer application
- Operations application
- React/TypeScript
- Testing
- Performance

### AI
- RAG
- Tool calling
- Agents
- Intelligent predictions
- AI security/evaluation

### Interview
The user should be able to independently explain and defend:

- What was built
- Why it was built this way
- Alternative approaches
- Technology trade-offs
- Failure scenarios
- Scaling strategy
- Security model
- Observability strategy
- Deployment strategy
- AI architecture and limitations

---

# 44. Document Maintenance Rules

This document is a living artifact.

It will be updated when:

- A new skill is discovered.
- A technology is added or removed.
- A project requirement creates a new learning opportunity.
- A concept reaches a new mastery level.
- An interview gate is completed.
- A technology is evaluated and rejected.
- The project architecture changes.

Major changes should be committed to Git with an explanatory commit message.

Example:

```text
docs: expand skills coverage for data engineering
```

or:

```text
docs: add AI engineering interview track
```

The matrix should always reflect the current intended project coverage.

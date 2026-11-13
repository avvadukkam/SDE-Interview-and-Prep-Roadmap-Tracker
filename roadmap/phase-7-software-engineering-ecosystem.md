# Phase 7: Software Engineering Ecosystem

**Difficulty:** Advanced | **Estimated Duration:** 3–4 Weeks | **Topics:** 5

> **Overview:** Consolidates Cloud, DevOps & Infrastructure (Section 3), Security Engineering & Authentication (Section 11), and Testing, Reliability & Observability (Section 14) into the production engineering ecosystem.

## Why This Phase Is Ordered Here
Once you understand how distributed systems are designed (Phase 6), Phase 7 teaches how they are deployed, containerized, secured, monitored, and operated in cloud production environments.

## Topics in This Phase

### 7.1 Cloud Computing, Compute, Storage & Cloud Networking
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers IaaS/PaaS/SaaS, regions/AZs, RTO/RPO disaster recovery, VPC networking, IAM least privilege, compute choices (EC2, ECS/Fargate, EKS, Lambda), and managed storage (S3, EBS, EFS, RDS, DynamoDB, ElastiCache).
- **Why It Is Important:** Modern backend systems run on cloud primitives; interviews test practical trade-offs like Serverless vs. Containers and S3 vs. EBS.
- **Completion Criteria:** Can compare cloud compute/storage options and design secure VPC/IAM topologies.

- [ ] Cloud fundamentals: Regions, Availability Zones, High Availability vs. Disaster Recovery (RTO & RPO), IaaS/PaaS/SaaS — `P1`
- [ ] Compute decisions: EC2 vs. ECS/Fargate vs. EKS vs. AWS Lambda (triggers, cold starts, concurrency, idempotency) — `P0`
- [ ] Storage decisions: EBS vs. EFS vs. S3 (versioning, lifecycle, presigned URLs), RDS/Aurora failover, DynamoDB, ElastiCache — `P0`
- [ ] Cloud Networking & Identity: VPC, public/private subnets, NAT/IGW, Security Groups vs. NACLs, IAM roles & temporary credentials — `P1`
- [ ] Cost & Capacity: Capacity planning (throughput/p95), Reserved vs. On-Demand vs. Spot, multi-region drills — `P1`

### 7.2 Docker Containerization & Kubernetes Orchestration
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers Docker images, layers, multi-stage builds, container security/isolation, and Kubernetes architecture (Pods, Deployments, Services, Ingress, ConfigMaps/Secrets, Probes, HPA, and troubleshooting).
- **Why It Is Important:** Containers and Kubernetes are the industry standard for packaging and scaling backend services.
- **Completion Criteria:** Can write optimized multi-stage Dockerfiles and troubleshoot Kubernetes Pod/Deployment lifecycles.

- [ ] Docker: Images, layers, registries, Dockerfiles, multi-stage builds, build caching, and non-root container security — `P0`
- [ ] Container networking, volumes, cgroups resource limits, and namespace isolation — `P1`
- [ ] Kubernetes Core: Pods, Deployments, ReplicaSets, Services, Ingress, ConfigMaps, Secrets, Namespaces, and RBAC — `P0`
- [ ] Kubernetes Operations: Liveness/Readiness/Startup probes, resource requests/limits, HPA, StatefulSets, and debugging CrashLoopBackOff — `P0`

### 7.3 CI/CD Release Engineering & Infrastructure as Code (IaC)
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `8 hrs`
- **What It Covers:** Covers automated build/test/deploy pipelines, GitHub Actions, safe deployment strategies (Blue-Green, Canary, Rolling, Feature Flags), backward-compatible DB migrations, and Terraform/CDK IaC.
- **Why It Is Important:** Shipping code safely without downtime requires automated quality gates, progressive rollouts, and reproducible infrastructure.
- **Completion Criteria:** Can design CI/CD pipelines and explain Expand-and-Contract database migrations and Canary rollouts.

- [ ] CI/CD pipelines, quality gates, and GitHub Actions (workflows, runners, permissions, artifacts) — `P1`
- [ ] Zero-downtime releases: Blue-Green, Canary, Rolling deployments, Feature Flags, and safe backward-compatible DB migrations — `P0`
- [ ] Infrastructure as Code (IaC): Terraform vs. CloudFormation/CDK, remote state locking, drift detection, secrets handling — `P1`
- [ ] Supply-chain security, dependency scanning, and artifact provenance — `P2`

### 7.4 Security Engineering, AuthN/AuthZ & Cryptography
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers Authentication vs. Authorization, OAuth 2.0 + PKCE, OIDC, JWTs, Sessions/Cookies, RBAC/ABAC, OWASP Top 10 (SQLi, XSS, CSRF, SSRF, BOLA/IDOR), TLS/mTLS, and password/data encryption.
- **Why It Is Important:** Security vulnerabilities can compromise an entire company; every backend engineer must know how to authenticate requests and prevent OWASP Top 10 attacks.
- **Completion Criteria:** Can design secure AuthN/AuthZ flows, explain TLS & Argon2/bcrypt, and mitigate OWASP Top 10 vulnerabilities.

- [ ] AuthN & AuthZ: Sessions/Cookies (HttpOnly, Secure, SameSite) vs. JWTs (claims, signature, rotation), OAuth 2.0 (Auth Code + PKCE), OIDC, SSO/MFA/Passkeys — `P0`
- [ ] Access Control: RBAC vs. ABAC, Broken Object-Level Authorization (BOLA/IDOR), and service-to-service workload identity — `P0`
- [ ] Application Security & OWASP Top 10: SQL/NoSQL Injection, XSS & CSP, CSRF, SSRF, CORS, rate limiting, and safe deserialization — `P0`
- [ ] Cryptography & Data Protection: TLS/mTLS handshake, symmetric vs. asymmetric encryption, envelope encryption, KMS, password hashing (Argon2/bcrypt + salt) — `P0`
- [ ] Threat modeling (STRIDE), least privilege, SAST/DAST/SCA, and tamper-evident security audit logs — `P1`

### 7.5 Observability, Performance Optimization & Reliability (SRE)
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers the 3 pillars of observability (Structured Logs, Metrics, Distributed Tracing with OpenTelemetry), RED/USE methods, SLIs/SLOs/SLAs, error budgets, resilience patterns (retries with jitter, backpressure, circuit breakers), load testing, and incident response.
- **Why It Is Important:** Designing reliable systems requires knowing how to measure p99 latency, correlate traces across services, and prevent retry storms during outages.
- **Completion Criteria:** Can define SLIs/SLOs, instrument logs/metrics/traces, and prevent cascading failures with jittered retries and circuit breakers.

- [ ] Three Pillars of Observability: Structured Logging (correlation IDs), Metrics (cardinality, histograms), and Distributed Tracing (OpenTelemetry spans) — `P0`
- [ ] Monitoring methodologies: RED (Rate, Errors, Duration), USE (Utilization, Saturation, Errors), and burn-rate alerting — `P1`
- [ ] SRE & Resilience: SLIs, SLOs, SLAs, Error Budgets, Exponential Backoff with Jitter, Circuit Breakers, Bulkheads, Graceful Degradation — `P0`
- [ ] Performance Engineering: Load vs. Stress vs. Soak vs. Spike testing, p50/p95/p99 tail latency, CPU/memory/DB query profiling — `P0`
- [ ] Incident Excellence: Triage, mitigation, rollback, root-cause analysis, and blameless postmortems — `P1`

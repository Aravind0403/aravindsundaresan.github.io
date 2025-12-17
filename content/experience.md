---
title: "Experience"
weight: 1
---

# Experience

---

## Microsoft R&D India

**Software Engineer II**
*Aug 2021 – 

### What I worked on

At Microsoft, I worked on internal infrastructure platforms used across 17,000+ microservices, with a focus on data integrity, reliability, and developer productivity at scale.

My primary responsibility was building and scaling a **Distributed Metadata Correction Platform** — a self-healing, event-driven system designed to maintain consistency across Microsoft’s service inventory during burst traffic and failure scenarios.

---

### Distributed Metadata Correction Platform

This platform continuously validated and corrected service metadata across Microsoft’s internal ecosystem. It was explicitly designed to handle retry storms, partial failures, and high-concurrency updates without human intervention.

**Key architectural decisions & impact:**
* **Event-driven architecture:** Designed a 3-layer system — ingestion, compute, and persistence — using Azure Service Bus, Azure Functions, and Cosmos DB, capable of processing millions of metadata events.
* **Concurrency & data integrity:** Introduced adaptive concurrency control after observing repeated retry storms in production. The system dynamically favored optimistic updates (≈95%), falling back to pessimistic locking (≈5%) for high-conflict paths using Redis, E-Tags, and Cosmos DB transactional semantics.
* **Resilience under burst traffic:** Implemented traffic reshaping and backoff strategies to absorb sudden spikes without cascading failures, achieving 99.9%+ metadata consistency.
* **Observability & diagnostics:** Integrated Azure Data Explorer (Kusto) to enable deep root-cause analysis across service boundaries, significantly reducing mean-time-to-diagnosis during incidents.

---

### Developer Productivity & Platform Tooling

Alongside core infrastructure work, I focused heavily on reducing developer toil:
* Built internal tooling that cut environment setup time from 60+ minutes to under 20 minutes
* Automated validation and correction workflows, reducing manual service audits by ~70%
* Designed admin tools for enforcing data hygiene across thousands of services
* Contributed to “test-in-production” telemetry patterns to improve observability for Windows platform teams
* Mentored teams and ran office hours to drive adoption of reliability and telemetry best practices

**Tech Stack:**
C#, Azure (Service Bus, Functions, Cosmos DB, Redis), Kusto, PowerApps, CI/CD, Event-driven systems

---

## Amazon

**Software Development Engineer**
*Sep 2017 – Jul 2021*

### What I worked on

At Amazon, I was a core engineer on the Alexa Device Farm Infrastructure, responsible for enabling deterministic, repeatable testing across physical Alexa devices running 24/7.

The challenge was fundamentally different from pure software systems: physical devices fail unpredictably, and flaky tests were blocking releases.

---

### Alexa Device Farm Infrastructure

I helped design and build a platform that orchestrated, diagnosed, and tested 100+ physical devices (Echo, Fire Tablets, Fire devices) continuously.

**Key contributions:**
* **Device orchestration platform:** Designed a multi-layer system managing device lifecycle, health checks, provisioning, and diagnostics for long-running physical test fleets.
* **Deterministic automation:** Converted 80–85% of manual test cases (from sanity to E2E) into automated, deterministic test suites, significantly accelerating release cycles.
* **Reliability improvements:** Introduced signature-based failure classification, reducing false positives from ~40% to ~15% and improving overall platform uptime to 98%+.
* **Operational efficiency:** Automated device provisioning and Wi-Fi registration, saving 1,000+ QA hours annually and reducing daily setup overhead for engineers.
* **CI/CD integration:** Integrated automated validation into pipelines to enable faster, more reliable build qualification for hardware-software integration.

**Tech Stack:**
Java, Python, AWS (EC2, Lambda), Docker, Device Automation, CI/CD

---

## OMG Labs

**Founding Engineer / Early Team Member**

At OMG Labs, I worked in an early-stage startup environment wearing product, engineering, and execution hats.
* Led end-to-end delivery from strategy and design to implementation and deployment
* Helped drive a subscription-based customer acquisition model, increasing traffic by 15–20%
* Integrated e-commerce tooling (search, email marketing), improving digital engagement by 25–35%
* Played a key role in securing Amazon Launchpad selection, enabling international exposure
* Coordinated across product, marketing, and engineering teams to ensure fast, agile execution

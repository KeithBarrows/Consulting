---
title: Modern Logging & Observability (Structured Logging)
author: Keith Barrows
tags: [logging, observability, OpenTelemetry, OTel, structured logging, JSON logs, NoSQL logging, architecture, .NET]
---

# Modern Logging & Observability

NoSQL-style logging in software is typically referred to as **Structured Logging**, where logs are treated as dynamic, key-value, or JSON-based documents rather than flat strings. It enables flexible schemas, high-volume ingestion, and efficient searching, often integrated within modern Observability frameworks to track live, real-time events alongside historical data.

This approach allows engineering teams to not just look at raw files, but to query complex behavioral patterns across distributed systems, which is the core of modern observability.

*- Note: Keith Barrows is highly passionate about this architectural approach.*

---

## Key Concepts in Modern Logging & Observability

### Structured Logging (JSON/Document Logs)
Instead of a plain text message, logs are emitted as structured data (e.g., JSON), allowing for complex querying of fields like `user_id` or `request_duration`.

### OpenTelemetry (OTel)
An open-source standard for collecting, processing, and exporting logs, metrics, and traces (telemetry) to observability backends. OTel allows logging to be structured and correlated with trace IDs for tracing requests across microservices.

### Log Management / Observability Platforms
* **Live Tracking (Real-time):** Tools like Datadog, Dynatrace, or Grafana Loki are used for live tailing, tail-based sampling, and real-time alerting.
* **Historical Analysis (Long-term Data):** Often stored in NoSQL-like systems like Elasticsearch (ELK Stack), ClickHouse, or managed cloud storage for cost-effective analysis over long periods.

### Log Pipelines (OTel Collector)
The OpenTelemetry Collector sits between applications and storage to process, filter, and enrich logs with metadata (e.g., Kubernetes pods) before storing them.

---

## Common "NoSQL-Style" Log Data Models

* **JSON-based:** `{ timestamp: ..., level: info, service: auth, metadata: {...} }`
* **Document-oriented:** Stored in Elasticsearch or MongoDB for flexible schema evolution.

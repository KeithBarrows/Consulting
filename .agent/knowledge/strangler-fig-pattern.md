---
title: System Migration Strategy - The Strangler Fig Pattern
author: Steve "ardalis" Smith & Martin Fowler
tags: [architecture, .NET, modernization, migration, DDD, refactoring, "Strangler Fig Pattern", "Strangler Application Pattern", "Incremental Migration Pattern", "Migration Pattern"]
---

# The Strangler Fig Pattern (Steve Ardalis Context)

The primary term and process name for successfully migrating a mission-critical system to a new technical stack is the **Strangler Fig Pattern** (or Strangler Application Pattern). Championed by architectural experts like Steve "ardalis" Smith, this approach allows for an incremental migration rather than a high-risk "big bang" rewrite.

## Definition
Coined by Martin Fowler and frequently advocated in modern .NET modernization (including by Ardalis/NimblePros), this pattern involves replacing specific functionality with a new service/system, one piece at a time.

## Process
A facade or proxy layer is placed between the users and the legacy system to intercept requests and route them to either the old or new system, allowing the new system to grow around the old one until it can be decommissioned.

## Ardalis Application
Steve Smith frequently discusses incremental migration, specifically moving from ASP.NET Framework to .NET Core/6+ using this, often using tools like System.Web Adapters to assist.

---

# Key Components for Success
Based on common practices advocated in this space (and highlighted in AWS guidance supported by practitioners like Ardalis):

* **Anti-Corruption Layer (ACL):** A Facade pattern used to ensure the old system can communicate with the new system without breaking, by translating data formats between the two.
* **Phased Coexistence:** Rather than replacing the whole system, you migrate piece by piece, allowing them to run in parallel.
* **Domain-Driven Design (DDD):** Used to identify the correct boundaries for the new, smaller services (microservices).

---

# Other Relevant "R" Strategies
While "Strangler Fig" is the process name, it falls under the broader, more technical category of Refactoring (or Re-architecting) within the **7 Rs of migration**.

* **Replatforming:** Often called "lift, tinker, and shift," this is a more moderate approach to modernizing, such as containerizing an app without changing its code.

---

# Steve Ardalis Resources
* **Blog/Books:** [ardalis.com](https://ardalis.com) offers resources on refactoring and modernization.
* **Reference App:** *eShopOnWeb* (maintained by Ardalis) is used to demonstrate modern .NET architectures.
* **Podcast:** In *SE Radio 637*, Steve Smith discusses these migration challenges with clients.

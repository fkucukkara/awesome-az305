# Awesome AZ-305

A short, read-only study guide for **Exam AZ-305: Designing Microsoft Azure Infrastructure Solutions**.

No labs. No deployments. No cost. Just what you need to understand and remember to pass.

> Based on the Microsoft AZ-305 skills measured **as of April 17, 2026**.
> Source of truth: [Microsoft study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/az-305).

## Who is this for

Engineers and administrators who already know Azure and want a fast, exam-focused pass over everything AZ-305 tests, including the traps. AZ-305 is a **design** exam: you recommend the right service and justify it. A companion repo for the prerequisite exam is **Awesome AZ-104**.

## What every topic answers

1. **What is it?**
2. **When do I recommend it (and over what)?**
3. **What could the exam trick me about?**

## Layout

| Domain | Weight (official) | Folder |
|---|---|---|
| Design identity, governance, and monitoring solutions | 25–30% | [01-identity-governance-monitoring](01-identity-governance-monitoring/README.md) |
| Design data storage solutions | 20–25% | [02-data-storage](02-data-storage/README.md) |
| Design business continuity solutions | 15–20% | [03-business-continuity](03-business-continuity/README.md) |
| Design infrastructure solutions | 30–35% | [04-infrastructure](04-infrastructure/README.md) |

Also:

- [EXAM-GUIDE.md](EXAM-GUIDE.md): verified exam facts and how to prepare
- [DECISION-MATRICES.md](DECISION-MATRICES.md): which service when, side by side
- [CASE-STUDY-GUIDE.md](CASE-STUDY-GUIDE.md): how to read case studies and design questions, Well-Architected and CAF mapping
- [QUICK-REVISION.md](QUICK-REVISION.md): one-pass review for the last days
- [EXAM-DAY-CHECKLIST.md](EXAM-DAY-CHECKLIST.md): how to read questions, last-hour list
- [references/microsoft-resources.md](references/microsoft-resources.md): official links and the objective-to-section coverage map

## Recommended study order

1. [EXAM-GUIDE.md](EXAM-GUIDE.md) (10 minutes)
2. [CASE-STUDY-GUIDE.md](CASE-STUDY-GUIDE.md) (15 minutes), so you study with the right mindset
3. Identity, governance and monitoring, then **Infrastructure** (networking and compute reappear everywhere), then Data storage, then Business continuity
4. Re-do the **Quick Check** questions in each domain and learn the **decision tables**
5. Take Microsoft's free [practice assessment](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-305/practice/assessment?assessment-type=practice&assessmentId=15)
6. Read [DECISION-MATRICES.md](DECISION-MATRICES.md) and [QUICK-REVISION.md](QUICK-REVISION.md) in the final week
7. Read [EXAM-DAY-CHECKLIST.md](EXAM-DAY-CHECKLIST.md) the day before

## How to read a domain file

Each topic has the same blocks:

- **What is it?** plain explanation and a mental model or architecture diagram
- **Know for AZ-305**: only what the exam needs, with decision tables
- **Common confusion**: pairs of services people mix up
- **Exam trap**: marked with `[!WARNING]`
- **Remember**: one-line takeaways

Each domain ends with **Scenarios** and **Quick Checks**. The top of each file has **Know This** (memorize) and **Understand This** (reason about it).

## Scope

This is a conceptual guide. Hands-on practice helps, and Microsoft recommends it, but it is deliberately outside this repo. Commands appear only where they clarify a concept.

Quick Check questions are original. They are **not** real exam questions.

## Found an error?

Azure changes often (services are retired and renamed). Open an issue and link the Microsoft Learn page that shows the correct behavior.

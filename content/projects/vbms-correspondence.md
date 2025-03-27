---
title: "Rebuilding VBMS Correspondence Web Service"
date: 2019-03-15
author: "Mike Wilcome"
---

## Facing the Monolith Monster

Back at Booz Allen Hamilton, from September 2015 to March 2019, I took on a large project: the *VBMS Correspondence Web Service*. When I started, it was a mess—**20+ modules** tangled up in a large monolithic app, part of an even bigger system for the Veterans Affairs. I had to rebuild it, and make it work for vets needing their benefits. Over the years, I led the charge to split it out into its own service, rewriting it as a lean **Jersey** and **Spring Boot** microservice, with a sprinkle of **Groovy** for good measure. This resulted in a streamlined system that churned out formatted PDF documents from requests, cutting through the VA’s correspondence mess.

---

### The Turnaround: Sweat and Code

This wasn’t a quick fix. That original setup was a nightmare—20+ modules of business logic baked into a sprawl that could choke a server. We didn’t just patch it; we reimagined it. By the end, I’d whittled it down to **two microservices**, running on the latest **Java 17**, and—get this—**100% unit tested**. Every line of code had to prove itself, and it did. I even wrote detailed docs on the tech stack, laying out the roadmap so my team could keep it humming. It’s bigger than it looks on paper, but seeing it go from a tangled mess to a tight, reliable service was pure gold.

> **Real Impact**: This wasn’t just tech for tech’s sake. VBMS Correspondence handles *all* VA mail—every letter, every notice vets rely on for benefits. My team and I made that happen, and it’s still helping folks today—check out [VA’s take](https://www.va.gov/vetdata/docs/SpecialReports/VBMS_Overview.pdf) on how VBMS transformed claims.

---

### Tools That Tamed It

Here’s what I was directed to use:
- **Jersey & Spring Boot**: The backbone—fast, modern, and built to scale.
- **Groovy**: Tossed in some scripting spice to smooth out the edges. (mixed with java yes)
- **Java 7 and 8 and 11**: Kept it cutting-edge, leveraging the latest features. (at the time)
- **Unit Tests**: 100% coverage—nothing slipped through the cracks.

---

### The Payoff: Awards and Pride

As a result of my effort, I received a **Team and Performance Award** for leading the crew, and an **Innovation in Action Award** for rethinking the whole thing. It’s one of my proudest wins—not just because of the shiny plaques, but because it *helped vets*. Streamlining how the VA sends mail—every piece of correspondence—means faster benefits, less hassle. That’s the stuff that sticks with you.

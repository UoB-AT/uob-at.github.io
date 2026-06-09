---
layout: project
title: "Agentic Navigation of User Interfaces Without Vision: A Screen Reader Only LLM Agent Under Partial Observability"
author: "Dixant Pant"
description: "An LLM agent restricted to screen reader output that acts as a practical diagnostic tool for auditing workflow-level accessibility."
status: "Completed"
order: 2
---

## Overview

The 2026 WebAIM Million report found that 95.9% of homepages contain detectable WCAG failures[cite: 4]. Despite these guidelines, modern websites remain highly challenging for visually impaired individuals to navigate seamlessly. State-of-the-art UI automation agents do not address this issue effectively because they rely on visual screenshots and accessibility trees, providing a fully observable spatial layout that screen reader users do not have access to.

This project addresses this limitation by formalising screen reader web UI navigation as an intractable Partially Observable Markov Decision Process (POMDP) and introducing an LLM agent restricted entirely to screen reader input and output. Because its observations strictly match those of a human screen reader user, its navigation failures reveal true participation restrictions that traditional static compliance tools fail to detect.

## Key Features & Findings

* **Screen-Reader Only Navigation:** The system introduces a functional screen reader agent on Windows using NVDA that integrates grammar-constrained action decoding, a sliding window context memory as an approximate belief state, loop detection, and layered goal verification.
* **Advanced Accessibility Auditing:** A four-tier custom benchmark (16 UIs, 48 tasks) was developed to successfully differentiate basic static compliance from true workflow navigability.
* **Identifying the Compliance Gap:** Three of the four tested UI tiers successfully passed static accessibility audits, yet the screen reader agent's success rates varied drastically across them (tier one: 88.9%, tier two: 58.3%, tier three: 41.7%, tier four: 72.2%), proving that the agent exposes critical accessibility failures completely missed by static testing.
* **Mapping Real-World Barriers:** Two comparative case studies evaluating context memory and command vocabulary demonstrated that the agent’s naturally occurring failures—such as hallucinated successes, heavy memory burdens, and sequential fallbacks—correspond directly to documented accessibility barriers faced by human users.

## Research Impact

This research demonstrates that a screen reader agent can function effectively as both an dynamic accessibility auditor and a workflow explorer. By automating workflow testing at a scale that manual testing cannot cover, this system evaluates true workflow-level participation and navigability, pushing digital environments beyond basic compliance into true usability.
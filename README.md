# Design System Leadership — Case Study

*Design System Manager · 3 years · Figma, Storybook, GitHub*

> This case study was completed under NDA. Identifying details (company, product names, visual identity) have been anonymized. Structure, process, and performance metrics shown are accurate.

## Context

When I stepped into the team, the existing "design system" lacked the structure and systematic thinking that makes a design system actually function as one. Rather than working around those limitations, I documented the gaps and shared insights from prior design system experience with leadership — outlining what a mature system could unlock: faster delivery, consistent UX, and less design debt. That analysis led to me being selected to lead the transformation as Design System Manager.

## The problem

Four issues were compounding across the org:

1. **Inconsistent design language** — similar components behaved differently across teams, with no single source of truth. Designers kept reinventing solutions that already existed.
2. **Development inefficiency** — no reusable, documented components meant developers rebuilt the same elements repeatedly, multiplying technical debt across teams.
3. **Designer-developer disconnect** — handoff was friction-heavy. Designers worked without technical constraints in mind; developers implemented without design context. Result: inconsistent builds and endless revision cycles.
4. **No shared vocabulary** — one team's "modal" was another's "dialog." Decisions were made in silos with no documented rationale.

## Team

- 1 Design System Manager (me)
- 1 Principal Engineer
- 1 UX/UI Designer
- 5 Core Frontend Developers
- plus rotating contributors across product teams

## What I built

### Token-based architecture
Established a token system as the single source of truth for color, typography, spacing, and elevation — defined once, propagated automatically across platforms and products. This removed manual, component-by-component updates and eliminated visual drift between teams.

### Accessibility as a default, not a checklist
Embedded WCAG standards into every component at the foundation level — contrast, keyboard navigation, screen reader support, and focus management — so accessibility didn't require a separate audit pass per product.

### Dual-platform component library
Built out a shared library in both **Figma** and **Storybook**, each component documented with usage guidelines, interaction patterns, and implementation standards. This gave designers and developers one shared source of truth instead of two disconnected artifacts, which was the main lever for reducing handoff friction.

### Handoff & open-source transition
As the org wound down local operations, I led preparing a full handoff of the system to another subsidiary — documenting every component, decision rationale, and usage guideline so a new team could pick it up without the original team in the room. In parallel, I pushed to open-source the Figma library (the dev library was already open-sourced), so the work has a life beyond the original team.

## How design and engineering actually worked together

- Component specs were written jointly with the Principal Engineer before build — not handed off as finished mockups.
- Every component shipped with documented states, edge cases, and accessibility behavior, so implementation didn't require guessing.
- Shared vocabulary (naming, taxonomy) was agreed and documented once, ending the "modal vs. dialog" kind of drift.
- Contribution was two-way — both designers and developers proposed and reviewed changes to the system, not just consumed it.

## Impact

- **Faster delivery** — teams built from standardized components instead of custom UI, meaningfully cutting design-to-dev time.
- **High adoption** — the system became the default starting point for all product work, not an optional layer.
- **Better UX consistency** — consistent patterns reduced user cognitive load; WCAG compliance became automatic rather than retrofitted.
- **Stronger design-eng collaboration** — shared documentation and language closed most of the original handoff gap.
- **Forward-looking** — the system was being prepared to support agentic AI workflows before the transition.

## What I'd do differently

The next evolution I wanted to lead was connecting the token/component pipeline to agentic AI workflows — not AI-generated UI, but AI-assisted system maintenance. A few directions I'd scoped:

- Automated drift detection — an agent that diffs Figma component states against their Storybook implementation and flags divergence before it ships, rather than catching it in design QA
- Token impact analysis — given a proposed token change, an agent that traces every component and product surface it touches and summarizes the impact, so a "small" color update doesn't become a surprise regression across 12 teams
- Contribution triage — routing incoming component requests from product teams to the right owner (design vs. eng vs. "already exists, here's the link") automatically, since some of my time went into that manual traffic-directing

None of this shipped before the handoff, but scoping it clarified something: agentic workflows are only as good as the system's own documentation and structure. A design system with ambiguous naming or undocumented rationale gives an agent nothing reliable to reason over. So the real prerequisite work — the rigorous documentation from the handoff effort — turned out to double as the foundation for this too.

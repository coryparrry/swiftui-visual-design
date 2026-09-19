---
name: swiftui-visual-design-research
description: Research visual direction for SwiftUI apps by assessing existing screens or planning an initial UI, gathering design and motion references, evaluating reusable component libraries, and producing a prioritized design brief. Use for an app redesign or when no UI has been built yet.
---

# SwiftUI visual design research

Turn visual dissatisfaction or a new app brief into an evidence-backed design direction and a practical component shortlist. Actively consider existing SwiftUI libraries and source components; do not default to a wholly custom, generic interface or equate visual polish with adding effects everywhere.

## Establish the app and its current state

Use the request and available project context to identify the app, target platforms, minimum OS, important flows, and any accepted design constraints. Do not assume the current repository is the app named in the request. Ask only for missing information that would materially change the research.

If the user asks where the project stands, briefly separate implemented behavior, verified behavior, and remaining work using current project evidence. Keep this scoped to the visual design work rather than launching a full code audit.

Choose the route from the actual project state. Missing screenshots do not by themselves mean no UI exists. For a partially built app, use the existing-UI route for implemented screens and the new-UI route for planned screens, clearly distinguishing them.

### Route A: Existing UI

Inspect actual app screenshots or the running interface before making screen-specific claims. Identify concrete weaknesses in hierarchy, typography, spacing, color, surfaces, navigation, feedback, and motion. Tie each finding to a screen and user action. If current visuals are unavailable, continue reference research but label the critique and screen mapping provisional.

### Route B: No UI built yet

Start from the product brief, intended audience, core user tasks, available data, and platform constraints. Use existing requirements and models when available. Establish the primary journey and a small initial screen map before choosing components. If details are missing, state reasonable assumptions and ask only about decisions that materially change the direction.

Research references for the planned tasks and interaction patterns. Do not invent current-screen flaws or require screenshots of an interface that does not exist. Propose a coherent visual foundation: hierarchy, typography, spacing, color, surfaces, navigation, and motion. Connect each choice to the product's purpose and expected content.

Describe the first complete user flow, its screen layouts, primary actions, and relevant empty, loading, error, and success states. Include accessibility and reduced-motion behavior. Use labeled wireframes or concepts when they help communicate the proposal; distinguish proposed layouts from implemented screens and tested behavior.

Continue through the shared research and shortlist steps below. Deliver an initial UI design brief and a prioritized first-build plan instead of an existing-screen critique or before/after comparison. Prioritize one usable end-to-end flow before decorative additions.

## Gather references deliberately

Start with the user's supplied links. For optional research starting points, read [references/research-seeds.md](references/research-seeds.md). These are starting points, not preapproved dependencies or a mandatory shopping list.

Search both visual inspiration and reusable SwiftUI implementations. Search GitHub repositories for `SwiftUI components`, optionally sort by stars, and open promising candidates to compare their demos and source. Use popularity for discovery, then judge fit from the actual project and source; star count alone is not evidence of quality.

Choose categories that solve observed problems or support planned user tasks: component systems, motion and transitions, overlays and feedback, shaders and materials, or native-control customization. Follow exact component/demo links rather than collecting homepages alone. Inspect screenshots and play demos where available; a README promise does not establish visual or interaction quality.

For each useful reference, explain what to borrow, which app screen or action it serves, and how to adapt it to the app's identity. Seek a coherent direction instead of unrelated showcase effects. Stop when the highest-priority problems or planned tasks have credible options and further browsing adds little decision value.

## Evaluate a small shortlist

Verify current facts using the publisher's site, repository, documentation, license, release history, and package manifest as relevant. Record the date checked. For serious candidates, capture:

- Exact source/component link and the app problem it addresses.
- Platform and minimum-OS support, Swift/package integration, and relevant dependencies.
- License, attribution, source access, and any cost or reuse restrictions.
- Maintenance signals and integration effort; state unknowns rather than assuming compatibility.
- Accessibility, reduced-motion behavior, and likely runtime cost, particularly for continuous animation or shaders. Distinguish documented support from behavior actually tested.

Classify each option as a package candidate, reusable source candidate, inspiration only, or unsuitable. Explain whether a native SwiftUI solution already meets the need and why an external component adds value where recommended. Treat introspection as an integration mechanism requiring version checks, not a visual design by itself. Never infer macOS support from an iOS demo.

## Produce the design brief

Lead with the recommended visual direction and the highest-value changes. Include enough evidence for the user to make a choice:

1. For existing UI, a concise current-state assessment with screen evidence and gaps. For new UI, a product summary, assumptions, primary journey, and proposed screen map.
2. A curated set of visual and motion references, linked to specific screen improvements or planned interactions. Use annotated images or a contact sheet when they clarify the comparison.
3. A compact shortlist table: candidate and link, intended use, adoption type, compatibility/license evidence, trade-off, and recommendation.
4. A prioritized plan describing each affected or planned screen, component choice, and how the result should be checked. Use before/after behavior for existing UI; use proposed layouts, actions, and states for new UI.
5. A ready-to-use implementation brief containing the chosen direction or clearly labeled proposal, relevant references, constraints, and unresolved decisions.

Specify motion as behavior: trigger, transition, purpose, and reduced-motion alternative. Do not present a static concept as proof of animation. Keep existing app captures, external references, and generated concepts visibly distinct.

## Scope and handoff

Research alone does not authorize app edits, dependency installation, paid purchases, or plugin installation. Finish the brief within that scope. If implementation is already requested, carry the findings into that authorized work without an unnecessary approval pause.

Use available design tools when they materially improve the requested output. Product Design may help with critique or concept exploration; creative-production tools belong only where actual visual assets are needed. This workflow must remain usable without specialized plugins.

Check that every recommendation maps to an observed problem, a stated product requirement, or an explicitly provisional hypothesis, source links support the claims, and compatibility gaps are visible. A future implementation should be checked in a freshly built app through the affected flows, including motion and accessibility behavior; browsing, mockups, and source edits alone do not prove a visual improvement.

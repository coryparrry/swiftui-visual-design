# SwiftUI Visual Design

> Bring SwiftUI components, animation libraries, and design inspiration into one Codex workflow—and turn them into a design that fits your app.

SwiftUI Visual Design is a Codex plugin for designing a new interface or improving an existing one. It helps Codex find reusable components, study real examples, compare libraries, and explain how those choices should fit together across your screens.

## Why I made it

I kept finding useful SwiftUI components scattered across GitHub repositories, component catalogs, and design websites. There were libraries for shaders, popups, animation, and complete UI patterns, but I couldn't find one place that brought the sources I wanted together and helped me apply them to an app.

I also wanted Codex to consider what already exists before building another basic interface from scratch. Good components and motion examples are available; the missing step in my workflow was finding them, understanding where they fit, and using them to create a consistent design.

This plugin brings those starting points and that process together. It connects external components to actual user flows, checks whether they are suitable, and produces a practical design brief. The libraries remain with their original creators; the plugin contains guidance and links, not bundled copies of their code.

## Install as a Codex plugin

### In the Codex app

1. Open **Plugins** in Codex.
2. Select **Add marketplace**.
3. Add `https://github.com/coryparrry/swiftui-visual-design`.
4. Install **SwiftUI Visual Design**.
5. Start a new task and invoke `$swiftui-visual-design`.

The repository is currently private. Your GitHub account must have access to fetch it. If the app cannot authenticate, use the authenticated clone method below.

### With the Codex CLI

Use a Codex CLI version that supports `codex plugin`:

```bash
codex plugin marketplace add coryparrry/swiftui-visual-design
codex plugin add swiftui-visual-design@swiftui-visual-design
```

For a private repository, Git must be able to authenticate. Alternatively, clone it with the GitHub CLI and register the local checkout:

```bash
gh auth login
gh repo clone coryparrry/swiftui-visual-design
cd swiftui-visual-design
codex plugin marketplace add .
codex plugin add swiftui-visual-design@swiftui-visual-design
```

Skip `gh auth login` if you are already signed in. Start a new Codex task after installation so the skill is available.

## What it does

| Capability | What you get |
|---|---|
| Review an existing interface | Specific observations about hierarchy, typography, spacing, surfaces, navigation, feedback, and motion, grounded in actual screens. |
| Plan an interface from scratch | A primary user journey, proposed screens, visual foundations, and a first-build plan based on your product brief. |
| Find reusable components | Relevant source components and libraries mapped to your screens and interactions. |
| Plan purposeful motion | Animation ideas described by their trigger, purpose, transition, and reduced-motion alternative. |
| Compare adoption options | A shortlist that distinguishes package dependencies, reusable source, visual inspiration, and unsuitable options. |
| Prepare implementation | A prioritized brief explaining what to build, why it fits, which references to use, and how to check the result. |

## How it works

### 1. Understand the app

Codex identifies the target platform, supported OS versions, important user tasks, and existing design constraints. If there is already a UI, it reviews the running app or screenshots. If there is no UI yet, it starts with the product brief and planned flows. Partially built apps can use both routes.

### 2. Find references that fit

It starts with your links and the included component sources, then explores relevant catalogs, repositories, screenshots, and demos. Each reference must serve a concrete screen or interaction—such as a clearer empty state, better feedback, or a transition that explains navigation.

### 3. Compare components before choosing

Promising options are checked against platform support, minimum OS, integration effort, license, maintenance, and relevant accessibility or performance concerns. Popularity helps discover candidates; it does not decide what belongs in your app. Unknowns remain explicit.

### 4. Bring the design together

The result is a coherent visual direction with a curated set of references, a component comparison, and a screen-by-screen plan. For a new app, that includes layouts and relevant empty, loading, error, and success states. For an existing app, it explains the proposed changes and their purpose.

### 5. Carry the brief into implementation

Use the brief to guide the next build, or ask Codex to implement it in the same task. A design-only request produces the brief; implementation happens when you ask for it. Visual improvements still need to be checked in the running app.

## Component and design sources

| Source | What to explore |
|---|---|
| [Inspora](https://www.inspora.design) | Visual design inspiration. |
| [SwiftUX](https://swiftux.app/uicomponents) | UI patterns and source components to adapt. |
| [ShipSwift](https://github.com/signerlabs/ShipSwift) | Reusable SwiftUI components. |
| [SwiftUIShaders](https://github.com/krispuckett/SwiftUIShaders) | Shader effects and visual treatments. |
| [PopupView](https://github.com/exyte/PopupView) | Popups, overlays, and transient feedback. |
| [SwiftUI Introspect](https://github.com/siteline/swiftui-introspect) | Access to underlying native controls where needed. |
| [SwiftUI Animations](https://github.com/Shubham0812/SwiftUI-Animations) | Animation and interaction examples. |
| [SwiftfulUI](https://github.com/SwiftfulThinking/SwiftfulUI) | Additional reusable UI components. |

These are starting points, not a fixed list of dependencies. Codex can use your own references and discover other suitable options. Source availability, licenses, and compatibility should be checked when choosing a component; an iOS demo does not establish macOS support.

## Try it

**Improve an existing app**

```text
Use $swiftui-visual-design to review these app screenshots. Find components
and motion references that would improve the main flow, compare the best
options, and prepare a screen-by-screen design brief.
```

**Start with no UI**

```text
Use $swiftui-visual-design for a new SwiftUI app. No UI exists yet.
Here is the product brief: [describe the app and its main user tasks].
Plan the first complete flow, explore visual directions, and recommend
components that fit the target platform.
```

**Work from your own references**

```text
Use $swiftui-visual-design with these links: [references]. Explain which
patterns fit my app, what we can reuse, and how to combine them into a
consistent interface.
```

## Requirements and scope

- Codex with plugin support and web access for current sources.
- A product brief for a new interface, or screenshots/running-app access for an existing one.
- No bundled MCP server, component subscription, or specialist design plugin is required. Individual external sources may have their own access or licensing terms.

The plugin provides a design workflow and reference collection. It does not bundle a UI toolkit or automatically install every library it finds.

## Inside the plugin

| File | Purpose |
|---|---|
| [Marketplace entry](.agents/plugins/marketplace.json) | Makes the plugin installable from this repository. |
| [Plugin manifest](plugins/swiftui-visual-design/.codex-plugin/plugin.json) | Codex plugin metadata and skill discovery. |
| [Skill](plugins/swiftui-visual-design/skills/swiftui-visual-design/SKILL.md) | The existing-UI and new-UI workflows. |
| [Component references](plugins/swiftui-visual-design/skills/swiftui-visual-design/references/components.md) | The reusable source list. |

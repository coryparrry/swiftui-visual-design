# SwiftUI Visual Design Research

A Codex plugin for researching polished SwiftUI interfaces, from an initial app idea to an existing UI that needs improvement.

## Two starting points

- **Existing UI:** review actual screens, identify specific weaknesses, and connect improvements to design references and reusable components.
- **No UI yet:** work from the product brief, define the main journey and planned screens, and propose a coherent visual foundation and first-build plan.

Partially built apps can use both routes.

## What it produces

A visual direction, curated design and motion references, a component shortlist with compatibility and license checks, and a prioritized implementation brief. Research alone does not install dependencies or change app code.

The included references cover Inspora, SwiftUX, ShipSwift, SwiftUIShaders, PopupView, SwiftUI Introspect, SwiftUI Animations, and SwiftfulUI. These are research starting points; suitability and current project details must be checked before adoption.

## Usage

Once the skill is available in Codex, invoke `$swiftui-visual-design-research`, for example:

> Use $swiftui-visual-design-research to assess my app's screens and propose a visual direction with reusable components.

> Use $swiftui-visual-design-research for a new SwiftUI app with no UI yet. Start from the product brief and research its first complete user flow.

## Package layout

- `.codex-plugin/plugin.json` — Codex plugin manifest.
- `skills/swiftui-visual-design-research/SKILL.md` — research workflow and both routes.
- `skills/swiftui-visual-design-research/references/research-seeds.md` — public research links.
- `skills/swiftui-visual-design-research/agents/openai.yaml` — skill display metadata.

The skill can also be used independently by copying its folder into your Codex skills directory. It requires no bundled MCP server or specialized design plugin. Live research requires web access; reviewing an existing interface requires access to its screens or running app.

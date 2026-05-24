# Agentic Discovery Skill

<p align="center">
  <img src="assets/logo.png" alt="CompleteTech LLC logo" width="260">
</p>

A CompleteTech LLC Codex skill for creating discovery and scoping artifacts before proposal/SOW creation for agentic development opportunities.

## About

Part of the CompleteTech LLC agentic services skill library. This skill turns early workflow opportunities into verified facts, readiness checks, risk boundaries, success criteria, and proposal handoff material.

## OpenClaw / ClawHub Metadata

- Skill key: `agentic-discovery-skill`
- Version-ready metadata: `1.0.0`
- Homepage: https://github.com/CompleteTech-LLC/agentic-discovery-skill
- README: https://github.com/CompleteTech-LLC/agentic-discovery-skill#readme
- Runtime binaries: `python3`
- Python packages: none
- Intended registry/discovery tags: `latest`, `complete-tech`, `codex-skill`, `agentic-development`, `agentic-workflows`, `discovery`, `scoping`, `requirements`
- License: repository code, templates, and documentation use MIT; ClawHub publishing is intentionally skipped for now.
- Brand assets: CompleteTech LLC names, logos, seals, and brand assets are reserved; see `BRAND_ASSETS.md`.

## Workflow Diagram

```mermaid
flowchart LR
  A[Lead or workflow idea] --> B[Qualification]
  B --> C[Workflow discovery]
  C --> D[Readiness, risk, and approvals]
  D --> E[Success criteria and examples]
  E --> F{Pilot-ready?}
  F -->|No| G[Assumptions and unknowns]
  F -->|Yes| H[Proposal/SOW handoff brief]
  classDef source fill:#eef6ff,stroke:#3778c2,color:#102a43;
  classDef gate fill:#fff7e6,stroke:#c97a12,color:#3d2600;
  classDef output fill:#eefaf0,stroke:#2f8f46,color:#12351d;
  class A,B,C,D,E source;
  class F gate;
  class G,H output;
```

## What It Does

- Selects the right discovery artifact by situation.
- Drafts intake questionnaires, discovery scripts, interview guides, workflow maps, readiness checklists, approval-gate reviews, risk checks, success criteria, evaluation worksheets, scorecards, recaps, and proposal handoff briefs.
- Helps gather verified facts for the existing agentic email, proposal, contract, invoice, and certificate skills.
- Keeps discovery focused on practical, bounded workflow scoping with human approvals, evaluation, logging, monitoring, documentation, support, and handoff.

## Contents

- `SKILL.md` - operating instructions and artifact-selection guide.
- `references/discovery-catalog.md` - reusable discovery/scoping artifact templates.
- `references/use-case-decision-table.md` - quick guide for choosing the right artifact.
- `references/discovery-lifecycle.md` - flow from qualification through proposal handoff.
- `references/discovery-positioning.md` - CompleteTech LLC discovery language and guardrails.
- `scripts/render_discovery.py` - deterministic template listing and rendering helper.

## Quick Start

```bash
python3 scripts/render_discovery.py --list
python3 scripts/render_discovery.py \
  --template client-intake-questionnaire \
  --var client_name=Acme \
  --var workflow="support triage"
```

Rendered artifacts are drafts. Replace placeholders with verified client, workflow, systems, approval, risk, and success criteria details before use.

## Example

![Discovery brief preview](assets/examples/example.png)

**Discovery brief: Claims intake assistant readiness**

```bash
python3 scripts/render_discovery.py \
  --template requirements-brief-for-proposal-sow-handoff \
  --var client_name="Harbor Claims Group" \
  --var workflow="first-pass claims intake summarization" \
  --var pain="adjusters retype intake notes before routing files" \
  --var approval_gate="licensed adjuster reviews every summary before use" \
  --var success_criteria="clearer routing notes, fewer missing fields, faster reviewer preparation"
```

Example handoff:

- Workflow: repeated intake summarization with human review.
- Readiness: needs sample intake packets, approved data boundaries, and reviewer checklist.
- Downstream: proposal can scope a pilot only after data access and excluded-use constraints are confirmed.

## Brand Notes

Use a direct, concrete, low-hype tone. Present discovery as bounded workflow scoping: repeated workflow, inputs, systems, tools, retrieval sources, decision points, human approvals, risks, exclusions, evaluation examples, logging, monitoring, documentation, support, and handoff. Do not invent proof, regulated-use assurances, legal claims, savings metrics, or client facts.

## License

Code, templates, and documentation are licensed under the MIT License. CompleteTech LLC names, logos, seals, and brand assets are reserved and are not licensed for reuse except to identify this project. See `LICENSE` and `BRAND_ASSETS.md`.

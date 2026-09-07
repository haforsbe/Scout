---
name: "frontier-partners-fy27"
description: "Work with FY27 Frontier partners in PMX and marketplace using Partner-IQ, PMX naming/tag rules, owner-only write safety, MPL/reseller rules, and user-provided reports as source material."
---

# Frontier Partners FY27 Skill

Use this skill for FY27 Frontier partner work involving PMX, marketplace, MPL partner planning, offer tracking, partner project hygiene, and user-provided reports.

## Core data source rule

- Use Partner-IQ for PMX and marketplace work.
- Do not use general Microsoft 365 search as the primary source for PMX or marketplace facts unless the user explicitly asks for email/Teams/calendar context.
- When the user provides reports, decks, spreadsheets, screenshots, or documents for Frontier partner work, treat those reports as important source material and incorporate their content into analysis, naming proposals, PMX updates, marketplace recommendations, and status summaries.
- If report content conflicts with PMX/Partner-IQ data, surface the conflict and ask before writing changes.

## PMX write safety

- Only update PMX projects where the user is the project owner.
- Do not update projects where the user only participates unless the user explicitly says to update non-owned projects.
- Before any PMX write, preview the exact changes: project id/name, current value, proposed value, and reason.
- After PMX writes, verify the changed records and report the count and any failures.

## FY27 PMX project naming convention

Use:

`FY## - Partner Name - Description (+ #tags)`

Example:

`FY27 - PAX8 - Copilot Studio Agent Offer #Copilot #Reseller: Storata`

Guidance:

- Remove older geography/quarter/noise-heavy prefixes unless the user asks to preserve them.
- Use clean partner names.
- Use a concise business-readable description.
- Use FY year, not quarter-heavy names, unless quarter is materially required.
- Keep tags at the end.

## PMX objectives

- Project objectives should be one clear, detailed sentence of intent and outcome.
- The objective should describe what the partner will build, modernize, deploy, or adopt and why it matters.

## PMX deliverables

- Deliverable titles should use activity type and purpose.
- Number deliverables only when work runs in sequence.
- Avoid vague deliverable names like “Meeting” or “Follow-up” without purpose.

## FY27 tags

Use these tags according to intent:

- `#BSKU`: M365 Copilot or Security projects in SMB, typically SSPs, distributors, or telcos.
- `#Copilot`: Copilot chat or paid seats in Corporate/SMB.
- `#A365`: Agent 365 in Corporate/SMB.
- `#ME7`: ME7 in Corporate/SMB.
- `#CoE`: Partner Center of Excellence build/enablement motions.
- `#CustomerZero`: Partner adoption/running the solution on their own estate first.
- `#FactoryAgent`: Repeatable AI agent solutions, including agent offers, marketplace publishing, and Customer Zero adoption.
- `#CopilotIn30`: CSP-led 30-day Microsoft 365 Copilot evaluation and transition to paid deployment.

## Frontier tags

- `#FrontierSpecialization`: Partner meets or is working toward Frontier capability/readiness requirements.
- `#FrontierFTEOffer`: Frontier Transformation Engineer offer identifying AI opportunities and transformation plans.
- `#FrontierDeployment`: Partner deployment services implementing the identified solution.
- `#FrontierManagedService`: Recurring services managing and optimizing deployed Frontier solutions.
- `#FrontierAccelerate`: Replaces former AFO. Use for Frontier Accelerate-aligned incentives, assessments, deployment accelerators, Cloud Accelerate Factory resources, and related investments.

## AFO replacement rule

- Do not create new `#AFO` tags for FY27 Frontier work.
- Use `#FrontierAccelerate` where former AFO tagging would have been used.
- When renaming legacy active owned projects, propose replacing `#AFO` with `#FrontierAccelerate` only when the project aligns to the Frontier Accelerate motion.

## Reseller / MPL convention

- If the reseller is not selectable in PMX or not on MPL, select the distributor as the Partner Account.
- Include `#Reseller: <Partner Name>` in the project title.
- For WE MPL FY27 work, use the supplied MPL image/list as the authority when available. If the MPL data has not been provided in the current session or memory, ask the user for it before making MPL-dependent changes.

## Reports and source material

The user has reports they wants included in Frontier partner work. When reports are provided:

- Extract partner names, offer names, marketplace status, specialization/readiness information, scorecards, priorities, blockers, and recommended actions.
- Cross-reference report content with Partner-IQ/PMX/marketplace data.
- Use report evidence to propose PMX project names, objectives, deliverables, and tags.
- Note source provenance in summaries, for example: `Source: FY27 Frontier report`, `Source: MPL screenshot`, or `Source: marketplace readiness report`.
- Do not overwrite PMX facts solely from a report if there is a conflict; preview and ask.

## Marketplace work

When working with marketplace/offer readiness:

- Identify partner, offer name, offer type, marketplace status, and missing readiness steps.
- Distinguish between offer build, offer modernization, marketplace publish/certification, and GTM/co-sell readiness.
- For repeatable AI agent marketplace offers, consider `#FactoryAgent` and possibly `#CustomerZero` if the partner is using it internally first.

## Output format for project naming proposals

When listing projects with proposed names, use a table with:

- Owner
- Partner
- Current name
- Proposed name
- Tags used
- Change allowed? yes/no based on ownership
- Source/reason when report content was used

Never write changes from a proposal table unless the user confirms.

## Default behavior

- Be conservative with PMX writes.
- Prefer read/preview/confirm/write/verify.
- If the user says “active projects,” interpret that as project status `In progress` unless they explicitly mean Dataverse record state `Active`.
- If the user says “my projects,” interpret that as projects owned by the user for write operations; for read-only summaries, include owned and optionally participated projects if useful, clearly separated.

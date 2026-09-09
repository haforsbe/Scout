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

## FY27 PMX project creation checklist

For new FY27 PMX projects, always validate and set the full required hygiene set before considering the project complete:

- Use `Source = Tech Plan` unless the user explicitly chooses another valid source.
- Use FY27 naming with relevant tags in the project title.
- Set Project Status to `In progress` once the project has started or once first deliverables/tasks are created, unless the user asks for `Not started`.
- Create the first deliverable(s) and at least one task; for complete offering-build motions, create the agreed full deliverable/task plan.
- Generate an MBR-ready `Project objective` that clearly states what the partner will build, modernize, deploy, or enable and the intended business outcome.
- Use relevant FY27 priority language where it applies: SQL, Fabric, GitHub Copilot, CAF, Sovereignty, FTE, Frontier Specialization, Frontier Deployment, Frontier Accelerate, migration, modernization, hosted agents, Azure OpenAI, Azure AI Foundry, security, governance, and reseller enablement.
- Set `Hero Product`; this is multi-value free text, so propose all applicable Hero Products instead of forcing a single value.
- Set `Country` (`gps_country`) from the linked PMX partner management account country. Do not rely on the PMA link alone.
- Set `Project BU Priority` (`gps_businesspriority`) using the project-level option set.
- Use the project Comment/notes field (`gps_notes`) to document key PMX context because PMX is the system of record.
- Verify after creation/update: Source, name/tags, status, objective, Hero Product, Country, Project BU Priority, comments, deliverable count, task count, and task metadata.

## PMX field defaults and known option sets

Project-level defaults for CAIP / Frontier partner projects:

- Source: `Tech Plan`
- Solution Area text: `Cloud and AI Platforms`
- Project Status: `In progress` when active work exists
- Project Priority: `Medium` unless the user chooses otherwise
- FY27 Q2 end date option: `921860009`
- Conversation Type: usually `Frontier`
- Conversation: usually `Ubiquitous Innovation` for Frontier agentic AI motions

Project BU Priority (`gps_businesspriority`) valid values observed:

- `921860000` = Copilot
- `921860001` = Grow the Core: M365+D365 Execution
- `921860003` = AI design solutions
- `921860004` = Migrations
- `921860005` = Cyber security

Task-level Task BU Priority (`gps_businessobjectiv`) is a different option set from project-level BU Priority. Valid task values observed:

- `921860000` = Copilot
- `921860001` = AI Design Solutions
- `921860002` = Cyber Security
- `921860003` = M365
- `921860004` = Migration
- `921860005` = AI Discovery Cards

For CAIP tasks, default to:

- Task Solution Area (`gps_solutionarea`): `Cloud and AI Platforms` / `394380000`
- Task BU Priority (`gps_businessobjectiv`): `AI Design Solutions` / `921860001`, unless the project is clearly migration-focused, where `Migration` / `921860004` is appropriate.
- Task Status (`gps_progressstate`): `Not Started` initially; use `In Progress` / `921860001` for tasks under deliverables that are started.

Important PMX status distinction:

- Task `gps_progressstate` / `Task Status` controls Not Started, In Progress, Completed, On hold, Cancelled.
- Task `statuscode` is the separate system Status Reason, typically Active/Inactive. Do not treat it as the task progress field.
- Deliverable `statuscode = 921860001` means In Progress.
- When setting deliverables to In Progress, also verify linked tasks have `gps_progressstate = 921860001`; the PMX UI may need refresh before it displays correctly.

## Hero Product guidance

Hero Product (`gps_heroproduct`) is free text and can contain multiple values separated by semicolons. Always propose and set Hero Products for new PMX projects.

Visible/observed options include:

- AI: Fireworks Models
- AI: Hosted Agents
- AI: OpenAI Models (PTU)
- AI: OpenAI Models (Standard)
- AI: Other Models
- Apps: Testing Services (Load testing)
- Data: Data Platform -Analytics - G...
- Data: Data Platform- Fabric - ADF...
- Dev: Azure DevOps (ADO)
- Dev: GitHub AI Credits
- Dev: GitHub Copilot (Business, Enterprise)
- Dev: GitHub Enterprise
- Dev: GitHub Security

Observed existing PMX examples also use broader text such as `Azure AI Foundry`, `Azure OpenAI`, `Microsoft Fabric`, `Copilot Studio`, `Agent 365`, and `GitHub Copilot`. If the PMX dropdown provides exact labels, prefer the exact visible labels from PMX. If only free text is available, use semicolon-separated values and clearly preview them before writing.

Example Hero Product mappings:

- Frontier FTE / hosted agent motions: `AI: Hosted Agents; AI: OpenAI Models (Standard)`
- Secure vibe coding / DevAI: `Dev: GitHub Copilot (Business, Enterprise); Dev: GitHub Security; Dev: GitHub Enterprise`
- Integration operations hub: `AI: Hosted Agents; AI: OpenAI Models (Standard); Data: Data Platform- Fabric - ADF...`
- Migration / modernization: `Dev: Azure DevOps (ADO); Data: Data Platform -Analytics - G...` when applicable
- BizTalk EOL / Azure Integration Services: `AI: Hosted Agents; Dev: Azure DevOps (ADO); Apps: Testing Services (Load testing)` when those are the closest available visible options
- Distributor reseller hackathon offerings: `AI: Hosted Agents; AI: OpenAI Models (Standard); Dev: GitHub Copilot (Business, Enterprise)`

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
- Usually use 2-3 tags; add more only when they materially improve filtering or explain the motion.

## PMX objectives and comments

- Project objectives should be one clear, detailed sentence of intent and outcome.
- The objective should describe what the partner will build, modernize, deploy, or adopt and why it matters.
- Comments (`gps_notes`) should document the PMX execution context, why the project exists, alignment to FY27 priorities, important scope notes, and MBR/reporting language.
- For comment text, prefer concise but descriptive wording that a PDM/manager can read without needing chat history.

Example comment styles:

- FTE Specialization: mention Frontier Transformation Engineer readiness, repeatable FTE-led customer discovery and transformation planning, Frontier Specialization readiness, AI opportunity identification, MBR reporting, and field alignment.
- Vibe Coding: mention secure AI-assisted development, GitHub Copilot, GitHub Security, governance, developer productivity, and Frontier Deployment.
- Integration Operations Hub: mention AI-enabled integration monitoring, hosted agents, Azure OpenAI, Fabric/ADF-aligned integration patterns, operational governance, and customer activation.

## PMX deliverables

- Deliverable titles should use activity type and purpose.
- Number deliverables only when work runs in sequence.
- Avoid vague deliverable names like “Meeting” or “Follow-up” without purpose.
- Ensure deliverable due date and deliverable end date are both populated when creating deliverables.

## Default partner offering deliverable sequence

For standard FY27 partner offering-build or modernization projects, use this sequence unless the user chooses a different template:

1. Planning
2. Envisioning
3. Architecture Design Sessions (ADS)
4. Build
5. Offering Validation
6. Offering Commercialization
7. Offering Activation

For distributor/reseller Frontier Agentic Hackathon offering-build motions, use this sequence:

1. Planning - reseller offering scope, readiness, and owners
2. Envisioning - reseller value proposition and commercial packaging
3. Tech Briefing - Frontier agent patterns and Microsoft alignment
4. Workshop - offering design and reseller delivery model
5. Hackathon - distributor dry-run and reseller scenario validation
6. Offering Validation - readiness, playbook, and feedback
7. Offering Commercialization - packaging, GTM, and reseller recruitment
8. Offering Activation - launch, reseller onboarding, and pipeline handoff

For the user's PMX work, do not include Strategic Deal Activation deliverables unless the user explicitly asks and ownership is clear.

## Default task guidance

Tasks should be actionable and tied to a deliverable. For each task, include:

- Clear task name
- Start date and due date
- Owner/assignee when known
- Task Status
- Task Solution Area
- Task BU Priority
- Comments describing the expected output

When creating tasks, always propose and confirm task-level Solution Area and Task BU Priority. Do not assume project-level BU Priority values can be reused as task-level values.

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
- `#Migration`: Azure migration motion.
- `#AzureModernization`: modernization of apps, workloads, or platforms on Azure.
- `#AzureIntegrationServices`: Logic Apps, Service Bus, Event Grid, API Management, Azure Functions, and related integration modernization work.

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
- Include `#Reseller: <Partner Name>` in the project title when the project is for a specific reseller under a distributor.
- For distributor-built reusable reseller offerings, use the distributor account and name the project as a reseller offering, for example: `FY27 - <Disti Name> - Frontier Agentic Hackathon Reseller Offering #FactoryAgent #CoE #FrontierAccelerate`.
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

<!-- Rapider Official App SOW & Specification | App #113: AI Coding Assistant (ai-coding-assistant) | Domain: AIA -->

# #113 AI Coding Assistant (`ai-coding-assistant`) — Scope of Work (SOW)

- **App Number & Name:** `#113` — AI Coding Assistant
- **Proposed App Key:** `ai-coding-assistant`
- **Suite / Domain Key & Model Prefix:** `AIA` (`Aia*`)
- **Function Category:** 12. AI & Intelligent Automation
- **Representative Product (`P1`):** GitHub Copilot (Enterprise & Coding Agent)
- **Combined Feature Catalog:** [../combined-features/113-ai-coding-assistant-features.md](../combined-features/113-ai-coding-assistant-features.md)
- **Target Release Posture:** Context-Grounded Developer Coding Studio, Autonomous Issue-to-PR Coding Tasks, Agentic PR Code Review & Engineering AI Governance Microapplication

---

## 1. Executive Outcome & Target Audience

### 1.1 Business Problem Solved
Software engineering teams face mounting backlog pressure, fragmented context across issue trackers and multi-repository codebases, slow pull request review bottlenecks, and compliance anxiety over unvetted AI-generated code, leaked secrets, and runaway LLM token spend. **Rapider AI Coding Assistant (`ai-coding-assistant`)** delivers a governed, context-grounded AI software engineering workspace that connects canonical `ApmIssue` specifications, indexed Git repositories, scoped architectural rule packs, interactive multi-file patch proposals, autonomous cloud sandbox coding tasks, and automated first-pass PR code reviews under unified security and cost controls.

### 1.2 Target Personas & Progressive Disclosure
- **SME Fast-Path Defaults (Startup & Lean Product Teams):** Connect a Git repository in two minutes, pick a built-in framework rule pack, open an interactive coding studio session or click **"Assign to Coding Assistant"** on an `ApmIssue`, inspect a clean unified diff with automated secret/SAST checks, and apply or publish a draft PR with default `\$40.00`/seat monthly token caps.
- **Enterprise Progressive Disclosure (VP Engineering, Staff Architects, AppSec & Platform Teams):** Enforce Zero-Data-Retention (`ZDR`) model allowlists, glob-scoped architectural `AiaCodingRulePack` hierarchies, public-code IP indemnity & copyleft license filters, parallel sub-task sandbox execution, protected-path human sign-off gates (`auth/**`, `migrations/**`, `billing/**`) via Rapider Home `WorkItem`s, and sprint-level velocity & code-persistence ROI analytics.

### 1.3 Measurable Business Outcomes
- **>= 35% Faster PR Review Turnaround:** Automated first-pass agentic code reviews (`AiaPrReviewRun`) surface cross-file logic defects, missing RBAC guards, and security autofixes within 90 seconds of PR creation.
- **Zero Plaintext Secret or Unapproved Path Merges:** Deterministic secret/SAST scanning and mandatory human `WorkItem` gates prevent autonomous commits to protected branches or sensitive security paths.
- **100% Attributable AI Compute Spend:** Append-only `Decimal128` token and sandbox minute metering (`AiaUsageLedgerEntry`) attributes every cent across repositories, `ApmProject`s, and model tiers.

### 1.4 Benchmark Summary (`P1`–`P6`)
Combines the Issue-to-PR coding agent, agentic PR code review, and IP governance of **`P1` GitHub Copilot Enterprise**, fast `@codebase` semantic indexing, scoped rules, and multi-file patch hunks of **`P2` Cursor**, real-time AST/flow context and strict ZDR controls of **`P3` Windsurf (Codeium)**, backlog-to-PR sandbox execution and cycle-time analytics of **`P4` Atlassian Rovo Dev**, schema-aware parallel worktree task orchestration of **`P5` Salesforce Agentforce for Developers**, and clean-core enterprise scaffolding and legacy modernization guides of **`P6` SAP Joule for Developers**.

---

## 2. In-Scope, Out-of-Scope & Suite Ownership Boundaries

### 2.1 In-Scope Capabilities
1. Repository and branch semantic context bindings (`AiaCodeRepoBinding`) with exclude globs, commit SHA watermarks, and Rapider canonical schema/component grounding.
2. Versioned architectural instructions, path-scoped coding standards, and reusable slash prompt recipes (`AiaCodingRulePack`).
3. Interactive multi-turn coding studio (`AiaCodingSession` backed by `projectChannelMessage` threads) with `@file`/`@symbol`/`@issue` citations and hunk-level patch proposals (`AiaCodePatchProposal`).
4. Autonomous Issue-to-PR coding tasks (`AiaCodingTask`) running build/lint/test loops in isolated ephemeral sandboxes with Kanban lifecycle tracking (`<rapider-kanban>`).
5. Automated first-pass agentic Pull Request code reviews (`AiaPrReviewRun`, `AiaReviewFinding`) with severity-ranked inline comments, security/secret checks, and one-click unified diff autofixes.
6. Workspace model allowlists, ZDR & copyleft filters (`AiaCodingPolicy`), and append-only `Decimal128` token/sandbox spend ledgers (`AiaUsageLedgerEntry`).

### 2.2 Out-of-Scope Capabilities (Delegated to Adjacent Rapider Apps)
- **Primary Git repository hosting, branch protection storage, and merge engine:** Owned by `#104 Source Code Hosting & Git / PRs` (`git-repos`) or connected external Git providers (GitHub, GitLab, Bitbucket).
- **CI/CD pipeline orchestration, artifact registries, and production release deployment:** Owned by `#105 CI/CD Pipelines & Release Automation`.
- **Sprint planning, backlog prioritization, story points, and timesheets:** Owned by `APM` suite (`apm`, `planning`, `time`).
- **General-purpose multi-agent business workflow builders and non-code orchestration:** Owned by `#114 AI Agent Development & Orchestration` (`ai-agent-development-and-orchestration`).
- **Custom model fine-tuning and ML experiment tracking:** Owned by `#115 AI Model Training & Experiment Tracking` (`ai-model-training-and-experiment-tracking`).
- **Standalone approval inbox UI:** Delegated strictly to Rapider Platform Home `WorkItem`s.

### 2.3 Cross-Suite Ownership & Integration Contract

| Domain / App | Owns (Canonical Models) | Integration Contract with `ai-coding-assistant` |
| :--- | :--- | :--- |
| **`ai-coding-assistant` (`#113` — This App)** | `AiaCodeRepoBinding`, `AiaCodingRulePack`, `AiaCodingSession`, `AiaCodingTask`, `AiaCodePatchProposal`, `AiaPrReviewRun`, `AiaReviewFinding`, `AiaCodingPolicy`, `AiaUsageLedgerEntry` | Indexes approved repo refs, hosts coding sessions & autonomous sandbox runs, generates patch proposals & PR reviews, and meters token/sandbox spend. |
| **`apm` (`APM` Suite)** | `ApmProject`, `ApmEpic`, `ApmSprint`, `ApmIssue` | `AiaCodingTask` and `AiaCodingSession` reference `apmProjectId` and `apmIssueId` for requirements grounding and emit task/PR status events back to `ApmIssue` timelines. |
| **`#104` Git / PRs & `#105` CI/CD** | Git repositories, Pull Requests, Pipeline Runs | Webhook/event integration triggers `AiaPrReviewRun` on PR open/synchronize and allows `AiaCodingTask` to propose draft PRs or inspect failed CI logs. |
| **`employees` (`HR` Suite) & Platform Identity** | `HrEmployee`, Workspace Users & RBAC Roles | Resolves developer seat entitlements, team hierarchy for aggregate ROI analytics, and RBAC permission boundaries. |
| **Rapider Platform Services** | Home `WorkItem`, `projectChannelMessage`, Files/Drive, Secret Vault | Routes protected-path & budget-cap approvals to Home `WorkItem`s, stores session/review chat on `projectChannelMessage` threads, and resolves Git/LLM secrets at runtime without persistence in app DB. |

---

## 3. Primary Web Pages & Sidebar Navigation Architecture (12 Pages)

All visible sidebar groups strictly satisfy the **Minimum 3 Items per Section Rule** (`Coding Workspace`: 3 items, `Agentic Delivery`: 3 items, `Governance & Insights`: 3 items = 9 menu-visible pages + 3 hidden detail/drawer routes = 12 total pages).

| # | Route | Page Title | Sidebar Section | Menu Visible | Key Components & UX |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | `dashboard` | Coding Assistant Overview | `Coding Workspace` | `true` (`order: 1`) | KPI cards (`countSWR`/`findSWR` for active tasks, patch acceptance %, PR review turnaround, monthly `Decimal128` spend vs. budget), active sandbox queue, and quick-launch bar. |
| 2 | `coding-studio` | Interactive Coding Studio | `Coding Workspace` | `true` (`order: 2`) | Split-pane grounded chat (`projectChannelMessage` thread), `@file`/`@symbol`/`@issue` context picker, slash recipe launcher, model selector, and hunk-level diff viewer (`AiaCodePatchProposal`). |
| 3 | `repositories` | Indexed Repositories | `Coding Workspace` | `true` (`order: 3`) | Searchable table of `AiaCodeRepoBinding` records with `#activeFilterTagsBar` + `Clear all`, index status badges, commit SHA watermark, clickable repo name -> detail, icon+text `Edit`, icon-only `Delete`. |
| 4 | `coding-tasks` | Autonomous Coding Tasks | `Agentic Delivery` | `true` (`order: 4`) | Dual List + `<rapider-kanban>` board (`QUEUED`, `PLANNING`, `SANDBOX_RUNNING`, `AWAITING_REVIEW`, `PR_OPENED`, `COMPLETED`, `FAILED`) linked to `ApmIssue`s with `#activeFilterTagsBar`. |
| 5 | `patch-proposals` | Patch Proposals & Diffs | `Agentic Delivery` | `true` (`order: 5`) | Filterable table of `AiaCodePatchProposal` changesets across sessions and tasks, security/license gate badges, test pass summary, and hunk acceptance counts. |
| 6 | `pr-reviews` | Agentic PR Reviews | `Agentic Delivery` | `true` (`order: 6`) | Real-time table of `AiaPrReviewRun` evaluations with severity breakdown (`CRITICAL`/`HIGH`/`MEDIUM`/`NIT`), autofix readiness, and clickable PR identifier navigation. |
| 7 | `rule-packs` | Coding Rules & Recipes | `Governance & Insights` | `true` (`order: 7`) | Catalog of versioned `AiaCodingRulePack` coding standards and slash prompt templates with path-glob scopes, acceptance signal scores, and drawer editor. |
| 8 | `governance-policies` | Guardrails & Model Policies | `Governance & Insights` | `true` (`order: 8`) | Admin policy console (`AiaCodingPolicy`) configuring allowed models, ZDR toggle, protected path globs, copyleft filter, seat/monthly `Decimal128` caps, and emergency contact `<rapider-phone-input>`. |
| 9 | `usage-analytics` | Usage Ledger & Velocity ROI | `Governance & Insights` | `true` (`order: 9`) | Team/repo/model spend breakdown (`AiaUsageLedgerEntry`), suggestion 14-day survival chart, PR cycle-time delta, and CSV audit export. |
| 10 | `coding-task-detail` | Coding Task & Sandbox Detail | *(Hidden)* | `false` | Full execution trace for `AiaCodingTask`: pinned `ApmIssue` spec, approved plan, sandbox step/test logs, proposed multi-file diff, `WorkItem` gate status, and `Back to Tasks` state restoration. |
| 11 | `pr-review-detail` | PR Review & Autofix Detail | *(Hidden)* | `false` | Architectural summary walkthrough, filterable `AiaReviewFinding` cards with inline diff previews, one-click **"Apply Autofix"** / **"Hand Off to Coding Task"**, and `projectChannelMessage` Q&A thread. |
| 12 | `new-coding-task` | Dispatch Coding Task (Drawer) | *(Hidden Drawer)* | `false` | Sliding drawer to launch an `AiaCodingTask` from an `ApmIssue` or prompt, choose `AiaCodeRepoBinding` + target branch + `AiaCodingRulePack`, auto-closing via `closePageDrawer()` in `try/catch/finally`. |

> **Rapider UI Standards Enforced Across All 12 Pages:**
> - Initial loads use `findSWR` / `countSWR` with clean filters (no client-side `isDeleted` where clauses) and defensive local `items.filter(it => it && it.isDeleted !== true)`.
> - Primary and destructive buttons strictly enforce `#ffffff !important` white text; zero `window.alert`, `window.confirm`, or `window.prompt` calls exist anywhere.
> - Data tables contain **no standalone View button** in `Actions`; clicking the primary identifier navigates to detail, paired with icon+text `Edit` and icon-only `Delete`.

---

## 4. Canonical Data Models (`Aia*` — 9 Models)

No model contains `projectId` or `workspaceId` (enforced by platform multi-tenant host context). Sample seed UUIDs follow `00000000-0113-0000-0000-xxxxxxxxxxxx`.

| Model Name | Key Fields & Types | Relationships & External Refs | Invariants & Lifecycle |
| :--- | :--- | :--- | :--- |
| **`AiaCodeRepoBinding`** | `id` (UUID), `repoName` (String), `providerType` (`GITHUB`\|`GITLAB`\|`BITBUCKET`\|`RAPIDER_GIT`), `repoUrl` (String), `defaultBranch` (String), `excludedGlobs` (String[]), `indexStatus` (`PENDING`\|`INDEXING`\|`READY`\|`ERROR`), `lastIndexedCommitSha` (String), `indexedSymbolCount` (Integer), `credentialSecretRef` (String), `version` (Integer) | `apmProjectId` -> `ApmProject.id`; `defaultRulePackId` -> `AiaCodingRulePack.id` | Never stores raw Git PATs/SSH keys (only vault `credentialSecretRef`). Secret/env globs (`**/.env*`, `**/*.pem`) are always force-excluded. |
| **`AiaCodingRulePack`** | `id` (UUID), `code` (String), `name` (String), `packType` (`ARCHITECTURE_RULE`\|`SLASH_RECIPE`\|`PR_CHECKLIST`), `pathGlobs` (String[]), `languageTags` (String[]), `instructionMarkdown` (Text), `status` (`DRAFT`\|`ACTIVE`\|`DEPRECATED`), `ruleVersion` (Integer), `acceptanceRatePct` (`Decimal128`), `version` (Integer) | `ownerUserId` -> Platform User | Published `ruleVersion` snapshots referenced by `AiaCodingTask` or `AiaPrReviewRun` remain immutable for audit reproducibility. |
| **`AiaCodingSession`** | `id` (UUID), `title` (String), `sessionMode` (`CHAT`\|`COMPOSER_DIFF`\|`LEGACY_EXPLAIN`), `selectedModelKey` (String), `pinnedRefsJson` (JSON), `status` (`ACTIVE`\|`ARCHIVED`), `totalPromptTokens` (Integer), `totalCompletionTokens` (Integer), `estimatedCostAmount` (`Decimal128`), `currencyCode` (String), `version` (Integer) | `repoBindingId` -> `AiaCodeRepoBinding.id`; `apmIssueId` -> `ApmIssue.id` (optional); `channelThreadId` -> Platform `projectChannelMessage` | Grounded strictly in indexed repo files and caller RBAC scope; accumulates exact `Decimal128` session cost. |
| **`AiaCodingTask`** | `id` (UUID), `taskNumber` (String), `title` (String), `specificationMarkdown` (Text), `sourceBranch` (String), `workingBranch` (String), `status` (`QUEUED`\|`PLANNING`\|`SANDBOX_RUNNING`\|`AWAITING_REVIEW`\|`PR_OPENED`\|`COMPLETED`\|`FAILED`\|`CANCELLED`), `planMarkdown` (Text), `iterationCount` (Integer), `maxIterations` (Integer), `sandboxMinutesUsed` (`Decimal128`), `externalPrUrl` (String), `version` (Integer) | `repoBindingId` -> `AiaCodeRepoBinding.id`; `apmIssueId` -> `ApmIssue.id`; `policyId` -> `AiaCodingPolicy.id`; `approvalWorkItemId` -> Platform `WorkItem.id` | `iterationCount <= maxIterations` (default `5`). Cannot transition to `PR_OPENED` on protected paths until linked `WorkItem` is `APPROVED`. |
| **`AiaCodePatchProposal`** | `id` (UUID), `summary` (String), `filesChangedCount` (Integer), `linesAdded` (Integer), `linesDeleted` (Integer), `unifiedDiffPayload` (Text), `hunkStatesJson` (JSON), `securityScanStatus` (`PASSED`\|`WARN`\|`BLOCKED_SECRET`\|`BLOCKED_SAST`), `licenseScanStatus` (`CLEAN`\|`FLAGGED_COPYLEFT`), `testRunStatus` (`NOT_RUN`\|`PASSED`\|`FAILED`), `resolutionStatus` (`PROPOSED`\|`PARTIALLY_ACCEPTED`\|`ACCEPTED`\|`REJECTED`), `version` (Integer) | `sessionId` -> `AiaCodingSession.id` (nullable); `codingTaskId` -> `AiaCodingTask.id` (nullable); `repoBindingId` -> `AiaCodeRepoBinding.id` | `ACCEPTED` blocked whenever `securityScanStatus == BLOCKED_SECRET` or `BLOCKED_SAST`. Once `ACCEPTED` and committed, diff snapshot is immutable. |
| **`AiaPrReviewRun`** | `id` (UUID), `externalPrId` (String), `prTitle` (String), `prAuthorHandle` (String), `headCommitSha` (String), `baseBranch` (String), `reviewStatus` (`RUNNING`\|`COMPLETED`\|`CHANGES_SUGGESTED`\|`BLOCKED`\|`FAILED`), `walkthroughMarkdown` (Text), `criticalCount` (Integer), `highCount` (Integer), `mediumCount` (Integer), `nitCount` (Integer), `durationMs` (Integer), `version` (Integer) | `repoBindingId` -> `AiaCodeRepoBinding.id`; `apmIssueId` -> `ApmIssue.id` (optional); `channelThreadId` -> `projectChannelMessage` | Idempotent per `(repoBindingId, externalPrId, headCommitSha)` so repeated webhooks never spam duplicate review comments. |
| **`AiaReviewFinding`** | `id` (UUID), `category` (`SECURITY`\|`BUG`\|`PERFORMANCE`\|`ARCHITECTURE`\|`STYLE`\|`LICENSE`), `severity` (`CRITICAL`\|`HIGH`\|`MEDIUM`\|`NIT`), `filePath` (String), `startLine` (Integer), `endLine` (Integer), `findingMarkdown` (Text), `autofixDiff` (Text), `disposition` (`OPEN`\|`AUTOFIX_APPLIED`\|`HANDED_TO_AGENT`\|`DISMISSED_FALSE_POSITIVE`\|`RESOLVED`), `version` (Integer) | `prReviewRunId` -> `AiaPrReviewRun.id`; `rulePackId` -> `AiaCodingRulePack.id` (optional); `remediationTaskId` -> `AiaCodingTask.id` (optional) | Dismissal of a `CRITICAL` security finding requires justification note and AppSec/Lead role or approved `WorkItem`. |
| **`AiaCodingPolicy`** | `id` (UUID), `policyName` (String), `allowedModelKeys` (String[]), `enforceZeroDataRetention` (Boolean), `blockPublicCodeMatches` (Boolean), `protectedPathGlobs` (String[]), `monthlySeatCapAmount` (`Decimal128`), `monthlyWorkspaceCapAmount` (`Decimal128`), `currencyCode` (String), `maxSandboxMinutesPerTask` (Integer), `securityEscalationPhone` (String, E.164), `isDefault` (Boolean), `version` (Integer) | `ownerUserId` -> Platform User | Exactly one active workspace default policy; `monthlySeatCapAmount` and `monthlyWorkspaceCapAmount` must be `>= 0` (`Decimal128`). |
| **`AiaUsageLedgerEntry`** | `id` (UUID), `recordedAt` (DateTime), `operationType` (`CHAT_COMPLETION`\|`PATCH_GEN`\|`SANDBOX_TASK`\|`PR_REVIEW`\|`REPO_INDEX`), `modelKey` (String), `promptTokens` (Integer), `completionTokens` (Integer), `sandboxMinutes` (`Decimal128`), `unitRatePer1kTokens` (`Decimal128`), `estimatedCostAmount` (`Decimal128`), `currencyCode` (String), `correlationId` (String) | `actorUserId` -> Platform User; `repoBindingId` -> `AiaCodeRepoBinding.id`; `apmProjectId` -> `ApmProject.id`; `codingTaskId` -> `AiaCodingTask.id` (nullable) | **Strictly append-only & immutable** post-creation; adjustments require compensating entries rather than in-place edits. |

---

## 5. Core End-to-End User Journeys

### Journey 1: SME Fast-Path — Interactive Multi-File Patch in Coding Studio
1. A developer opens **Interactive Coding Studio** (`#/coding-studio`), selects an indexed repository (`AiaCodeRepoBinding`), and invokes `/unit-test` referencing `@file:order-validator.ts` and `@issue:APM-204`.
2. The assistant retrieves pinned repo symbols and active `AiaCodingRulePack` conventions, posts a cited explanation on the `projectChannelMessage` thread, and creates an `AiaCodePatchProposal` adding edge-case unit tests across two files.
3. Automatic secret and SAST checks mark `securityScanStatus = PASSED`. The developer accepts 3 of 4 diff hunks (`PARTIALLY_ACCEPTED` -> `ACCEPTED`), exports/applies the patch to a feature branch, and `AiaUsageLedgerEntry` records exact `Decimal128` token spend (`\$0.0420`).

### Journey 2: Backlog-to-PR Autonomous Coding Task (`APM` -> `AIA` -> Git PR)
1. From **Autonomous Coding Tasks** (`#/coding-tasks`), a tech lead clicks **Dispatch Coding Task**, opens the `new-coding-task` drawer, picks `ApmIssue` *"Add CSV export filter tags to Vendor directory"*, selects target repo/branch, and submits.
2. The drawer resets its button inside `finally`, invalidates SWR cache, broadcasts `RECORD_CREATED`, closes via `closePageDrawer()`, and adds the new card under `QUEUED` on `<rapider-kanban>`.
3. OpenWhisk workflow `aiaRunSandboxCodingTask` spins up an ephemeral sandbox (`SANDBOX_RUNNING`), drafts `planMarkdown`, edits files, executes unit tests (self-healing a lint error on iteration 2 of 5), and generates a clean `AiaCodePatchProposal` (`AWAITING_REVIEW`).
4. The lead clicks the task number `TASK-1048` on the board -> navigates to `#/coding-task-detail?id=...`, inspects test logs and diff hunks, clicks **Publish Draft PR**, and the status updates to `PR_OPENED` while posting a timeline link back to `ApmIssue`.

### Journey 3: Protected-Path & Budget Exception via Rapider Home `WorkItem`
1. An autonomous `AiaCodingTask` proposes edits touching `src/security/rbac-guard.ts`, which matches `protectedPathGlobs` (`**/security/**`) in `AiaCodingPolicy`.
2. Guarded command `PublishTaskPullRequest` blocks automatic branch push and emits a high-priority **Rapider Home `WorkItem`** assigned to the AppSec/Engineering Lead role with direct deep-link context to `#/coding-task-detail`.
3. Simultaneously, if a developer hits 100% of their `\$50.00` `monthlySeatCapAmount`, requesting temporary burst quota emits a budget-override `WorkItem` to Engineering Management. Once approved in Home `WorkItem`s, `aia.workitem.resolved` unlocks the task/quota cleanly with an immutable audit entry.

### Journey 4: Automated First-Pass Agentic PR Review & One-Click Autofix
1. Opening or updating a Pull Request triggers `aiaTriggerAgenticPrReview` idempotently for `(repoBindingId, externalPrId, headCommitSha)`.
2. `AiaPrReviewRun` analyzes the diff against cross-file callers and `AiaCodingRulePack` rules (including checking for Rapider rules like hardcoded secrets or missing `Decimal128` on money fields), creating 1 `HIGH` security `AiaReviewFinding` and 2 `MEDIUM` bug findings with unified `autofixDiff` patches.
3. On `#/pr-reviews`, the author clicks `PR #418` -> opens `#/pr-review-detail?id=...`, clicks **Apply Autofix** on the `HIGH` finding (committing the verified patch and setting `disposition = AUTOFIX_APPLIED`), or clicks **Hand Off to Coding Task** to address multi-file review feedback autonomously, then clicks **Back to PR Reviews** restoring their active severity filter tags (`#activeFilterTagsBar`).

### Journey 5: Governance Tuning & Velocity ROI Inspection
1. An Engineering Director visits **Usage Ledger & Velocity ROI** (`#/usage-analytics`) filtered by `ApmProject` and date window.
2. They review total `Decimal128` spend (`\$1,284.65` of `\$2,000.00` workspace cap), 14-day accepted-code survival rate (`84.2%`), and average PR review cycle-time reduction paired with `AiaCodingRulePack` false-positive dismissal rates, then tune noisy rules in `#/rule-packs` with optimistic UI updates.

---

## 6. Consolidated Feature Priorities & Work Packages

### 6.1 `P0` Foundation Work Packages (Must-Have Release Core)
- **WP-P0-1 — Repo Context & Scoped Rule Packs (`ACA-001`, `ACA-002`):** `AiaCodeRepoBinding` CRUD, forced secret-glob exclusions, indexing watermarks, and `AiaCodingRulePack` standards authoring.
- **WP-P0-2 — Grounded Coding Studio & Hunk Proposals (`ACA-006`, `ACA-007`, `ACA-008`):** `AiaCodingSession` + `projectChannelMessage` studio, `@file`/`@symbol`/`@issue` context grounding, multi-model selector, and hunk-level `AiaCodePatchProposal` workflow.
- **WP-P0-3 — Sandbox Issue-to-PR Tasks & Human Gates (`ACA-011`, `ACA-012`, `ACA-014`):** `AiaCodingTask` `<rapider-kanban>` + list views, bounded sandbox execution loop, and mandatory Home `WorkItem` gates on protected paths.
- **WP-P0-4 — Agentic PR Review & Secret/SAST Blocking (`ACA-016`, `ACA-017`):** Idempotent `AiaPrReviewRun` engine, inline `AiaReviewFinding` generation, and hard block on `BLOCKED_SECRET` / `BLOCKED_SAST` diffs.
- **WP-P0-5 — Policy Guardrails & `Decimal128` Spend Ledger (`ACA-021`, `ACA-022`):** `AiaCodingPolicy` console (`<rapider-phone-input>` for AppSec escalation) and immutable `AiaUsageLedgerEntry` metering.

### 6.2 `P1` Scale & Enterprise Work Packages
- **WP-P1-1 — Schema/Issue Grounding & Slash Recipes (`ACA-003`, `ACA-004`, `ACA-005`):** Rapider manifest/component schema grounding, `ApmIssue` acceptance criteria pinning, and parameterized team slash recipes.
- **WP-P1-2 — Test Synthesis, Parallel Worktrees & Autofix Handoffs (`ACA-009`, `ACA-013`, `ACA-018`, `ACA-019`):** Unit/E2E test generator, parallel sub-task branch decomposition, one-click PR review autofix, and public-code/copyleft license screening.
- **WP-P1-3 — Persistence Telemetry, CLI Bridge & Quota Escalations (`ACA-023`, `ACA-024`, `ACA-025`):** 14-day code survival metrics, scoped CLI/webhook bridge tokens, and `WorkItem` seat budget override workflows.

### 6.3 `P2` Adjacent & Advanced Intelligence Work Packages
- **WP-P2-1 — Legacy Modernization, CI Auto-Triage & Drift Checks (`ACA-010`, `ACA-015`, `ACA-020`):** Legacy dependency maps, `#105` failed CI log remediation proposals, and cross-suite schema drift detection.
- **WP-P2-2 — Sprint Velocity Correlation, Rule Tuning & Onboarding (`ACA-026`, `ACA-027`, `ACA-028`):** Aggregate `ApmSprint` velocity correlation, rule noise analytics, and grounded repo onboarding guides.

---

## 7. Roles, Permissions & Field-Level Governance

| Role | Permitted Actions | Restricted / Field-Level Boundaries |
| :--- | :--- | :--- |
| **Developer (`aia.developer`)** | Create own `AiaCodingSession`s; generate/accept `AiaCodePatchProposal`s on permitted repos; dispatch `AiaCodingTask`s; apply PR autofixes; view own `AiaUsageLedgerEntry` spend. | Cannot edit `AiaCodingPolicy`, raise own `monthlySeatCapAmount`, bypass `BLOCKED_SECRET`/`BLOCKED_SAST` blocks, or view individual token logs of peers. |
| **Tech Lead / Reviewer (`aia.tech_lead`)** | All Developer actions + author/publish team `AiaCodingRulePack`s, manage `AiaCodeRepoBinding`s for assigned `ApmProject`s, approve standard PR handoffs, view aggregate team velocity/spend. | Cannot disable workspace-wide `enforceZeroDataRetention` or override `CRITICAL` security findings without AppSec role. |
| **AppSec / Governance Admin (`aia.security_admin`)** | Configure `AiaCodingPolicy` (ZDR, model allowlists, `protectedPathGlobs`, copyleft blocking); approve/reject protected-path & `CRITICAL` security `WorkItem`s; export audit logs. | Cannot mutate historical `AiaUsageLedgerEntry` records (append-only invariant enforced at storage/command layer). |
| **Engineering FinOps / Workspace Admin (`aia.admin`)** | Configure workspace & seat `Decimal128` spend caps, approve budget-override `WorkItem`s, manage provider secret references (`credentialSecretRef`). | Raw secret values in platform vault remain write-only/masked (`********`) on all UI responses and API reads. |

---

## 8. Technical APIs, Guarded Commands, Events & `requiredWorkflows`

### 8.1 Idempotent Guarded Commands
Every state-mutating API requires `idempotencyKey` (UUID), `correlationId` (UUID), and `expectedVersion` (optimistic concurrency):
- `TriggerRepoContextIndex` — Validates `credentialSecretRef`, enforces secret-file exclusion globs, and enqueues incremental symbol/vector indexing on `AiaCodeRepoBinding`.
- `ProposeSessionCodePatch` — Executes grounded prompt against allowed ZDR model, runs deterministic secret/SAST & license scanners, creates `AiaCodePatchProposal`, and appends `AiaUsageLedgerEntry`.
- `DispatchAutonomousCodingTask` — Checks caller's remaining `Decimal128` seat/workspace cap, links `apmIssueId`, creates `AiaCodingTask` (`QUEUED`), and starts sandbox workflow.
- `PublishTaskPullRequest` — Verifies `testRunStatus`, checks changed files against `protectedPathGlobs` (creating a Platform `WorkItem` if matched), or opens draft PR and records `externalPrUrl`.
- `ApplyReviewFindingAutofix` — Commits `AiaReviewFinding.autofixDiff` to PR head branch and updates `disposition = AUTOFIX_APPLIED`.

### 8.2 Domain Events (Kafka)
- **Published:** `aia.repo.indexed.v1`, `aia.coding_task.dispatched.v1`, `aia.coding_task.awaiting_approval.v1`, `aia.coding_task.pr_opened.v1`, `aia.pr_review.completed.v1`, `aia.security.secret_blocked.v1`, `aia.usage.cap_threshold_reached.v1`.
- **Consumed:** `apm.issue.assigned_to_agent.v1` (auto-creates draft `AiaCodingTask`), `git.pull_request.synchronized.v1` (triggers `AiaPrReviewRun`), `cicd.pipeline.failed.v1` (optional `P2` remediation draft), `platform.workitem.completed.v1` (unlocks gated `AiaCodingTask` or budget cap).

### 8.3 `requiredWorkflows` (Declared in `app.manifest.json`)
1. `aiaIndexRepositoryContextWorkflow` — Incremental AST/symbol + embedding indexer with strict `.env`/keyfile scrubbing.
2. `aiaRunSandboxCodingTaskWorkflow` — Ephemeral isolated container orchestrator executing plan -> edit -> lint/test -> patch scan up to `maxIterations`.
3. `aiaTriggerAgenticPrReviewWorkflow` — Webhook/event-driven cross-file PR diff analyzer and inline autofix generator.
4. `aiaEvaluateSpendThresholdWorkflow` — Real-time `Decimal128` spend aggregator emitting 80% warning notifications and 100% hard-cap `WorkItem` escalations.

### 8.4 Grounded Rapider AI Guardrails
- **Citation Mandate:** Every coding session answer, legacy walkthrough, and PR review finding MUST cite concrete repository file paths, line ranges (`file.ts:L42-L68`), or canonical `ApmIssue` IDs.
- **Zero ACL Bypass:** Context retrieval queries strictly intersect with the requesting user's repository and `ApmProject` read permissions.
- **Human Confirmation for Consequential Actions:** Autonomous tasks can **never** merge a Pull Request, push directly to `main`/`production`, alter `AiaCodingPolicy`, or deploy infrastructure without explicit human confirmation.

---

## 9. Security, Privacy, Compliance & Non-Functional Requirements

- **Zero-Data-Retention (ZDR) & Prompt Privacy (SOC 2 Type II / ISO 27001 / GDPR):** When `enforceZeroDataRetention = true`, requests route exclusively to ZDR-contracted model endpoints where prompts and code snippets are never retained or used for model training. Customer PII and credentials detected via regex/entropy pre-filters are redacted before external LLM egress.
- **Strict Secret Ban:** Zero hardcoded API keys, Git tokens, database URIs, or webhook secrets in source code, `Aia*` records, or E2E harnesses; only masked vault pointers (`credentialSecretRef`) are persisted.
- **Immutable Audit & Retention:** `AiaUsageLedgerEntry` and accepted `AiaCodePatchProposal` / `AiaPrReviewRun` snapshots are append-only for SOC 2 change-management traceability (configurable 1–7 year retention; session chat logs support configurable 90-day auto-purge).
- **Accessibility & Responsive UX:** Full **WCAG 2.2 AA** compliance (keyboard-navigable diff hunks, ARIA labels on icon-only delete buttons, high-contrast syntax themes in both Dark and Light modes, `#ffffff !important` text on primary/danger actions) and responsive layouts across `390px` (mobile status/review triage), `768px` (tablet), and `1440px` (desktop split-pane studio).
- **Performance Targets:** Initial page render `< 400ms` via `findSWR`/`countSWR`; client-side search/tag filtering `< 50ms`; first-pass agentic PR review `< 90s` p95 for diffs up to 1,500 lines.

---

## 10. Deterministic Acceptance Criteria

1. **Sidebar 3-Item Grouping Rule:** Inspecting `app.manifest.json` confirms 9 menu-visible pages organized into 3 sidebar sections (`Coding Workspace`, `Agentic Delivery`, `Governance & Insights`) with **3 items each**, while `coding-task-detail`, `pr-review-detail`, and `new-coding-task` set `displayOnMenu: false`.
2. **SWR Clean Query & Soft-Delete Hygiene:** Every page mounts via `findSWR` / `countSWR` with zero client-side `isDeleted` where filters and defensively filters local arrays (`item.isDeleted !== true`).
3. **Table Actions & Click-Through Navigation:** Tables on `repositories`, `coding-tasks`, `patch-proposals`, `pr-reviews`, and `rule-packs` contain **no View button**; clicking the primary identifier navigates to the detail route, `Edit` renders icon+text, and `Delete` renders icon-only with ARIA tooltip and custom confirmation modal (zero `window.alert`/`confirm`/`prompt`).
4. **Search, `#activeFilterTagsBar` & `Clear all`:** Typing a search query or clicking a status/severity pill synchronously filters both List and `<rapider-kanban>` views, displays HTML-escaped dismissible chips in `#activeFilterTagsBar`, and clicking `Clear all` resets all filters and restores the full dataset.
5. **Custom Elements Adoption:** `coding-tasks` uses `<rapider-kanban>` for task pipeline stages, and `governance-policies` uses `<rapider-phone-input>` for E.164 AppSec escalation phone entry.
6. **Drawer Lifecycle & `finally` Reset:** Submitting or cancelling `new-coding-task` restores button label/disabled state inside a `finally` block, clears `AiaCodingTask` SWR cache, broadcasts `RECORD_CREATED`, and closes the drawer via `closePageDrawer()`.
7. **Optimistic Edit & Delete with Rollback:** Editing a rule pack (`AiaCodingRulePack`) or deleting a draft repo binding immediately mutates in-memory state, re-renders List/Kanban views, clears SWR `sessionStorage` keys, and rolls back cleanly with an error toast on simulated API failure.
8. **Secret & SAST Hard Block Invariant:** Any `AiaCodePatchProposal` containing simulated AWS/Git/DB secret patterns transitions to `securityScanStatus = BLOCKED_SECRET` and deterministically rejects `Accept` / `Publish PR` commands.
9. **Protected-Path Home `WorkItem` Gate:** Dispatching an `AiaCodingTask` whose diff modifies a path matching `AiaCodingPolicy.protectedPathGlobs` halts at `AWAITING_REVIEW` and creates a linked Rapider Home `WorkItem` rather than opening an external PR automatically.
10. **Idempotent Agentic PR Review:** Re-delivering the identical `(repoBindingId, externalPrId, headCommitSha)` event returns the existing `AiaPrReviewRun` without duplicating `AiaReviewFinding` records.
11. **Exact `Decimal128` Metering & Hard Cap Enforcement:** All token rates, monthly caps (e.g., `\$50.00`), and `AiaUsageLedgerEntry.estimatedCostAmount` persist as `Decimal128` with `currencyCode`; attempts to mutate or delete a posted `AiaUsageLedgerEntry` are rejected, and exceeding 100% seat cap blocks new non-exempt tasks while issuing a budget-override `WorkItem`.
12. **No `projectId` Leakage:** Schema inspection across all 9 `Aia*` models confirms zero `projectId` or `workspaceId` fields.
13. **Dark & Light Theme Contrast:** Automated `validate_theme` passes across all 12 routes in both Light and Dark modes, verifying `#ffffff !important` contrast on all primary and destructive buttons.
14. **Real Click-Through & Back Restoration E2E:** E2E test clicks a filtered `TASK-1048` link on `#/coding-tasks`, asserts parameter hydration and diff rendering on `#/coding-task-detail?id=...` (zero `<base href>` 404 diversion), clicks `Back to Tasks`, and verifies active filter chips remain intact.

# v5.1.3 — targeted implementation

Baseline: accepted v5.1.2 ZIP SHA256 `0D61850144615AAB86000A5C13A2E0A67550FB518DB51989AE35A2611F07D31E`. Previous releases remain unchanged. No production deployment.

| Requirement | Source | Change | Acceptance |
|---|---|---|---|
| Live manual bulk criteria | BulkScoringModal.tsx; bulkScoring.ts | Profile-driven candidates; explicit scored status; changed records only | Test 1 |
| Real roster/job registry | realSourceMapping.ts; jobFamilyRegistry.ts; JobFamilyMapping.tsx | Business-field-only preview; 21 families; exact title suggestions; approval reference + 100-weight profile required | Test 4 (partial) |
| Production/downtime, maintenance, Kasra | realSourceMapping.ts; realSourcePlan.ts; RealSourceImport.tsx | Exact tracking/code joins; missing metrics stay pending; weighted ratios; custom configured thresholds; one source-authorized changed-set commit | Tests 2–3 |
| Violations | disciplinaryViolations.ts; state.ts; ViolationManager.tsx; ViolationPolicyEditor.tsx | Server command validation, independent approval, policy dates/cap, duplicate incident/import checks, immutable history, appeal/reversal, finalized protection | Test 5 |
| Deduction visibility | formulaEngine.ts; MyEvaluation.tsx | Separate base/approved deduction/final; KPI values unchanged | Test 5 |
| Access/live state | authorization.ts; accessControl.ts; navigation.ts; domainEvents.ts; syncState.ts; App.tsx; GranularPermissionEditor.tsx | Dedicated scoped module; server-filtered cases; accepted-state invalidation | Tests 1, 5 |

Boundaries: no policy is auto-approved or activated in production; no historical employee activation; no full-suite or large benchmark. 21 inactive KPI model drafts are supplied. Specialized subprofiles, activation in approved role profiles and reviewed internal/mixed-role allocations remain unfinished. This is a partial implementation, not full acceptance of the requested enterprise scope.

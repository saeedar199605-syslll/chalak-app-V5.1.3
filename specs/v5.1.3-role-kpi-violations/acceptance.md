# Focused local acceptance

## Final targeted completion — 2026-10-10

Actual input: `C:/Users/Saeed/Downloads/عملکرد پرسنل نت.xls`, confirmed SpreadsheetML XML (not binary XLS). The worker-compatible streaming reader preserves typed/sparse cells and rejects malformed XML/DTD or excessive dimensions. Actual MIS headers are reused; no new guessed mapping. Canonical request/person/date/time/activity keys reject repeated activities; conflicting duplicate durations quarantine all versions. A second duplicate guard applies before aggregation; reimport replaces the same source metric instead of accumulating it.

Only two checks on isolated Pages Functions/CHALAK_DB KV with the existing 626-employee baseline:

1. Actual XML: 5233 data rows including blanks, 5174 valid unique activities, 43 rejected/ambiguous rows. A complete real August group contains 81 work minutes and 30 standard minutes: exact efficiency `30/81*100 = 37.03703703703704`; local-only test thresholds give score 2. One MIS commit HTTP 200, revision 2; fresh server GET confirms the exact score/raw metric. Missing/zero standards stay null; duplicate input is counted once. Test thresholds are not production approvals.
2. Real browser roster preview for codes 1306 (production operator), 5086 (mechanical technician), 13434 (administrative employee): title/internal responsibility and respective criteria/weights displayed; each total 100. No model was activated. One authorized manual score on a disposable isolated record: HTTP 200, revision 3, exact 4 persisted after a fresh server GET.

Typecheck PASS once; production build PASS once. Violation module retained; policy inactive in the source and the isolated test. No production deployment or claim about live 503/1102.

Personnel assignment now requires an exact unique existing code, reviewed title/description, explicit confirmation, valid existing approved profile, and approval reference; assignment and reference are saved together through the existing audited Admin save. Industrial-worker and mixed-duty models remain suggestions until responsibility allocation and weights are approved. Historical evaluation profiles and global proposed models are not activated automatically.

Completion source/config files: `src/utils/spreadsheetXml.ts`, `src/utils/excelWorkbook.ts`, `src/utils/realSourceMapping.ts`, `src/utils/realSourcePlan.ts`, `src/utils/personnelRolePreview.ts`, `src/utils/jobFamilyRegistry.ts`, `src/components/RealSourceImport.tsx`, `src/components/JobFamilyMapping.tsx`, `package.json`, `package-lock.json`. Input workbooks, local data/secrets/test scripts and dependencies are excluded from the new release. Earlier acceptance results below are historical, not repeated.

Backend: actual local Wrangler Pages Functions + CHALAK_DB KV, isolated persistence directory. Existing 626-employee state retained; disposable records used for scoring/violations. No production writes or deployment.

| Check | Result |
|---|---|
| 1 bulk manual score, two disposable records | HTTP 200; exact 4 and 3 survived fresh backend GET. A new criterion was added while the real bulk dialog stayed open; it appeared without reload. Supervisor saved 3 for both disposable records through the UI; HTTP 200, revision 13, dialog closed only after acknowledgement; fresh backend read confirmed [3,3], and reload showed the persisted results. |
| 2 real production/downtime slice | Three actual input rows; two parsed, one rejected due conflicting duplicate personnel-code columns. One eligible evaluation HTTP 200, exact scores persisted; unrelated scores preserved. |
| 3 real maintenance + Kasra slices | Three actual rows per source; each one eligible evaluation committed HTTP 200 and exact values persisted. Missing standard time remained null; no efficiency fabricated. XML maintenance file absent. |
| 4 role families/profiles | 21 families and 61 exact title suggestions checked; three isolated source profiles used. 21 inactive engineering drafts are supplied; production approval, specialized subprofiles, mixed-role effective allocations and complete internal mappings remain unfinished. |
| 5 manual + Excel violation lifecycle | HTTP 200 create/submit/review/approve/appeal/reverse; draft deduction 0, approved 2, base 80/final 78; duplicate import HTTP 409, no second record/deduction; reversal 0 after fresh backend GET; audit preserved. |

Typecheck and production build passed initially. A focused real-file check caught use of a Gregorian-only date helper for Jalali dates; corrected to the existing Jalali calendar converter. Final validation of this correction is recorded below. No broad regression suite was run.

Production remains unverified. Final status is PARTIAL: no claim that all requested v5.1.3 features, production policies, or the production 1102 failure are resolved.

Final validation: typecheck PASS; production build PASS after the Jalali correction and scoped-history protections. Focused guard checks returned HTTP 403 for forged deduction, direct case/history writes and deletion of an evaluation with violation history. All 21 inactive models have weights totaling 100 and unset approved targets/thresholds. The two builds were required by the real-file date failure; no full acceptance/regression loop was repeated.

Exact changed source/config files (27):

- `src/App.tsx`
- `src/types.ts`
- `src/components/BulkScoringModal.tsx`
- `src/components/ExcelIntegrationCenter.tsx`
- `src/components/GranularPermissionEditor.tsx`
- `src/components/JobFamilyMapping.tsx`
- `src/components/JobProfiles.tsx`
- `src/components/MyEvaluation.tsx`
- `src/components/RealSourceImport.tsx`
- `src/components/ViolationManager.tsx`
- `src/components/ViolationPolicyEditor.tsx`
- `src/utils/accessControl.ts`
- `src/utils/authorization.ts`
- `src/utils/bulkScoring.ts`
- `src/utils/businessDate.ts`
- `src/utils/disciplinaryViolations.ts`
- `src/utils/domainEvents.ts`
- `src/utils/formulaEngine.ts`
- `src/utils/jobFamilyRegistry.ts`
- `src/utils/navigation.ts`
- `src/utils/realSourceMapping.ts`
- `src/utils/realSourcePlan.ts`
- `src/utils/roleKpiDrafts.ts`
- `functions/api/state.ts`
- `cloudflare/syncState.ts`
- `package.json`
- `package-lock.json`

Final UI read after reload: the dedicated violations page showed both disposable cases as reversed, retained their historical approved points and exposed their audit histories. No production data changed.

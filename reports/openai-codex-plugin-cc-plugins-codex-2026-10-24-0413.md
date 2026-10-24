# SkillSpector Security Report

**Skill:** unknown  
**Source:** `/home/runner/work/_temp/target/plugins/codex`  
**Scanned:** 2026-10-24 04:14:01 UTC  

## Risk Assessment

| Metric | Value |
|--------|-------|
| Score | 38/100 |
| Severity | MEDIUM |
| Recommendation | CAUTION |

## Components (43)

| File | Type | Lines | Executable |
|------|------|-------|------------|
| `.claude-plugin/plugin.json` | json | 8 | No |
| `CHANGELOG.md` | markdown | 5 | No |
| `LICENSE` | other | 201 | No |
| `NOTICE` | other | 13 | No |
| `agents/codex-rescue.md` | markdown | 46 | No |
| `commands/adversarial-review.md` | markdown | 66 | No |
| `commands/cancel.md` | markdown | 8 | No |
| `commands/rescue.md` | markdown | 49 | No |
| `commands/result.md` | markdown | 15 | No |
| `commands/review.md` | markdown | 61 | No |
| `commands/setup.md` | markdown | 37 | No |
| `commands/status.md` | markdown | 17 | No |
| `commands/transfer.md` | markdown | 10 | No |
| `hooks/hooks.json` | json | 38 | No |
| `prompts/adversarial-review.md` | markdown | 84 | No |
| `prompts/stop-review-gate.md` | markdown | 36 | No |
| `schemas/review-output.schema.json` | json | 87 | No |
| `scripts/app-server-broker.mjs` | other | 252 | Yes |
| `scripts/codex-companion.mjs` | other | 1073 | Yes |
| `scripts/lib/app-server-protocol.d.ts` | typescript | 75 | Yes |
| `scripts/lib/app-server.mjs` | other | 354 | Yes |
| `scripts/lib/args.mjs` | other | 128 | Yes |
| `scripts/lib/broker-endpoint.mjs` | other | 41 | Yes |
| `scripts/lib/broker-lifecycle.mjs` | other | 209 | Yes |
| `scripts/lib/claude-session-transfer.mjs` | other | 44 | Yes |
| `scripts/lib/codex.mjs` | other | 1219 | Yes |
| `scripts/lib/fs.mjs` | other | 40 | Yes |
| `scripts/lib/git.mjs` | other | 347 | Yes |
| `scripts/lib/job-control.mjs` | other | 308 | Yes |
| `scripts/lib/process.mjs` | other | 135 | Yes |
| `scripts/lib/prompts.mjs` | other | 13 | Yes |
| `scripts/lib/render.mjs` | other | 465 | Yes |
| `scripts/lib/state.mjs` | other | 191 | Yes |
| `scripts/lib/tracked-jobs.mjs` | other | 204 | Yes |
| `scripts/lib/workspace.mjs` | other | 9 | Yes |
| `scripts/session-lifecycle-hook.mjs` | other | 133 | Yes |
| `scripts/stop-review-gate-hook.mjs` | other | 184 | Yes |
| `skills/codex-cli-runtime/SKILL.md` | markdown | 43 | No |
| `skills/codex-result-handling/SKILL.md` | markdown | 21 | No |
| `skills/gpt-5-4-prompting/SKILL.md` | markdown | 54 | No |
| `skills/gpt-5-4-prompting/references/codex-prompt-antipatterns.md` | markdown | 100 | No |
| `skills/gpt-5-4-prompting/references/codex-prompt-recipes.md` | markdown | 150 | No |
| `skills/gpt-5-4-prompting/references/prompt-blocks.md` | markdown | 172 | No |

## Issues (3)

### 🔴 HIGH: P6

**Location:** `commands/setup.md:34`  
**Confidence:** 85%  

**Message:** Direct Prompt Extraction

**Remediation:** Remove any instructions that reveal, print, or output system prompts or internal rules\. System instructions should never be exposed to end users\.

---

### 🟡 MEDIUM: BH1

**Location:** `hooks/hooks.json:1`  
**Confidence:** 95%  

**Message:** Bundled hooks can execute when matching lifecycle events occur\.

**Remediation:** Review bundled hook handlers, destinations, and event reach before install\.

**Evidence:**
- **activation\_reason:** `requires_hook_activation`
- **activation\_state:** `conditional`
- **declaration\_count:** `3`
- **events:** `['SessionEnd', 'SessionStart', 'Stop']`
- **handler\_types:** `['command']`
- **matcher\_breadth:** `['all', 'not_applicable']`
- **payload\_analysis\_level:** `unmodeled`
- **reach:** `ambient`
- **target\_summary:** `command`
- **unknown\_event\_count:** `0`
- **unknown\_handler\_count:** `0`

---

### 🟡 MEDIUM: EA2

**Location:** `skills/gpt-5-4-prompting/references/prompt-blocks.md:47`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

## Inspection Completeness

| Metric | Value |
|--------|-------|
| Execution | successful |
| Status | partial |
| Coverage | 60\.5% |
| Fully inspected | 26 |
| Partially inspected | 17 |
| Entirely uninspected | 0 |

### Ledger Exceptions

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| static\_parse\_limit | `commands/rescue.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| opaque\_content | `hooks/hooks.json` | Artifact contents could not be fully interpreted\. |
| static\_parse\_limit | `scripts/app-server-broker.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| obfuscated\_instruction\_text | `scripts/codex-companion.mjs` | Obfuscated instruction text could not be fully evaluated by the deterministic layer\. |
| static\_parse\_limit | `scripts/codex-companion.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/app-server.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/broker-endpoint.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/broker-lifecycle.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/claude-session-transfer.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/codex.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/fs.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/git.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/process.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/render.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/state.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/lib/tracked-jobs.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/session-lifecycle-hook.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `scripts/stop-review-gate-hook.mjs` | A security\-relevant expression exceeded a bounded static parser's span limit\. |

### Analyzer Statuses

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| completed | `artifact_integrity` |  |
| no\_applicable\_files | `behavioral_ast` | No files matched this analyzer's applicability contract\. |
| no\_applicable\_files | `behavioral_taint_tracking` | No files matched this analyzer's applicability contract\. |
| degraded | `bundled_execution_surface` |  |
| manifest\_absent | `mcp_least_privilege` | No compatible manifest was present for this analyzer\. |
| completed | `mcp_rug_pull` |  |
| manifest\_absent | `mcp_tool_poisoning` | No compatible manifest was present for this analyzer\. |
| disabled\_by\_configuration | `meta_analyzer` | Analyzer was disabled by the requested configuration\. |
| disabled\_by\_configuration | `semantic_developer_intent` | Analyzer was disabled by the requested configuration\. |
| disabled\_by\_configuration | `semantic_quality_policy` | Analyzer was disabled by the requested configuration\. |
| disabled\_by\_configuration | `semantic_security_discovery` | Analyzer was disabled by the requested configuration\. |
| degraded | `static_patterns_agent_snooping` |  |
| degraded | `static_patterns_anti_refusal` |  |
| completed | `static_patterns_data_exfiltration` |  |
| degraded | `static_patterns_deserialization` |  |
| degraded | `static_patterns_excessive_agency` |  |
| degraded | `static_patterns_harmful_content` |  |
| degraded | `static_patterns_memory_poisoning` |  |
| completed | `static_patterns_output_handling` |  |
| degraded | `static_patterns_privilege_escalation` |  |
| degraded | `static_patterns_prompt_injection` |  |
| degraded | `static_patterns_rogue_agent` |  |
| degraded | `static_patterns_ssrf` |  |
| degraded | `static_patterns_supply_chain` |  |
| degraded | `static_patterns_system_prompt_leakage` |  |
| degraded | `static_patterns_tool_misuse` |  |
| completed | `static_yara` |  |

### Limitations

- Analyzer bundled\_execution\_surface status: degraded\.
- Analyzer static\_patterns\_agent\_snooping status: degraded\.
- Analyzer static\_patterns\_anti\_refusal status: degraded\.
- Analyzer static\_patterns\_deserialization status: degraded\.
- Analyzer static\_patterns\_excessive\_agency status: degraded\.
- Analyzer static\_patterns\_harmful\_content status: degraded\.
- Analyzer static\_patterns\_memory\_poisoning status: degraded\.
- Analyzer static\_patterns\_privilege\_escalation status: degraded\.
- Analyzer static\_patterns\_prompt\_injection status: degraded\.
- Analyzer static\_patterns\_rogue\_agent status: degraded\.
- Analyzer static\_patterns\_ssrf status: degraded\.
- Analyzer static\_patterns\_supply\_chain status: degraded\.
- Analyzer static\_patterns\_system\_prompt\_leakage status: degraded\.
- Analyzer static\_patterns\_tool\_misuse status: degraded\.

## Metadata

- **Executable Scripts:** Yes

*Generated by SkillSpector v2.12.0*
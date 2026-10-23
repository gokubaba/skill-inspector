# SkillSpector Security Report

**Skill:** unknown  
**Source:** `/home/runner/work/_temp/target/plugins/claude-security`  
**Scanned:** 2026-10-23 21:23:50 UTC  

## Risk Assessment

| Metric | Value |
|--------|-------|
| Score | 100/100 |
| Severity | CRITICAL |
| Recommendation | DO NOT INSTALL |

## Components (46)

| File | Type | Lines | Executable |
|------|------|-------|------------|
| `.claude-plugin/plugin.json` | json | 20 | No |
| `.gitattributes` | other | 3 | No |
| `LICENSE` | other | 28 | No |
| `NOTICE.md` | markdown | 9 | No |
| `README.md` | markdown | 100 | No |
| `SECURITY.md` | markdown | 23 | No |
| `agents/claude-security.md` | markdown | 21 | No |
| `agents/explore.md` | markdown | 30 | No |
| `agents/patch-generator.md` | markdown | 49 | No |
| `agents/patch-verifier.md` | markdown | 52 | No |
| `agents/scan-inventory.md` | markdown | 32 | No |
| `agents/scan-loader.md` | markdown | 10 | No |
| `agents/scan-redactor.md` | markdown | 16 | No |
| `agents/scan-researcher.md` | markdown | 64 | No |
| `agents/scan-verifier.md` | markdown | 52 | No |
| `hooks/hooks.json` | json | 70 | No |
| `hooks/hooks.py` | python | 492 | Yes |
| `hooks/hooks.sh` | shell | 31 | Yes |
| `scripts/keep-waiting.sh` | shell | 14 | Yes |
| `scripts/lib/__init__.py` | python | 1 | Yes |
| `scripts/lib/absolute.py` | python | 26 | Yes |
| `scripts/lib/chain.py` | python | 67 | Yes |
| `scripts/lib/console.py` | python | 17 | Yes |
| `scripts/lib/cwe-categories.json` | json | 1473 | No |
| `scripts/lib/cwe.py` | python | 79 | Yes |
| `scripts/lib/finding.py` | python | 467 | Yes |
| `scripts/lib/git.py` | python | 27 | Yes |
| `scripts/lib/link.py` | python | 23 | Yes |
| `scripts/lib/plugin.py` | python | 52 | Yes |
| `scripts/lib/revision.py` | python | 28 | Yes |
| `scripts/lib/sarif.py` | python | 385 | Yes |
| `scripts/lib/secret.py` | python | 43 | Yes |
| `scripts/lib/source.py` | python | 94 | Yes |
| `scripts/lib/strictjson.py` | python | 89 | Yes |
| `scripts/patch_artifacts.py` | python | 1283 | Yes |
| `scripts/render_report.py` | python | 980 | Yes |
| `scripts/save_result.py` | python | 533 | Yes |
| `scripts/write_scan_meta.py` | python | 550 | Yes |
| `skills/claude-security/SKILL.md` | markdown | 69 | No |
| `skills/claude-security/jobs/scan-changes.md` | markdown | 146 | No |
| `skills/claude-security/jobs/scan-codebase.md` | markdown | 126 | No |
| `skills/claude-security/jobs/suggest-patches.md` | markdown | 125 | No |
| `skills/claude-security/role.md` | markdown | 65 | No |
| `skills/claude-security/specs/patch-spec.md` | markdown | 99 | No |
| `skills/claude-security/specs/report-spec.md` | markdown | 219 | No |
| `workflows/scan.js` | javascript | 156 | Yes |

## Issues (14)

### 🔴 HIGH: AR2

**Location:** `agents/patch-generator.md:12`  
**Confidence:** 85%  

**Message:** Anti\-Refusal Statement

**Remediation:** Remove instructions that suppress warnings, disclaimers, or ethical commentary\. Let the agent surface safety\-relevant caveats to the user\.

---

### 🔴 HIGH: AR1

**Location:** `agents/scan-researcher.md:51`  
**Confidence:** 85%  

**Message:** Anti\-Refusal Statement

**Remediation:** Remove any instruction telling the agent to never refuse or always comply\. The agent must retain the ability to decline unsafe, out\-of\-scope, or harmful requests\.

---

### 🔴 HIGH: E2

**Location:** `scripts/lib/git.py:9`  
**Confidence:** 70%  

**Message:** Env Variable Harvesting

**Remediation:** Read only explicitly required environment variables by name\. Avoid enumerating or copying the full environment, and never log or transmit credentials to untrusted destinations\.

---

### 🔴 HIGH: AR2

**Location:** `skills/claude-security/role.md:17`  
**Confidence:** 80%  

**Message:** Anti\-Refusal Statement

**Remediation:** Remove instructions that suppress warnings, disclaimers, or ethical commentary\. Let the agent surface safety\-relevant caveats to the user\.

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-security/specs/patch-spec.md:39`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🟡 MEDIUM: EA2

**Location:** `agents/claude-security.md:17`  
**Confidence:** 85%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `agents/scan-verifier.md:48`  
**Confidence:** 85%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: BH1

**Location:** `hooks/hooks.json:1`  
**Confidence:** 95%  

**Message:** Bundled hooks can execute when matching lifecycle events occur\.

**Remediation:** Review bundled hook handlers, destinations, and event reach before install\.

**Evidence:**
- **activation\_reason:** `requires_hook_activation`
- **activation\_state:** `conditional`
- **declaration\_count:** `6`
- **events:** `['PermissionRequest', 'PostToolUse', 'PostToolUseFailure', 'UserPromptExpansion']`
- **handler\_types:** `['command']`
- **matcher\_breadth:** `['scoped', 'unsupported']`
- **payload\_analysis\_level:** `unmodeled`
- **reach:** `ambient`
- **target\_summary:** `command`
- **unknown\_event\_count:** `0`
- **unknown\_handler\_count:** `0`

---

### 🟡 MEDIUM: AST4

**Location:** `hooks/hooks.py:322–328`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: EA2

**Location:** `scripts/lib/cwe-categories.json:60`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: AST4

**Location:** `scripts/lib/git.py:15–22`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: AST4

**Location:** `scripts/patch_artifacts.py:535–542`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: EA2

**Location:** `skills/claude-security/role.md:61`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟢 LOW: EA3

**Location:** `skills/claude-security/jobs/suggest-patches.md:122`  
**Confidence:** 75%  

**Message:** Scope Creep

**Remediation:** Limit the skill's scope to its documented purpose\. Remove instructions that enable the agent to perform actions outside its stated functionality\.

---

## Inspection Completeness

| Metric | Value |
|--------|-------|
| Execution | successful |
| Status | partial |
| Coverage | 93\.5% |
| Fully inspected | 43 |
| Partially inspected | 3 |
| Entirely uninspected | 0 |

### Ledger Exceptions

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| opaque\_content | `hooks/hooks.json` | Artifact contents could not be fully interpreted\. |
| static\_parse\_limit | `skills/claude-security/jobs/suggest-patches.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| obfuscated\_instruction\_text | `workflows/scan.js` | Obfuscated instruction text could not be fully evaluated by the deterministic layer\. |
| static\_parse\_limit | `workflows/scan.js` | A security\-relevant expression exceeded a bounded static parser's span limit\. |

### Analyzer Statuses

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| completed | `artifact_integrity` |  |
| completed | `behavioral_ast` |  |
| completed | `behavioral_taint_tracking` |  |
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
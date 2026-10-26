# SkillSpector Security Report

**Skill:** unknown  
**Source:** `/home/runner/work/_temp/target/skills`  
**Scanned:** 2026-10-26 00:14:07 UTC  

## Risk Assessment

| Metric | Value |
|--------|-------|
| Score | 38/100 |
| Severity | MEDIUM |
| Recommendation | CAUTION |

## Components (9)

| File | Type | Lines | Executable |
|------|------|-------|------------|
| `claudex-loop/ADR-FORMAT.md` | markdown | 34 | No |
| `claudex-loop/CONTEXT-FORMAT.md` | markdown | 35 | No |
| `claudex-loop/SKILL.md` | markdown | 90 | No |
| `claudex-loop/references/build.md` | markdown | 37 | No |
| `claudex-loop/references/runtime.md` | markdown | 57 | No |
| `claudex-loop/scripts/runner.py` | python | 491 | Yes |
| `claudex-route/SKILL.md` | markdown | 62 | No |
| `codex-build/SKILL.md` | markdown | 17 | No |
| `codex-review/SKILL.md` | markdown | 16 | No |

## Issues (9)

### 🟡 MEDIUM: TT2

**Location:** `claudex-loop/scripts/runner.py:47`  
**Confidence:** 65%  

**Message:** Tainted flow: 'value' from pathlib\.Path\.read\_bytes \(line 383, file read\) → pathlib\.Path\.write\_text \(file write\)

**Remediation:** Validate tainted variables before passing them to sinks\. Use allowlists, type checks, or sanitization functions on data from external sources\.

---

### 🟡 MEDIUM: AST4

**Location:** `claudex-loop/scripts/runner.py:83`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: AST4

**Location:** `claudex-loop/scripts/runner.py:155–156`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: AST4

**Location:** `claudex-loop/scripts/runner.py:216–217`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: TT2

**Location:** `claudex-loop/scripts/runner.py:216–217`  
**Confidence:** 65%  

**Message:** Tainted flow: 'argv' from pathlib\.Path\.read\_text \(line 431, file read\) → subprocess\.Popen \(code execution\)

**Remediation:** Validate tainted variables before passing them to sinks\. Use allowlists, type checks, or sanitization functions on data from external sources\.

---

### 🟡 MEDIUM: AST4

**Location:** `claudex-loop/scripts/runner.py:222–223`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: EA2

**Location:** `claudex-loop/scripts/runner.py:227`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: AST4

**Location:** `claudex-loop/scripts/runner.py:332`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

### 🟡 MEDIUM: AST4

**Location:** `claudex-loop/scripts/runner.py:418`  
**Confidence:** 70%  

**Message:** subprocess module call

**Remediation:** Use subprocess\.run\(\) with shell=False and an explicit argument list\. Validate all inputs and avoid passing user\-controlled data to commands\.

---

## Inspection Completeness

| Metric | Value |
|--------|-------|
| Execution | successful |
| Status | complete |
| Coverage | 100\.0% |
| Fully inspected | 9 |
| Partially inspected | 0 |
| Entirely uninspected | 0 |

### Analyzer Statuses

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| completed | `artifact_integrity` |  |
| completed | `behavioral_ast` |  |
| completed | `behavioral_taint_tracking` |  |
| no\_applicable\_files | `bundled_execution_surface` | No files matched this analyzer's applicability contract\. |
| manifest\_absent | `mcp_least_privilege` | No compatible manifest was present for this analyzer\. |
| completed | `mcp_rug_pull` |  |
| manifest\_absent | `mcp_tool_poisoning` | No compatible manifest was present for this analyzer\. |
| disabled\_by\_configuration | `meta_analyzer` | Analyzer was disabled by the requested configuration\. |
| disabled\_by\_configuration | `semantic_developer_intent` | Analyzer was disabled by the requested configuration\. |
| disabled\_by\_configuration | `semantic_quality_policy` | Analyzer was disabled by the requested configuration\. |
| disabled\_by\_configuration | `semantic_security_discovery` | Analyzer was disabled by the requested configuration\. |
| completed | `static_patterns_agent_snooping` |  |
| completed | `static_patterns_anti_refusal` |  |
| completed | `static_patterns_data_exfiltration` |  |
| completed | `static_patterns_deserialization` |  |
| completed | `static_patterns_excessive_agency` |  |
| completed | `static_patterns_harmful_content` |  |
| completed | `static_patterns_memory_poisoning` |  |
| completed | `static_patterns_output_handling` |  |
| completed | `static_patterns_privilege_escalation` |  |
| completed | `static_patterns_prompt_injection` |  |
| completed | `static_patterns_rogue_agent` |  |
| completed | `static_patterns_ssrf` |  |
| completed | `static_patterns_supply_chain` |  |
| completed | `static_patterns_system_prompt_leakage` |  |
| completed | `static_patterns_tool_misuse` |  |
| completed | `static_yara` |  |

## Metadata

- **Executable Scripts:** Yes

*Generated by SkillSpector v2.12.0*
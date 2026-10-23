# SkillSpector Security Report

**Skill:** unknown  
**Source:** `/home/runner/work/_temp/target/plugins/claude-code-setup`  
**Scanned:** 2026-10-23 21:00:00 UTC  

## Risk Assessment

| Metric | Value |
|--------|-------|
| Score | 100/100 |
| Severity | CRITICAL |
| Recommendation | DO NOT INSTALL |

## Components (10)

| File | Type | Lines | Executable |
|------|------|-------|------------|
| `.claude-plugin/plugin.json` | json | 9 | No |
| `LICENSE` | other | 202 | No |
| `README.md` | markdown | 29 | No |
| `automation-recommender-example.png` | other | 14331 | No |
| `skills/claude-automation-recommender/SKILL.md` | markdown | 289 | No |
| `skills/claude-automation-recommender/references/hooks-patterns.md` | markdown | 226 | No |
| `skills/claude-automation-recommender/references/mcp-servers.md` | markdown | 276 | No |
| `skills/claude-automation-recommender/references/plugins-reference.md` | markdown | 98 | No |
| `skills/claude-automation-recommender/references/skills-reference.md` | markdown | 408 | No |
| `skills/claude-automation-recommender/references/subagent-templates.md` | markdown | 181 | No |

## Issues (12)

### 🔴 HIGH: P6

**Location:** `skills/claude-automation-recommender/SKILL.md:13`  
**Confidence:** 85%  

**Message:** Direct Prompt Extraction

**Remediation:** Remove any instructions that reveal, print, or output system prompts or internal rules\. System instructions should never be exposed to end users\.

---

### 🔴 HIGH: EA5

**Location:** `skills/claude-automation-recommender/SKILL.md:273`  
**Confidence:** 90%  

**Message:** External Model or Provider Selection

**Remediation:** Remove the model/provider override or disclose it prominently and require explicit operator approval before invoking an external coding CLI or billed model\.

**Evidence:**
- **selection\_surface:** `command`

---

### 🔴 HIGH: EA5

**Location:** `skills/claude-automation-recommender/SKILL.md:276`  
**Confidence:** 90%  

**Message:** External Model or Provider Selection

**Remediation:** Remove the model/provider override or disclose it prominently and require explicit operator approval before invoking an external coding CLI or billed model\.

**Evidence:**
- **selection\_surface:** `command`

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:85`  
**Confidence:** 70%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:85`  
**Confidence:** 70%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:133`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:133`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:209`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:209`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🟡 MEDIUM: EA2

**Location:** `skills/claude-automation-recommender/references/hooks-patterns.md:3`  
**Confidence:** 80%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: RP1

**Location:** `skills/claude-automation-recommender/references/mcp-servers.md:85`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx convex'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `skills/claude-automation-recommender/references/skills-reference.md:188`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx prisma'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

## Inspection Completeness

| Metric | Value |
|--------|-------|
| Execution | successful |
| Status | partial |
| Coverage | 88\.9% |
| Fully inspected | 8 |
| Partially inspected | 1 |
| Entirely uninspected | 0 |

### Scope Exclusions

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| binary\_content | `automation-recommender-example.png` | Binary content is unsupported by this analyzer\. |

### Ledger Exceptions

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| static\_parse\_limit | `skills/claude-automation-recommender/references/skills-reference.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |

### Analyzer Statuses

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| completed | `artifact_integrity` |  |
| no\_applicable\_files | `behavioral_ast` | No files matched this analyzer's applicability contract\. |
| no\_applicable\_files | `behavioral_taint_tracking` | No files matched this analyzer's applicability contract\. |
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
| degraded | `static_patterns_tool_misuse` |  |
| completed | `static_yara` |  |

### Limitations

- Analyzer static\_patterns\_tool\_misuse status: degraded\.

## Metadata

- **Executable Scripts:** No

*Generated by SkillSpector v2.12.0*
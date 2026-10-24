# SkillSpector Security Report

**Skill:** unknown  
**Source:** `/home/runner/work/_temp/target/c-level-agents`  
**Scanned:** 2026-10-24 04:14:20 UTC  

## Risk Assessment

| Metric | Value |
|--------|-------|
| Score | 14/100 |
| Severity | LOW |
| Recommendation | SAFE |

## Components (39)

| File | Type | Lines | Executable |
|------|------|-------|------------|
| `.claude-plugin/plugin.json` | json | 15 | No |
| `README.md` | markdown | 92 | No |
| `agents/cs-caio-advisor.md` | markdown | 176 | No |
| `agents/cs-cco-advisor.md` | markdown | 174 | No |
| `agents/cs-cdo-advisor.md` | markdown | 162 | No |
| `agents/cs-cfo-advisor.md` | markdown | 129 | No |
| `agents/cs-chief-of-staff.md` | markdown | 132 | No |
| `agents/cs-chro-advisor.md` | markdown | 119 | No |
| `agents/cs-ciso-advisor.md` | markdown | 124 | No |
| `agents/cs-cmo-advisor.md` | markdown | 123 | No |
| `agents/cs-coo-advisor.md` | markdown | 124 | No |
| `agents/cs-cpo-advisor.md` | markdown | 123 | No |
| `agents/cs-cro-advisor.md` | markdown | 120 | No |
| `agents/cs-general-counsel-advisor.md` | markdown | 167 | No |
| `agents/cs-vpe-advisor.md` | markdown | 162 | No |
| `references/llm-wiki-bridge.md` | markdown | 95 | No |
| `references/persona-voices.md` | markdown | 116 | No |
| `skills/boardroom/SKILL.md` | markdown | 134 | No |
| `skills/brief/SKILL.md` | markdown | 118 | No |
| `skills/c-level-agents/SKILL.md` | markdown | 119 | No |
| `skills/caio-review/SKILL.md` | markdown | 140 | No |
| `skills/cco-review/SKILL.md` | markdown | 130 | No |
| `skills/cdo-review/SKILL.md` | markdown | 126 | No |
| `skills/cfo-review/SKILL.md` | markdown | 105 | No |
| `skills/ciso-review/SKILL.md` | markdown | 113 | No |
| `skills/cmo-review/SKILL.md` | markdown | 101 | No |
| `skills/cpo-review/SKILL.md` | markdown | 110 | No |
| `skills/cro-review/SKILL.md` | markdown | 110 | No |
| `skills/cross-eval/SKILL.md` | markdown | 115 | No |
| `skills/cto-review/SKILL.md` | markdown | 117 | No |
| `skills/decide/SKILL.md` | markdown | 104 | No |
| `skills/execute/SKILL.md` | markdown | 99 | No |
| `skills/founder-mode/SKILL.md` | markdown | 108 | No |
| `skills/freeze/SKILL.md` | markdown | 101 | No |
| `skills/gc-review/SKILL.md` | markdown | 132 | No |
| `skills/office-hours/SKILL.md` | markdown | 114 | No |
| `skills/onboard/SKILL.md` | markdown | 126 | No |
| `skills/post-mortem/SKILL.md` | markdown | 115 | No |
| `skills/vpe-review/SKILL.md` | markdown | 129 | No |

## Issues (6)

### 🟡 MEDIUM: AS3

**Location:** `agents/cs-caio-advisor.md:170`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `agents/cs-cco-advisor.md:168`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `agents/cs-cdo-advisor.md:157`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `agents/cs-general-counsel-advisor.md:161`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `agents/cs-vpe-advisor.md:157`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `skills/post-mortem/SKILL.md:111`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

## Inspection Completeness

| Metric | Value |
|--------|-------|
| Execution | successful |
| Status | complete |
| Coverage | 100\.0% |
| Fully inspected | 39 |
| Partially inspected | 0 |
| Entirely uninspected | 0 |

### Scope Exclusions

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| not\_regular\_file | `vendor/c-level-advisor/agent-protocol` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/board-meeting` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/cfo-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/change-management` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/chief-ai-officer-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/chief-customer-officer-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/chief-data-officer-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/chief-of-staff` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/chro-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/ciso-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/cmo-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/company-os` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/context-engine` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/coo-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/cpo-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/cro-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/cs-onboard` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/cto-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/decision-logger` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/general-counsel-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/ma-playbook` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/strategic-alignment` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/c-level-advisor/vpe-advisor` | Inventoried path is no longer a regular file\. |
| not\_regular\_file | `vendor/product-team/product-manager-toolkit` | Inventoried path is no longer a regular file\. |

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
| completed | `static_patterns_tool_misuse` |  |
| completed | `static_yara` |  |

## Metadata

- **Executable Scripts:** No

*Generated by SkillSpector v2.12.0*
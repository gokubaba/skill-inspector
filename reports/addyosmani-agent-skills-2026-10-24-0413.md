# SkillSpector Security Report

**Skill:** unknown  
**Source:** `/home/runner/work/_temp/target/skills`  
**Scanned:** 2026-10-24 04:15:08 UTC  

## Risk Assessment

| Metric | Value |
|--------|-------|
| Score | 100/100 |
| Severity | CRITICAL |
| Recommendation | DO NOT INSTALL |

## Components (32)

| File | Type | Lines | Executable |
|------|------|-------|------------|
| `api-and-interface-design/SKILL.md` | markdown | 367 | No |
| `browser-testing-with-devtools/SKILL.md` | markdown | 317 | No |
| `ci-cd-and-automation/SKILL.md` | markdown | 390 | No |
| `code-review-and-quality/SKILL.md` | markdown | 398 | No |
| `code-simplification/SKILL.md` | markdown | 331 | No |
| `constraint-driven-development/SKILL.md` | markdown | 311 | No |
| `constraint-driven-development/references/floor-guard.md` | markdown | 182 | No |
| `context-engineering/SKILL.md` | markdown | 353 | No |
| `debugging-and-error-recovery/SKILL.md` | markdown | 300 | No |
| `deprecation-and-migration/SKILL.md` | markdown | 247 | No |
| `documentation-and-adrs/SKILL.md` | markdown | 297 | No |
| `doubt-driven-development/SKILL.md` | markdown | 243 | No |
| `frontend-ui-engineering/SKILL.md` | markdown | 340 | No |
| `git-workflow-and-versioning/SKILL.md` | markdown | 355 | No |
| `idea-refine/SKILL.md` | markdown | 193 | No |
| `idea-refine/examples.md` | markdown | 238 | No |
| `idea-refine/frameworks.md` | markdown | 99 | No |
| `idea-refine/refinement-criteria.md` | markdown | 113 | No |
| `idea-refine/scripts/idea-refine.sh` | shell | 15 | Yes |
| `incremental-implementation/SKILL.md` | markdown | 249 | No |
| `interview-me/SKILL.md` | markdown | 235 | No |
| `observability-and-instrumentation/SKILL.md` | markdown | 238 | No |
| `performance-optimization/SKILL.md` | markdown | 267 | No |
| `performance-optimization/references/optimization-patterns.md` | markdown | 250 | No |
| `planning-and-task-breakdown/SKILL.md` | markdown | 257 | No |
| `security-and-hardening/SKILL.md` | markdown | 216 | No |
| `security-and-hardening/references/hardening-patterns.md` | markdown | 324 | No |
| `shipping-and-launch/SKILL.md` | markdown | 336 | No |
| `source-driven-development/SKILL.md` | markdown | 216 | No |
| `spec-driven-development/SKILL.md` | markdown | 259 | No |
| `test-driven-development/SKILL.md` | markdown | 398 | No |
| `using-agent-skills/SKILL.md` | markdown | 192 | No |

## Issues (48)

### 🔴 HIGH: TM1

**Location:** `api-and-interface-design/SKILL.md:226`  
**Confidence:** 80%  

**Message:** Tool Parameter Abuse

**Remediation:** Validate all tool parameters against an allowlist\. Reject dangerous parameter values \(shell=True, \-\-force, \-rf /\) and use safe defaults\.

---

### 🔴 HIGH: YR1

**Location:** `browser-testing-with-devtools/SKILL.md:64`  
**Confidence:** 75%  

**Message:** YARA rule 'info\_stealer': Information stealer patterns \(credential harvesting, browser data theft\) \[malware\]

**Remediation:** Remove the malware payload or compromised file entirely\. Investigate how it entered the skill and audit all other artifacts for additional indicators of compromise\.

---

### 🔴 HIGH: P1

**Location:** `browser-testing-with-devtools/SKILL.md:77`  
**Confidence:** 80%  

**Message:** Instruction Override

**Remediation:** Remove or rewrite any text that instructs the agent to ignore prompts, override safety rules, or trust unverified content\. Ensure skill content cannot be injected to alter agent behavior\.

---

### 🔴 HIGH: YR4

**Location:** `browser-testing-with-devtools/SKILL.md:77`  
**Confidence:** 80%  

**Message:** YARA rule 'agent\_skill\_prompt\_injection\_hidden\_instructions': Prompt injection or hidden instructions embedded in AI agent skill text \[agent\_skills\]

**Remediation:** Remove offensive tool references and exploit code\. Legitimate agent skills should not contain penetration testing tools, exploit frameworks, or reconnaissance utilities\.

---

### 🔴 HIGH: PE3

**Location:** `ci-cd-and-automation/SKILL.md:275`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `context-engineering/SKILL.md:65`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `security-and-hardening/references/hardening-patterns.md:276`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `security-and-hardening/references/hardening-patterns.md:278`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `security-and-hardening/references/hardening-patterns.md:282`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: RA1

**Location:** `code-simplification/SKILL.md:155`  
**Confidence:** 70%  

**Message:** Self\-Modification

**Remediation:** Prevent the skill from modifying its own code, SKILL\.md, or configuration files\. Treat skill files as read\-only at runtime\.

---

### 🔴 HIGH: EA5

**Location:** `doubt-driven-development/SKILL.md:144`  
**Confidence:** 90%  

**Message:** External Model or Provider Selection

**Remediation:** Remove the model/provider override or disclose it prominently and require explicit operator approval before invoking an external coding CLI or billed model\.

**Evidence:**
- **selection\_surface:** `command`

---

### 🔴 HIGH: TM1

**Location:** `git-workflow-and-versioning/SKILL.md:189`  
**Confidence:** 65%  

**Message:** Tool Parameter Abuse

**Remediation:** Validate all tool parameters against an allowlist\. Reject dangerous parameter values \(shell=True, \-\-force, \-rf /\) and use safe defaults\.

---

### 🔴 HIGH: YR4

**Location:** `security-and-hardening/SKILL.md:21`  
**Confidence:** 80%  

**Message:** YARA rule 'agent\_skill\_prompt\_injection\_hidden\_instructions': Prompt injection or hidden instructions embedded in AI agent skill text \[agent\_skills\]

**Remediation:** Remove offensive tool references and exploit code\. Legitimate agent skills should not contain penetration testing tools, exploit frameworks, or reconnaissance utilities\.

---

### 🔴 HIGH: MP3

**Location:** `security-and-hardening/SKILL.md:129`  
**Confidence:** 80%  

**Message:** Memory Manipulation

**Remediation:** Protect agent memory and state from modification by untrusted content\. Use read\-only memory for critical instructions and validate all state changes\.

---

### 🔴 HIGH: SSRF1

**Location:** `security-and-hardening/references/hardening-patterns.md:150`  
**Confidence:** 90%  

**Message:** Cloud Metadata Access

**Remediation:** Remove access to cloud metadata endpoints unless strictly required\. If metadata is needed, restrict it \(e\.g\. IMDSv2 with hop limit\) and never expose returned credentials\.

---

### 🔴 HIGH: PE3

**Location:** `security-and-hardening/references/hardening-patterns.md:279`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: PE3

**Location:** `security-and-hardening/references/hardening-patterns.md:283`  
**Confidence:** 60%  

**Message:** Credential Access

**Remediation:** Remove references to credential paths\. Use environment variables or secrets managers\. For docs, use placeholder paths \(e\.g\., /path/to/config\)\. Never load \.env or token files in production code paths\.

---

### 🔴 HIGH: AR2

**Location:** `shipping-and-launch/SKILL.md:25`  
**Confidence:** 80%  

**Message:** Anti\-Refusal Statement

**Remediation:** Remove instructions that suppress warnings, disclaimers, or ethical commentary\. Let the agent surface safety\-relevant caveats to the user\.

---

### 🔴 HIGH: YR4

**Location:** `source-driven-development/SKILL.md:101`  
**Confidence:** 80%  

**Message:** YARA rule 'agent\_skill\_prompt\_injection\_hidden\_instructions': Prompt injection or hidden instructions embedded in AI agent skill text \[agent\_skills\]

**Remediation:** Remove offensive tool references and exploit code\. Legitimate agent skills should not contain penetration testing tools, exploit frameworks, or reconnaissance utilities\.

---

### 🔴 HIGH: P1

**Location:** `source-driven-development/SKILL.md:110`  
**Confidence:** 80%  

**Message:** Instruction Override

**Remediation:** Remove or rewrite any text that instructs the agent to ignore prompts, override safety rules, or trust unverified content\. Ensure skill content cannot be injected to alter agent behavior\.

---

### 🟡 MEDIUM: RP1

**Location:** `browser-testing-with-devtools/SKILL.md:41`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx install'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:88`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx tsc'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:348`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx tsc'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `context-engineering/SKILL.md:55`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx tsc'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `git-workflow-and-versioning/SKILL.md:229`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx tsc'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `incremental-implementation/SKILL.md:206`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx tsc'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:128`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx prisma'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:152`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx playwright'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:156`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx playwright'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:207`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx vercel'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `ci-cd-and-automation/SKILL.md:268`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx vercel'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: EA2

**Location:** `context-engineering/SKILL.md:66`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `source-driven-development/SKILL.md:194`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `test-driven-development/SKILL.md:378`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `using-agent-skills/SKILL.md:120`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `context-engineering/SKILL.md:342`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: RP1

**Location:** `deprecation-and-migration/SKILL.md:91`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx migrate\-check'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `performance-optimization/SKILL.md:206`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx bundlesize'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: RP1

**Location:** `performance-optimization/SKILL.md:209`  
**Confidence:** 70%  

**Message:** MCP server referenced without pinned version: 'npx lhci'\.

**Remediation:** Pin the version: npx @scope/server@1\.2\.3

---

### 🟡 MEDIUM: EA2

**Location:** `planning-and-task-breakdown/SKILL.md:234`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `planning-and-task-breakdown/SKILL.md:237`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `security-and-hardening/SKILL.md:198`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: EA2

**Location:** `spec-driven-development/SKILL.md:113`  
**Confidence:** 75%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟡 MEDIUM: AS3

**Location:** `spec-driven-development/SKILL.md:214`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `spec-driven-development/SKILL.md:214`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: AS3

**Location:** `spec-driven-development/SKILL.md:214`  
**Confidence:** 80%  

**Message:** Skill Enumeration

**Remediation:** Remove all code or instructions that list or read other skills' files or directories\. Skills should operate independently; cross\-skill access is a privilege escalation\.

---

### 🟡 MEDIUM: EA2

**Location:** `using-agent-skills/SKILL.md:135`  
**Confidence:** 85%  

**Message:** Autonomous Decision Making

**Remediation:** Add human\-in\-the\-loop confirmation for destructive, irreversible, or high\-impact operations\. Never auto\-execute commands that modify files, send data, or alter system state\.

---

### 🟢 LOW: EA3

**Location:** `code-simplification/SKILL.md:103`  
**Confidence:** 75%  

**Message:** Scope Creep

**Remediation:** Limit the skill's scope to its documented purpose\. Remove instructions that enable the agent to perform actions outside its stated functionality\.

---

## Inspection Completeness

| Metric | Value |
|--------|-------|
| Execution | successful |
| Status | partial |
| Coverage | 81\.2% |
| Fully inspected | 26 |
| Partially inspected | 6 |
| Entirely uninspected | 0 |

### Ledger Exceptions

| Reason / Status | Location | Details |
|-----------------|----------|---------|
| static\_parse\_limit | `api-and-interface-design/SKILL.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| obfuscated\_instruction\_text | `code-review-and-quality/SKILL.md` | Obfuscated instruction text could not be fully evaluated by the deterministic layer\. |
| static\_parse\_limit | `constraint-driven-development/SKILL.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `constraint-driven-development/references/floor-guard.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `observability-and-instrumentation/SKILL.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |
| static\_parse\_limit | `security-and-hardening/references/hardening-patterns.md` | A security\-relevant expression exceeded a bounded static parser's span limit\. |

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
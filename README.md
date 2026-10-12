# OWASP Top 10 for LLMs & AI Agent Shield Studio

> **Production Repository:** `Pradeeptalari14/tp-owasp-llm-agent-shield`  
> **Interactive Studio Workspace:** [https://talaripradeep.info/tools/owasp-llm-agent-shield/](https://talaripradeep.info/tools/owasp-llm-agent-shield/)  
> **Visual Flow Canvas:** [https://talaripradeep.info/studios/flow/?studio=owasp-llm-agent-shield](https://talaripradeep.info/studios/flow/?studio=owasp-llm-agent-shield)

## Overview
Protect agent swarms and RAG workflows against OWASP Top 10 for LLMs: prompt injections, insecure tool hijacking, sensitive data leakage, and denial of service.

## Primary Specification Manifest: `guardrails-config.yaml`
```yaml
guardrails:
  version: "2.0"
  owaspCompliance:
    llm01_prompt_injection:
      classifier: "meta-llama/Llama-Guard-3-8B"
      action: "BLOCK_AND_LOG"
    llm02_insecure_output:
      sanitizer: "html-escape-strict"
    llm06_sensitive_info:
      masking: "PII_REGEX_ENTITIES"
    llm08_tool_hijacking:
      humanInTheLoop: true
      sandbox: "gVisor"
```

## Verification & Execution
```bash
# Run local verification
git verify-commit HEAD
```

## License
MIT License. Copyright (c) 2026 Talari Pradeep.

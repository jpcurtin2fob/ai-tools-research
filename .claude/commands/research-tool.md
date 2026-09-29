---
description: Research a tool and draft its evaluation in tools/
argument-hint: <tool name>
---
Research **$ARGUMENTS** for this repository.

1. Read `CLAUDE.md` and `templates/tool-evaluation.md`.
2. If `tools/<tool-name>.md` exists, update it; otherwise create it from the template.
3. Research using official sources (the tool's docs, GitHub releases, AWS docs).
   Focus on AWS integration with SageMaker AI and Bedrock, overlap with
   AWS-native services, security, operations, and cost.
4. Fill every section. Mark anything you couldn't verify with `> ⚠️ Unverified:`.
5. Set Status to "Researching", fill Version evaluated and Last reviewed (today).
6. Update the Tool index in `README.md` and `landscape/ml-lifecycle-map.md` if needed.
7. Summarize what you found and list the open questions for a human to check.

# Project context for Claude

## Purpose
This repository holds a team's research on tools for machine learning and
generative-AI applications. The output is Markdown documents that are shared
with teammates and reviewed through pull requests.

## Our environment
- **Cloud:** AWS only. ML workloads run on **Amazon SageMaker AI**; generative-AI
  workloads use **Amazon Bedrock**.
- **Team:** DevOps / platform engineers working with data scientists. Readers are
  comfortable with AWS, IaC, CI/CD, and containers, but may be new to ML/AI.
- **Primary concerns:** how a tool deploys and runs on AWS, IAM and networking
  (VPC, private endpoints), cost, operational burden, and overlap with
  AWS-native services.

## Conventions
- Tool evaluations go in `tools/<tool-name>.md` and MUST follow
  `templates/tool-evaluation.md` exactly (same headings, same order).
- Comparisons go in `comparisons/<topic>.md` and follow `templates/comparison.md`.
- Decision records go in `decisions/NNNN-short-title.md` and follow `templates/adr.md`.
- File names: lowercase, hyphen-separated.
- After adding or changing a tool file, update the **Tool index** table in `README.md`
  and, if the tool is new, `landscape/ml-lifecycle-map.md`.
- Write plainly. Explain ML jargon briefly the first time it appears.

## Research rules
- **Look things up; don't rely on memory** for anything version-specific: feature
  availability, AWS integrations, pricing, licensing, and release status. Prefer
  official documentation (the tool's docs, AWS docs, GitHub releases).
- Every document ends with a **Sources** section of links actually used.
- Set **Version evaluated** and **Last reviewed** (YYYY-MM-DD) in every tool file.
- Always compare against the AWS-native alternative (for example SageMaker Model
  Monitor vs. Evidently, SageMaker managed MLflow vs. self-hosted MLflow,
  Bedrock Guardrails vs. third-party guardrails).
- If something is uncertain or couldn't be verified, mark it `> ⚠️ Unverified:`
  instead of guessing.
- Clearly separate facts (with sources) from our recommendation.

## Spikes
Proofs of concept live in `spikes/<tool-name>-<topic>/` with a `README.md`
explaining how to run them. Keep them small, never commit credentials, and
use AWS profiles/roles rather than access keys.

# ML / AI Lifecycle Map

Where each tool we research fits. Update this when a tool is added to `tools/`.

> Starting point only. Verify AWS feature details against current AWS docs.

| Lifecycle stage | What happens | AWS-native option | Tools to research |
|---|---|---|---|
| Data validation | Check data/schema correctness | SageMaker Data Wrangler, AWS Glue Data Quality | Pydantic, Great Expectations, Pandera |
| Experiment tracking | Log runs, params, metrics | SageMaker managed MLflow | MLflow (self-hosted), Weights & Biases |
| Model registry | Version and approve models | SageMaker Model Registry | MLflow Model Registry |
| Pipelines / orchestration | Automate train → deploy | SageMaker Pipelines, Step Functions | Airflow (MWAA), Kubeflow |
| Deployment / serving | Host models for inference | SageMaker endpoints, Bedrock | BentoML, KServe |
| Monitoring & drift | Detect data/model drift | SageMaker Model Monitor, CloudWatch | Evidently, WhyLabs |
| LLM app frameworks | Build RAG/agents | Bedrock Agents, Bedrock Knowledge Bases | LangChain, LlamaIndex |
| LLM structured output | Validate model responses | Bedrock tool use / structured output | Pydantic, Instructor |
| LLM evaluation | Measure quality of LLM output | Bedrock model evaluation | Ragas, DeepEval, promptfoo |
| Guardrails & safety | Filter inputs/outputs | Bedrock Guardrails | Guardrails AI, NeMo Guardrails |
| LLM observability | Trace prompts, cost, latency | CloudWatch, X-Ray | Langfuse, Arize Phoenix |

# GenAI Usage & Evaluation Monitor (Open Source)

## Overview
An open-source tool designed for SMBs (especially Legal Tech firms) using Azure OpenAI + OSS LLMs to track token usage, estimate GenAI costs, and perform post-hoc AI evaluations for hallucinations, PII leaks, and more.

## Problem
SMBs adopting GenAI on Azure face the following challenges:
- No unified view of AOAI + OSS model usage
- No clear link between app/agent behavior and cost
- No built-in tools for post-hoc LLM output evaluation
- Limited capacity to manage MLOps or AI risk infrastructure

## Solution
This tool provides:
- Token + model usage tracking across AOAI and OSS models
- Cost estimation using configurable token price inputs
- AI Evals: post-hoc analysis for PII, hallucinations, toxicity
- Unified dashboard and Slack/email alerts
- Audit reports for compliance-readiness

## Architecture
- Python-based middleware intercepts LLM API calls
- Token tracking using `tiktoken` and `tokenizers`
- Eval layer using Presidio, Detoxify, heuristics
- Streamlit dashboard + Prometheus/Grafana (optional)
- Dockerized for easy deployment

## OSS Stack
- tiktoken, HuggingFace tokenizers
- Presidio, Detoxify, Ragas (optional)
- Streamlit or FastAPI
- SQLite/Postgres
- Docker, GitHub Actions

## Use Cases
1. Cost driver analysis and prompt optimization
2. Post-hoc evals for output safety and hallucinations
3. AI audit trail generation
4. Alerting for excessive cost or risk

## Privacy & Ethics
- Optional logging of inputs/outputs with redaction
- Configurable eval thresholds and model registry

## Getting Started
1. Clone this repo
2. Configure AOAI token prices in `config.yaml`
3. Insert middleware into your app’s LLM call flow
4. Launch dashboard via `streamlit run dashboard.py`

## License
MIT

## Maintainers
Supriya Kashyap

# GenAI-eval-monitor
Open source GenAI usage and evaluation monitor for SMBs on Public cloud [focused on Legal tech use case]

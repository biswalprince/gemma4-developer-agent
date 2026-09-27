cat << 'EOF' > README.md
# Gemma 4 Developer Agent 🤖

This repository contains an autonomous software engineering agent built for the **Kaggle Gemma 4 Developer Agent Competition**. The agent is designed to navigate large codebases, resolve bugs, and submit validation patches using an LLM-driven tool loop.

## 🏗️ Architecture & Strategy
- **Base Model:** `gemma-4-31b-it-qat-w4a16-ct`
- **Agent Framework:** ADK (`LlmAgent`)
- **System Prompting:** 4-Phase Standard Operating Procedure (Investigation → Verification → Resolution → Finalization)
- **Constraint:** Heavily optimized for local evaluation due to the strict 1-submission-per-day Kaggle limit.

## 💻 Local Development Environment
- **OS:** Windows Subsystem for Linux (WSL2 - Ubuntu)
- **Hardware:** Intel i5-14450HX | NVIDIA GeForce RTX 5050 (8GB VRAM)
- **ML Stack:** PyTorch (CUDA 12.1), Hugging Face (`transformers`, `peft`, `trl`), Unsloth (for 4-bit QLoRA fine-tuning)

## 🚀 Current Status
- [x] Baseline zero-shot agent configured (`agent.yaml` + `system.md`).
- [x] Local GPU ML environment established.
- [ ] Parse Kaggle `tasks.jsonl` into Unsloth-compatible training trajectories.
- [ ] Run local QLoRA fine-tuning experiments.
EOF
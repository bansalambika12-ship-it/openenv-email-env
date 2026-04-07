# OpenEnv Email Hackathon (Minimal)

This is a lightweight, runnable Python project with an OpenEnv-style environment and three email tasks:

- Easy: spam classification (`easy_spam`)
- Medium: email prioritization (`medium_priority`)
- Hard: short reply generation (`hard_reply`)

## Project layout

- `env/email_env.py`: environment + Pydantic models (`Observation`, `Action`, `Reward`)
- `tasks/tasks.py`: graders (0..1) + incremental reward helper
- `inference.py`: runs one episode and prints `[START]`, `[STEP]`, `[END]`
- `openenv.yaml`: minimal OpenEnv config

## Quickstart (local)

```bash
python -m venv .venv
source .venv/bin/activate  # (Windows PowerShell: .venv\Scripts\Activate.ps1)
pip install -r requirements.txt
python inference.py
```

By default, if you **do not** set `HF_TOKEN` or `OPENAI_API_KEY`, `inference.py` uses a small built-in fallback policy so it still runs end-to-end without crashing.

## Using a model (OpenAI-compatible)

Environment variables:

- `API_BASE_URL`: optional (set for OpenAI-compatible endpoints)
- `MODEL_NAME`: model id/name (default: `gpt-4o-mini`)
- `HF_TOKEN`: API key/token (preferred name per spec)
- `OPENAI_API_KEY`: also supported as a fallback
- `TASK`: `easy_spam` | `medium_priority` | `hard_reply` (default: `easy_spam`)

Example:

```bash
export API_BASE_URL="https://api.openai.com/v1"
export MODEL_NAME="gpt-4o-mini"
export HF_TOKEN="YOUR_KEY"
export TASK="hard_reply"
python inference.py
```

## Docker

```bash
docker build -t openenv-email .
docker run --rm -e TASK=easy_spam openenv-email
```


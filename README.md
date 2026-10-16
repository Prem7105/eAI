# EternalAI

Predictive cloud recovery with controlled actions and verified application recovery.

## Build status

Implementation is in progress. This repository is not yet a runnable release.
No end-to-end recovery or cross-system accuracy results have been established for
this implementation. Results in the supplied prototype are historical input,
not benchmarks of this rebuild.

## Implementation contract

- Python services and dashboard, with FastAPI and validated Pydantic schemas.
- Separate application, reliability controller, and blind evaluator.
- The controller cannot read evaluator ground truth or injection controls.
- Shared feature extraction for training and live inference.
- Incident-grouped evaluation and leave-one-system-out evaluation.
- Missing measurements remain explicit; model features exclude labels.
- Reviewed, bounded recovery actions with deterministic permissions.
- A successful restart is insufficient: checkout must pass an observation window.
- Unsupported or unsuccessful recovery escalates without repeated interventions.
- Optional LLM explanations fall back to local templates. LLMs cannot execute commands.

## Configuration

Copy `.env.example` to `.env` and configure credentials locally when the services
are implemented. Never commit secrets. Watch-only is the default operating mode.

## Validation environment

The current build workspace has no Docker executable or container-management
capabilities. Python checks can run here; live Docker recovery, rollback, network
isolation, and benchmark results require a Docker-enabled runner. These checks
must pass before this repository can be described as live-demo ready.

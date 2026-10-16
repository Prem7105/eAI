# Input review

The supplied deck describes the observe/detect/predict/diagnose/act/verify loop.
Its performance figures describe the previous prototype, not this implementation.
The ZIP contains rules and live-trained Isolation Forest detection, but no
workbook-trained diagnosis artifact loader. Its browser JavaScript is not reused.

The workbook separates telemetry, knowledge and action outcomes. Metadata-only
RCAEval rows must not be treated as measured telemetry. Many disk features are
missing. Unverified incident articles are retrieval material, not training labels.
Existing mixed-system scores must not be substituted for unseen-system results.

The rebuild must keep evaluator secrets and ground truth outside the controller,
persist real application state, enforce runbook permissions independently of the
LLM, and verify checkout after interventions. Docker-level behavior cannot be
validated in the current workspace; it has no Docker daemon or container-management
capabilities. No successful container benchmark is claimed.

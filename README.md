
# ScamTrace

**Detect. Remember. Protect. Adapt.**

ScamTrace is a prototype for adaptive fraud detection. It is designed to analyze transaction behavior, identify suspicious activity, retain recurring scam patterns, and evaluate proposed detection updates before they are activated.

## Problem

Fraud patterns evolve. A detection system based only on fixed rules or previously observed examples may miss emerging behavior, while overly sensitive detection can generate too many false alarms.

## Proposed solution

ScamTrace combines multiple signals to support fraud-risk assessment:

1. **Hybrid AI detection:** supervised machine learning and anomaly detection.
2. **Scam DNA and threat memory:** fingerprints of previously observed scam patterns and relationships between suspicious cases.
3. **Temporal graph analysis:** account and transaction relationships modeled over time, with STGCN explored as an advanced detection component.
4. **Adaptive defense:** candidate rules and model updates evaluated against legitimate and suspicious cases before activation.
5. **Monitoring and versioning:** track detection performance and preserve the ability to roll back a problematic update.
6. **Explainable assessments:** provide risk indicators and reasons that help a human reviewer investigate suspicious activity.

## Planned technology stack

- Python 3.11
- Pandas and scikit-learn
- PyTorch for advanced model experiments
- NetworkX for initial graph analysis
- FastAPI for the analysis API
- SQLite initially, with PostgreSQL considered for later deployment
- Streamlit and Plotly for the dashboard
- pytest for automated tests

Dependencies will be introduced incrementally as the corresponding features are built.

## Planned data flow

Transaction data  
→ Input validation  
→ Feature engineering  
→ Hybrid detection  
→ Scam-pattern matching  
→ Risk assessment and explanation  
→ Review or alert  
→ Feedback and controlled evaluation  
→ Versioned defense update

## Prototype scope and limitations

- Development and initial evaluation will use synthetic and appropriately sourced historical data.
- The prototype will not connect to live banking systems or independently authorize, reject, or block payments.
- Detection scores are risk indicators, not guaranteed fraud probabilities.
- Performance claims will be made only after reproducible evaluation.
- Feedback and candidate rules will not automatically change the active model without validation.

## Development approach

ScamTrace is being developed incrementally in 60 planned commits. Each commit should have a clear purpose and a verifiable result.

See [ROADMAP.md](ROADMAP.md) for the build sequence and [BUILD_LOG.md](BUILD_LOG.md) for progress.

## Current status

**Commit 1/60:** Project initialization and development documentation.

No detection model or API has been implemented yet.

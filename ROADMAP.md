
# ScamTrace: 60-Commit Roadmap

## Phase 1: Foundation and data quality

- [ ] 01. Initialize project and documentation
- [ ] 02. Add Python project configuration
- [ ] 03. Create the application package structure
- [ ] 04. Add configuration loading and environment examples
- [ ] 05. Define transaction data fields and contracts
- [ ] 06. Generate reproducible synthetic transactions
- [ ] 07. Validate transaction inputs
- [ ] 08. Add data-quality checks
- [ ] 09. Create the initial unit-test suite
- [ ] 10. Add a reproducible data preparation command

## Phase 2: Baseline detection engine

- [ ] 11. Implement transaction feature engineering
- [ ] 12. Add time-based and behavioral features
- [ ] 13. Establish train, validation, and test splits
- [ ] 14. Train a supervised baseline classifier
- [ ] 15. Evaluate precision, recall, and PR-AUC
- [ ] 16. Add anomaly detection with Isolation Forest
- [ ] 17. Normalize and inspect anomaly scores
- [ ] 18. Define risk-score fusion and thresholds
- [ ] 19. Add human-readable detection reasons
- [ ] 20. Persist model artifacts and metadata
- [ ] 21. Add repeatable inference
- [ ] 22. Compare baseline detection approaches

## Phase 3: Scam DNA and threat memory

- [ ] 23. Define a scam-pattern data model
- [ ] 24. Build stable pattern fingerprints
- [ ] 25. Store known patterns in a local repository
- [ ] 26. Match new assessments against stored patterns
- [ ] 27. Add transaction-entity graph structures
- [ ] 28. Extract initial graph-based features
- [ ] 29. Detect suspicious relationship patterns
- [ ] 30. Link related cases and entities
- [ ] 31. Integrate threat-memory signals into assessments
- [ ] 32. Test unseen and related scam-pattern scenarios

## Phase 4: API, persistence, and dashboard

- [ ] 33. Create the FastAPI application
- [ ] 34. Add request and response schemas
- [ ] 35. Implement single-transaction analysis
- [ ] 36. Implement batch analysis
- [ ] 37. Add SQLite persistence
- [ ] 38. Store versioned risk assessments
- [ ] 39. Add alert and case retrieval
- [ ] 40. Build the Streamlit dashboard shell
- [ ] 41. Add risk indicators and case details
- [ ] 42. Add plots and assessment explanations

## Phase 5: Controlled adaptive defense

- [ ] 43. Define analyst feedback records
- [ ] 44. Capture feedback against specific assessments
- [ ] 45. Generate candidate detection rules
- [ ] 46. Build a rule evaluation harness
- [ ] 47. Test candidates on legitimate and suspicious cases
- [ ] 48. Measure false-positive and false-negative changes
- [ ] 49. Add versioned model and rule metadata
- [ ] 50. Introduce approval-gated activation
- [ ] 51. Add drift and performance monitoring
- [ ] 52. Implement rollback to a previous version

## Phase 6: Integration, safety, and demonstration

- [ ] 53. Add end-to-end integration tests
- [ ] 54. Test malformed and boundary-case inputs
- [ ] 55. Add API security and privacy checks
- [ ] 56. Add reproducible evaluation reports
- [ ] 57. Explore temporal graph model feasibility, including STGCN
- [ ] 58. Integrate advanced graph modeling only if justified by results
- [ ] 59. Complete documentation and demo scenarios
- [ ] 60. Run the final test suite and prepare the release

## Scope guardrails

- Build and measure a useful baseline before adding complex models.
- Do not claim STGCN performance before implementing and evaluating it.
- Do not combine incompatible model scores without a documented method.
- Do not treat analyst feedback as verified ground truth automatically.
- Do not activate candidate rules or models without evaluation.
- Do not use live payment access or claim automatic fraud prevention.
- Keep evaluation data separate from training data.

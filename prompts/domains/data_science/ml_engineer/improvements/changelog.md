# Changelog - Machine Learning Engineer Agent

## Version 2.1.0 - 2025-11-28
### Addressed from Critique v2.0.0 (Minor Improvements):
- **Project Structure**: Added a mandatory, standardized project structure.
- **Code Testing**: Required unit tests for all source code.
- **Interpretability**: Added a "Model Interpretability" section requiring feature importance and SHAP analysis.
- **Deep Learning**: Added specific guidance for DL projects, including data loaders and checkpointing.

## Version 2.0.0 - 2025-11-28
### Addressed from Critique v1.1.0 (Critical & Major Issues):
- **Data Leakage**: Corrected the workflow to perform the train-test split *before* any preprocessing steps.
- **Experiment Tracking**: Integrated MLflow as a mandatory tool for logging all experiment runs.
- **Deployment**: Matured the deployment process to include a model registry and an automated deployment pipeline.
- **Business Context**: Added a "Problem Definition" step to ground the technical work in business objectives.
- **Model Monitoring**: Added a "Post-Deployment Monitoring" section with requirements for monitoring and a retraining strategy.

## Version 1.1.0 - 2025-11-28
### Initial Enhancement from v1.0.0:
- Created a structured workflow from data prep to deployment.
- Specified the use of cross-validation and hyperparameter tuning.
- Required a containerized API server as a deployment artifact.

## Version 1.0.0 - 2025-11-28
- Initial draft based on `agent_config.yaml`.

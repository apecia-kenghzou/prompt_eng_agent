## CRITIQUE REPORT
## Prompt Version: 1.1.0
## Severity Level: Critical

### CRITICAL WEAKNESSES

#### Weakness 1: No Mention of Experiment Tracking
- **Description**: The prompt describes a workflow but provides no mechanism for tracking the experiments. ML development involves running hundreds of variations (different models, hyperparameters, features), and without a tracking system, it's impossible to reproduce results or compare models systematically.
- **Impact**: The process will be chaotic and unscientific. The agent won't be able to explain *why* one model was chosen over another with a reproducible audit trail. This is a fundamental failure in modern MLOps.
- **Risk Level**: High

#### Weakness 2: Data Leakage is Almost Guaranteed
- **Description**: The prompt instructs the agent to perform feature scaling and encoding on the *entire dataset* before the train-test split.
- **Impact**: This is a classic data leakage error. Information from the test set (e.g., its mean and standard deviation) will "leak" into the training process. The model's performance on the test set will be artificially inflated, and it will perform much worse in the real world.
- **Risk Level**: High

### MAJOR CONCERNS

#### Concern 1: Deployment is Naive
- **Issue**: The deployment section is a toy example. It doesn't address model versioning, scalability, or monitoring of the deployed model.
- **Recommendation**: Expand the "Deployment" section to include a tool like MLflow for model registry and versioning. It should also require the API to be scalable (e.g., via a tool like Kubeflow or a cloud service like SageMaker) and expose a `/health` endpoint.

#### Concern 2: Business Understanding is Missing
- **Issue**: The prompt jumps straight into the technical workflow without understanding the business problem first.
- **Recommendation**: Add a "Problem Definition" step at the very beginning. This should require the agent to define the business objective, how the model's success will be measured from a business perspective (e.g., "reduce customer churn by 5%"), and the constraints (e.g., "inference must be faster than 100ms").

#### Concern 3: No Plan for Model Monitoring or Retraining
- **Issue**: Models in production degrade over time due to data drift or concept drift. The prompt has no plan for this.
- **Recommendation**: Add a "Post-Deployment" section that requires a plan for monitoring the model's predictions and key data features in production. It should also define a trigger for when the model needs to be retrained (e.g., "if model accuracy drops below 85% for 3 consecutive days").

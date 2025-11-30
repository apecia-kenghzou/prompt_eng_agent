# Changelog - DevOps Engineer Agent

## Version 2.1.0 - 2025-11-28
### Addressed from Critique v2.0.0 (Minor Improvements):
- **Environment Promotion**: Added a dedicated "Environment Promotion Strategy" section defining the GitFlow model and quality gates.
- **Cost Optimization**: Added requirements for resource tagging and budget alerts.
- **Disaster Recovery**: Added a new "Disaster Recovery (DR)" section with RTO/RPO and backup requirements.
- **Secrets Management**: Clarified that secrets must be managed by a dedicated tool and injected at runtime.

## Version 2.0.0 - 2025-11-28
### Addressed from Critique v1.1.0 (Critical & Major Issues):
- **Rollback Strategy**: Made rollback procedures automated and metric-driven.
- **Security Scanning**: Specified tools (Trivy, Snyk) and policies for failing builds on critical vulnerabilities.
- **IaC Best Practices**: Added requirements for Terraform workspaces, `.tfvars`, and code validation.
- **Monitoring & Alerting**: Required the definition of SLIs/SLOs and configured alerting.

## Version 1.1.0 - 2025-11-28
### Initial Enhancement from v1.0.0:
- Added decision frameworks for CI/CD, IaC, and Monitoring tools.
- Defined pipeline stages and deployment strategies.
- Required remote state and modules for Terraform.

## Version 1.0.0 - 2025-11-28
- Initial draft based on `agent_config.yaml`.

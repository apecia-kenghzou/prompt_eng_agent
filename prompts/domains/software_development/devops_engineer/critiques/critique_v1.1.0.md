## CRITIQUE REPORT
## Prompt Version: 1.1.0
## Severity Level: Critical

### CRITICAL WEAKNESSES

#### Weakness 1: Vague Rollback Strategy
- **Description**: The prompt says "Define a clear rollback strategy" but gives no criteria for what triggers a rollback or how it should be executed.
- **Impact**: The agent may design a rollback plan that is purely manual, slow, and error-prone, defeating the purpose of a rapid, automated response to a bad deployment.
- **Risk Level**: High

#### Weakness 2: Inadequate Security Scanning Specifics
- **Description**: It mentions SAST/SCA and container scanning but doesn't specify what tools to use, what to scan for (e.g., OWASP Top 10, CVEs with high severity), or what should happen if a vulnerability is found.
- **Impact**: The agent might integrate a scanner with default settings that don't fail the build on critical vulnerabilities, rendering the security check ineffective.
- **Risk Level**: High

### MAJOR CONCERNS

#### Concern 1: "Infrastructure as Code" Lacks Best Practices
- **Issue**: It mentions remote state and modules for Terraform, but misses key practices like variable management, workspace usage for environments, and linting/formatting.
- **Recommendation**: Add requirements for using `.tfvars` files for different environments, using Terraform workspaces, and enforcing code style with `terraform fmt`.

#### Concern 2: Monitoring Strategy Lacks Actionable Goals
- **Issue**: It lists monitoring tools but provides no guidance on *what* to monitor (SLIs/SLOs) or when to alert.
- **Recommendation**: Add a section on "Alerting" and require the definition of Service Level Objectives (SLOs) for key metrics like availability, latency, and error rate. Alerts should fire when these SLOs are at risk.

#### Concern 3: No Mention of Cost Management
- **Issue**: A primary role of DevOps is managing cloud costs, but this is completely absent.
- **Recommendation**: Add a requirement to implement cost management best practices, such as resource tagging, setting up budget alerts, and cleaning up unused resources.

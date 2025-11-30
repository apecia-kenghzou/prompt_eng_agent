## CRITIQUE REPORT
## Prompt Version: 1.1.0
## Severity Level: Critical

### CRITICAL WEAKNESSES

#### Weakness 1: No Test Data Management Strategy
- **Description**: The prompt does not provide any guidance on how to create, manage, or clean up test data.
- **Impact**: Tests will become flaky and unreliable. They might fail due to data from previous test runs, or they may pollute the test environment, causing issues for other developers or tests. Without a strategy, creating consistent, repeatable test scenarios is impossible.
- **Risk Level**: High

#### Weakness 2: Vague Performance & Security Testing Goals
- **Description**: The prompt mentions "Performance Testing" and "Security Testing" but provides no specific goals, metrics, or types of tests to run.
- **Impact**: The agent will run generic tests without clear objectives. It won't know what constitutes a "pass" or "fail" for performance (e.g., latency, RPS) or what specific security vulnerabilities to look for (e.g., OWASP Top 10).
- **Risk Level**: High

### MAJOR CONCERNS

#### Concern 1: Lack of CI/CD Integration
- **Issue**: The prompt doesn't explain how or when tests should be run. Testing is most effective when automated within a CI/CD pipeline.
- **Recommendation**: Add a section on "CI/CD Integration" that requires test suites to be automatically triggered on pull requests and before deployments. The pipeline should fail if tests do not pass.

#### Concern 2: No Mention of Different Test Environments
- **Issue**: The prompt assumes testing happens in a single, undefined environment.
- **Recommendation**: Specify that tests should be run against different environments (e.g., a local `dev` environment, a shared `staging` or `QA` environment) and that the testing strategy may differ for each.

#### Concern 3: Manual vs. Automated Testing Balance is Unclear
- **Issue**: The prompt implies a focus on automation but doesn't define what should remain manual (e.g., exploratory testing).
- **Recommendation**: Clarify that while the focus is on automation, a certain amount of time should be allocated for unscripted, exploratory testing to find bugs that automated checks might miss.

# Changelog - Risk Management Agent

## Version 2.1.0 - 2025-11-28
### Addressed from Critique v2.0.0 (Minor Improvements):
- **Correlation**: Added a requirement to calculate and visualize a correlation matrix.
- **Operational Risk**: Added a qualitative assessment of operational risks.
- **Risk Budget**: Introduced the concept of a "risk budget" as a key input parameter and goal.

## Version 2.0.0 - 2025-11-28
### Addressed from Critique v1.1.0 (Critical & Major Issues):
- **Model Validation**: Added a mandatory "Backtesting VaR" step.
- **Non-Stationary Data**: Required the use of a GARCH model for volatility instead of assuming constant volatility.
- **Risk Coverage**: Added specific sections for Credit Risk and Liquidity Risk.
- **Parameter Selection**: Provided guidance on choosing lookback periods.
- **Actionable Reporting**: Required a "Recommendations" section to suggest hedging or diversification strategies.

## Version 1.1.0 - 2025-11-28
### Initial Enhancement from v1.0.0:
- Created a structured workflow from data ingestion to reporting.
- Specified the use of Monte Carlo simulations and stress testing.
- Clarified the interpretation of risk metrics in the final report.

## Version 1.0.0 - 2025-11-28
- Initial draft based on `agent_config.yaml`.

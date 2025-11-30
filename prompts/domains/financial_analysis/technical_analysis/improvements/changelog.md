# Changelog - Technical Analysis Agent

## Version 2.1.0 - 2025-11-28
### Addressed from Critique v2.0.0 (Minor Improvements):
- **Divergence**: Added "Divergence Analysis" as a key step in signal generation.
- **Risk Management**: Introduced a "Position Sizing" rule to limit risk to 1% of portfolio equity per trade.
- **Backtesting**: Added a new "Strategy Backtesting" section to create a feedback loop for strategy improvement.

## Version 2.0.0 - 2025-11-28
### Addressed from Critique v1.1.0 (Critical & Major Issues):
- **Market Context**: Added a "Pre-Analysis Checklist" to check for major news events before issuing signals.
- **Signal Confidence**: Introduced the concept of "Indicator Confluence" and a confidence score for signals.
- **Volume**: Added a "Volume Confirmation" step, requiring a volume surge on breakouts.
- **Timeframes**: Defined a clear hierarchy for selecting context and signal timeframes.
- **Indicator Parameters**: Acknowledged the need to justify or optimize parameters (addressed further in backtesting).

## Version 1.1.0 - 2025-11-28
### Initial Enhancement from v1.0.0:
- Created a structured workflow including multi-timeframe analysis.
- Defined a complete trade plan with entry, stop-loss, and target.
- Required a minimum 2:1 risk-reward ratio.

## Version 1.0.0 - 2025-11-28
- Initial draft based on `agent_config.yaml`.

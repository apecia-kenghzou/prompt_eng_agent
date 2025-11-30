## CRITIQUE REPORT
## Prompt Version: 1.1.0
## Severity Level: Critical

### CRITICAL WEAKNESSES

#### Weakness 1: Ignores Market Context and News
- **Description**: The prompt defines a purely mechanical technical process. It completely ignores fundamental context, such as major economic data releases (e.g., CPI, NFP) or company-specific news (e.g., earnings reports).
- **Impact**: The agent will generate technical signals that are immediately invalidated by real-world events. It might issue a "buy" signal moments before a disastrous earnings report is released, leading to huge losses. Technical analysis does not work in a vacuum.
- **Risk Level**: High

#### Weakness 2: No Concept of Signal Confidence or Confluence
- **Description**: The prompt treats all signals as equal. It lacks a framework for assessing the *quality* or *confidence* of a signal.
- **Impact**: The agent will generate a high volume of low-probability signals. A professional trader looks for "confluence," where multiple, independent indicators or patterns point to the same conclusion. This prompt doesn't guide the agent to do that.
- **Risk Level**: High

### MAJOR CONCERNS

#### Concern 1: Static Indicator Parameters
- **Issue**: The prompt uses default parameters for all indicators (e.g., RSI 14, standard MACD settings). These parameters may not be optimal for all assets or market conditions.
- **Recommendation**: Require the agent to justify its choice of parameters or even perform a basic optimization to find settings that have worked well for the specific asset in the past.

#### Concern 2: No Volume Analysis
- **Issue**: Volume is a critical component for confirming chart patterns and trend strength, but it's completely missing from the analysis.
- **Recommendation**: Add a requirement to analyze volume. For example, a breakout from a pattern must be accompanied by a significant increase in volume to be considered valid.

#### Concern 3: Vague Timeframe Selection
- **Issue**: The prompt says to start on a "higher timeframe" and trade on a "lower timeframe" but gives no guidance on how to choose them. The relationship (e.g., 4x to 6x) between the timeframes is critical.
- **Recommendation**: Define a clear structure for timeframe selection. For example: "If the primary trading timeframe is Daily, the context timeframe must be Weekly. If the primary is 1-Hour, the context must be 4-Hour."

# Y TREE Mobile PM Take-Home

## Problem Statement and Prioritisation (One Page)

### Context
Y TREE's app currently organizes wealth in one fixed way. This works well for most clients, but not for a high-value minority (notably private-equity and highly detail-oriented clients) who think in exposure, liquidity, and ownership entities rather than platform structure.

### Problem Framing
- One rigid structure cannot represent the different mental models clients use to reason about wealth.
- Illiquid assets and liquid assets are shown together in ways that hide valuation rhythm differences.
- Joint and multi-entity households struggle to isolate ownership views for tax and accounting.
- Performance is visible but not sufficiently explainable (what changed, why, and vs benchmark).
- Reporting still leans on manual adviser workflows that should be productized.
- Grouped asset-class views that omit liabilities will disagree with headline net worth (gross vs net).

### Prioritisation Logic
1. **Home with 3 curated lenses** (default-safe, highest strategic impact)
   - Keep default structure unchanged for the majority.
   - Add opt-in `Asset class` and `Liquidity` views.
2. **Performance explainability**
   - Add attribution and benchmark interpretation, not just line movement.
3. **Ownership + export + pivot**
   - Reduce manual accountant/adviser workflow burden.
4. **Private equity liquidity clarity**
   - Show commitments, calls, and coverage to support planning decisions.

### What not to focus on now
- Fully custom dashboard builder.
- Trading-like UX patterns and high-frequency alerting.
- Broad personalization before core interpretation trust is fixed.

### Assumptions
- Majority users prefer current structure and should not be disrupted.
- Sophisticated minority needs depth as an option, not as a forced flow.
- Benchmark logic and export fields are available to power in-app interpretation.

### Outstanding Questions
- Compliance-approved benchmark disclosure detail.
- Data completeness thresholds by asset type for attribution views.
- Scope/timing for Trust/SPV ownership filters in MVP.
- Notification policy for decision prompts and escalation.

### Where to Start
Start with **Home architecture**:
- Keep familiar default path.
- Introduce two opt-in lenses.
- Keep a global ownership filter.

This addresses the core structural mismatch first, while minimizing change risk and creating the right foundation for explainability and reporting.

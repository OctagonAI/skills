# Skill: SEC 8-K Analysis

## Purpose

Analyze 8-K filings to extract material events and corporate changes.

## When to Use

- Tracking material events between periodic filings
- M&A announcements and completions
- Leadership changes
- Earnings releases
- Contract announcements

## Example Prompt

```
Analyze recent 8-K filings for AAPL and extract material events and corporate changes.
```

## Key Information Returned

| Section | Content |
|---------|---------|
| Event Type | Item category (2.01, 5.02, etc.) |
| Event Description | Summary of disclosure |
| Filing Date | When disclosed |
| Materiality | Significance assessment |

## Integration with Other Skills

- **Pairs with**: sec-10k-analysis, sec-10q-analysis for context
- **Feeds into**: Report material events section
- **Validates**: News announcements with official filings

## Report Section Mapping

| Report Section | Usage |
|----------------|-------|
| Material Events | Primary source |
| Executive Summary | Key events |
| Governance | Leadership changes |

## Data Source

octagon-sec-agent

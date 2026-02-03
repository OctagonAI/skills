# Stock Grades Skill

## Purpose

Retrieve latest analyst ratings, upgrades, and downgrades from financial institutions.

## When to Use

- Tracking rating changes
- Identifying sentiment shifts
- Evaluating institutional views
- Monitoring upgrade/downgrade activity

## Example Prompt

```
Get the latest stock grades for the symbol AAPL from top analysts and financial institutions.
```

## Key Information Returned

| Data Point | Description |
|------------|-------------|
| Analyst/Firm | Source of rating |
| Action | Upgrade/Downgrade/Maintain |
| Previous Rating | Prior grade |
| New Rating | Current grade |
| Date | Rating date |

## Integration with Other Skills

| Combine With | For |
|--------------|-----|
| price-target-consensus | Ratings + targets |
| stock-quote | Rating impact on price |
| price-target-summary | Sentiment alignment |

## Report Section Mapping

→ Analyst Sentiment section
→ Recent Rating Activity table

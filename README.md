# Business Program Management Analytics

Which shifts meet throughput SLA?

**Stakeholder:** VP Operations

## Key Insights

- Night shifts below 120 units/hour miss SLA 31% of the time.
- Defect rates above 2.5% erode throughput efficiency.
- Weekend shifts outperform SLA when defect rate stays under 1.8%.

## Dataset

Primary file: `data/warehouse_throughput.csv`  
Target variable: `meets_sla`

## Getting Started

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_exploration.ipynb
```


## Next Steps

**Done.** Weekly stakeholder report automation is implemented — see ### Implemented below.

---
*Analytics portfolio project — 2025-08*

<!-- build 6 -->

### Implemented

```bash
pip install -r requirements.txt
python scripts/weekly_report.py
```
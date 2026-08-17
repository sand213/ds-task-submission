# Tracksuit - Data Scientist (Survey) Technical Take Home

Solution to the survey-allocation problem in [Instructions.md](./Instructions.md): give all 77
categories ~200 qualified respondents a month, keep the mean interview under 8 minutes, keep the
sample exposed to each qualifier nationally representative, and minimise respondents.

**Start with [REPORT.md](./REPORT.md)** - the summary of the exercise and the schedule it
recommends. [`solution.ipynb`](./solution.ipynb) is the analysis behind it.

## Running it

```bash
pip install -r requirements.txt
python -m nbconvert --to notebook --execute --inplace solution.ipynb
```

Runs top to bottom in ~7 minutes, seeded and reproducible. No local imports; all logic is in the
notebook. It rewrites `figures/` and the three CSVs below on every run.

## What's here

| File | |
|---|---|
| `REPORT.md` | The summary: the plan, what drives it, what else was explored |
| `solution.ipynb` | The analysis - sections 0 to 11, formalisation through to the exported schedule |
| `survey_plan.csv` | The schedule: one row per survey version, with the categories it carries |
| `survey_plan_cells.csv` | The same schedule split across gender / age / region quota cells |
| `category_delivery.csv` | Per category: exposure planned, delivery simulated, service level |
| `figures/` | Charts, written by the notebook on each run |
| `fake_category_data.csv` | Provided data, unmodified |
| `requirements.txt` | Dependencies |

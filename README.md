# Car Fuel Efficiency Analysis (1970–1982)

**Course:** 2323 CIS — Introduction to Data Science · King Khalid University
**Lab:** 14–15 — Lab Project Development, GitHub Publishing and Presentation

## 1. Objective

**Data question:** How did car fuel efficiency change between 1970 and 1982, and which car characteristics (weight, cylinders, horsepower, region of origin) are most strongly linked to it?

## 2. Data source

| Item | Details |
| --- | --- |
| Dataset | Auto MPG (398 cars, model years 1970–1982) |
| Original source | UCI Machine Learning Repository — https://archive.ics.uci.edu/dataset/9/auto+mpg |
| Copy used | seaborn-data — https://github.com/mwaskom/seaborn-data/blob/master/mpg.csv |
| How it is loaded | `seaborn.load_dataset("mpg")` inside the notebook (no manual entry) |
| Licence / access | Public dataset, no confidential or personal data |

More detail: [`data/README.md`](data/README.md).

## 3. Repository structure

```
car-fuel-efficiency-analysis/
├── README.md                 ← this file
├── .gitignore
├── notebooks/
│   └── analysis.ipynb        ← full analysis, runs top to bottom
├── data/
│   └── README.md             ← data source and column notes
└── outputs/
    ├── mpg_clean.csv         ← final analysis-ready dataset (created by the notebook)
    └── figures/              ← charts saved by the notebook
```

## 4. How to run

1. Open `notebooks/analysis.ipynb` in Google Colab (File → Open notebook → GitHub tab → paste this repo link).
2. Click **Runtime → Run all**.
3. The notebook downloads the data, cleans it, draws the charts and saves results to `outputs/`.

Requirements: Python 3, pandas, numpy, seaborn, matplotlib (all pre-installed in Colab).

## 5. Steps

1. **Data understanding:** shape, columns, data types, missing values, descriptive statistics, and a diagnosis of data-quality problems.
2. **Data preparation:**
   - *Cleaning:* missing `horsepower` values filled with the median of cars with the same number of cylinders.
   - *Regular-expression extraction:* brand and model pulled out of the `name` text; misspelled brands fixed (e.g. `chevroelt` → `chevrolet`, `vw` → `volkswagen`).
   - *Transformation:* metric units added (L/100 km, kg, litres), full year, weight classes.
   - *Aggregation + reshaping (time series):* average mpg per year and region, pivoted into a year × region table.
3. **Visualizations:** (saved in `outputs/figures/`)
   1. Average mpg per year by region, with the 1973 and 1979 oil crises marked.
   2. Car weight vs mpg, coloured by region, with a correlation table.
   3. mpg by number of cylinders (box plot).
4. **Final dataset:** `outputs/mpg_clean.csv` (398 rows, 12 columns, no missing values) and `outputs/yearly_mpg_by_region.csv`.

## 6. Results

_To be completed after the analysis._

## 7. Limitations

_To be completed after the analysis._

## 8. Team contribution

| Member | Contribution |
| --- | --- |
| Fuad Abdullahi Hashi | _to be completed_ |
| Member 2 | _to be completed_ |
| Member 3 | _to be completed_ |
| Member 4 | _to be completed_ |

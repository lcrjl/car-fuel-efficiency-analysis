# Data

The raw data is **not stored** in this folder. The notebook downloads it automatically with:

```python
import seaborn as sns
df = sns.load_dataset("mpg")
```

## Source

- **Auto MPG dataset**, UCI Machine Learning Repository: https://archive.ics.uci.edu/dataset/9/auto+mpg
- Copy used by seaborn: https://github.com/mwaskom/seaborn-data/blob/master/mpg.csv
- Original citation: R. Quinlan, "Combining Instance-Based and Model-Based Learning," Proc. 10th Int. Conf. on Machine Learning, 1993.

## Columns

| Column | Meaning | Unit |
| --- | --- | --- |
| mpg | Fuel efficiency | miles per US gallon |
| cylinders | Number of engine cylinders | count |
| displacement | Engine size | cubic inches |
| horsepower | Engine power (has missing values) | hp |
| weight | Car weight | pounds |
| acceleration | Time from 0 to 60 mph | seconds |
| model_year | Model year (70 = 1970) | year |
| origin | Region of manufacture | usa / europe / japan |
| name | Car make and model (brand must be extracted) | text |

## Known data-quality issues

- `horsepower` has missing values.
- `name` mixes the brand and model in one string, and some brands are misspelled (for example `chevroelt`, `toyouta`, `vokswagen`) or abbreviated (`vw`, `chevy`).
- Units are imperial (miles, gallons, pounds).

These are handled in the data preparation section of `notebooks/analysis.ipynb`.

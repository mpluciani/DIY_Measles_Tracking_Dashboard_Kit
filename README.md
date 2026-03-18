# DIY Measles Tracking Dashboard Kit

This project helps you explore UKHSA measles data in a simple, interactive dashboard.

It uses:
- `ipywidgets` for controls
- `Voila` to turn the notebook into a dashboard
- `Binder` for a shareable web version

Data source:
- UKHSA measles page: https://ukhsa-dashboard.data.gov.uk/vaccine-preventable-diseases/measles

## What You Can See

The dashboard includes:
1. Weekly measles bars with rolling average overlay
2. Week-over-week change chart
3. Age distribution chart
4. Regional ranking chart (by selected week)

## Quick Start (Local)

1. Create and activate a virtual environment.
2. Install packages:
   - `pip install -r requirements.txt`
3. Run the dashboard:
   - `voila Dashboard.ipynb`
4. Open the local URL shown in your terminal.

## Shareable Binder Website

After pushing this repo to GitHub, share this Binder dashboard link:

`https://mybinder.org/v2/gh/<your-github-username>/<your-repo-name>/HEAD?urlpath=%2Fvoila%2Frender%2FDashboard.ipynb`

Example format:
- Replace `<your-github-username>` and `<your-repo-name>` with your real repo path.
- Keep `%2Fvoila%2Frender%2FDashboard.ipynb` exactly as written.

Optional Binder home page (without opening Voila directly):

`https://mybinder.org/v2/gh/<your-github-username>/<your-repo-name>/HEAD`

## Dataset Configuration

If you want to change datasets later, edit `DATASET_CONFIG` in `Dashboard.ipynb`:
- `json_path`: local JSON file to load
- `records_path`: path to the list of records in the JSON
- `date_field`: date column used as the time index
- `value_fields`: numeric columns to chart
- `rename`: optional output column names

The chart controls are built dynamically from these settings.

## Notes

- Default area is `England`.
- Use the **Area** dropdown + **Fetch data** to switch to UKHSA regions.
- Use **Fetch regional data** to populate the regional ranking chart.

---

Adapted from the original [DIY Disease Tracking Dashboard Kit](https://github.com/fsmeraldi/diy-covid19dash) by Fabrizio Smeraldi.

**(C) 2020, 2024 Fabrizio Smeraldi** ([f.smeraldi@qmul.ac.uk](mailto:f.smeraldi@qmul.ac.uk), [web](http://www.eecs.qmul.ac.uk/~fabri/)).
Released under the [GNU GPLv3.0 or later](https://www.gnu.org/licenses/).

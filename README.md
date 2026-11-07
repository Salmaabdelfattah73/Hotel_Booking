# Hotel Booking Demand - HMS Project

## Project

This repository analyses booking demand for a city hotel and a resort hotel in Portugal. It covers data quality, exploratory analysis, guest segmentation, monthly metrics, feature engineering, cancellation classification, ADR regression and two operational decision cards.

## Data source

N. António, A. de Almeida and L. Nunes (2019), “Hotel booking demand datasets,” *Data in Brief*, 22, 41-49. DOI: https://doi.org/10.1016/j.dib.2018.11.126. Licence: CC BY 4.0.

Place `hotel_bookings.csv` inside `data/`. The repository intentionally ignores the `data/` directory.

## Setup

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```

Run notebooks `01_clean.ipynb` through `07_decision.ipynb` in order. Each notebook rebuilds the files required by the next task. Generated model results and decision summaries are written to `outputs/`; charts used in the presentation are written to `slides/`.

## Main predictions

1. Cancellation risk at booking creation.
2. Expected ADR at booking creation.

Training arrivals end in December 2016. Test arrivals cover January through August 2017.

## Important limitations

- The source has no booking ID. Exact duplicate rows remain in the analysis with a flag.
- The source lacks historical room inventory, so occupancy and fully-booked dates cannot be calculated.
- Revenue is an estimate based on ADR and completed nights. It excludes taxes, extras and refunds.
- Model actions require staff review and monthly monitoring.

## AI tools

AI tools helped structure notebook drafts, review leakage risks and prepare presentation layouts. The team checked the cleaning rules, target definition, time split, model metrics, decision thresholds and every number used in the presentation by rerunning the notebooks from the original CSV.

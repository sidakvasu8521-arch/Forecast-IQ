# ForecastIQ AI - Hackathon Submission

AI-powered probabilistic revenue forecasting and budget optimization platform for digital marketing agencies.

---

## 1. Submission Details
- **Team Name**: Team ForecastIQ
- **College Name**: NetElixir Hackathon Center
- **Python Version**: **3.11.15** (CPython 3.11.15 managed via `uv`)

---

## 2. Installation & Setup
To install dependencies in your Python environment:
```bash
pip install -r requirements.txt
```

---

## 3. How to Run (Automated Testing)
The automated testing pipeline invokes `run.sh` to extract features and predict:

```bash
bash run.sh ./data ./pickle/model.pkl ./output/predictions.csv
```

### Script Arguments:
1. `DATA_DIR`: Folder containing input CSV files (Default: `./data`)
2. `MODEL_PATH`: Location of pre-trained model pickle file (Default: `./pickle/model.pkl`)
3. `OUTPUT_PATH`: Target output CSV containing forecast projections (Default: `./output/predictions.csv`)

---

## 4. Contract Output Schema
The resulting `predictions.csv` contains predictions for the next 30 days:
- **Date**: Projection Date (YYYY-MM-DD)
- **Channel**: Marketing Channel (e.g. Google Ads, Meta Ads, MS Ads, Organic/Direct)
- **Revenue_P10**: 10th percentile revenue interval
- **Revenue_P50**: Median expected revenue
- **Revenue_P90**: 90th percentile revenue interval
- **Spend**: Projected budget allocation
- **ROAS**: Estimated Return on Ad Spend (Revenue / Spend)

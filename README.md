
# Kebele-level PPS Village & Household Sampler (Streamlit)

This app performs:
1) **PPS village selection** at kebele level (Systematic or Independent PPS), and
2) **Systematic household sampling** within each sampled village for **Eligible** and **Non-eligible** groups.

## Run locally
```bash
python -m venv .venv
# Windows
.venv\Scriptsctivate
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt
streamlit run app.py
```

## Deploy on Streamlit Cloud
1. Push this folder to GitHub.
2. On https://streamlit.io/cloud → **New app** → pick repo/branch and `app.py` → **Deploy**.

## Inputs
- **Village frame (Excel/CSV):** `Woreda | Kebele | Village | HHs`
- **Roster (Excel/CSV):** `Woreda | Kebele | Village | Eligibility | HH_ID | Household Head Name | Phone | Other ID`
- **(Optional) Quotas (Excel/CSV):** `Woreda | Kebele | Village | nE | nNE`

## Outputs
- `Sampled_Villages.csv` and `Sampled_Villages.xlsx (Diagnostics)`
- `HH_Sample.csv` and `HH_Sample.xlsx (HH_Summary)`

## Branding
- Replace placeholders in `assets/` with official `wfp_logo.png` and `favicon.png`.

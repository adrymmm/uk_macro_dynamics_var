# Inflation, Wages and Productivity (UK, ONS) #

## Headline Results
+ Real wages and productivity are both I(1) but **not cointegrated** - no long-run equilibrium relationship, so the model is a VAR in first differences rather than a VECM
+ **Productivity growth Granger-causes real wage growth** (p = 0.024); the reverse does not hold (p = 0.426) - the causality chain runs one way
+ A positive productivity growth shock raises real wage growth, but the effect is **short-lived**, dissipating within a couple of quarters (IRF)
+ Real wage growth fluctuations are mostly driven by **its own shocks**; productivity shocks explain only a minority share (~15-20%) of its forecast error variance (FEVD)

## EDA 
+ Line plots,
+ MA (Moving Average) Plots
+ Static Correlation
+ Rolling Correlation (24 months)
+ Seasonal Plots (Business cycle)

## Analysis
### 1. Stationarity Tests
+ Augmented Dickey Fuller (ADF) Test
+ KPSS Test
### 2. Cointegration Tests
+ Johansen Trace Test
### 3. Model Specification
+ Optimal Lag Selection
+ Final VAR specification
### 4. Diagnostics
+ Portmanteau Test
+ Stability Test
+ Normality Test
### 5. Dynamic Analysis
+ Granger Causality Tests
+ Impulse Response Functions (IRF)
+ Forecast Error Variance Decomposition (FEVD)

## Repo Structure
+ 'data/' -> Pre-processed and raw datasets
+ 'data_exploration.ipynb' -> Jupyter notebook of pre-processing and exploratory plots
+ 'model.ipynb' -> Jupyter notebook of diagnostic tests and VAR model

## Reproduce Results
### Step 1) Set up Environment
```bash
python -m venv .venv

# Windows:
.venv\Scripts\activate

# macOS/Linux:
source .venv/bin/activate
```
### Step 2) Install dependencies
```bash
pip install -U pip

pip install -r requirements.txt
```
### Step 3) Run notebooks
```bash
jupyter lab
```
# Open:
data_exploration.ipynb

model.ipynb

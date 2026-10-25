# TrendSight-SaaS: Comprehensive Technical Analysis & Setup Guide

**Project**: [TrendSight-saas](file:///d:/Alive/Practice/github/TrendSight-saas)  
**Architecture**: Production Full-Stack FinTech SaaS (Django 4.2 + SQLite/PostgreSQL + yFinance + Pandas/NumPy + Tailwind CSS + Stripe + Unfold Admin)  
**Core Domain**: Algorithmic Market Analytics, Sector Relative Strength (RS/RSI), Exponential Moving Averages (EMA 10–200), and Portfolio Management

---

## 🎯 1. What TrendSight-SaaS Is and What It Is Used For

**TrendSight-SaaS** is an end-to-end **financial analytics and equity intelligence SaaS platform**. It was built to solve a major problem faced by active traders and swing investors: **discovering market leadership before individual breakouts occur**.

Instead of only tracking a static watchlist of prices, TrendSight provides:
1. **Automated Market Data Harvesting**: Connects directly to Yahoo Finance (`yfinance`) with custom 700-day rolling lookbacks for equities and market sectors.
2. **Quantitative Technical Indicator Engine**: Uses high-performance vectorized computations in **Pandas** and **NumPy** to calculate:
   - **RSI (Relative Strength Index)** with Wilder's 14-period smoothing.
   - **Mansfield / Relative Strength (RS)** against sectoral benchmarks.
   - **Multi-Period EMAs**: 10, 20, 30, 50, 100, and 200-day Exponential Moving Averages.
   - **Volume Moving Averages**: 20-day and 50-day average volume accumulation.
3. **Sectoral Heatmaps & Rotation Analysis**: Aggregates individual equities into industry sectors (`Technology`, `Energy`, `Healthcare`, etc.) to track institutional capital flow across industries.
4. **Subscription & Monetization Layer**: Native Stripe billing integration with recurring subscriptions, user tier limits, and Unfold modern admin UI.

---

## ⚖️ 2. How TrendSight is Better & Different from Basic Projects

| Evaluation Factor | Basic Stock Tracker (e.g. `StockTracker-Django`) | **TrendSight-SaaS** ⭐ |
|---|---|---|
| **Architectural Scope** | Single monolithic Django app with raw price logging. | **Enterprise Modular Monolith**: 6 decoupled Django apps (`stocks`, `user`, `transaction`, `blog`, `inquiry`, `styling`). |
| **Financial Computation** | Raw Open/High/Low/Close price storage only. | **Deep Vectorized Analytics**: Full algorithmic engine computing RSI, RS, EMAs (10–200), and 20/50 volume averages. |
| **Sector Intelligence** | No sector grouping or macro market visibility. | **Sector Aggregation**: Computes average sector performance and relative strength rotation. |
| **Monetization & SaaS** | None (free demo app). | **Production Billing Ready**: Stripe integration with webhooks, checkout sessions, and subscription tiers. |
| **Database & Scaling** | Simple SQLite tables without indexes. | **Optimized Schema**: Compound indexes (`stock + date`), bulk insertions (`bulk_create`), and PostgreSQL production config. |
| **User Experience & Admin** | Default unstyled Django admin and plain templates. | **Modern Tailwind CSS** design system + **Unfold Admin** modern dashboard module. |

---

## 🧠 3. What It Demonstrates on Your Resume

Featuring TrendSight-SaaS on your resume signals senior-level capabilities:

1. **Applied Quantitative Finance & Data Engineering**:
   - You didn't just display static data; you engineered vectorized mathematical pipelines in **Pandas** and **NumPy** for statistical indicators (RSI, EMAs, RS).
2. **Database Performance Optimization**:
   - Replaced row-by-row queries with `bulk_create` operations for hundreds of thousands of historical candle records.
   - Designed composite database indexes (`models.Index(fields=['date', 'stock'])`) ensuring fast lookups on a 11MB+ historical dataset.
3. **Full SaaS Lifecycle & Monetization**:
   - Proves you understand how to monetize software: authentication, transactional emails, webhooks, and Stripe subscription lifecycles.
4. **Production Release Discipline**:
   - 91 commits across 4 release branches (`main`, `final`, `last`, `test`) with automated GitHub Actions CI/CD workflows.

---

## 🛠️ 4. Local Setup Guide (Step-by-Step)

The project includes an initialized SQLite database (`db.sqlite3`, 11.1MB) containing pre-loaded historical data, sectors, and stock records.

### Step 1: Navigate to the Django Root
```powershell
cd "d:\Alive\Practice\github\TrendSight-saas\Django-SAAS-Boilerplate"
```

### Step 2: Create and Activate a Virtual Environment
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### Step 3: Install Core Dependencies
Install the required packages:
```powershell
pip install django yfinance pandas numpy dj-database-url django-environ django-unfold stripe psycopg2-binary
```
*(Or install from `requirements.txt` with `pip install -r requirements.txt`).*

### Step 4: Environment Variables (`.env`)
A local development `.env` has already been generated at `d:\Alive\Practice\github\TrendSight-saas\Django-SAAS-Boilerplate\.env`:
```ini
DEBUG=1
SECRET_KEY=django-insecure-trendsight-local-development-key-12345
DOMAIN=http://localhost:8000
ALLOWED_HOSTS=localhost,127.0.0.1
STRIPE_TEST_API_KEY=sk_test_placeholder
STRIPE_WEBHOOK_TEST_API_KEY=whsec_placeholder
STRIPE_PUB_TEST_KEY=pk_test_placeholder
EMAIL_HOST=smtp.gmail.com
EMAIL_HOST_USER=placeholder@example.com
EMAIL_HOST_PASSWORD=placeholder
```

### Step 5: Run Migrations & Start Server
```powershell
python manage.py migrate
python manage.py runserver
```
Open **[http://localhost:8000](http://localhost:8000)** in your browser to view the live dashboard!

---

## 📝 5. Resume Bullet Points for TrendSight-SaaS

* **Option 1 (Full-Stack & Quantitative Focus)**:
  > *Architected an equity intelligence SaaS platform in Django, computing real-time technical indicators (RSI, 10–200 day EMAs, Relative Strength) across 700-day rolling lookbacks using vectorized Pandas/NumPy pipelines.*

* **Option 2 (SaaS, Database & Backend Focus)**:
  > *Engineered a multi-tenant FinTech SaaS with Stripe subscription billing, PostgreSQL composite indexing, and batch ingestion pipelines (`bulk_create`) processing high-density historical financial data with sub-second API response times.*

* **Option 3 (DevOps & Release Engineering Focus)**:
  > *Managed end-to-end continuous delivery across 4 release branches using GitHub Actions CI/CD, integrating modern Unfold admin dashboards, transactional emails, and Docker/Render cloud deployment pipelines.*

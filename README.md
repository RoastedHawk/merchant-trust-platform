# Merchant Trust Platform

AI-assisted commerce safety platform for merchant risk scoring, fraud detection, and onboarding verification.

---

## Problem

Online commerce platforms face a constant challenge:

- Fraudulent merchants create fake storefronts
- High-risk merchants generate chargebacks and refunds
- Excessive manual reviews create operational cost
- Overly strict systems block legitimate merchants and reduce growth

This project simulates a **Commerce Safety decisioning system** that balances fraud prevention with merchant experience.

---

## Product Vision

Build a merchant onboarding risk system that:

- Detects risky merchants early
- Reduces fraud exposure
- Minimizes manual review workload
- Preserves a smooth onboarding experience for legitimate merchants

---

## Decision Philosophy

This system is designed around a core tradeoff in commerce safety:

> Maximizing fraud prevention while minimizing friction for legitimate merchants.

To manage this tradeoff, the system uses a 3-tier decision model:

- **Low Risk (0–30):** Automatically approved to ensure smooth onboarding
- **Medium Risk (30–70):** Routed to manual review for ambiguous cases
- **High Risk (70–100):** Rejected or blocked to prevent fraud exposure

This reflects how real-world trust and safety systems avoid binary decisions and instead apply **graduated enforcement policies**.

---

## System Overview

Merchant data flows through multiple layers:

```
Merchant Data
    ↓
Rule-Based Risk Engine
    ↓
Machine Learning Model
    ↓
Hybrid Risk Scoring
    ↓
Policy Decision Layer
    ↓
Final Outcome (Approve / Review / Reject)
```

---

## Current Features

### 1. Synthetic Merchant Dataset

Simulated merchant profiles include:

- Verification status
- Merchant age
- Category
- Average order value
- Number of orders
- Chargeback rate
- Refund rate
- Traffic source

---

### 2. Rule-Based Risk Engine

A transparent scoring system based on known fraud signals:

- Unverified merchants
- High chargeback rates
- High refund rates
- New merchant accounts
- Unusual transaction patterns

This provides interpretability and fast policy iteration.

---

### 3. Machine Learning Model

A Logistic Regression model predicts merchant risk based on historical signals.

Features include:

- Merchant age
- Chargeback rate
- Refund rate
- Verification status
- Traffic source
- Category
- Order behavior

---

### 4. Hybrid Risk Scoring

The final risk score combines:

- Rule-based risk score (policy-driven)
- ML probability score (data-driven)

This ensures a balance between:
- interpretability
- predictive accuracy

---

### 5. Merchant Decision System

Final decisions are derived from risk scores:

| Risk Level | Decision |
|------------|----------|
| Low (0–30) | APPROVE |
| Medium (30–70) | SEND_TO_REVIEW |
| High (70–100) | REJECT |

---

### 6. Risk Explainability

Each decision includes human-readable reasoning:

- Unverified merchant
- High chargeback rate
- High refund rate
- New account behavior

This improves transparency for reviewers and supports auditability.

---

## Key Tradeoffs

### 1. Fraud Prevention vs Merchant Friction
Stricter thresholds reduce fraud but increase onboarding friction for legitimate merchants.

### 2. Automation vs Human Review
More automation reduces operational cost but increases risk of misclassification in edge cases.

### 3. Explainability vs Model Complexity
Rule-based systems are transparent but limited, while ML models are more powerful but less interpretable.

---

## Why a Hybrid Approach?

This system combines both approaches:

### Rule-Based System
- Encodes known fraud heuristics
- Highly interpretable
- Easy to adjust for policy updates

### Machine Learning Model
- Learns hidden patterns in data
- Scales with complexity
- Improves predictive accuracy

### Hybrid Score
Balances both systems to support real-world production constraints.

---

## Current Limitations

- Small synthetic dataset
- Simplified fraud signals
- No real-time streaming data
- No network/graph fraud detection
- No feedback loop from reviewers

---

## Future Improvements

- Larger-scale realistic datasets
- Graph-based fraud detection (merchant networks)
- Real-time anomaly detection
- Human review feedback loop
- Threshold optimization based on business metrics
- Production-grade monitoring system

---

## What I Would Do Next

If this system were extended in a production environment, I would:

- Introduce fraud network detection (graph modeling)
- Build a reviewer feedback loop to improve model accuracy
- Add real-time merchant monitoring
- Optimize thresholds based on fraud vs friction tradeoffs
- Deploy a lightweight decisioning API for onboarding flow

---

## Why This Project

This project was built to simulate real-world challenges in:

- Commerce Safety
- Fraud Detection
- Risk Scoring Systems
- AI-driven Product Decisioning

It demonstrates how product, policy, and machine learning interact in large-scale platforms.

---

## Tech Stack

- Python
- Pandas
- Scikit-learn
- Jupyter Notebook

---
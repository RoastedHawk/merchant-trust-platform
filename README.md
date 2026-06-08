# Merchant Trust Platform

AI-assisted commerce safety platform for merchant risk scoring, fraud detection, and onboarding verification.

## Problem

Online commerce platforms face a constant challenge:

- Fraudulent merchants create fake storefronts
- High-risk merchants generate chargebacks and refunds
- Excessive manual reviews create operational costs
- Overly strict controls create onboarding friction for legitimate businesses

The goal of this project is to simulate how a Commerce Safety team can balance trust, safety, and merchant growth.

---

## Product Vision

Create a scalable merchant onboarding system that:

1. Detects risky merchants before activation
2. Reduces fraud exposure
3. Minimizes manual review workload
4. Preserves a smooth onboarding experience for legitimate merchants

---

## Current Features

### Synthetic Merchant Dataset

Simulated merchant profiles containing:

- Verification status
- Merchant age
- Average order value
- Chargeback rate
- Refund rate
- Traffic acquisition source

---

### Rule-Based Risk Engine

Risk scores are generated using interpretable business rules.

Example signals:

- Unverified merchant
- High chargeback rate
- High refund rate
- Newly created account
- Unusual transaction behavior

---

### Machine Learning Model

A Logistic Regression model predicts merchant risk using historical merchant signals.

Features include:

- Chargeback rate
- Refund rate
- Merchant age
- Verification status
- Traffic source
- Category

---

### Hybrid Risk Scoring

The platform combines:

- Rule-based risk score
- ML risk probability

into a single hybrid risk score.

---

### Merchant Decisions

Based on risk score thresholds:

| Risk Level | Decision |
|------------|-----------|
| Low | APPROVE |
| Medium | SEND_TO_REVIEW |
| High | REJECT |

---

### Risk Explanations

The system generates human-readable explanations for risk decisions.

Example:

- Unverified merchant
- High chargeback rate
- New merchant account

This improves transparency and reviewer efficiency.

---

## Project Structure

```text
merchant-trust-platform/
├── data/
├── docs/
├── notebooks/
├── dashboard/
├── diagrams/
├── assets/
└── README.md
```

---

## Future Improvements

- Larger synthetic datasets
- Threshold optimization
- Fraud network detection
- Merchant behavior monitoring
- Streamlit dashboard
- Human review workflow simulation
- Explainable AI enhancements

---

## Why This Project

This project was built to explore product management challenges in:

- Commerce Safety
- Fraud Detection
- Merchant Trust
- Risk Scoring Systems
- AI/ML Product Development

It is designed as a portfolio project inspired by large-scale commerce ecosystems.
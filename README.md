# FinTech AI Governance & Model Risk Management (MRM) Toolkit

An end-to-end **Socio-Technical AI Governance, Post-Deployment Drift Telemetry, Fair Lending Parity, and Explainable AI (XAI) Auditing Framework** designed for regulated FinTech credit underwriting, payment fraud detection, and AML decision engines.

Built by **Huzaifa Saleem Khan** (*M.Sc. (Tech.) in Software Product Management and Business, LUT University, Finland; B.Sc. in Computer Engineering, COMSATS*), this repository operationalizes the research findings from his 2025 Master's Thesis:
> **"Organizational Governance of Artificial Intelligence for Model Risk Management in FinTech"**  
> *Lappeenranta–Lahti University of Technology LUT (2025) — Supervised by Assoc. Prof. Damian Kedziora & Dr. Micheal Tuape.*

## Why This Toolkit Exists

Traditional financial Model Risk Management (MRM) frameworks (such as static back-testing and periodic validation under SR 11-7) were designed for deterministic, stationary statistical models. When applied to adaptive Machine Learning (ML) and Deep Learning (DL) systems in FinTech, three critical governance failures emerge:

1. **Silent Post-Deployment Model Drift (RQ1 / Theme 1):** Macroeconomic shifts and evolving fraud vectors cause silent distribution decay between validation cycles.
2. **Accountability Fragmentation & Third-Party Vendor Opacity (RQ2 / Theme 2):** High-level ethical principles rarely translate into binding operational controls across Strategic (Board), Tactical (Product Manager), and Operational (MLOps) layers—especially when integrating external KYC/scoring APIs.
3. **Cosmetic Explainability ("XAI Theater") (RQ3 / Theme 3):** Generating post-hoc SHAP or LIME plots without verifying surrogate fidelity (R²) and local stability creates an illusion of transparency while failing regulatory audit standards under **EU AI Act Annex III (Point 5b)** and **GDPR Article 22**.

## Core Modules & Capabilities

- **Post-Deployment Concept & Data Drift (`src/fintech_mrm/drift.py`):** Population Stability Index (PSI) and Two-Sample Kolmogorov-Smirnov (KS) drift telemetry for credit scoring and payment fraud features (RQ1 / Theme 1).
- **Algorithmic Fairness & EU AI Act Art. 10 Parity (`src/fintech_mrm/fairness.py`):** Disparate Impact Ratio (4/5ths Rule), Statistical Parity Difference (SPD), and Equal Opportunity Difference (EOD) auditing across protected cohorts (RQ1 & RQ2).
- **Socio-Technical Governance & Vendor Risk Evaluator (`src/fintech_mrm/governance.py`):** Multi-level lifecycle accountability (Strategic, Tactical, Operational), EU AI Act Annex III Point 5(b) conformity checks, and Third-Party Vendor AI Risk Register (RQ2 / Theme 2).
- **Explainable AI Fidelity & Stability Auditor (`src/fintech_mrm/explainability.py`):** Global marginal feature attributions, linear surrogate R² fidelity verification, and perturbation stability scoring to prevent cosmetic XAI compliance (RQ3 / Theme 3).

## Sample Audit Output Summary

| Governance Dimension | Evaluated Metric | Sample Audit Result | Regulatory / MRM Action |
| :--- | :--- | :--- | :--- |
| **Post-Deployment Drift (RQ1)** | `debt_to_income_ratio` PSI & KS | `PSI = 0.7905` (`CRITICAL_DRIFT`) | Escalate to Model Risk Committee; initiate Art. 15 recalibration |
| **Fair Lending Bias (RQ1/RQ2)** | Disparate Impact Ratio (DIR) | `DIR = 1.0761` (`COMPLIANT`) | Passes 80% four-fifths rule & EU AI Act Art. 10 parity check |
| **Socio-Technical Governance (RQ2)** | Multi-Level Lifecycle Controls | `8 / 9 Controls (88.9%)` | Flag third-party KYC vendor lacking model weight escrow |
| **Explainable AI Fidelity (RQ3)** | Surrogate R² & Stability | `R² = 0.9813`, `Stability = 0.9831` | `AUDIT_READY` for GDPR Art. 22 & EU AI Act Art. 13 traceability |

## Related Publications & Academic Context

- **Master's Thesis (2025):** Khan, H. S. (2025). *Organizational Governance of Artificial Intelligence for Model Risk Management in FinTech.* Lappeenranta–Lahti University of Technology LUT, Finland.
- **Peer-Reviewed Dataset (2025):** Khan, R., Khan, H. S., & Ijaz, S. (2025). *English-Pashto Language Dataset (EPLD).* Mendeley Data, V1. DOI: 10.17632/vmgv4s6vrn.1

# Lab 3A: Phishing Simulation and Quantitative Risk Analysis

**Student:** Chioma Ameh | **Registration number:** C11/26/CGRCE/17567 | **Course:** GRC103 | **Date:** 2 November 2026

Analysis of three phishing simulation campaigns at GlobalTech Inc.: campaign rates and conversions, financial exposure, control cost-benefit, risk matrix, confidence intervals, and a check of the errors in the lab brief. Every figure comes from visible formulas in the workbook.

## Headline results

| Campaign | Open | Click | Credential | Data entry | Click to credential |
|---|---|---|---|---|---|
| A (HR bonus) | 82.0% | 47.0% | 18.0% | 5.0% | 38.3% |
| B (IT password reset) | 80.0% | 60.0% | 30.0% | 10.0% | 50.0% |
| C (CEO document review) | 90.0% | 75.0% | 15.0% | 10.0% | 20.0% |

- Campaign B (IT password reset) is significantly higher than A and C (p = 0.022 and 0.008); A and C cannot be told apart (p = 0.59).
- Scaled to 2,000 employees, Campaign B implies about 600 compromised accounts.
- The brief's model gives $652,500,000 a year by treating every account as a separate breach. This is shown as Scenario A only. My base case (Scenario B: one phishing attack a year, 25% chance of a major breach) gives **$1,087,500 a year**.
- Control ranking is the same in both scenarios: MFA, then training, then email filtering.

## Controls (base case, Scenario B)

| Control | Cost | Effectiveness | Annual risk reduction | ROI | Payback |
|---|---|---|---|---|---|
| MFA | $90,000 | 99.9% | $1,086,412 | 1,107% | 1.0 months |
| Enhanced training | $100,000 | 60.0% | $652,500 | 552% | 1.8 months |
| Email filtering | $50,000 | 20.0% | $217,500 | 335% | 2.8 months |
| Full programme (brief) | $490,000 | 90.0% | $978,750 | 100% | 6.0 months |

Break-even for the $490,000 programme: prevent 0.1126 breaches, or remove 45.1% of the base-case annual loss.

## Corrections to the brief

The brief's Campaign A and C exposures, email-filtering ROI, 90% risk-reduction total and 22.1% overall credential rate do not follow from its own formulas, and several statements are unsupported (the 93.75% breach probability, the industry-average column, and the treatment of accounts as independent breaches). Details and corrected values are in the report (Section 6) and the workbook (`Corrections` sheet).

## Repository map

| Path | Content |
|---|---|
| `spreadsheet/Lab3A_Phishing_Risk_Workbook.xlsx` | Calculation workbook with visible formulas (README_Assumptions, Inputs, Phase1_Rates, Phase2_Exposure, Controls, Risk_Matrix, Statistics, Corrections) |
| `docs/Lab3A_Phishing_Risk_Report.docx` | Written report with the executive briefing, risk matrix, statistics, corrections and limitations |

## Assumptions and limitations

Breach cost, the 25% breach probability and the control effectiveness percentages are scenario assumptions from the brief, not verified benchmarks. Attack frequency (1 a year in the base case) is my assumption, with a sensitivity table. The three campaigns used different target groups and sample sizes, so comparisons are indicative. Full list: report Section 7.

## AI-assistance declaration

I used Claude (Anthropic) throughout this lab for explanation of the formulas, checking my work against the brief, finding the errors in it, building the workbook and drafting the report. I reviewed the results and spot-checked the key figures in the workbook myself. Full declaration: report Section 8.

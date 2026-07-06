\# 🐱 Cookie Cats A/B Test Analysis

\## Gate 30 vs Gate 40 — Player Retention Study



!\[Python](https://img.shields.io/badge/Python-3.8+-blue)

!\[Status](https://img.shields.io/badge/Status-Complete-green)

!\[Dataset](https://img.shields.io/badge/Dataset-90%2C189%20players-orange)



\---



\## 📋 Business Question



> Should Cookie Cats move its first in-game gate from \*\*level 30\*\* to \*\*level 40\*\*?  

> Does this change significantly impact player retention — and is the impact large enough to justify the rollout?



\---



\## 🎯 Key Findings



| Metric | Gate 30 | Gate 40 | Significant? | Verdict |

|--------|---------|---------|--------------|---------|

| Day-1 Retention | 46.75% | 46.22% | NO (p=0.1147) | No proven effect |

| Day-7 Retention | 19.84% | 19.03% | YES (p=0.0026) | Gate 30 wins |



\### ✅ Recommendation: Keep the gate at level 30



Moving the gate to level 40 provides \*\*no proven benefit\*\* on Day-1 retention  

and causes a \*\*statistically significant decrease\*\* in Day-7 retention.



\---



\## 📊 Visualizations



!\[A/B Test Analysis](images/ab\_test\_analysis.png)



\---



\## 🔍 Project Overview



Cookie Cats is a popular mobile puzzle game. Players encounter  

a "gate" that requires them to wait or pay to continue playing.  

This project analyzes whether moving that gate from level 30  

to level 40 affects how many players return the next day and  

after 7 days.



\### What is an A/B Test?

An A/B test randomly splits users into two groups:

\- \*\*Control (gate\_30):\*\* Gate stays at level 30 — 42,763 players

\- \*\*Treatment (gate\_40):\*\* Gate moved to level 40 — 43,432 players



Only one thing changes between groups — the gate position.  

Everything else stays the same.



\---



\## 📈 Methodology



| Step | Description |

|------|-------------|

| Exploratory Analysis | Examined distributions, group sizes, retention rates |

| Experiment Validation | Checked sample ratio mismatch, zero-round players, outliers |

| Hypothesis Formulation | Defined H0/H1 for both metrics, set α=0.05 |

| Statistical Test | Z-test for proportions (binary outcome, large samples) |

| Confidence Intervals | 95% CI calculated for both metrics |

| Effect Size | Cohen's H computed to assess practical significance |

| Visualization | 4 charts covering retention, CI, distribution, summary |



\---



\## 🧪 Statistical Results



\### Day-1 Retention

\- \*\*Observed difference:\*\* 0.53% (gate\_30 higher)

\- \*\*Z-statistic:\*\* 1.577

\- \*\*P-value:\*\* 0.1147 ❌ Not significant

\- \*\*95% CI:\*\* (-0.130%, 1.202%) — crosses zero

\- \*\*Cohen's H:\*\* 0.0107 — small effect



\### Day-7 Retention

\- \*\*Observed difference:\*\* 0.81% (gate\_30 higher)

\- \*\*Z-statistic:\*\* 3.013

\- \*\*P-value:\*\* 0.0026 ✅ Significant

\- \*\*95% CI:\*\* (0.284%, 1.341%) — entirely positive

\- \*\*Cohen's H:\*\* 0.0205 — small effect



\### Key Insight: Statistical vs Business Significance

The Day-7 result is statistically significant (p=0.0026)  

but has a small effect size (Cohen's H=0.0205).  

At scale however — 0.81% of millions of players  

represents thousands of retained users and  

meaningful revenue impact.



\---



\## 📁 Project Structure
---

## 🛠️ Technologies Used

- **Python 3.8+**
- **pandas** — data manipulation
- **numpy** — numerical calculations
- **scipy** — statistical testing
- **statsmodels** — Z-test for proportions
- **matplotlib** — visualizations
- **seaborn** — visual styling

---

## 📦 Dataset

- **Source:** [Kaggle — Mobile Games A/B Testing](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)
- **Size:** 90,189 players
- **Columns:** userid, version, sum_gamerounds, retention_1, retention_7
- **Provided by:** Mursid Eyarkin on Kaggle

---

## 💡 Limitations

1. Effect size is small — real world impact may be modest
2. Minor sample ratio mismatch (1.77%) noted
3. Retention measured — not direct revenue
4. Long term effects beyond 7 days unknown
5. Player segments not analyzed separately

---

## 🚀 Next Steps

1. Keep gate at level 30 (current design)
2. Investigate player psychology around gate position
3. Test other gate positions (level 20, level 25)
4. Measure revenue impact directly in future tests
5. Segment analysis by player type

---

## 👤 Author

Fayaz Ahamed F 
Aspiring Data / Product Analyst  


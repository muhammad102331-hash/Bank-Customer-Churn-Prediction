# 🏦 Bank Customer Churn Analysis

> **What is this project about?**
> We looked at data from **10,000 bank customers** to figure out *who is likely to leave the bank* — and *why*.
> This helps the bank take action early (e.g. special offers, personal calls) to keep those customers.

---

## 📋 What Data Did We Use?

We had two files of customer information:

| Info We Had | Example |
|---|---|
| Country | France, Germany, Spain |
| Age | 42 years old |
| Account Balance | €83,000 |
| Credit Score | 608 / 850 |
| Number of Products | 1 (e.g. just a savings account) |
| Is Active Member? | Yes / No |
| Estimated Salary | €112,000 |
| **Did They Leave?** | **Yes (1) or No (0)** ← this is what we predicted |

---

## 🔍 Key Findings (What the Data Told Us)

### 1. How Many Customers Left?
- Out of every **100 customers**, about **20 left** the bank and **80 stayed**.
- This means churn is a real problem — 1 in 5 customers is walking out the door.

---

### 2. Who Is Most Likely to Leave?

#### 🌍 By Country
- **German customers churn the most** — roughly 1 in 3 German customers leaves.
- French and Spanish customers are much more loyal.
- 👉 *The bank should pay special attention to customers in Germany.*

#### 👶👴 By Age
- **Older customers (45–60 years old) are more likely to leave** than younger ones.
- Most customers in the data are between 30–40 years old.
- 👉 *Middle-aged and senior customers need more personalised attention.*

#### 💳 By Number of Products
- Customers with **only 1 product** (e.g. just a bank account) churn frequently.
- Customers with **2 products** (e.g. account + credit card) are the most loyal.
- Customers with **3 or 4 products** also churn a lot — possibly because they feel overwhelmed.
- 👉 *The "sweet spot" is 2 products — the bank should try to get customers to a second product.*

#### ⚡ By Activity
- Customers who are **NOT actively using the bank's services** are **twice as likely to leave**.
- 👉 *Reaching out to inactive customers could save a lot of them.*

#### 💰 By Balance
- About **36% of customers have a zero balance** in their account.
- Zero-balance customers tend to churn more.
- 👉 *Customers with empty accounts are a warning sign.*

#### 🚻 By Gender
- **Women churn slightly more than men**, but the difference is small.

---

## 🤖 We Built 3 Prediction Models

We trained computers to *predict which customer will leave*, using 3 different methods:

| Model | Accuracy | How Good at Catching Churners? |
|---|---|---|
| 🔵 Logistic Regression | 82% | Weak — catches only 22% of churners |
| 🟢 Random Forest | 87% | Better — catches 48% of churners |
| 🏆 XGBoost | **87%** | **Best — catches 48% of churners, slightly sharper** |

> **What does "catches churners" mean?**
> Out of 100 customers who actually left, our best model correctly identified 48 of them in advance.
> The other 52 "slipped through." This is a hard problem because churners are a minority.

### 🏆 Winner: XGBoost
- Most accurate overall
- Best at identifying potential churners before they leave
- Used by major banks and tech companies worldwide

---

## 💡 What Should the Bank Do?

Based on our analysis, here are **5 simple actions** the bank can take:

1. **Focus on Germany** — run a customer retention campaign specifically for German customers.

2. **Re-engage inactive members** — send personalised messages or offers to customers who haven't used their account recently.

3. **Encourage a second product** — customers with 2 products are the most loyal. Offer a free credit card or savings account upgrade.

4. **Watch customers aged 45–60** — this group needs more personal attention, perhaps check-in calls or loyalty rewards.

5. **Follow up on zero-balance accounts** — these customers have likely mentally "left" already. A small incentive could bring them back.

---

## 📊 Summary in One Line

> **Older, inactive German customers with only one bank product and an empty account are the most likely to leave — and XGBoost can identify them with 87% accuracy.**

---

## 🗂️ Project Structure

```
Bank_Churn/
│
├── data/
│   ├── raw/                    # Original, unmodified data files
│   │   ├── Bank_Churn.csv      # Clean customer data (10,000 rows)
│   │   └── Bank_Churn_Messy.xlsx  # Raw data with quality issues
│   └── processed/              # Cleaned / feature-engineered data
│
├── notebooks/
│   └── Bank_churn.ipynb        # Full analysis notebook (EDA → Modelling)
│
├── reports/
│   └── figures/                # Saved plots and charts
│
├── .gitignore
└── README.md
```

# loan-logic-audit
An audit of retail lending data to uncover the "hidden rules" of loan approvals. Focused on financial risk logic, credit gatekeepers, and identifying data gaps that lead to unexpected rejections.
# Project: The Loan Logic Audit (Why Banks Say No)

### What is this project about?
I took a dataset of bank loan applications and acted as a "Data Auditor." Usually, people just try to build a computer model to guess who gets a loan, but I wanted to find out the "why" behind the decisions. 

I dug into the numbers to see which factors actually move the needle and identified where the data seems to have "hidden rules" that don't always follow basic math.

### The Problem
In banking, a person who looks perfect on paper might still get rejected. This project is about finding those "breakpoints." I investigated:
* Why people with high salaries still get turned down.
* Why tiny loans ($9,000) are sometimes stretched out over 30 years.
* Which factors are the real "Gatekeepers" for a "Yes."

### What I did (The Audit)
* **The "Stress" Test:** I created a **Monthly Debt-to-Income (DTI)** metric. It’s not about how much you borrow; it's about how much of your monthly paycheck goes to the bank. 
* **Shape Analysis:** I used "Violin Plots" to see the actual crowd of applicants. This helped me see that while Graduates have a few super-rich outliers, the "average" person earns about the same regardless of their degree.
* **Hunting for Errors:** I looked for "Perfect Rejections"—people with good credit and high pay who were still rejected. This proved the data is missing key info like property value or existing debts.

### Top Findings
1. **Credit is King:** Your credit history is roughly 5x more important than your salary in this data. A bad score is almost always an automatic "No."
2. **The Salary Floor:** Most applicants earn around $4,000 a month. Unless you are in the top 5% of earners, your income doesn't help you as much as a clean credit record does.
3. **Hidden Factors:** The "noise" in the data proves that banks use information we can't see (like how much you have in savings) to make the final call.

### Tools I Used
* **Python** (Pandas/NumPy) for the heavy lifting.
* **Seaborn & Matplotlib** for the charts (Heatmaps and Violin Plots).
* **Financial Logic** to turn raw numbers into "Debt Stress" scores.

---
**Note:** This is an EDA-focused project. Instead of building a "Bad" model on noisy data, I focused on a high-quality audit to understand the business logic first.

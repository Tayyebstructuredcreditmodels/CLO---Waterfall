# CLO Waterfall Analyser

**Structured Credit | Interactive Tranche Model**

---

## 📌 Overview

This project is an interactive **CLO (Collateralized Loan Obligation) waterfall model** built in HTML, CSS, and JavaScript.

It simulates how cash flows from a portfolio of leveraged loans are distributed across different tranches of debt and equity under varying credit conditions.

The model is designed to demonstrate key structured credit concepts such as:

* Payment priority (waterfall structure)
* Tranche risk hierarchy
* Default and recovery dynamics
* OC (Overcollateralization) and IC (Interest Coverage) tests
* Equity residual returns

---

## 🧠 What This Model Does

The analyser takes user inputs and:

1. Generates **loan portfolio income** based on:

   * SOFR (base rate)
   * WAS (weighted average spread)

2. Applies **credit stress**:

   * Default rate
   * Recovery rate
   * CCC bucket impact

3. Runs a **cashflow waterfall**:

   * Fees paid first
   * Senior tranches paid in order (AAA → BB)
   * Remaining cash flows to equity

4. Evaluates **structural protections**:

   * OC Test (collateral vs debt)
   * IC Test (income vs interest obligations)

5. Outputs:

   * Tranche-level payments and shortfalls
   * Equity return estimate
   * Visual waterfall breakdown
   * Stress sensitivity chart

---

## 🏗️ Structure of a CLO (Simplified)

A CLO splits risk into layers:

| Tranche  | Priority | Risk    | Return  |
| -------- | -------- | ------- | ------- |
| AAA      | Highest  | Lowest  | Lowest  |
| AA / A   | High     | Low     | Low     |
| BBB / BB | Medium   | Medium  | Medium  |
| Equity   | Last     | Highest | Highest |

* **Senior tranches** are paid first and are protected from losses
* **Equity** absorbs losses first but receives any remaining profits

---

## ⚙️ Key Concepts Implemented

### 1. Waterfall Mechanics

Cash is distributed sequentially:

* Expenses
* Interest payments (top-down)
* Residual to equity

---

### 2. Credit Loss Modeling

Losses are calculated as:

Net Loss = Default Rate × (1 − Recovery Rate)

This reduces the income-generating asset base.

---

### 3. OC (Overcollateralization) Test

Measures collateral coverage:

OC Ratio = Collateral Value / Debt Outstanding

---

### 4. IC (Interest Coverage) Test

Measures ability to pay interest:

IC Ratio = Interest Income / Interest Due

---

### 5. Excess Spread

Remaining income after:

* Losses
* Fees
* Debt costs

This is a key driver of equity returns.

---

## 📊 Features

* Interactive parameter inputs
* Real-time waterfall simulation
* Visual tranche breakdown
* Stress scenario presets:

  * Base
  * Stress
  * Severe
  * GFC 2008
  * COVID shock
* Dynamic OC/IC test indicators
* Loss sensitivity chart

---

## 🚀 How to Use

1. Open the HTML file in a browser
2. Adjust:

   * Pool size, rates, fees
   * Tranche sizes and spreads
   * Default / recovery assumptions
3. Click **“Run Waterfall”**
4. Analyse outputs and visualisations

---

## ⚠️ Limitations

This is a **simplified, single-period model**:

* No multi-year cashflow simulation
* No principal repayment or reinvestment logic
* Equity IRR is an approximation
* Does not fully implement trigger-driven cash diversion

This model is intended for **educational and illustrative purposes**

---

## 👤 Author

**Tayyeb Shamsher**

Built independently with some assistance from AI tools for implementation support and refinement.

---

## 📌 Disclaimer

All figures and outputs are illustrative and do not represent real investment advice or actual CLO structures.

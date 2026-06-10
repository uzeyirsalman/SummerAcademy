# Lesson 6: Spreadsheet Mastery
## Thinking in Structured Data: Formulas, References, and Budgets

*   **Estimated Time**: 60–90 minutes
*   **Ages**: 12 & 15
*   **Key Vocabulary**: Cell, Formula vs. Function, Relative vs. Absolute Reference (`A1` vs. `$A$1`), Data Types, `SUM`, `AVERAGE`, `IF`, `XLOOKUP`.
*   **Prerequisites**: Google Sheets or Microsoft Excel.

---

## 1. Parent Prep Guide (3-Minute Refresh)
*   **Structured Data**: Grid systems allow us to map data in columns (fields/attributes) and rows (records).
*   **Formulas vs. Functions**:
    *   **Formula**: A mathematical equation you write (e.g., `=A1 + A2`). Always starts with `=`.
    *   **Function**: A pre-built shortcut code provided by the software (e.g., `=SUM(A1:A5)`).
*   **Relative vs. Absolute Referencing**: 
    *   **Relative (`A1`)**: If you write `=A1*2` and copy/drag the formula down one cell, it automatically changes to `=A2*2`. The reference moves relative to the formula.
    *   **Absolute (`$A$1`)**: The dollar signs lock the reference. If you write `=$A$1*2` and drag it down, it stays `=$A$1*2`. This is crucial when referencing a single cell containing a tax rate, exchange rate, or budget goal.
*   **`XLOOKUP` (or `VLOOKUP`)**: Searches a column for a search key and returns the value of a cell in a different column on the same row. It’s like looking up a word in a dictionary to find the definition.

---

## 2. Teaching Script & Discussion Flow

### The Magic Calculator Analogy
*Explain spreadsheets by comparing them to a smart grid:*

*   **You (the Parent)**: "If you have a sheet of paper and write down your monthly expenses: Rent $500, Food $100, Games $50. You add them up to get $650. Now, you change the Games expense from $50 to $80. What do you have to do to the total?"
*   **Teens**: "Erase the $650, calculate the math again, and write $680."
*   **You**: "In a spreadsheet, you write the numbers in boxes called **cells** (like A1, A2). In the total box, instead of writing $650, you write a command: `=SUM(A1:A3)`. If you change the Games box from $50 to $80, what happens to the total?"
*   **Teens**: "It updates automatically!"
*   **You**: "Exactly. A spreadsheet is a living network of cells. If one cell changes, everything connected to it updates in a millisecond. It's the most widely used data tool in the business world."

### Socratic Discussion Questions
1.  *“We want to calculate the Sales Tax of 10 items in a list. The tax rate (e.g., 5%) is written in cell `Z1`. If we write `=A1 * Z1` for the first item and drag it down to calculate the rest, what error will happen?”*
    *   **Answer**: The formula will shift to `=A2 * Z2`, then `=A3 * Z3`. Since cells `Z2` and `Z3` are empty (or contain other text), the calculations will fail or return zero. We must lock it as `=A1 * $Z$1` so that `Z1` remains fixed while `A1` shifts.
2.  *“Why is it a bad idea to type numbers directly into formulas, like `=A1 * 0.05` instead of `=A1 * Z1`?”*
    *   **Answer**: Hardcoding values makes the spreadsheet rigid. If the tax rate changes from 5% to 6%, you would have to manually edit every single formula. If you reference `Z1`, you only have to change the value in one cell, and the entire sheet updates itself.

---

## 3. Hands-On Lab: The Teen Budget Dashboard

The teens will build a dynamic, formula-driven personal budget from scratch.

### Step 1: Set Up the Transaction Log
1.  Open a new spreadsheet in Google Sheets or Excel.
2.  Name the sheet tab at the bottom: **Transactions**.
3.  Create the following columns in row 1:
    *   `A1`: Date
    *   `B1`: Category (e.g., Income, Food, Games, Clothes, Savings)
    *   `C1`: Description
    *   `D1`: Amount
4.  Enter 5-8 sample rows of data, for example:
    *   `06/10/2026` | `Income` | `Allowance` | `50`
    *   `06/11/2026` | `Food` | `Smoothie` | `6`
    *   `06/12/2026` | `Games` | `Steam game` | `15`
    *   `06/13/2026` | `Clothes` | `T-Shirt` | `20`
    *   `06/14/2026` | `Savings` | `Birthday money` | `30`

---

### Step 2: Set Up the Dashboard
1.  Create a second sheet tab at the bottom and name it: **Dashboard**.
2.  In cell `A1`, write: **Savings Goal %**. In cell `B1`, write: `20%` (0.20).
3.  Let's create the Summary Table. Set up these labels:
    *   `A4`: Total Income
    *   `A5`: Total Expenses
    *   `A6`: Net Savings
    *   `A7`: Savings Rate %
    *   `A8`: Goal Status
4.  Write the formulas in Column B to automate the math:
    *   **Total Income** (Sum all "Income" amounts):
        `=SUMIF(Transactions!B:B, "Income", Transactions!D:D)`
    *   **Total Expenses** (Sum everything that is NOT Income or Savings):
        `=SUMIFS(Transactions!D:D, Transactions!B:B, "<>Income", Transactions!B:B, "<>Savings")`
    *   **Net Savings** (Total Income - Total Expenses):
        `=B4 - B5`
    *   **Savings Rate %** (Net Savings / Total Income):
        `=B6 / B4` (Format this cell as percentage: `%`)
    *   **Goal Status** (Check if Savings Rate is >= Savings Goal % in `B1`):
        `=IF(B7 >= $B$1, "Goal Met! 🎉", "Need to Save More! 🪫")`
        *(Note the absolute reference `$B$1` to lock the goal cell!)*

---

### Step 3: Add the Chart
1.  Select your Summary Table categories (or create a small summary of expenses by category using `=SUMIF(Transactions!B:B, "Food", Transactions!D:D)`, etc.).
2.  Click **Insert > Chart**.
3.  Choose a **Pie Chart** or **Bar Chart** showing the distribution of expenses.
4.  **Test the Automation**: Add a new row to the *Transactions* tab (e.g., `06/15/2026` | `Games` | `Xbox pass` | `30`). Look at the *Dashboard* tab. Did the Expenses, Net Savings, Goal Status, and Pie Chart update automatically?

---

## 4. Teens' Reflection & Log
*Have the kids answer these questions:*

1.  **What formula did you write to calculate your Net Savings?**
2.  **Why did you need the dollar signs in the `$B$1` cell reference inside the `IF` statement?**
3.  **What is the difference between `=SUM(D2:D10)` and `=SUMIF(B2:B10, "Food", D2:D10)`?**
4.  **How would a business owner use a spreadsheet like this to make decisions about their spending?**

---

## 5. End-of-Lesson Quiz

1.  **What character must every formula or function begin with in a spreadsheet?**
    *   *Answer*: The equals sign (`=`).
2.  **If you write `=A5` in cell B5 and then copy B5 into B6, what will the formula in B6 become?**
    *   *Answer*: `=A6` (because it is a relative reference).
3.  **How do you lock cell D3 in a formula so it doesn't change when copied?**
    *   *Answer*: Write it as absolute: `=$D$3`.
4.  **What does the `IF` function do?**
    *   *Answer*: It checks a condition (logical test) and returns one value if the condition is True, and another value if the condition is False.

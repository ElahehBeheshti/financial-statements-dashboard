#Financial statements in Tableau
    Understanding the Dataset and Data Structure
    The Data is stored in Excel file, and it stored like an ERP system, with separate worksheets.
    In Databases, data is stored in separate tables to avoid redundancy and improve efficiency.

Key Data Tables & Their Purpose
    1.General Ledger (GL): Stores all transaction details, foundation for reporting.
    2.Chart of Accounts: Defines GL accounts (PNL, Balance Sheet, Assets, Liabilities).
    3.Calendar Table: Provides date-related attributes for time-based analysis.
    4.Territory Table: Links transactions to country/region without duplication.

Data Structuring for Efficiency
    Uses keys (Territory Key, Account Key) instead of repeating data.
    Chart of Accounts classifies accounts into structured categories.
    Calendar Table enables time-based comparisons (e.g., Q1 2018 vs. Q1 2019).
    
    ############################################################################################
    
Creating a Profit and Loss (PNL) Statement in Tableau
  Step 1: Setting Up the Worksheet
    Drag Account & Sub-Account fields (from Chart of Accounts) to Rows.
    Drag Date field (from Calendar Table) to Columns (to allow Year > Quarter > Month hierarchy).

  Step 2: Filtering & Structuring
  
    Filter to show only Profit & Loss (PNL) accounts (exclude cash accounts).
    Sort and group transactions into:
    Trading Accounts (Sales, Cost of Sales)
    Operating Accounts (Expenses, Marketing)
    Non-Operating Accounts (Interest, Tax)
    Manually sort categories in a logical order for readability.
    
  Step 3: Adding & Formatting Totals
  
    Add Grand Totals & Subtotals:
    Gross Profit, Operating Expenses Total, Non-Operating Income/Expense Total, Interest & Tax Total.
    Format the PNL report:
    Rename "Grand Total" → Net Profit.
    Remove unnecessary labels for clarity.

    Final Outcome
✔ Correct sorting of revenue & expense categories
✔ Grand total reflects net profit
✔ Clean, structured, and formatted report


    ############################################################################################
    
3. Profitability Analysis in Tableau

    Step 1: Calculating Key Metrics
    Each metric requires a new worksheet with calculated fields:
    
    A. Gross Profit (GP)
    
    Formula: Sales - Cost of Sales
    Filter transactions using Trading Account.
    B. Operating Profit
    
    Formula: Gross Profit - Operating Expenses
    C. EBITDA (Earnings Before Interest, Tax, Depreciation, and Amortization)
    
    Formula: Operating Profit + Depreciation & Amortization
    Remove Depreciation & Amortization from Operating Expenses.
    D. Profit Before Interest & Tax (PBIT)
    
    Formula: Operating Profit + Non-Operating Income - Non-Operating Expenses
    E. Net Profit
    Formula: PBIT - Interest & Taxes
  Step 2: Creating Profitability Ratios
    Gross Profit Margin: (Gross Profit ÷ Sales) × 100
    Net Profit Margin: (Net Profit ÷ Sales) × 100
    Operating Profit Margin: (Operating Profit ÷ Sales) × 100
    ✔ Format as percentages for better visualization.

    <img width="1412" alt="image" src="https://github.com/user-attachments/assets/e6bcc6a5-eed4-4b5b-ae68-7794ab5ac99c" />


############################################################################################

4. Advanced Balance Sheet & Financial Ratios in Tableau

Key Balance Sheet Components
Assets (Current & Non-Current)
Liabilities (Current & Non-Current)
Owner's Equity
Step 1: Calculating Financial Ratios
A. Return on Assets (ROA)

Net Profit ÷ Total Assets (measures efficiency).
B. Return on Equity (ROE)

Net Profit ÷ Shareholders’ Equity (profitability for investors).
C. Asset Turnover Ratio

Sales ÷ Average Total Assets (measures revenue generation from assets).
D. Debt-to-Equity Ratio

Total Liabilities ÷ Total Equity (measures financial leverage).
✔ Format values as percentages in Tableau.


<img width="1372" alt="image" src="https://github.com/user-attachments/assets/4ed1ae69-d96f-448b-acd1-ed061872adcd" />

    ############################################################################################

  5. Creating Financial Dashboards in Tableau
  
  Step 1: Building Key Charts
  Stacked Bar Chart (Sales, Gross Profit, Net Profit)
  Area Chart (Gross Profit vs. Operating Profit)
  Dual-Axis Chart (Sales vs. Marketing Expense)
  Line Chart (Total Assets vs. Asset Turnover)
  Bubble Chart (Peak sales periods using circle sizes).
  Step 2: Enhancing Interactivity
  Add filters (Year, Quarter, Region) for dynamic analysis.
  Enable dual-axis for better comparisons.
  Manually adjust colors for clarity.
  ✔ Final Dashboard provides deep financial insights 📊🚀
  
      ############################################################################################

  6. Cash Flow Statement Analysis
  
  Cash Flow Statement Structure
  Operating Activities
  Adjust for non-cash expenses and working capital changes.
  Investing Activities
  Purchase/Sale of assets, dividends, and interest received.
  Financing Activities
  Debt issuance/repayment, equity transactions.
  Opening & Closing Cash Balances
  Ensuring accuracy of cash equivalents over time.
  Step 1: Data Structuring for Cash Flow Statement
  Upload Cash Flow Statement Structure and Chart of Accounts into Tableau.
  Define One-to-Many relationships for accurate mapping.
  Step 2: Calculating Cash Flow Components
  Opening & Closing Balances: Use Total-to-Date (TD) calculations.
  Adjust for Working Capital Changes: Inventory, Receivables, Payables.
  Identify CAPEX and Financing Transactions.
  Validate results against Income & Balance Sheet.
  Step 3: Preparing the Dashboard
  Link Chart of Accounts to Cash Flow Statement.
  Apply filters to categorize cash flow items correctly.
  Ensure correct ordering & sign adjustments (debits/credits).
  ✔ Structured Cash Flow Analysis for better decision-making.


  <img width="634" alt="image" src="https://github.com/user-attachments/assets/c761ecb5-afd0-4baf-9f7b-c75dc1f77fd8" />


  
  <img width="760" alt="image" src="https://github.com/user-attachments/assets/aaa06ab0-6ad7-40dd-9608-bf6927b94a0c" />


  <img width="861" alt="image" src="https://github.com/user-attachments/assets/20ef3913-6330-49f4-9884-ae9f30a2c478" />




      ############################################################################################
  
  7. Statement of Changes in Equity (SoC)
  
  Purpose
  Tracks share capital, retained earnings, and dividends.
  Step 1: Structuring the Report
  Define Opening & Closing Balances in Tableau.
  Adjust for dividends, share capital transactions, and net income changes.
  ✔ Final report integrates with Cash Flow & Balance Sheet.


<img width="588" alt="image" src="https://github.com/user-attachments/assets/d9e3d629-a243-4e27-9dd7-d00d5b76a3e0" />


      ############################################################################################
  
  8. Final Takeaways from this project
  
  ✅ Structured financial data preparation.
  ✅ Used calculated fields to dynamically update statements.
  ✅ Defined relationships in Tableau for seamless integration.
  ✅ Financial dashboards to provide actionable insights.

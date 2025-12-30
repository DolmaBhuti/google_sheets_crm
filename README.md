# My CRM System (Google Sheets)

> **Note:** This CRM system was originally built in Google Sheets. Since GitHub cannot host live Google Sheets files, the full system is shared here as a read-only Excel export for portfolio demonstration.

## Description

A lightweight **Customer Relationship Management (CRM)** system built in Google Sheets for small organizations and solo operators who need a structured way to track customers and sales pipelines without the learning curve or cost of traditional CRM software.

The system provides clear data relationships, guided workflows, and basic automation while remaining flexible and familiar to spreadsheet workflows.

## Live Link
https://docs.google.com/spreadsheets/d/1aqYFwOjovnKIPd1yP8T5PGYEwuOs0Ctzx_umjM4ujyM/edit?usp=sharing  

- Click **File → Make a copy**  
- Authorize **Apps Script**

## Usage

### 1. Add a Customer
1. Open the **1 - Customers** sheet.
2. Enter a new row with the client’s name and required details.
3. The client ID is generated automatically.
4. The client will immediately appear in all customer reference dropdowns across the system.

### 2. Create a Sales Opportunity
1. Open the **2 - Sales Pipeline** sheet.
2. Add a new row for the opportunity.
3. Select the client from the **Client ID** dropdown.
4. Enter the opportunity details:
   - Opportunity name  
   - Deal value  
   - Stage  
   - Probability  
5. The opportunity is now linked to the selected customer.

### 3. Log Activities (Calls, Emails, Meetings)
1. Open the **3 - Activity Timeline** sheet.
2. Add a new row for each interaction.
3. Select the related **Client ID** and **Opportunity ID**.
4. Enter:
   - Date of interaction  
   - Type of interaction (Call, Email, Meeting, etc.)  
   - Summary of the interaction  
   - Next action  
   - Follow-up date  
5. The activity is now linked to both the customer and opportunity.

### 4. Track Follow-Ups
1. Enter a follow-up date when logging an activity.
2. The **Overdue Follow-Up** status updates automatically based on today’s date.
3. Overdue activities are visually flagged for quick attention.

### 5. Update Sales Pipeline Stages
1. In the **2 - Sales Pipeline** sheet, update the **Stage** column as the deal progresses.
2. Move opportunities through each stage:
   - Prospecting  
   - Qualification  
   - Proposal / Demo  
   - Negotiation  
   - Closed Won  
   - Closed Lost  
3. Closed opportunities remain available for reporting and performance analysis.

## Automations & Business Logic

This CRM system includes light automation to reduce manual work while preserving data accuracy and flexibility.

### Customer Automations
- **Automatic Client ID generation**  
  When a new client name is entered, the system generates a permanent, unique Client ID (e.g. `C001`) that acts as the primary identifier across all sheets.

- **Automatic Customer Created Date**  
  The Created Date is set automatically when a client is first added and is not overwritten on future edits.

- **Customer reference table**  
  A dynamic customer reference table is generated and used to power dropdown selections throughout the system.

### Sales Pipeline Automations
- **Automatic Opportunity ID generation**  
  When a client is selected for a new opportunity, the system generates a unique Opportunity ID (e.g. `OPP-001`) that remains stable over time.

- **Stage-driven probability**  
  Deal probability is automatically determined based on the selected sales stage using a centralized configuration list.

- **Forecast value calculation**  
  Forecasted revenue is calculated automatically using deal value and probability.

- **Automatic Opportunity Created Date**  
  Opportunity creation dates are captured automatically for reporting and trend analysis.

### Activity Tracking Automations
- **Optional activity-to-opportunity linking**  
  Activities can optionally be associated with an Opportunity ID selected from a controlled dropdown, supporting both pre-deal and post-deal interactions.

- **Overdue follow-up detection**  
  Follow-up dates are monitored automatically, and overdue activities are clearly flagged.

### Data Integrity Controls
- System-generated fields (IDs, created dates, calculated values, and lookup fields) are protected to prevent accidental edits.
- User-facing fields remain editable to support flexible workflows.

## Technical Highlights
- **Google Sheets** — Structured data storage, validation, formulas, and reporting  
- **Google Apps Script** — Automation for workflow support and data integrity

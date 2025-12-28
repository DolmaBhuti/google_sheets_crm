# My CRM System (Google Sheets)

## Description
A lightweight **Customer Relationship Management (CRM)** system built in Google Sheets for small organizations and solo operators who need a structured way to track customers and sales pipelines without the learning curve or cost of traditional CRM software.

The system provides clear data relationships, guided workflows, and basic automation while remaining flexible and familiar to spreadsheet users.

## Usage

### 1. Add a Customer
1. Open the **Customers** sheet.
2. Enter a new row with the customer’s name and required details.
3. The customer ID is generated automatically.
4. The customer will immediately appear in all customer reference dropdowns across the system.

### 2. Create a Sales Opportunity
1. Open the **Sales Pipeline** sheet.
2. Add a new row for the opportunity.
3. Select the customer from the **Customer Name / ID** dropdown.
4. Enter the opportunity details:
   - Opportunity name  
   - Deal value  
   - Stage  
   - Probability  
   - Created date
5. The opportunity is now linked to the selected customer.

### 3. Log Activities (Calls, Emails, Meetings)
1. Open the **Activity Timeline** sheet.
2. Add a new row for each interaction.
3. Select the related **Customer ID** and **Opportunity ID**.
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
1. In the **Sales Pipeline** sheet, update the **Stage** column as the deal progresses.
2. Move opportunities through each stage:
   - Prospecting  
   - Qualification  
   - Proposal / Demo  
   - Negotiation  
   - Closed Won  
   - Closed Lost
3. Closed opportunities remain available for reporting and performance analysis.

## Technology Used
- **Google Sheets** — Structured data storage, validation, formulas, and reporting
- **Google Apps Script** — Automation for workflow support and data integrity

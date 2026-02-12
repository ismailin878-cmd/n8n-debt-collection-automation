# Automated Debt Collection System (n8n)

### The Story Behind the Project
Growing up, I watched my father manage his business, and one of the biggest challenges he faced was tracking and collecting debts from customers. It was a manual, time-consuming process of phone calls and visits that often led to unnecessary stress.

When I started learning automation with n8n, this was the first problem I wanted to solve. I wanted to turn that manual "chasing" into a streamlined, automated engine to protect a business's most valuable asset: Time.

### How the Workflow Works
This workflow automates the entire follow-up cycle:
* **Schedule Trigger**: Runs the check automatically every day.
* **Data Retrieval**: Fetches 100+ invoice records directly from Google Sheets.
* **Logic Engine**: A custom JavaScript node filters unpaid invoices and calculates exactly how many days a payment is overdue.
* **Smart Delay**: Includes a "Wait" node to manage email delivery rates safely.
* **Automated Outreach**: Sends professional, personalized HTML reminders via Mailtrap/SMTP.
* **Database Sync**: Automatically updates the sheet with the latest notice date and reminder count.

### Technical Components
* **n8n**: Workflow orchestration.
* **Google Sheets**: Acting as the primary database.
* **JavaScript**: Custom logic for data filtering.
* **SMTP/Mailtrap**: Email delivery and testing.

### Setup Instructions
1. **Workflow**: Download the `Daily_Invoice_Followup.json` file from this repo and import it into your n8n instance.
2. **Database**: I have included an Excel template in this repository. Upload this to your Google Drive to use as the data source.
3. **Credentials**: You will need to link your own Google Sheets and SMTP credentials within the nodes, as they are not included in the JSON for security reasons.

Medical Billing System
A simple Python-based command-line application designed to manage patient registration, track hospital expenses (consultations, room stays, and medications), and automatically calculate billing breakdowns based on insurance coverage.

Features
Patient Record Management: Captures patient info, registration IDs, and insurance details.

Dynamic Expense Tracking: Adds and categorizes multiple billing items like consultation fees, room charges (calculated by days stayed), and medication costs.

Automated Billing Logic: Computes total costs, co-pays, and insurance contributions dynamically.

Persistent Data Logging: Automatically exports and appends finalized bills to a structured CSV file (billing_records1.csv) for easy record-keeping.

How It Works (Sample Walkthrough)
When you run the script, it will guide you through a series of prompts to input patient details and costs:

Plaintext
Patient ID / Registration no: 113
Patient Name: Syria
Insurance Provider: No
Consultation Description: Anxiety
Room Description: Special
Number of Days: 0
Medication Description: Therapy
Medication Cost: 500
Insurance Covers Medication? (yes/no): no 
Generated Output

The system immediately calculates the breakdown and saves the record:

Plaintext
------ BILL ------
Patient: Syria
Total Cost: $ 2000.0
Insurance Paid: $ 0
Patient Pays: $ 2000.0
***---------Breakdown---------***
Consultation fee: $1500
charge for single day: $1000 and days stayed 0
Room charge: $ 0
Medication cost: $ 500.0
Record saved.
Data Storage
All finalized transactions are saved in billing_records1.csv with the following structure:

Patient ID	Name	Insurance	Total	Insurance Paid	Patient Due
113	Syria	No	2000.0	0	2000.0
Future Roadmap / Enhancements
[ ] Implement a Graphical User Interface (GUI) using Tkinter.

[ ] Add input validation to prevent crashes on invalid number types.

[ ] Integrate a database backend (like SQLite) instead of a CSV file.

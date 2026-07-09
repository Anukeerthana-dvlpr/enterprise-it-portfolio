# Enterprise Multi-Functional Printer (MFP) Cost Optimization Framework

## Project Overview
Designed an automated print management architecture for a hybrid corporate office to reduce paper/toner waste, enforce secure badge printing, and recover department costs.

## Technical Design Specifications

### 1. Cost Charging Matrix Model
*   **Monochrome (Black & White) Page:** $0.02
*   **Color Page:** $0.10
*   **Duplex (Double-sided) Incentive:** 20% discount applied automatically by the print server software to encourage eco-friendly printing.

### 2. Active Directory User Quotas
*   **Group Mapping:** Synced via LDAP to corporate Active Directory groups.
*   **Standard Employee Profile:** Allocated a strict monthly credit limit of $15.00. 
*   **Enforcement Rule:** If account balances reach $0.00, the print spooler intercepts and automatically holds jobs until the next month's refresh.

### 3. Secure "Find-Me" Release Workflow
1. User prints a document from their laptop to a single virtual print queue named `Global-Secure-Print`.
2. The print server holds the job encrypted in transit using **IPPS (Port 631)**.
3. The user walks up to *any* physical physical Ricoh/HP MFP printer on the network and swipes their RFID employee badge.
4. The embedded software authenticates the user token against the central database and releases the print job directly to that specific machine. This eliminates unattended paperwork left on printer trays.

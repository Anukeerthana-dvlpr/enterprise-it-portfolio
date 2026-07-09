# Enterprise IT Engineering Portfolio

## Projects Overview

This section highlights the fundamental blueprints and concepts I mapped out during a half-day intensive study session to understand modern enterprise IT infrastructure.

---

### Project 1: CyberArk EPM Policy Architecture
*   **Objective:** Design a basic endpoint security blueprint focused on administrative rights removal and privilege management.
*   **What I Learnt:** 
    *   The principle of least privilege (PoLP) and its role in reducing corporate attack surfaces.
    *   How to structure application policies to separate everyday corporate tools from development applications.
    *   Using digital certificate validation and sandboxing to control unknown executables safely.
*   **File Link:** [View CyberArk EPM Blueprint](./cyberark-epm-blueprint.md)

---

### Project 2: Enterprise Printer Management & Cost Recovery
*   **Objective:** Model a central network print server architecture designed to reduce paper waste and track departmental operational costs.
*   **What I Learnt:** 
    *   The core architecture of network print servers and management utilities like PaperCut.
    *   How to configure print quotas linked directly to Active Directory user profiles.
    *   Setting up administrative rules to automatically redirect high-volume print jobs to cost-effective devices.
*   **File Link:** [View Print Management Blueprint](./print-management-blueprint.md)

---

### Project 3: M365 Cloud OS Deployment Brief
*   **Objective:** Detail a provisioning strategy for cloud-hosted Windows 365 Cloud PCs tailored for standard enterprise users.
*   **What I Learnt:** 
    *   The workflows involved in cloud provisioning and remote workspace management.
    *   Using Microsoft Intune to push uniform software baselines and administrative policies over-the-air.
    *   Implementing fundamental Data Loss Prevention (DLP) controls, such as clipboard and local drive redirection blocks.
*   **File Link:** [View M365 Cloud OS Brief](./m365-cloud-os-brief.md)

---

### Project 4: MFP Management & Secure Print Framework
*   **Objective:** Map out an identity-verified printing workflow across corporate Multi-Function Printers (MFPs) to prevent data leaks and physical tray waste.
*   **What I Learnt:** 
    *   The mechanics of a "Hold and Release" virtual queue that keeps jobs paused until the user is physically present.
    *   Integrating employee badge or PIN authentication with central directory services at the physical device interface.
    *   Securing print jobs in transit using IPPS (Secure IP) and setting up automated purge windows for unclaimed documents.
*   **File Link:** [View MFP Secure Print Blueprint](./mfp-secure-print-blueprint.md)

# CyberArk EPM Least Privilege Implementation Blueprint

## Project Overview
Designed an enterprise-grade endpoint security blueprint to enforce the Principle of Least Privilege (PoLP) for 500 standard corporate workstations, reducing the local attack surface by 90%.

## Architecture & Logic Flow
*The flowchart below maps out the application interception logic designed for this rollout:*
![Application Interception Logic](YOUR_UPLOADED_DIAGRAM_IMAGE_URL_HERE)

## Policy Configuration Specification
I engineered three distinct rule tiers to balance absolute security with user productivity:

1. **Tier 1: Core Trusted Applications (Auto-Allow)**
   * **Criteria:** Signed by trusted vendors (`O=Microsoft Corporation`, `O=Google LLC`).
   * **Action:** Run in standard user context without prompts.

2. **Tier 2: Developer Tooling (Just-In-Time Elevation)**
   * **Target Executable:** `vs_installer.exe` (Visual Studio Installer).
   * **Matching Criteria:** File SHA-256 Hash + Publisher Certificate validation.
   * **Action:** Elevate to admin privileges.
   * **User Interaction:** Prompts user for a valid Jira/ServiceNow ticket number before unlocking.

3. **Tier 3: Unrecognized Software (Restricted Execution)**
   * **Criteria:** Any unsigned binary running from `\AppData\Local\` or `\Downloads\`.
   * **Action:** Run inside a restricted EPM Sandbox. Completely blocks reads to the `LSASS` memory space to prevent credential theft.

  <img width="4096" height="1519" alt="image" src="https://github.com/user-attachments/assets/29d84354-9ccf-48d2-b377-a371b8b469f7" />

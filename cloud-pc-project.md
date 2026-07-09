# Microsoft 365 Cloud PC (Windows 365) Enterprise Deployment Blueprint

## Project Overview
Engineered a scalable, cloud-native virtual desktop solution using Microsoft Intune to provision Windows 11 Enterprise Cloud PCs securely for a distributed remote workforce.

## Step-by-Step Deployment Architecture

### 1. Identity & Network Setup
*   **Identity Architecture:** Implemented a cloud-only native **Microsoft Entra ID Join**.
*   **Network Mapping:** Deployed Cloud PCs directly to Microsoft-hosted networks inside local geographic Azure regions to keep user latency under 30ms.

### 2. Intune Provisioning Policy Configuration
*   **Policy Target Group:** `SG-CloudPC-Standard-Users` (Dynamic User Group targeting remote contractors).
*   **OS Image Definition:** `Windows 11 Enterprise + Microsoft 365 Productivity Apps (Version 23H2)`.
*   **User Account Type:** Configured as standard **Standard User** (Local Admin rights explicitly stripped for security baseline alignment).

### 3. Configuration Profiles & Security Hardening
*   **Update Strategy:** Integrated **Windows Autopatch** to automate monthly quality and security updates across 4 deployment rings without manual IT admin intervention.
*   **Data Loss Prevention (DLP) Policies:**
    *   *Clipboard Redirection:* Blocked (Prevents copying corporate data to personal home PCs).
    *   *USB Drive Redirection:* Disabled via administrative device configuration profile.

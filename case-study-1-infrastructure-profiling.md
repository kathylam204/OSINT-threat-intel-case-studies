# Case Study 1: Infrastructure Profiling & Mitigating Deceptive Domains (Operation Frankenstein)

**Author:** Kathy Lam  
**Focus Area:** Threat Intelligence, OSINT Tracking, Infrastructure Takedown  
**Target Action Status:** Successfully Mitigated & Reported to CISA  

---

## 1. Executive Summary

* **Incident Overview:** This case study outlines the structural investigation, tracking, and defensive mitigation of an active corporate impersonation and phishing infrastructure. Threat actors stood up a malicious lookalike domain designed to visually deceive job seekers and harvest highly sensitive Personally Identifiable Information (PII) under the pretext of an active corporate recruitment workflow.
* **The Challenge:** Traditional job board applications are targeted by increasingly sophisticated social engineering operations that abuse trusted brand credentials. Because these attacks leverage legitimate third-party hosting systems, tracking them requires defensive OSINT (Open Source Intelligence) techniques to unmask their footprints without altering the attacker's active state.
* **Operational Impact:** By analyzing domain telemetry, tracking unauthenticated infrastructure assets, and cross-referencing public records database clusters, this investigation completely isolated a multi-state "Frankenstein identity" used to deploy the campaign. A formal threat brief was compiled and routed directly to platform abuse desks and federal security systems (**CISA**) to feed global DNS defense filters.

---

## 2. Incident Background & Attack Surface

The threat vector initiated through unsolicited, deceptive remote job offers targeting technology and operations professionals. The actors executed a three-pronged threat sequence:

1. **Brand Weaponization:** Exploited the trusted corporate brand identity of **Triumph Group, Inc.** to bypass applicant skepticism and project procedural legitimacy.
2. **Lookalike Infrastructure Deployment:** Set up a typo-squatted, lookalike root domain designed to serve as a deceptive interface imitating an applicant management platform.
3. **Data & Credential Harvesting:** Structured fraudulent onboarding interviews to compel targets into surrendering background check clearances, banking documentation, and critical foundational PII.

---

## 3. Infrastructure Dissection & DNS Telemetry

To bypass on-server defensive logs, a completely out-of-band, passive examination of the public registration profile and DNS network mapping was performed. The data footprint isolated the following core infrastructure indicators:

| Technical Indicator Field | Collected Telemetry Asset |
| :--- | :--- |
| **Target Malicious Domain** | `[REDACTED][.]com` |
| **Upstream Infrastructure Host** | Squarespace, Inc. / Squarespace Domains LLC |
| **Administrative Contact Handle** | `[REDACTED[@]outlook[.]com` |
| **Associated Phone Asset** | `+1-808-xxx-xxxx` |
| **Infrastructure Profile** | Multi-State Composite Identity (Stitched Data Layout) |

### Strategic Anomaly Discovery
Legitimate enterprise organizations maintain fully authenticated internal mail setups (e.g., `@triumphgroup.com`) paired with tightly monitored SPF, DKIM, and DMARC record verification policies. The inclusion of a free, unverified consumer-tier handler (`michael35563@outlook.com`) as the root administrative contact exposed an irreconcilable enterprise anomaly, confirming a malicious infrastructure setup.

---

## 4. OSINT Pivoting & Composite Identity Analysis

Using the specific naming structures, addresses, and telephone parameters extracted from the registration profile, independent pivoting was conducted across public property registries, localized corporate filings, and commercial data brokers. 

### Core Intelligence Discoveries:
* **The "Frankenstein" Matrix:** The physical address, mobile phone provider routing, and registrant name had zero matching data links across historical public profiles. 
* **Data Sources Exploited:** The elements belonged to three completely independent, innocent citizens located across distinct geographical states in the US.
* **Evasion Functionality:** Threat actors purposefully combined disparate, valid consumer data points into a single composite entry to pass baseline automated fraud-detection checks used by web hosts and payment systems, masking their malicious intent.

---

## 5. Mitigation, Counter-Measures, & Global Defense

To render the campaign useless and disrupt ongoing operations, a dual-action threat intelligence package was built and distributed:

### A. Upstream Platform Abuse Mitigation
A formal breach-of-service violation report was submitted directly to the host's trust and safety department, providing documented evidence of brand impersonation, consumer fraud, and acceptable use policy (AUP) violations to accelerate site suspension.

### B. Federal Intelligence Pipeline Submission
To protect global consumers on a systemic scale, a formal threat notification was built and routed directly to the **Cybersecurity and Infrastructure Security Agency (CISA)** at `phishing-report@us-cert.gov` for blocklist integration.

```text
### STRUCTURED INDICATORS OF COMPROMISE (IoCs) ###
Domain Name: [REDACTED][.]com
Registrar: Squarespace Domains LLC
Registrant Admin Email: [REDACTED[@]outlook[.]com
Registrant Phone Asset: +1-808-xxx-xxxx
Impersonated Legal Corporate Entity: Triumph Group, Inc.
Classification: Active Phishing / Cyber-Enabled Employment Fraud Campaign
Target Action Requested: Global DNS Ingestion Filter Updates / Blacklist Integration
```
---
*Note: In accordance with professional data privacy standards and operational security protocols, all specific handles, real-world names, exact IP spaces, and server domains have been strictly redacted or defanged ([REDACTED]) to protect the security boundaries of the surviving user base.*

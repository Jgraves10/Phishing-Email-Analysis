# Phishing Email Analysis Lab

## Overview
This project documents the analysis of a real-world phishing email i got. This project shows examples of identify indicators of compromise (IOCs), how to validate a suspicious URL, and review email authentication results. The goal of this lab was to practice the type of investigation a cybersecurity analyst or SOC analyst might perform when reviewing a suspicious email.

## Objective
- Analyze a phishing email for suspicious characteristics
- Identify social engineering tactics and technical indicators
- Validate the embedded URL using VirusTotal
- Review header authentication results to assess legitimacy
- Document findings in a structured, incident-style format

## Tools Used
- VirusTotal
- Gmail
- Microsoft Excel
- Microsoft Word

## Skills Demonstrated
- Phishing email analysis
- IOC identification
- URL reputation analysis
- Header analysis
- Security documentation

---

## Scenario
I recieved a suspicious email claiming that my icloud account had been blocked and that files would be deleted unless me the recipient renewed a subscription. The email used urgent language, a suspicious sender, and a malicious link to pressure me into clicking.

---

## Email Details
- **Theme:** Account storage / account blocked scam
- **Subject:** We've blocked your account! Your photos and videos will be deleted...
- **Sender:** `noreply@apipdpjtujt.us`
- **Type:** Real-world phishing email sample

---

## Investigation Process

### 1. Manual Email Review
<img width="1555" height="702" alt="Screenshot 2026-04-09 154201" src="https://github.com/user-attachments/assets/530e3247-5ece-4fd0-8601-0892963e51fc" />


The email was reviewed for visible phishing indicators such as:
- suspicious sender domain
- urgent and fear-based language
- deceptive call-to-action
- suspicious link behavior
- unusual routing information

### 2. Link Inspection
<img width="1919" height="907" alt="Screenshot 2026-04-09 154327" src="https://github.com/user-attachments/assets/1dce520b-d3b0-4ec1-8540-4f8857ee9377" />

The embedded link was hovered over and inspected without clicking. The link preview showed a suspicious destination URL unrelated to a legitimate cloud storage provider.

### 3. URL Validation
<img width="1886" height="921" alt="Screenshot 2026-04-09 154549" src="https://github.com/user-attachments/assets/35dc6c15-746e-47be-ab27-fbed895891ef" />

The suspicious URL was submitted to VirusTotal for reputation analysis.

### 4. Header Review
<img width="1847" height="532" alt="Screenshot 2026-04-09 170735" src="https://github.com/user-attachments/assets/22bc6c51-fab1-4e8d-b135-4a79ad20d9c9" />

Header details were reviewed to examine sender information and email authentication results, including SPF and DMARC.

---

## Key Findings

### Indicators of Compromise Identified
- Suspicious sender domain not associated with a legitimate service provider.
- Urgent social engineering language.
- Deceptive message claiming account deletion unless action was taken.
- Malicious URL embedded in the email.
- Multiple clickable areas redirecting to the same suspicious destination with HTML link.
- DMARC failure indicating possible domain spoofing.

### Threat Validation
- **URLs analyzed:** 1
- **VirusTotal result:** 5/95 vendors flagged the URL as malicious/phishing
- **Header observation:** DMARC failed despite SPF passing

### Interpretation
Although SPF passed, the DMARC failure indicates the sender could not be properly authenticated, which is a strong sign of spoofing or impersonation. Combined with the malicious URL, urgent wording, and suspicious domain, the email was assessed as a phishing attempt.



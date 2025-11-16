# cyber-security-assignment_2
Phishing Email Analysis Report :

Task 2: Analyze a Phishing Email Sample
Cyber Security Internship
📋 Table of Contents
Objective
Tools Used
Email Overview
Analysis Process
Phishing Indicators Found
Header Analysis Results
Conclusion
Screenshots
Key Learnings
🎯 Objective
To identify and analyze phishing characteristics in a suspicious email sample claiming to be from Microsoft
account team regarding unusual sign-in activity.
🛠 Tools Used
1. Google Admin Toolbox Messageheader - For comprehensive email header analysis
2. MXToolbox Email Header Analyzer - For SPF, DKIM, DMARC verification
3. Text Editor - For extracting and examining raw email headers
4. Manual Analysis - For identifying social engineering tactics
📧 Email Overview
Subject: Microsoft account unusual signin activity
From: Microsoft account team no-reply@access-accsecurity.com
Reply-To: solutionteamrecognizd03@gmail.com
Date: Wed, 2 Aug 2023 03:34:32 +0000
Claimed Issue: Unusual sign-in from Russia/Moscow
🔍Analysis Process
Step 1: Email Header Extraction
Extracted complete email headers from the .eml file including:
Sender information
Authentication results
Routing information
IP addresses
Step 2: Header Analysis
Used online tools to analyze:
SPF (Sender Policy Framework) records
DKIM (DomainKeys Identified Mail) signatures
DMARC (Domain-based Message Authentication) policies
Email routing path
Step 3: Content Analysis
Examined email body for:
Suspicious links
Social engineering tactics
Grammar/spelling errors
Urgency indicators
Step 4: Domain Verification
Checked legitimacy of:
Sender domain (access-accsecurity.com)
Reply-to address domain
Return-path domain (iustozncau.co.uk)
🚩 Phishing Indicators Found
1. Email Spoofing - CRITICAL
 
Element Value Issue
From Address no-reply@access-accsecurity.com Fake domain (not microsoft.com)
Reply-To solutionteamrecognizd03@gmail.com Generic Gmail account
Return-Path bounce@iustozncau.co.uk Completely different domain
Analysis: Three different domains used - clear sign of email spoofing. Legitimate Microsoft emails would use
@microsoft.com or @account.microsoft.com domains.
2. Authentication Failures
✗ SPF: None/Failed - Domain doesn't authorize this sender
✗ DKIM: Not signed - Email not cryptographically signed
✗ DMARC: permerror - Domain authentication policy error
Impact: Email failed all major authentication checks, indicating it's not from legitimate source.
3. Suspicious Sender IPAddress
IP: 89.144.9.91
Expected: Microsoft's IP ranges (typically Azure/Office 365 infrastructure)
Actual: Non-Microsoft IP address
4. Malicious Links
All links in the email redirect to:
Links disguised as Microsoft security actions
"Report The User" button sends email to attacker's Gmail
No legitimate Microsoft security portal links
5. Tracking Pixel
Hidden tracking image:
Used to track if email was opened.
6. Social Engineering Tactics
mailto:solutionteamrecognizd03@gmail.com
http://thebandalisty.com/track/o40000GbeUR18708448ECDL1821750Mhi33740nqxV176
 
Tactic Implementation
Urgency "Unusual sign-in activity" creates immediate concern
Fear Claims someone from Russia accessed the account
Authority Impersonates Microsoft, a trusted entity
Call-to-Action "Report The User" button pressures quick response
Priority Flag Marked as "High" importance to stand out
7. Content Red Flags
Generic greeting (no personalized name)
Suspicious sign-in details (Russia/Moscow)
Fake IP address presented as evidence
Grammar issue: "sign.in" instead of "sign-in"
Unprofessional email structure
8. Domain Inconsistencies
Claimed sender: Microsoft
Actual domains used:
access-accsecurity.com (typosquatting attempt)
iustozncau.co.uk (random unrelated domain)
Gmail (free email service, not corporate)
📊 Header Analysis Results
Authentication Summary
Spam Score
X-Microsoft-Antispam-Mailbox-Delivery: Multiple spam indicators detected
X-MS-Exchange-Organization-SCL: 5 (Medium-High spam confidence level)
X-Microsoft-Antispam: BCL:6 (Bulk Complaint Level indicates spam)
Authentication-Results:
 spf=none (sender IP is 89.144.9.91) smtp.mailfrom=iustozncau.co.uk
 dkim=none (message not signed) header.d=none
 dmarc=permerror action=none header.from=access-accsecurity.com
Email Route
Email traveled through suspicious routing:
1. Originated from iustozncau.co.uk (89.144.9.91)
2. Passed through Outlook protection systems
3. Flagged but delivered to inbox
✅ Conclusion
Verdict: CONFIRMED PHISHING EMAIL
This email is definitively a phishing attempt based on:
1. Failed authentication (SPF, DKIM, DMARC all failed)
2. Multiple domain mismatches (3 different domains used)
3. Suspicious sender IP (not Microsoft infrastructure)
4. Fake Microsoft branding with typosquatting domain
5. Social engineering tactics designed to create urgency
6. Malicious links redirecting to attacker's email
7. No legitimate Microsoft security portal links
Threat Level: HIGH
Recommended Actions:
✗ DO NOT click any links in the email
✗ DO NOT reply to the email
✗ DO NOT provide any personal information
✓ DELETE the email immediately
✓ REPORT to IT/Security team if received at work
✓ MARK as spam/phishing in email client
✓ VERIFY actual account security by logging in directly (not via email links)
📸 Screenshots
The following screenshots are included in this repository:
1. Google Admin Toolbox Analysis - Shows complete header analysis with authentication results
2. MXToolbox Header Analysis - Displays SPF/DKIM/DMARC verification failures
3. Raw Email Headers - Complete header information extracted from .eml file
4. Email Body Content - Visual representation of the phishing email with highlighted red flags
All screenshots are compiled in the analysis_screenshots.pdf file.
📚 Key Learnings
What is Phishing?
Phishing is a cybersecurity attack where attackers impersonate legitimate organizations to trick victims into
revealing sensitive information or clicking malicious links.
How to Identify Phishing Emails:
1. Check sender's email address for suspicious domains
2. Verify authentication (SPF, DKIM, DMARC)
3. Look for grammar/spelling errors
4. Examine links before clicking (hover to preview)
5. Be suspicious of urgent or threatening language
6. Verify unexpected requests through official channels
Email Spoofing:
Technique where attackers forge the "From" field to make emails appear from legitimate sources. Prevented by
proper SPF/DKIM/DMARC implementation.
Social Engineering in Phishing:
Attackers exploit human psychology using:
Urgency: Creating time pressure
Authority: Impersonating trusted entities
Fear: Threatening account compromise
Curiosity: Promising interesting information
Tools for Email Header Analysis:
Google Admin Toolbox Messageheader
MXToolbox Email Header Analyzer
MailHeader.org
WhatIsMyIPAddress Email Header Analyzer

🔐 Security Best Practices
1. Always verify sender authenticity through official channels
2. Never click links in suspicious emails
3. Enable multi-factor authentication (MFA)
4. Check URLs before clicking (look for HTTPS and correct domain)
5. Report phishing attempts to security teams
6. Keep email client and security software updated
7. Be skeptical of urgent requests for personal information
📂 Repository Contents
👨‍💻Author
[NITHISH RAM]
Cyber Security Internship - Task 2
Date: [16-11-2025]
📖 References
CISA Phishing Guidance
Microsoft Anti-Phishing
SPF, DKIM, DMARC Explained

⚠️ Disclaimer: This analysis is for educational purposes only. The email sample analyzed is a known phishing
attempt and should not be interacted with.
phishing-email-analysis/
│
├── README.md # This file
├── analysis_screenshots.pdf # Screenshots from Google Admin Toolbox & MXToolbox
├── email_sample/
│ └── 55555555.txt # Original phishing email with headers
└── findings/
 └── phishing_indicators.txt # Detailed list of all red flags found

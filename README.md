# Digital Forensic Investigation — Insider Data Leak Case

## Overview
Full digital forensic investigation of a real forensic dataset 
(nps-2008-jean.E01, the publicly available M57-Jean training case) to 
determine whether a confidential company spreadsheet was leaked 
accidentally, intentionally, or as the result of external compromise.

## Case Background
A confidential spreadsheet containing employee salary and SSN data was 
discovered leaked online. The file was believed to exist only on one 
employee's laptop. The investigation determined the actual cause of 
the leak using forensic evidence rather than assumption.

## Tools Used
FTK Imager · Windows Registry Analysis · Prefetch Analysis · Browser 
Forensics · Outlook OST Analysis

## Investigation Process
1. **Image Verification** — Loaded the forensic image and verified 
   integrity via MD5/SHA1 hash comparison, confirming zero bad blocks 
   and an unaltered evidence chain
2. **File System Analysis** — Explored the NTFS file system and located 
   the confidential spreadsheet within the user profile
3. **Metadata Analysis** — Examined MAC timestamps and Prefetch 
   execution artifacts to establish a precise activity timeline
4. **Registry Analysis** — Reviewed Windows Registry hives (SAM, 
   SECURITY, SYSTEM, SOFTWARE) for evidence of external device use
5. **Browser Forensics** — Analysed history, cookies, and temporary 
   internet files for relevant account and communication activity
6. **Deleted File Investigation** — Examined Recycle Bin/INFO2 
   artifacts for evidence of anti-forensic activity
7. **Timeline Reconstruction** — Correlated all artifacts into a single 
   chronological timeline of events
8. **Email Forensics** — Analysed the Outlook OST file, uncovering the 
   root cause of the leak

## Key Finding
The confidential spreadsheet was leaked as the direct result of a 
targeted spear-phishing email impersonating an internal contact — not 
through malware, external hacking, or intentional insider action. The 
investigation concluded the user was deceived rather than at fault.

## Full Report
See [full report](./report/data-leak-forensic-ivestigation.pdf) 
for complete findings, evidence screenshots, and the investigation timeline.

## Skills Demonstrated
Disk Forensics · Evidence Integrity Verification · Registry Analysis · 
Timeline Reconstruction · Email/Phishing Forensics · 
Evidence-Based Conclusion Writing

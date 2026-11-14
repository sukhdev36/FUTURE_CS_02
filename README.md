# FUTURE_CS_02: Phishing Email Detection & Awareness Report

**Future Interns | Cyber Security Internship | Task 2**

**Author:** Sukh Ram Godara

**Date of analysis:** 13 November 2026

## Overview

This repository contains a phishing detection and awareness report based on 12 sample emails. Each email was checked for phishing indicators, classified as **Safe**, **Suspicious** or **Phishing**, and explained in simple language. The report also gives prevention and awareness guidelines for users and organisations.

**Final report:** [`report/Phishing_Detection_Awareness_Report.pdf`](report/Phishing_Detection_Awareness_Report.pdf)

## Samples Analysed

| Method | Count | Source |
|---|---|---|
| Content analysis | 10 emails | Nazario phishing corpus, Kaggle phishing email dataset, SpamAssassin corpus |
| Header and authentication analysis | 2 emails | phishing_pot public email collection |

All samples come from public research datasets. Names, addresses and phone numbers from the original emails were removed, and domains are written in defanged form (for example `example[.]com`).

## Classification Method

| Class | Meaning |
|---|---|
| Phishing | Clearly tries to trick the reader into giving credentials, money or access, or into running malware |
| Suspicious | Has warning signs but no clear attempt to steal credentials or run malware; needs checking |
| Safe | Looks like normal communication, with no pressure or request for sensitive information |

Checklist used for each email: sender and domain, greeting, pressure or urgency, what is requested (password, payment, attachment, phone call), links and attachments (described only, never opened), and email headers where available (From, Return-Path, Message-ID, SPF, DKIM, DMARC).

## Summary of Results

| Result | Count |
|---|---|
| Phishing | 7 |
| Suspicious | 2 |
| Safe | 3 |
| **Total** | **12** |

**Key findings**
- Most phishing samples pretended to be a known brand (retailer, courier, bank or mail system).
- Common tactics were urgency, fear of losing access, surprise purchases and free prizes.
- The goals were stealing passwords, getting an attachment opened, or getting the victim to call a number.
- In both header samples SPF failed and the sender used a random free domain. DKIM passed, but its signing domain did not match the sender, so it did not prove who sent the email.

Per-email notes are in [`emails/`](emails/) and header notes are in [`headers/`](headers/).

## Tools Used

- Kali Linux (virtual machine)
- Terminal tools (`sed`, `grep`) and Python (`pandas`) to read the datasets
- Public datasets: Nazario phishing corpus, Kaggle phishing email dataset, SpamAssassin corpus, phishing_pot
- Canva for report design

## Repository Structure

```
FUTURE_CS_02/
├── README.md
├── report/
│   └── Phishing_Detection_Awareness_Report.pdf
├── emails/
│   ├── README.md
│   └── email-01.md ... email-10.md
└── headers/
    ├── H-01-sample-5-header-analysis.md
    ├── H-02-sample-6-header-analysis.md
    ├── H-01-sample5-auth.png
    └── H-02-sample6-auth.png
```

## Limitations

- The 10 content samples came from datasets without full headers, so SPF, DKIM and DMARC could not be checked for them.
- The Kaggle text is preprocessed (lowercase, punctuation removed, some words dropped), so wording was judged by meaning only.
- The sample size is small, and classifications are the author's judgement based on the available evidence.

## Ethics Statement

All analysis was done inside a virtual machine, with emails read as plain text only. No link was opened, no attachment was run, and no sender was contacted.

## Disclaimer

This work was done for learning purposes as part of the Future Interns Cyber Security internship. The samples come from public research datasets and do not represent any real organisation or individual.

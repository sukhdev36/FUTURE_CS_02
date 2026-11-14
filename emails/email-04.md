# Email E-04

- **Source:** Nazario phishing corpus, row 1086
- **Subject:** [recipient address] Messages could not be delivered.
- **Classification:** Phishing
- **Type:** Credential harvesting (fake email quarantine notice)

## Indicators

- The display name shows the recipient's own domain, but the real sender address belongs to an unrelated ISP domain (kabel-deutschland[.]de). This is a sender mismatch.
- It shows a fake quarantine summary with tempting subjects (a bank transfer, an invoice copy, a courier shipment).
- It includes "Release" and "Deliver all messages" actions that would lead to a fake login page.
- It asks the reader to move the message to the inbox if it landed in spam, which tries to get around spam filtering.
- It creates urgency by saying quarantined messages will be removed after 7 days.

## Why this classification

Fake IT or mail-system notices are a common way to steal email passwords. The mismatched sender, bait subjects and urgency are typical.

## Recommended action

Do not click Release or any link. Check the real mail quarantine by logging in through the official mail portal. Report the email to the IT or security team.

---
*Names, addresses and phone numbers from the original email were removed or replaced. Domains are written in defanged form.*

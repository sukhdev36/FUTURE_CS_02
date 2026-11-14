# Email E-01

- **Source:** Nazario phishing corpus, row 1267
- **Subject:** Your Order of MacBook Air with Order ID# [removed]
- **Classification:** Phishing
- **Type:** Callback phishing (fake order confirmation with a phone number)

## Indicators

- The sender domain, amazn-usshipping2[.]co, imitates a well-known retailer: the brand name is misspelled, an extra word is added, and the .co extension is used.
- The greeting names a person who does not match the recipient, which points to a bulk template.
- It confirms an unexpected order of about $780 that the recipient never placed, which is meant to cause worry.
- The body contains no link, only a customer help-desk phone number. The goal is to make the victim call, so the scammer can ask for payment details or remote access.
- The message says it comes from a notification-only address, which discourages replying by email.

## Why this classification

The email creates panic with a surprise purchase and moves the victim away from email to a phone call, where the scammer controls the conversation. The lookalike sender domain and mismatched greeting confirm it is not a genuine order confirmation.

## Recommended action

Do not call the number. Check recent orders by opening the retailer's official website or app directly. Delete the email and report it as phishing.

---
*Names, addresses and phone numbers from the original email were removed or replaced. Domains are written in defanged form.*

# Email E-10

- **Source:** SpamAssassin corpus, row 5002
- **Subject:** (empty subject)
- **Classification:** Suspicious
- **Type:** Unsolicited business offer

## Indicators

- The greeting is generic ("Dear Sirs") and does not name the recipient's company.
- The subject line is empty.
- It is a cold message from an unknown overseas company offering to supply products.
- The wording looks like a template sent to many businesses.
- The sender's domain (a .cn regional domain) cannot be matched to the company name given in the email.

## Why this classification

There is no link or login request, and real suppliers also send cold emails, so it is not clearly phishing. It can still be the first step of advance-payment or fake-supplier fraud.

## Recommended action

Verify the company independently (website, phone, reviews). Never send an advance payment based on an unsolicited email.

---
*Names, addresses and phone numbers from the original email were removed or replaced. Domains are written in defanged form.*

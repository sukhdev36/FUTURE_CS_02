# Sample Emails: Content Analysis

| ID | Source | Classification | Type |
|---|---|---|---|
| [E-01](email-01.md) | Nazario phishing corpus, row 1267 | Phishing | Callback phishing (fake order confirmation with a phone number) |
| [E-02](email-02.md) | Nazario phishing corpus, row 894 | Phishing | Credential harvesting (fake document login) |
| [E-03](email-03.md) | Nazario phishing corpus, row 270 | Phishing | Malicious attachment lure (fake courier notice) |
| [E-04](email-04.md) | Nazario phishing corpus, row 1086 | Phishing | Credential harvesting (fake email quarantine notice) |
| [E-05](email-05.md) | Kaggle phishing email dataset (phishing_email.csv), row 80949 | Phishing | Brand impersonation and credential harvesting |
| [E-06](email-06.md) | Kaggle phishing email dataset (phishing_email.csv), row 42327 | Safe | Legitimate marketing email |
| [E-07](email-07.md) | Kaggle phishing email dataset (phishing_email.csv), row 11429 | Safe | Normal business email |
| [E-08](email-08.md) | Kaggle phishing email dataset (phishing_email.csv), row 22330 | Safe | Normal business email |
| [E-09](email-09.md) | SpamAssassin corpus, row 5454 | Suspicious | Unsolicited bulk promotion |
| [E-10](email-10.md) | SpamAssassin corpus, row 5002 | Suspicious | Unsolicited business offer |

**Total:** 5 Phishing, 2 Suspicious, 3 Safe.

The Nazario, Kaggle and SpamAssassin datasets are public research datasets. Kaggle text is preprocessed, and the datasets do not include full headers, so SPF, DKIM and DMARC could not be checked for these samples. Header analysis is in the `headers/` folder.

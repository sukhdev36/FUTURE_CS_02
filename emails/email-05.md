# Email E-05

- **Source:** Kaggle phishing email dataset (phishing_email.csv), row 80949
- **Subject:** Not available (dataset stores combined text only)
- **Classification:** Phishing
- **Type:** Brand impersonation and credential harvesting

## Indicators

- It impersonates a bank and claims a "worldwide internet upgrade" that may block access, a pretext real banks do not use.
- It sets a deadline and calls the message a "final reminder", which creates pressure.
- It tells the reader to log in to "update the account", which would send them to a login page.
- The greeting is generic ("Dear valued member").
- The template is sloppy: style (CSS) code appears in the text and the whole message is repeated twice.
- It gives a toll-free number to call for "technical support", a possible callback scam.

## Why this classification

The message frightens the reader with loss of account access and pushes them to log in or call a number. Visible template code and repetition show it was mass-produced. Note: the dataset text is preprocessed (lowercase, no punctuation, some words removed), so wording was judged by content only.

## Recommended action

Do not log in through the email or call the number. Open the bank's official website or app by typing the address yourself. Report the message to the bank.

---
*Names, addresses and phone numbers from the original email were removed or replaced. Domains are written in defanged form.*

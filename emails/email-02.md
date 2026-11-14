# Email E-02

- **Source:** Nazario phishing corpus, row 894
- **Subject:** Re: Quote
- **Classification:** Phishing
- **Type:** Credential harvesting (fake document login)

## Indicators

- The subject starts with "Re:" although there was no earlier conversation, which suggests a fake reply.
- The greeting is "Dear ," with the name missing, so the template was never filled in.
- It offers a large business quotation (about USD 101,810), which tempts the reader to open it.
- The message includes a fake "Adobe PDF Document" sign-in form that asks for the recipient's email address and password to view the document.
- It mixes a foreign-language disclaimer with a line saying it was scanned for viruses and is believed to be clean, which is false reassurance.

## Why this classification

A real document does not require typing an email password into a form inside the message. The purpose is to steal login details.

## Recommended action

Do not enter any credentials. Verify the quotation with the sender through a known phone number or contact. Report and delete the email.

---
*Names, addresses and phone numbers from the original email were removed or replaced. Domains are written in defanged form.*

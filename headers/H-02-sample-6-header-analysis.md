# Header Analysis H-02: sample-6

- **Source:** phishing_pot public phishing email collection, file `sample-6.eml`
- **Method:** Only the headers were read in the terminal (`sed` and `grep`). The body was not opened and no link was clicked.
- **Classification:** Phishing (scam lure)

## Key headers

| Header | Observed value | Observation |
|---|---|---|
| From | Display name "free spin", address `[name]@bnvftbfantay[.]onmicrosoft[.]com` | The display name looks like a brand, but the address is a random-looking free Microsoft (onmicrosoft) domain, not an official brand domain. |
| Return-Path | Same address as From | No mismatch here, but this alone does not make the message safe. |
| Subject | 100 Balls. $5 No Deposit Required ! | Offers a $5 no-deposit gambling offer to tempt the reader to click. |
| Message-ID | Ends with `@mail.gmail.com` | The message appears to have been sent through Gmail, although the From domain is a Microsoft domain. |

## Authentication results

| Check | Result | Meaning |
|---|---|---|
| SPF | **fail** (sender IP 74.125.224.52) | The domain `bnvftbfantay[.]onmicrosoft[.]com` does not list this IP as an allowed sender. |
| DKIM | **pass**, signing domain `bnvftbfantay-onmicrosoft-com.20251104.gappssmtp[.]com` | The signature is valid, but the signing domain is different from the From domain, so it is not aligned and does not prove who sent the message. |
| DMARC | **none** (action = none) | No enforcing policy was applied, so the failed SPF check did not cause the message to be blocked. |

## Conclusion

SPF failed, the From domain is random and not a brand domain, the signing domain does not match, and no strict DMARC policy was in place. Together with the offer lure, this indicates a phishing or scam email.

## Notes

- A DKIM "pass" alone is not proof that a message is genuine. Alignment between the signing domain and the From domain must also be checked.
- The sender IP appears to be in a Google mail server range and the signing domain looks like a Google mail signing domain (not verified further here). This does not mean Google sent the scam; any Gmail account can be used to send messages.
- Sender names were removed. Domains are defanged.
- Evidence: `H-02-sample6-auth.png`

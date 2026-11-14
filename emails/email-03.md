# Email E-03

- **Source:** Nazario phishing corpus, row 270
- **Subject:** Your Parcel Has Arrived
- **Classification:** Phishing
- **Type:** Malicious attachment lure (fake courier notice)

## Indicators

- The greeting is generic ("Dear Customer").
- The story is that the courier could not deliver because of incorrect delivery details, a common parcel scam pretext.
- It asks the reader to download an attached receipt and forward it to the nearest courier office, which a real courier would not ask.
- It pushes the reader to download the attachment, which may carry malware.
- The sender address appears to belong to the courier company, but display names and addresses can be spoofed. The dataset has no headers, so SPF and DKIM could not be checked.

## Why this classification

The message uses a delivery problem to make the reader open an attachment. Unusual instructions and the generic greeting show it is not a real courier notice.

## Recommended action

Do not download or open the attachment. Check parcel status on the courier's official website using a tracking number you already have.

---
*Names, addresses and phone numbers from the original email were removed or replaced. Domains are written in defanged form.*

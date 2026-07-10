# Evidence

## Collected Evidence

- Sender: **finance-payments@vendor-payments.com**
- Subject: **Updated July Invoice**
- Attachment: **July_Invoice.xlsm**
- User opened the attachment.
- User clicked **Enable Content**.
- Computer became noticeably slow.
- Endpoint monitoring showed Excel launching **PowerShell**.
- PowerShell executed an encoded command.
- **invoice.exe** was created in the temporary directory.
- The executable established outbound HTTPS connections.
- CPU usage increased to **95%**.
- SOC detected unusually high outbound network traffic.

---

## Unknowns

- Is the sender domain legitimate or spoofed?
- Does the attachment contain a malicious macro?
- What actions did the encoded PowerShell command perform?
- What is the reputation of the destination IP addresses?
- Did other employees receive the same email?
- Was any sensitive data accessed or exfiltrated?
- Has the malware established persistence on the system?
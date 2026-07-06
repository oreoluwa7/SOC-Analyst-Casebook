# Case 001 - Suspicious Microsoft Login Email

## Scenario

An employee named Sarah reported receiving an email claiming that someone had logged into her Microsoft account. She clicked the **Verify Account** button but closed the webpage without entering her password.

---

## Evidence

- The sender email address was `account-security@micr0soft-login-support.com`.
- The email subject was **"Action Required: Unusual Sign-in Activity Detected."**
- Microsoft 365 logs show the email was received at **08:41 AM**.
- Sarah clicked the **Verify Account** button at **08:43 AM**.
- Sarah closed the webpage without entering her Microsoft account credentials.
- Microsoft 365 authentication logs showed no successful login after the link was clicked.
- Sarah reported that the webpage appeared suspicious.
- Sarah reported the incident to the SOC at **08:50 AM**.

---

## Observations

- The sender's email address appears to imitate Microsoft's legitimate domain.
- The email uses an urgent subject line to encourage the user to act quickly.
- Sarah recognized that something was unusual and closed the webpage before entering her credentials.
- Microsoft 365 authentication logs show no successful sign-in after the link was clicked.

---

## Unknowns

- It is unknown whether the embedded link is malicious.
- It is unknown whether other employees received the same email.
- It is unknown whether the webpage attempted to download malware or perform other malicious actions.
- It is unknown whether the sender's domain was recently registered.
- It is unknown whether any other employees clicked the link or entered their credentials.
- It is unknown whether Sarah was specifically targeted.

---

## Initial Assessment

Based on the available evidence, this incident is assessed with **medium confidence** to be a phishing attempt. There is currently no evidence of a successful account compromise, as no credentials were entered and Microsoft 365 authentication logs show no successful sign-in after the link was clicked. However, additional investigation is required to determine whether the embedded link hosted phishing content or malware and whether other employees were targeted or affected.

---

## Recommended Next Steps

- Review the email headers to verify the SPF, DKIM, and DMARC authentication results.
- Analyze the embedded URL and sender domain using VirusTotal and other reputation tools.
- Review Sarah's account activity and endpoint for signs of compromise.
- Determine whether other employees received or interacted with the same email.
- If the email is confirmed malicious, block the sender's domain and remove the email from users' mailboxes.
- Continue monitoring Sarah's account for unusual sign-in activity.

---

## Skills Practiced

- Phishing investigation
- Evidence collection
- Incident documentation
- Analytical thinking
- Initial incident assessment

## Reflection

This was my first SOC investigation. I learned the importance of separating evidence, observations, unknowns, and assessments. I also learned that the absence of suspicious logins does not necessarily mean credentials were not compromised.
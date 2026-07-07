## Scenario

An employee named Sarah reported receiving an email claiming that someone had logged into her Microsoft account. She clicked the **Verify Account** button but closed the webpage without entering her password.

## Observations

- The sender's email address appears to imitate Microsoft's legitimate domain.
- The email uses an urgent subject line to encourage the user to act quickly.
- Sarah recognized that something was unusual and closed the webpage before entering her credentials.
- Microsoft 365 authentication logs show no successful sign-in after the link was clicked.

## Initial Assessment

Based on the available evidence, this incident is assessed with **medium confidence** to be a phishing attempt. There is currently no evidence of a successful account compromise, as no credentials were entered and Microsoft 365 authentication logs show no successful sign-in after the link was clicked. However, additional investigation is required to determine whether the embedded link hosted phishing content or malware and whether other employees were targeted or affected.

## Recommended Next Steps

- Review the email headers to verify the SPF, DKIM, and DMARC authentication results.
- Analyze the embedded URL and sender domain using VirusTotal and other reputation tools.
- Review Sarah's account activity and endpoint for signs of compromise.
- Determine whether other employees received or interacted with the same email.
- If the email is confirmed malicious, block the sender's domain and remove the email from users' mailboxes.
- Continue monitoring Sarah's account for unusual sign-in activity.

## Skills Practiced

- Phishing investigation
- Evidence collection
- Incident documentation
- Analytical thinking
- Initial incident assessment


## Reflection

This was my first SOC investigation. I learned the importance of separating evidence, observations, unknowns, and assessments. I also learned that the absence of suspicious logins does not necessarily mean credentials were not compromised.
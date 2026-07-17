# Incident Report

## Scenario

An employee reported that Outlook prompted them to sign in again when they arrived at work, despite not remembering signing out the previous day. Authentication logs and Microsoft 365 audit logs were reviewed to determine whether the account had been compromised.

## Observations

- Two failed login attempts originated from a Moscow IP address associated with password spraying campaigns.
- The failed login attempts were followed by successful logins from Mary's normal location in Lagos.
- Multi-factor authentication (MFA) was enabled on the account.
- No password reset, password change, or unfamiliar registered devices were observed.
- A mailbox rule named **"Move invoices to Archive"** was created shortly after the authentication activity.

## Assessment

The authentication logs indicate that Mary's account was targeted by a password spraying attempt from a known malicious IP address. However, there is no evidence that the attacker successfully authenticated.

The creation of the mailbox rule shortly after the login attempts is unusual and warrants further investigation. Based on the available evidence, it cannot be confirmed whether the rule was created legitimately by the user or as a result of unauthorized activity.

**Confidence Level:** Medium

## Recommended Actions

1. Verify with Mary whether she intentionally created the mailbox rule.
2. Review mailbox rules for any unauthorized or suspicious configurations.
3. Examine additional authentication logs to determine whether any successful logins occurred outside the provided time window.
4. Continue monitoring the account for suspicious sign-in activity.
5. Search for similar password spraying attempts targeting other users.
6. Ensure MFA remains enabled and educate users about password spraying attacks.

## Skills Practiced

- Authentication log analysis
- Microsoft 365 audit log analysis
- Evidence-based reasoning
- Threat intelligence correlation
- Incident documentation

## Reflection

This investigation demonstrated that suspicious activity does not always indicate a confirmed compromise. I learned the importance of distinguishing between observed evidence and assumptions, especially when available logs are incomplete. Rather than forcing a conclusion, I documented what was known, identified the remaining unknowns, and recommended additional investigative steps.
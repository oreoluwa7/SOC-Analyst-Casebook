# Case 006 - Impossible Travel Login

## Scenario

David reported receiving a Microsoft 365 notification indicating a successful login from Brazil. Five minutes later, he successfully accessed his account from Lagos and contacted the Help Desk because he did not recognize the Brazil login.

---

## Observations

- The login from Brazil originated from a previously unseen IP address.
- Multi-factor authentication (MFA) was enabled on the account.
- No password changes or password reset events were recorded.
- No mailbox rules were created.
- No unfamiliar devices were registered to the account.
- The user reported that they have never traveled to Brazil.

---

## Unknowns

- It is unknown whether the Brazil login was authorized.
- It is unknown whether the user approved an MFA prompt at the time of the Brazil login.
- It is unknown whether the user was connected through a VPN or another service that could explain the Brazil IP address.
- It is unknown whether the IP geolocation is accurate.
- It is unknown whether additional suspicious activity occurred after the reported login.

---

## Assessment

**Confidence Level:** Medium

The successful login from a previously unseen IP address in Brazil is suspicious, particularly because the user reported never traveling to Brazil. However, the available evidence is insufficient to confirm account compromise. MFA was enabled, there were no password changes, no mailbox rules were created, and no unfamiliar devices were registered.

Additional investigation is required to determine whether the Brazil login resulted from unauthorized access, a legitimate VPN connection, inaccurate IP geolocation, or another explanation.

---

## Recommended Actions

- Review detailed authentication logs, including the authentication method and MFA events.
- Verify with the user whether they approved any MFA prompts around the time of the Brazil login.
- Determine whether the user was connected to a VPN or another service that could explain the Brazil IP address.
- Review Microsoft Entra ID sign-in risk information for the authentication events.
- Continue monitoring the account for additional suspicious sign-in activity.
- Reset credentials and revoke active sessions if subsequent investigation confirms unauthorized access.

---

## Skills Practiced

- Authentication log analysis
- Identity investigation
- Hypothesis-driven investigation
- Impossible travel detection
- Evidence-based assessment
- Incident documentation

---

## Reflection

This case taught me that not every security alert leads to a clear conclusion. I learned to avoid making assumptions and instead develop multiple hypotheses supported by evidence. I also learned that identifying suspicious activity is only the beginning of an investigation; additional evidence is often required before confirming account compromise.
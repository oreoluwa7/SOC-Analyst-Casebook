# Incident Report

## Incident Summary

There were multiple failed login attempts from John's home network, followed by a successful login from a previously unseen IP address in Romania. The password was changed within one minute of the successful login, indicating that the account was likely compromised by an unauthorized party. The activity is consistent with the use of stolen credentials.

## Analysis and Findings

- The successful login originated from a previously unseen IP address in Romania.
- The password was changed immediately after the successful authentication.
- The user reported not logging in and was unable to access the account.
- The sequence of events indicates likely unauthorized access.
- The activity is consistent with account compromise using previously obtained credentials.

## Assessment

This case is likely a case of stolen credentials.

**Confidence Level:** High

## Recommended Actions

1. Terminate all active sessions.
2. Force a password reset for John's account.
3. Enable or enforce Multi-Factor Authentication (MFA).
4. Investigate recent account activity for unauthorized actions.
5. Notify the user and advise against reusing the compromised password.
6. Review the Romanian IP address and block it if organizational policy permits.
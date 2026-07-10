# Incident Report

## Scenario

David from the Finance department reported to the Security Operations Center (SOC) that after opening a macro-enabled Excel attachment and clicking **Enable Content**, his computer became noticeably slow and started freezing intermittently. Shortly afterward, the SOC monitoring system generated an alert indicating unusually high outbound network connections originating from David's workstation.

## Observations

- David received an email from **finance-payments@vendor-payments.com**.
- The email contained a macro-enabled Excel attachment named **July_Invoice.xlsm**, which David opened.
- David clicked the **Enable Content** button when prompted by Microsoft Excel.
- Shortly after enabling the document, David reported that his computer became noticeably slow and frequently froze.
- The SOC detected unusually high outbound network connections from David's workstation at **10:23 AM**.
- Endpoint monitoring showed that Microsoft Excel launched **PowerShell**, which executed an encoded command.
- PowerShell created an executable file named **invoice.exe** in the temporary directory.
- The executable initiated outbound HTTPS connections.
- CPU usage increased to **95%** shortly after the executable began running.

## Assessment

**Confidence Level:** High

The evidence strongly suggests that the macro-enabled Excel attachment executed malicious code after David enabled content. The attack chain—including Excel launching PowerShell, execution of an encoded command, creation of an executable in the temporary directory, and suspicious outbound network activity—indicates a likely malware compromise requiring immediate containment and further investigation.

## Recommendations

1. Immediately isolate David's workstation from the network.
2. Verify the legitimacy of the sender's domain using threat intelligence sources and email authentication checks (SPF, DKIM, and DMARC).
3. Analyze the PowerShell command and the dropped executable (`invoice.exe`).
4. Review endpoint, PowerShell, and security logs to reconstruct the complete attack timeline.
5. Determine whether other employees received or interacted with the same email.
6. Block any confirmed malicious IP addresses or domains at the firewall.
7. Perform a full antivirus/EDR scan and continue monitoring the endpoint.

## Skills Practiced

- Email investigation
- Endpoint analysis
- Timeline reconstruction
- Hypothesis development
- Incident assessment
- Containment decision-making

## Reflection

This case taught me that Microsoft Office documents can contain macros capable of executing code after a user enables content. I also learned how an attack chain is built by connecting multiple pieces of evidence instead of relying on a single indicator. Finally, I improved my understanding of how to make investigation and containment decisions based on the available evidence.
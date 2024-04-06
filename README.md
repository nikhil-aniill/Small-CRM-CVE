# CVE-2024-xxxx
# Vulnerability Description

The Registration page on Small CRM v3.0 is vulnerable to SQL injection, allowing unauthorized remote code execution (RCE). This vulnerability arises from inadequate input validation in the email input field, coupled with the absence of parameterized queries.

## Step by Step POC

1. Navigate to the registration page.
2. Fill out all the fields and intercept the request.
3. Send the intercepted request to the repeater and drop it.
4. Inject a SQL injection payload into the email field, observing its execution.
5. Modify the payload to create a webshell on the server and utilize it to generate the file.
6. Access the URL associated with the generated file, triggering its execution.

## Impact

The described vulnerability and proof of concept (PoC) pose severe risks, including unauthorized access, remote code execution (RCE), system compromise.

## Remediation

Implement strict input validation, use parameterized queries, provide security training.

## Screenshots (Placeholders)
![Affected Code](code.png)
![Intercepted Request](reg_req.png)
![Payload Execution](sqli_payload.png)
![RCE](rce.png)

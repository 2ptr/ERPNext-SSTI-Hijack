# ERPNext Account Hijack and SSTI to RCE
ERPNext has a SQL injection vulnerability that allows for account takeover due to information disclosure. Authenticated users may create a malicious email template and escape the Jinja templating engine to achieve remote code execution.

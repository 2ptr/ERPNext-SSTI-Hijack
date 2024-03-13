# ERPNext Account Hijack and SSTI to RCE
ERPNext has a SQL injection vulnerability that allows for account takeover due to information disclosure. Authenticated users may create a malicious email template and escape the Jinja templating engine to achieve remote code execution.

## Troubleshooting
The script assumes ERPNext is being run with Python version >= 3.0. If it isn't, you'll need to manually edit the object chain in the malicious template. Specifically, you will need to verify the Object class index in the mro. Don't be lazy and just use [-1], as that can cause issues in older versions of Python. 

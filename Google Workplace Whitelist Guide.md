## How to whitelist GoPhish in Google Workplace

### Step 1: Enabling SMTP Relay

The public IP of your GoPhish server should be added to the list of relay servers.

 1. Log into Google Workplace Admin
 2. Navigate to `Apps>Google Workspace>Gmail>Routing`
 3. Choose the organization that you'd like to modify
 4. Scroll down in the main pane until you see `SMTP relay service`
 5. Click `Add` and use the following settings:
    - Allowed Senders: Any addresses (not recommended)
    - Authentication: 
        - Only accept mail from the specified IP addresses: ☑ _checked_
        - IP addresses / ranges: _add your IPs_
        - Require SMTP Authentication
        - Require SMTP Authentication: ☐ _unchecked_
    - Encryption: ☑ _checked_

### Step 2: Bypassing the Spam Filters
 1. Go to `Apps>Google Workspace>Gmail>Spam, phishing and malware`
 2. Choose the organization that you'd like to modify
 3. Scroll down in the main pane until you see `Spam`
 4. Click `Add` and use the following settings:
    - Name: GoPhish-Bypass Domains
    - Options:
        - Be more aggressive when filtering spam: ☐ _unchecked_
        - Put spam in administrative quarantine: ☐ _unchecked_
    - Bypass spam filters and hide warnings for messages from senders or domains in selected lists: ☑ _checked_
        - Click `Create or edit list` and add all the domains you would like to spoof.


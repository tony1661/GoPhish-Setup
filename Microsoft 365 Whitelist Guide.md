## How to whitelist GoPhish in Microsoft 365

### Step 1: Get your SMTP Relay address

The public IP of your GoPhish server should be added to the list of relay servers.

 1. Log into Microsoft 365
 2. Navigate to `Settings>Domains`
 3. Choose your domain
 4. Go to the `DNS records` tab
 5. Write down the `Value` for your MX record as this will be needed in Step 3
    - It should be something like: _domain-com.mail.protection.outlook.com_
 

### Step 2: Enabling SMTP Relay
 1. Go to `Admin centers>Exchange`
 2. Go to `Mail flow>Connectors`
 3. Click `Add a connector` and use the following settings:
    - Connection from: Your organization's email server
    - Click `Next`
    - Name: Go Phish
    - Turn it on: ☑ _checked_
    - Retain internal Exchange email headers: ☑ _checked_
    - By verifying that the IP address of the sending server matches one of the following IP addresses, which belong exclusively to your organization: ☑ _checked_
        - Add your Public IP of your GoPhish server

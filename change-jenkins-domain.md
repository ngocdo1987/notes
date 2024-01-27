How to change Jenkins domain

You get this warning when your Jenkins URL refers to "localhost" instead of an IP address or domain name. To fix this warning:
1/ Go to Jenkins > Manage Jenkins > Configure System, and locate the section titled "Jenkins Location". You should see the warning here as well.
2/ Replace "localhost" with a valid hostname.
3/ Click Save.

URLs do not match

If you access Jenkins from a URL other than what is configured in the "Jenkins Location" section of Jenkins > Manage Jenkins > Configure System, then you should see a warning that URLs do not match.
To fix it, click Take me to the recommended URL.
You may be required to sign in again.

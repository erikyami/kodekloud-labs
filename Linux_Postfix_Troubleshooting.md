## Problem

Some users of the monitoring app have reported issues with xFusionCorp Industries mail server. They have a mail server in Stork DC where they are using postfix mail transfer agent. Postfix service seems to fail. Try to identify the root cause and fix it.


## Solution

```
ssh groot@stmail01
```

```
postfix check
postfix: fatal: parameter inet_interfaces: no local interface found for ::1
```

```
vi /etc/postfix/main.cf

# Enable IPv4, and IPv6 if supported
inet_protocols = ipv4
```

```
systemctl start postfix
systemctl status postfix
```

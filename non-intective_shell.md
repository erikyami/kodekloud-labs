## Problem

Create a Linux User with non-interactive shell

The System admin team of xFusionCorp Industries has installed a backup agent tool on all app servers. As per the tool's requirements they need to create a user with a non-interactive shell.

Therefore, create a user named mark with a non-interactive shell on the App Server 3


## Solution

```
[root@stapp03 banner]# useradd -s /bin/false mark
[root@stapp03 banner]# getent passwd mark
mark:x:1002:1002::/home/mark:/bin/false
```


## Problem
One of the Nautilus developers has copied confidential data on the jump host in Stratos DC. That data must be copied to one of the app servers. Because developers do not have access to app servers, they asked the system admins team to accomplish the task for them.

Copy /tmp/nautilus.txt.gpg file from jump server to App Server 2 at location /home/nfsshare.


## Solution

```
thor@jump_host ~$ scp /tmp/nautilus.txt.gpg steve@172.16.238.11:/home/nfsshare/
The authenticity of host '172.16.238.11 (172.16.238.11)' can't be established.
ECDSA key fingerprint is SHA256:SySamszyWhhLGFiybhGBqfrr8g55wS/3e37ZpBOvICs.
ECDSA key fingerprint is MD5:6d:31:18:2a:f9:07:f3:29:dd:0a:d3:1f:6e:04:0a:db.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '172.16.238.11' (ECDSA) to the list of known hosts.
steve@172.16.238.11's password:
nautilus.txt.gpg                                                                             100%   74   172.9KB/s   00:00


thor@jump_host ~$ ssh steve@172.16.238.11
steve@172.16.238.11's password:


[steve@stapp02 ~]$ ls /home/nfsshare/
nautilus.txt.gpg
```



## Problem

There are new requirements to automate a backup process that was performed manually by the xFusionCorp Industries system admins team earlier. To automate this task, the team has developed a new bash script xfusioncorp.sh. They have already copied the script on all required servers, however they did not make it executable on one the app server i.e App Server 2 in Stratos Datacenter.

Please give executable permissions to /tmp/xfusioncorp.sh script on App Server 2. Also make sure every user can execute it.


## Solution

```
thor@jump_host ~$ ssh stapp02 -l steve
steve@stapp02's password:
[steve@stapp02 ~]$ sudo -s

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for steve:
[root@stapp02 steve]# chmod 755 /tmp/xfusioncorp.sh
[root@stapp02 steve]#
[root@stapp02 steve]#
[root@stapp02 steve]# exit
[steve@stapp02 ~]$ logout
Connection to stapp02 closed.
thor@jump_host ~$
```

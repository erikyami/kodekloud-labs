## Problem
As per details shared by the development team, the new application release has some dependencies on the back end. There are some packages/services that need to be installed on all app servers under Stratos Datacenter. As per requirements please perform the following steps:

a. Install nscd package on all the application servers.

b. Once installed, make sure it is enabled to start during boot.

## Solution

```
ssh tony@stapp01
ssh steve@stapp02
ssh banner@stapp03


sudo yum install nscd -y
sudo systemctl start nscd
^start^enable
^enable^status
```

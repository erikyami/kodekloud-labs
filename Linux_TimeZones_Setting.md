## Problem

During the daily standup, it was pointed out that the timezone across Nautilus Application Servers in Stratos Datacenter doesn't match with that of the local datacenter's timezone, which is America/Argentina/Mendoza.

Correct the mismatch.

## Solution
[root@stapp02 steve]# timedatectl set-timezone America/Argentina/Mendoza
[root@stapp02 steve]# timedatectl
      Local time: Mon 2021-06-14 18:11:33 -03
  Universal time: Mon 2021-06-14 21:11:33 UTC
        RTC time: n/a
       Time zone: America/Argentina/Mendoza (-03, -0300)
     NTP enabled: n/a
NTP synchronized: yes
 RTC in local TZ: no
      DST active: n/a

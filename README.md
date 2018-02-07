# rpi
```
pi@raspberrypi:~ $ cat /etc/issue
Raspbian GNU/Linux 9 \n \l
```

```
pi@raspberrypi:~ $ uname -a
Linux raspberrypi 4.9.59-v7+ #1047 SMP Sun Oct 29 12:19:23 GMT 2017 armv7l GNU/Linux
```

```
pi@raspberrypi:~ $ cat /boot/config.txt
...
arm_freq=1150
core_freq=400
sdram_freq=400
over_voltage=4
#disable_splash=1
force_turbo=1
boot_delay=1
```
(which I consider a "decent" overclock since my raspberry pi 3 does not heat up, without a fan)


## Kamailio
Built `.deb`s with all modules except `exclude_modules=db_mongodb ndb_mongodb db_cassandra ndb_cassandra db_oracle nsq osp phonenum`

- kamailio 5.1.1 - 45233bf


## RTPEngine

- rtpengine 6.1.1.0 - f3af4c4


## FreeSWITCH

- freeswitch 1.8 -> [TODO]

# rpi
Overclocked raspberry pi 3 running raspbian stretch with a U3 MicroSD card.

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
total_mem=1024
arm_freq=1300
core_freq=500
sdram_freq=500
sdram_schmoo=0x02000020
over_voltage=2
sdram_over_voltage=2
```




# rpi repo
Add repo key:

```
wget -qO - https://repo.govoip.ro/repo.key | sudo apt-key add -
```


Add repo:

```
echo 'deb https://repo.govoip.ro stretch main' | sudo tee --append /etc/apt/sources.list > /dev/null
```


Get repo:

```
sudo apt-get update

sudo apt-get install kamailio
sudo apt-get install ngcp-rtpengine
sudo apt-get install freeswitch
```




### 1. Kamailio
Built `.deb`s with all modules except `exclude_modules=db_mongodb ndb_mongodb db_cassandra ndb_cassandra db_oracle nsq osp phonenum`.

- kamailio 5.1.1 - 45233bf




### 2. RTPEngine
Built `.deb`s with all modules.

- rtpengine 6.1.1.0 - f3af4c4
- rtpengine 7.0.0.0 - 3102357




### 3. FreeSWITCH
Built `.deb`s with the minimal `modules.conf` from master branch.

- freeswitch 1.9.0 (master) - 38153a3

# Linux Basics

Examples of using basic commands in Linux (and SSH), initailly primarily for Raspberry Pi Zero W.




```C++

ssh pi@192.168.1.253

ls -l

chmod +rwx server

ps

./server

kill [ID#]

pkill server

netstat -lepunt

sudo reboot

jobs

kill $(jobs -p)

```


And from Windows command line:

```C++

set GOOS=linux
set GOARCH=arm
set GOARM=6

scp server pi@192.168.1.253:/home/pi/
scp homepage.html pi@192.168.1.253:/home/pi/


```

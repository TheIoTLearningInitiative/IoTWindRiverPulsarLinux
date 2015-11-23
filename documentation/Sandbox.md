SandBox
==

## Extra Documentation

- [Binary Option](http://linuxgizmos.com/wind-river-linux-taps-yocto-1-7-and-adds-binary-option/)
- http://linuxgizmos.com/wind-river-launches-helix-cloud-iot-platform-with-rocket-rtos-and-pulsar-linux/


1. Download
2. Load
3. Boot

user@host:~$ sudo apt-get install virtualbox qemu
user@host:~$     VBoxManage convertfromraw --format VDI pulsar.img pulsar.vdi
user@host:~$ qemu-system-x86_64 pulsar.img
user@host:~$ qemu-system-x86_64 -nographic pulsar.img

Helix Application Cloud Agent
https://github.com/WindRiver-OpenSourceLabs/tcf-c-core
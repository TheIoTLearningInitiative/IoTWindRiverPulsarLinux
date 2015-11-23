SandBox
==

## Extra Documentation

- [Binary Option](http://linuxgizmos.com/wind-river-linux-taps-yocto-1-7-and-adds-binary-option/)
- http://linuxgizmos.com/wind-river-launches-helix-cloud-iot-platform-with-rocket-rtos-and-pulsar-linux/


1. Download
2. Load
3. Boot

1. Download
2. Unzip
3. Launch


    user@host:~$ sudo apt-get install virtualbox qemu
    user@host:~$ VBoxManage convertfromraw --format VDI pulsar.img pulsar.vdi
    user@host:~$ qemu-system-x86_64 pulsar.img
    user@host:~$ qemu-system-x86_64 -nographic pulsar.img
    
    
    Pulsar Linux 7.0.0.10 cube-03-11-15-domE ttyS0
    
    cube-03-11-15-domE login: root
    Pulsar Linux 7.0.0.10 cube-03-11-15-domE ttyS0
    Password: incendia
    Last login: Mon Nov 23 16:03:51 EST 2015 on ttyS0
    root@cube-03-11-15-domE:~# 
    

## To Review

- Helix Application Cloud Agent
- https://github.com/WindRiver-OpenSourceLabs/tcf-c-core
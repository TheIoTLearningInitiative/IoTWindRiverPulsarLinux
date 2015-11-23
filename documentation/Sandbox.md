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
    
    root@cube-03-11-15-domE:~# ifconfig
    br0       Link encap:Ethernet  HWaddr ca:ae:9e:a4:4e:5b  
              inet addr:10.0.2.17  Bcast:10.0.2.255  Mask:255.255.255.0
              inet6 addr: fe80::c8ae:9eff:fea4:4e5b/64 Scope:Link
    
    eth0      Link encap:Ethernet  HWaddr 4a:17:2d:81:3d:7c  
              inet6 addr: fe80::4817:2dff:fe81:3d7c/64 Scope:Link
              UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1

    
    lo        Link encap:Local Loopback  
              inet addr:127.0.0.1  Mask:255.0.0.0
              inet6 addr: ::1/128 Scope:Host
    

## To Review

- Helix Application Cloud Agent
- https://github.com/WindRiver-OpenSourceLabs/tcf-c-core
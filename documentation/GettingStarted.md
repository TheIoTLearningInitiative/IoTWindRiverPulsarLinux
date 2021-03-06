# Getting Started


# MinnowBoard MAX


## Pulsar™ Linux @ Wind River® Webpage

[Wind River Pulsar Linux Quick Start for MinnowBoard MAX, 7.0](https://knowledge.windriver.com/en-us/000_Products/000/060/000/030/000_Wind_River_Pulsar_Linux_Quick_Start_for_MinnowBoard_MAX%2C_7.0)

- MinnowBoard MAX Quick Start
  - Downloading the Certified MinnowBoard MAX Image
  - Loading the Certified Image onto a Memory Device
  - Booting Up the MinnowBoard MAX Device

## Pulsar™ Linux @ MinnowBoard MAX Webpage

> Wind River® Pulsar™ Linux is a small, high-performance, secure, and manageable Open Source Linux distribution designed to simplify and speed your embedded and Internet of Things (IoT) development projects. Based on 35 years of Wind River industry-leading experience and the latest Yocto Project Compatible releases, Pulsar ensures your team is working with the highest-quality commercial open source embedded operating system on the market. [MinnowBoard MAX Wind River® Pulsar™ Linux](http://wiki.minnowboard.org/Wind_River_Pulsar_Linux)

> Pulsar Linux is certified on the MinnowBoard MAX development board: download an image and begin development immediately without any of the headaches and hassles of setting up your own embedded operating system. [MinnowBoard MAX Wind River® Pulsar™ Linux](http://wiki.minnowboard.org/Wind_River_Pulsar_Linux)

# Wind River® Helix Lab Cloud

> A Virtual Lab, For Your Virtual Hardware. Wind River® Helix™ Lab Cloud is an instantly accessible software lab that improves team collaboration and shortens development cycles. [Homepage](https://lab.cloud.windriver.com/)

1. [Sign in to Lab Cloud](https://lab.cloud.windriver.com/user/login/sso)
2. Add a new session using "Intel Core i7 Virtual System with Wind River Pulsar Linux 7" called "MyPulsar"
3. Start Simulation
4. Enable Helix Lab Network Proxy

```sh
xe1gyq@jessie:~/Downloads/helix-lab-network-proxy$ ./helix-lab-network-proxy.sh Helix Network Proxy v1.3.3

You are using a Wind River account to connect to the Helix server.
Your credentials are read from the file /home/xe1gyq/.helix-network-proxy.cred

...
...

Authentication successful.
MyPulsar: Secured communication established with target.
MyPulsar: Network proxy server running: 53984 -> 22 (UDP)
MyPulsar: Network proxy server running: 40695 -> 22 (TCP)
MyPulsar: Network proxy server running: 33143 -> 1534 (UDP)
MyPulsar: Network proxy server running: 34300 -> 1534 (TCP)
```

5. Connect to "MyPulsar" via your host

```sh
xe1gyq@jessie:~/Downloads/helix-lab-network-proxy$ ssh root@127.0.0.1 -p 40695
The authenticity of host '[127.0.0.1]:40695 ([127.0.0.1]:40695)' can't be established.
ECDSA key fingerprint is 90:d9:d5:8a:cd:2a:0c:f2:72:0e:74:a9:9a:7e:d5:22.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '[127.0.0.1]:40695' (ECDSA) to the list of known hosts.
root@127.0.0.1's password: 
Last login: Mon Nov  2 14:14:36 2015 from simics0.network.sim
root@cube-31-10-15-domE:~# 
```

6. Explore domE container content

```sh
root@cube-31-10-15-domE:~# ls
wr_pulsar_linux_getting_started_70.pdf
wr_pulsar_linux_software_development_guide_70.pdf
wr_pulsar_linux_system_integrators_guide_70.pdf
root@cube-31-10-15-domE:~# 
```

7. Ping google.com and see its response

```sh
root@cube-31-10-15-domE:~# ping google.com
PING google.com (74.125.28.113) 56(84) bytes of data.
From simics0.network.sim (10.10.0.1) icmp_seq=1 Destination Host Unreachable
From simics0.network.sim (10.10.0.1) icmp_seq=2 Destination Host Unreachable
From simics0.network.sim (10.10.0.1) icmp_seq=3 Destination Host Unreachable
From simics0.network.sim (10.10.0.1) icmp_seq=4 Destination Host Unreachable
^C
--- google.com ping statistics ---
4 packets transmitted, 0 received, +4 errors, 100% packet loss, time 2999ms

root@cube-31-10-15-domE:~# 
```

8. Update Date and Time

```sh
root@cube-31-10-15-domE:~# date -s "2016/06/04 22:51:15"
Sat Jun  4 22:51:15 EDT 2016
root@cube-31-10-15-domE:~# npm install -g n
```

9. Clean screen with "Ctrl - l"

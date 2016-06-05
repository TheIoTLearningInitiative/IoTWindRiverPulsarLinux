# Labs

```sh
root@cube-31-10-15-domE:~# git clone https://github.com/xe1gyq/TheIoTLearningInitiative.git
Cloning into 'TheIoTLearningInitiative'...
fatal: unable to access 'https://github.com/xe1gyq/TheIoTLearningInitiative.git/': server certificate verification failed. CAfile: /etc/ssl/certs/ca-certificates.crt CRLfile: none
root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# git config --global http.sslverify false
root@cube-31-10-15-domE:~# git clone https://github.com/xe1gyq/TheIoTLearningInitiative.git
Cloning into 'TheIoTLearningInitiative'...
remote: Counting objects: 63, done.
remote: Compressing objects: 100% (16/16), done.
remote: Total 63 (delta 9), reused 0 (delta 0), pack-reused 43
Unpacking objects: 100% (63/63), done.
Checking connectivity... done.
root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# cd TheIoTLearningInitiative/
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/embeddedlinux
  remotes/origin/master
  remotes/origin/windriver
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# git checkout -b windriver origin/windriver
Branch windriver set up to track remote branch windriver from origin.
Switched to a new branch 'windriver'
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# cd WindRiver/
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# ls
mainpulsar.py
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install paho-mqtt
/usr/lib64/python2.7/site-packages/pip/_vendor/requests/packages/urllib3/util/ssl_.py:90: InsecurePlatformWarning: A true SSLContext object is not available. This prevents urllib3 from configuring SSL appropriately and may cause certain SSL connections to fail. For more information, see https://urllib3.readthedocs.org/en/latest/security.html#insecureplatformwarning.
  InsecurePlatformWarning
You are using pip version 7.1.0, however version 8.1.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
Collecting paho-mqtt
/usr/lib64/python2.7/site-packages/pip/_vendor/requests/packages/urllib3/util/ssl_.py:90: InsecurePlatformWarning: A true SSLContext object is not available. This prevents urllib3 from configuring SSL appropriately and may cause certain SSL connections to fail. For more information, see https://urllib3.readthedocs.org/en/latest/security.html#insecureplatformwarning.
  InsecurePlatformWarning
  Downloading paho-mqtt-1.2.tar.gz (49kB)
    100% |################################| 53kB 804kB/s 
Installing collected packages: paho-mqtt
  Running setup.py install for paho-mqtt
Successfully installed paho-mqtt
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# python mainpulsar.py 
Hello Internet of Things 101
Data Sensor: 95 
Hello Internet of Things 101
Data Sensor: 54 
Hello Internet of Things 101
Data Sensor: 20 
^C^Z
[1]+  Stopped(SIGTSTP)        python mainpulsar.py
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
```




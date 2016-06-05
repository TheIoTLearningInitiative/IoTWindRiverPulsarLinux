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

Pip Installion Error

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install psutil
You are using pip version 7.1.0, however version 8.1.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
Collecting psutil
/usr/lib64/python2.7/site-packages/pip/_vendor/requests/packages/urllib3/util/ssl_.py:90: InsecurePlatformWarning: A true SSLContext object is not available. This prevents urllib3 from configuring SSL appropriately and may cause certain SSL connections to fail. For more information, see https://urllib3.readthedocs.org/en/latest/security.html#insecureplatformwarning.
  InsecurePlatformWarning
  Downloading psutil-4.2.0.tar.gz (311kB)
    100% |################################| 315kB 642kB/s 
Installing collected packages: psutil
  Running setup.py install for psutil
    Complete output from command /usr/bin/python -c "import setuptools, tokenize;__file__='/tmp/pip-build-xhZ1wn/psutil/setup.py';exec(compile(getattr(tokenize, 'open', open)(__file__).read().replace('\r\n', '\n'), __file__, 'exec'))" install --record /tmp/pip-csRx60-record/install-record.txt --single-version-externally-managed --compile:
    running install
    running build
    running build_py
    creating build
    creating build/lib.linux-x86_64-2.7
    creating build/lib.linux-x86_64-2.7/psutil
    copying psutil/_pswindows.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_pslinux.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_psposix.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_psbsd.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_pssunos.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_psosx.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_common.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/_compat.py -> build/lib.linux-x86_64-2.7/psutil
    copying psutil/__init__.py -> build/lib.linux-x86_64-2.7/psutil
    creating build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_posix.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_sunos.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_memory_leaks.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_bsd.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_linux.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/runner.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_process.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_osx.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_windows.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_system.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/test_misc.py -> build/lib.linux-x86_64-2.7/psutil/tests
    copying psutil/tests/__init__.py -> build/lib.linux-x86_64-2.7/psutil/tests
    running build_ext
    building 'psutil._psutil_linux' extension
    creating build/temp.linux-x86_64-2.7
    creating build/temp.linux-x86_64-2.7/psutil
    x86_64-wrs-linux-gcc -m64 -march=core2 -mtune=core2 -msse3 -mfpmath=sse -fno-strict-aliasing -O2 -pipe -g -DNDEBUG -g -O3 -Wall -Wstrict-prototypes -fPIC -DPSUTIL_VERSION=420 -I/usr/include/python2.7 -c psutil/_psutil_linux.c -o build/temp.linux-x86_64-2.7/psutil/_psutil_linux.o
    psutil/_psutil_linux.c:12:20: fatal error: Python.h: No such file or directory
     #include <Python.h>
                        ^
    compilation terminated.
    error: command 'x86_64-wrs-linux-gcc' failed with exit status 1
    
    ----------------------------------------
Command "/usr/bin/python -c "import setuptools, tokenize;__file__='/tmp/pip-build-xhZ1wn/psutil/setup.py';exec(compile(getattr(tokenize, 'open', open)(__file__).read().replace('\r\n', '\n'), __file__, 'exec'))" install --record /tmp/pip-csRx60-record/install-record.txt --single-version-externally-managed --compile" failed with error code 1 in /tmp/pip-build-xhZ1wn/psutil
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install setuptools
You are using pip version 7.1.0, however version 8.1.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
Collecting setuptools
/usr/lib64/python2.7/site-packages/pip/_vendor/requests/packages/urllib3/util/ssl_.py:90: InsecurePlatformWarning: A true SSLContext object is not available. This prevents urllib3 from configuring SSL appropriately and may cause certain SSL connections to fail. For more information, see https://urllib3.readthedocs.org/en/latest/security.html#insecureplatformwarning.
  InsecurePlatformWarning
  Downloading setuptools-22.0.5-py2.py3-none-any.whl (510kB)
    100% |################################| 512kB 403kB/s 
Installing collected packages: setuptools
Successfully installed setuptools-22.0.5
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver#  
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# smart update
Loading cache...
Updating cache...               ######################################## [100%]

Fetching information for 'all'...                                              
-> https://distro.windriver.com/public_feeds/.../repomd.xml                    
repomd.xml                      ######################################## [ 12%]
                                                                               
Fetching information for 'core2_64_intel_common'...
-> https://distro.windriver.com/public_feeds/.../repomd.xml                    
repomd.xml                      ######################################## [ 31%]
                                                                               
Fetching information for 'core2_64'...
-> https://distro.windriver.com/public_feeds/.../repomd.xml                    
repomd.xml                      ######################################## [ 50%]
                                                                               
Fetching information for 'intel_corei7_64'...
-> https://distro.windriver.com/public_feeds/.../repomd.xml                    
repomd.xml                      ######################################## [ 68%]

Updating cache...               ######################################## [100%]

Channels have no new packages.
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
```

```sh
```

```sh
```

```sh
```

```sh
```




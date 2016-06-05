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
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# smart install python-dev
Loading cache...
Updating cache...               ######################################## [100%]

Computing transaction...

Upgrading packages (6):
  bzip2-1.0.6-r5.1@core2_64              libreadline6-6.3-r0.1@core2_64         
  db-6.0.30-r0.1@core2_64                ncurses-5.9-r15.1.1@core2_64           
  libbz2-0-1.0.6-r5.1@core2_64           openssl-1.0.1j-r0.1@core2_64           

Installing packages (14):
  bzip2-dev-1.0.6-r5.1@core2_64                                                 
  cryptodev-linux-1.6-r0.1@core2_64                                             
  cryptodev-linux-dev-1.6-r0.1@core2_64                                         
  db-dev-6.0.30-r0.1@core2_64                                                   
  libbz2-dev-1.0.6-r5.1@core2_64                                                
  libformw5-5.9-r15.1.1@core2_64                                                
  libmenuw5-5.9-r15.1.1@core2_64                                                
  libreadline-dev-6.3-r0.1@core2_64                                             
  libsqlite3-dev-3:3.8.6.0-r0.1@core2_64                                        
  libtic5-5.9-r15.1.1@core2_64                                                  
  libticw5-5.9-r15.1.1@core2_64                                                 
  ncurses-dev-5.9-r15.1.1@core2_64                                              
  openssl-dev-1.0.1j-r0.1@core2_64                                              
  python-dev-2.7.3-r0.3.1@core2_64                                              

1.8MB of package files are needed. 3.0MB will be used.

Confirm changes? (Y/n): Y
...
...
Committing transaction...
Preparing...                    ######################################## [  0%]
   1:Installing libmenuw5       ######################################## [  3%]
   2:Installing libformw5       ######################################## [  7%]
   3:Installing db              ######################################## [ 11%]
   4:Cleaning db                ######################################## [ 15%]
   5:Installing bzip2           ######################################## [ 19%]
Output from bzip2-1.0.6-r5.1@core2_64:                                         
update-alternatives: Linking //usr/bin/bunzip2 to /usr/bin/bunzip2.bzip2       
update-alternatives: Linking //usr/bin/bzcat to /usr/bin/bzcat.bzip2
   6:Cleaning bzip2             ######################################## [ 23%]
   7:Installing cryptodev-linux ######################################## [ 26%]
   8:Installing libreadline6    ######################################## [ 30%]
   9:Cleaning libreadline6      ######################################## [ 34%]
  10:Installing libbz2-0        ######################################## [ 38%]
  11:Cleaning libbz2-0          ######################################## [ 42%]
  12:Installing python-dev      ######################################## [ 46%]
  13:Installing ncurses         ######################################## [ 50%]
  14:Cleaning ncurses           ######################################## [ 53%]
  15:Installing libtic5         ######################################## [ 57%]
  16:Installing openssl         ######################################## [ 61%]
  17:Cleaning openssl           ######################################## [ 65%]
  18:Installing libticw5        ######################################## [ 69%]
  19:Installing libsqlite3-dev  ######################################## [ 73%]
  20:Installing db-dev          ######################################## [ 76%]
  21:Installing bzip2-dev       ######################################## [ 80%]
  22:Installing cryptodev-lin.. ######################################## [ 84%]
  23:Installing libreadline-dev ######################################## [ 88%]
  24:Installing libbz2-dev      ######################################## [ 92%]
  25:Installing openssl-dev     ######################################## [ 96%]
  26:Installing ncurses-dev     ######################################## [100%]


root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install --upgrade pip
You are using pip version 7.1.0, however version 8.1.2 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
/usr/lib64/python2.7/site-packages/pip/_vendor/requests/packages/urllib3/util/ssl_.py:90: InsecurePlatformWarning: A true SSLContext object is not available. This prevents urllib3 from configuring SSL appropriately and may cause certain SSL connections to fail. For more information, see https://urllib3.readthedocs.org/en/latest/security.html#insecureplatformwarning.
  InsecurePlatformWarning
Collecting pip
  Downloading pip-8.1.2-py2.py3-none-any.whl (1.2MB)
    100% |################################| 1.2MB 175kB/s 
Installing collected packages: pip
  Found existing installation: pip 7.1.0
    Uninstalling pip-7.1.0:
      Successfully uninstalled pip-7.1.0
Successfully installed pip-8.1.2
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install --upgrade setuptools
Requirement already up-to-date: setuptools in /usr/lib/python2.7/site-packages
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# rm -rf /usr/lib64/python2.7/site-packages/distribute-0.6.32-py2.7.egg/
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install -U distribute
Collecting distribute
  Using cached distribute-0.7.3.zip
Requirement already up-to-date: setuptools>=0.7 in /usr/lib/python2.7/site-packages (from distribute)
Installing collected packages: distribute
  Running setup.py install for distribute ... done
Successfully installed distribute-0.7.3
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# pip install psutil
Collecting psutil
  Using cached psutil-4.2.0.tar.gz
Installing collected packages: psutil
  Running setup.py install for psutil ... done
Successfully installed psutil-4.2.0
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# 
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/WindRiver# cd
root@cube-31-10-15-domE:~# cd TheIoTLearningInitiative/
root@cube-31-10-15-domE:~/TheIoTLearningInitiative# cd InternetOfThings101/
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/InternetOfThings101# 
```

```
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/InternetOfThings101# python main.py 
Traceback (most recent call last):
  File "main.py", line 5, in <module>
    import pywapi
ImportError: No module named pywapi
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/InternetOfThings101#    
```

```sh
root@cube-31-10-15-domE:~/TheIoTLearningInitiative/InternetOfThings101# cd 
root@cube-31-10-15-domE:~# wget https://launchpad.net/python-weather-api/trunk/0.3.8/+download/pywapi-0.3.8.tar.gz
--2015-11-02 16:13:37--  https://launchpad.net/python-weather-api/trunk/0.3.8/+download/pywapi-0.3.8.tar.gz
Resolving launchpad.net... 91.189.89.223
Connecting to launchpad.net|91.189.89.223|:443... connected.
ERROR: The certificate of 'launchpad.net' is not trusted.
ERROR: The certificate of 'launchpad.net' is not yet activated.
The certificate has not yet been activated
root@cube-31-10-15-domE:~# wget --no-check-certificate  https://launchpad.net/python-weather-api/trunk/0.3.8/+download/pywapi-0.3.8.tar.gz
--2015-11-02 16:14:23--  https://launchpad.net/python-weather-api/trunk/0.3.8/+download/pywapi-0.3.8.tar.gz
Resolving launchpad.net... 91.189.89.223
Connecting to launchpad.net|91.189.89.223|:443... connected.
WARNING: The certificate of 'launchpad.net' is not trusted.
WARNING: The certificate of 'launchpad.net' is not yet activated.
The certificate has not yet been activated
HTTP request sent, awaiting response... 302 Moved Temporarily
Location: https://launchpadlibrarian.net/166317636/pywapi-0.3.8.tar.gz [following]
--2015-11-02 16:14:24--  https://launchpadlibrarian.net/166317636/pywapi-0.3.8.tar.gz
Resolving launchpadlibrarian.net... 91.189.89.228
Connecting to launchpadlibrarian.net|91.189.89.228|:443... connected.
WARNING: The certificate of 'launchpadlibrarian.net' is not trusted.
WARNING: The certificate of 'launchpadlibrarian.net' is not yet activated.
The certificate has not yet been activated
HTTP request sent, awaiting response... 200 OK
Length: 25166 (25K) [application/x-tar]
Saving to: 'pywapi-0.3.8.tar.gz'

100%[======================================>] 25,166       123KB/s   in 0.2s   

2015-11-02 16:14:26 (123 KB/s) - 'pywapi-0.3.8.tar.gz' saved [25166/25166]

root@cube-31-10-15-domE:~# 
```

```sh
root@cube-31-10-15-domE:~# tar zxvf pywapi-0.3.8.tar.gz
pywapi-0.3.8/examples/pywapi-countries-example.py
pywapi-0.3.8/setup.py
pywapi-0.3.8/MANIFEST
pywapi-0.3.8/examples/
pywapi-0.3.8/examples/pywapi-noaa-example.py
pywapi-0.3.8/examples/pywapi-example.py
pywapi-0.3.8/pywapi.pyc
pywapi-0.3.8/LICENSE
pywapi-0.3.8/examples/pywapi-weather-com-example.py
pywapi-0.3.8/pywapi.py
pywapi-0.3.8/examples/pywapi-cities-example.py
pywapi-0.3.8/CHANGELOG
pywapi-0.3.8/README
pywapi-0.3.8/
pywapi-0.3.8/examples/pywapi-yahoo-example.py
pywapi-0.3.8/examples/get-weather.py
root@cube-31-10-15-domE:~# 
```

```sh
```

```sh
```

```sh
```

```sh
```
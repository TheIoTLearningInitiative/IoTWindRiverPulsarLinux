# Building

## Setup, Minnowboard MAX

```sh
    user@host:~$ cd wr-core
    user@host:~/wr-core$ sudo ./scripts/host_package_install.sh --install --yes
    grep: /etc/lsb-release: No such file or directory
    You need to install additional software on your host system
        in order to use the development environment.
    
    Executing: sudo apt-get -y install expect kpartx btrfs-tools help2man texi2html 
    
    user@host:~/wr-core$ . init-intel-x86-env
        You can now run 'bitbake <target>'

    Common targets are:
    
        cube-essential 
        cube-dom0 
        cube-domE
        cube-server
```

## Bitbake

```sh
user@host:~/wr-core$ bitbake cube-domE cube-dom0 cube-essential
        
xe1gyq@jessie:~/WindRiver/wr-core/build-intel-x86$ bitbake cube-domE cube-dom0 cube-essential
Parsing recipes: 100% |###################################################################################| Time: 00:03:44
Parsing of 2246 .bb files complete (0 cached, 2246 parsed). 2821 targets, 108 skipped, 5 masked, 0 errors.
NOTE: Resolving any missing task queue dependencies
NOTE: multiple providers are available for runtime lmsensors-sensors (lm-sensors, lmsensors)
NOTE: consider defining a PREFERRED_PROVIDER entry to match lmsensors-sensors
NOTE: multiple providers are available for jpeg (jpeg, libjpeg-turbo)
NOTE: consider defining a PREFERRED_PROVIDER entry to match jpeg
NOTE: multiple providers are available for jpeg-native (jpeg-native, libjpeg-turbo-native)
NOTE: consider defining a PREFERRED_PROVIDER entry to match jpeg-native
    
Build Configuration:
BB_VERSION        = "1.24.0"
BUILD_SYS         = "i686-linux"
NATIVELSBSTRING   = "Debian-8.3"
DISTRO            = "wrlinux-small"
DISTRO_VERSION    = "7.0.0.11"
MACHINE           = "intel-corei7-64"
DEFAULTTUNE       = "core2-64"
TARGET_SYS        = "x86_64-wrs-linux"
TUNE_FEATURES     = "m64 core2"
TARGET_FPU        = ""
wrlinux           = "(detachedfrom4ba70d8):4ba70d81b884270bf93e9911e11f952e3546b104"
meta              = "(detachedfromb1fd2f8):b1fd2f8c930237ced32aee41cceef367ab2bb7dd"
oe-meta-go        = "(detachedfromb29b384):b29b384eae4a40933d07cc64c51e890c289d9621"
meta-virtualization = "(detachedfrom9377e68):9377e68bcd4bd4dd686807f43adac90dfed20da7"
meta-xfce         
meta-webserver    
meta-perl         
meta-python       
meta-oe           
meta-gnome        
meta-networking   
meta-filesystems  = "(detachedfrom62bfd1f):62bfd1f93f8873611e818c7cc8c13a761d629502"
meta-browser      = "(detachedfromb6d46d6):b6d46d69a261fe6bd7c1e9811dc2a9bbd0b79aeb"
meta-cloud-services = "(detachedfrom9ed0aef):9ed0aef7b244773a9db644090b4e361fa7b3eea8"
meta-cube         = "(detachedfrom01403ec):01403ecce3dfc3c1c1ad77010516dd35e15b777a"
meta-gateway      = "(detachedfrom63393ff):63393ff0fea75c1db40b8e3f139e88bac6d96702"
wrll-hac          = "(detachedfrom3b18a32):3b18a320dee41ff3ee10782e8231bb8b85746726"
wr-tools-debug    = "(detachedfrom76bf838):76bf838b043136e424502f015e4d414d03fc4df4"
wr-fixes          = "(detachedfromae22cb9):ae22cb9d28e2c03ce8d7de264f96c9db2b4253a7"
wr-base           = "(detachedfromd93ef81):d93ef81244198cc9fea5347904967191eff7abc8"
meta-valleyisland 
meta-intel        = "(detachedfrom1ebb73f):1ebb73f847be7df8838738561da09eeece55fede"
wr-kernel         = "(detachedfrom94a317e):94a317e4f8207a822b7e8dd1349016409295a75d"
wrlabs-integration = "(detachedfrom6c53310):6c5331098b71eddbfa80d513f6e5aa4d9918d217"

    
NOTE: Preparing runqueue
NOTE: Executing SetScene Tasks
NOTE: Executing RunQueue Tasks
WARNING: Failed to fetch URL http://zlib.net/pigz/pigz-2.3.1.tar.gz, attempting MIRRORS if available
Currently 2 running tasks (320 of 8598):
0: db-native-6.0.30-r0 do_fetch (pid 14452)
1: libpcre-native-8.35-r0 do_configure (pid 30379)
...
```

```
| Checking for HAVE_UNIXSOCKET                                                      : ok
| Checking for HAVE_SECURE_MKSTEMP                                                  : /home/xe1gyq/Projects/WindRiver/wr-core/build-intel-x86/tmp/work/core2-64-wrs-linux/talloc/2.1.1-r0/talloc-2.1.1/lib/replace/wscript:549: error: the configuration failed (see '/home/xe1gyq/Projects/WindRiver/wr-core/build-intel-x86/tmp/work/core2-64-wrs-linux/talloc/2.1.1-r0/talloc-2.1.1/bin/config.log')
| WARNING: exit code 1 from a shell command.
| ERROR: Function failed: do_configure (log file is located at /home/xe1gyq/Projects/WindRiver/wr-core/build-intel-x86/tmp/work/core2-64-wrs-linux/talloc/2.1.1-r0/temp/log.do_configure.26774)
ERROR: Task 4793 (/home/xe1gyq/Projects/WindRiver/wr-core/layers/meta-openembedded/meta-networking/recipes-support/talloc/talloc_2.1.1.bb, do_configure) failed with exit code '1'
NOTE: Tasks Summary: Attempted 1977 tasks of which 0 didn't need to be rerun and 1 failed.
NOTE: Build completion summary:
NOTE:   From shared state: 0
NOTE:   From scratch: 234
Waiting for 0 running tasks to finish:

Summary: 1 task failed:
  /home/xe1gyq/Projects/WindRiver/wr-core/layers/meta-openembedded/meta-networking/recipes-support/talloc/talloc_2.1.1.bb, do_configure
Summary: There were 9 WARNING messages shown.
Summary: There was 1 ERROR message shown, returning a non-zero exit code.
xe1gyq@jessie:~/Projects/WindRiver/wr-core/build-intel-x86$ 
```

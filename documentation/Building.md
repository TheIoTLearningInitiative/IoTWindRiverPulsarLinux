Building
==

Quick start instructions to build Wind River Pulsar Linux for Intel Minnowboard MAX

    user@host:~$ git clone --recurse-submodules https://github.com/WindRiver-OpenSourceLabs/wr-core
         Submodule 'bitbake' (https://github.com/WindRiver-OpenSourceLabs/bitbake) registered for path 'layers/bitbake'
        Submodule 'layers/fsl-ls10xx' (https://github.com/WindRiver-OpenSourceLabs/fsl-ls10xx) registered for path 'layers/fsl-ls10xx'
        Submodule 'meta-intel' (git://git.yoctoproject.org/meta-intel) registered for path 'layers/meta-intel'
        Submodule 'meta-openembedded' (git://git.openembedded.org/meta-openembedded) registered for path 'layers/meta-openembedded'
        Submodule 'meta-overc' (https://github.com/WindRiver-OpenSourceLabs/meta-overc) registered for path 'layers/meta-overc'
        Submodule 'meta-virtualization' (git://git.yoctoproject.org/meta-virtualization) registered for path 'layers/meta-virtualization'
        Submodule 'oe-core' (https://github.com/WindRiver-OpenSourceLabs/oe-core) registered for path 'layers/oe-core'
        Submodule 'oe-meta-go' (https://github.com/WindRiver-OpenSourceLabs/oe-meta-go) registered for path 'layers/oe-meta-go'
        Submodule 'qemuarm' (https://github.com/WindRiver-OpenSourceLabs/qemuarm) registered for path 'layers/qemuarm'
        Submodule 'qemuarma9' (https://github.com/WindRiver-OpenSourceLabs/qemuarma9) registered for path 'layers/qemuarma9'
        Submodule 'wr-base' (https://github.com/WindRiver-OpenSourceLabs/wr-base) registered for path 'layers/wr-base'
        Submodule 'wr-fixes' (https://github.com/WindRiver-OpenSourceLabs/wr-fixes) registered for path 'layers/wr-fixes'
        Submodule 'wr-kernel' (https://github.com/WindRiver-OpenSourceLabs/wr-kernel) registered for path 'layers/wr-kernel'
        Submodule 'wr-tools-debug' (https://github.com/WindRiver-OpenSourceLabs/wr-tools-debug) registered for path 'layers/wr-tools-debug'
        Submodule 'wrlabs-integration' (https://github.com/WindRiver-OpenSourceLabs/wrlabs-integration) registered for path 'layers/wrlabs-integration'
        Submodule 'wrlinux' (https://github.com/WindRiver-OpenSourceLabs/wrlinux) registered for path 'layers/wrlinux'
        Submodule 'layers/wrll-hac' (https://github.com/WindRiver-OpenSourceLabs/wrll-hac) registered for path 'layers/wrll-hac'
        Submodule 'xilinx-zynq' (https://github.com/WindRiver-OpenSourceLabs/xilinx-zynq) registered for path 'layers/xilinx-zynq'
        Submodule 'overc-installer' (https://github.com/WindRiver-OpenSourceLabs/overc-installer) registered for path 'overc-installer'
    user@host:~$ cd wr-core
    user@host:~/wr-core$ ./scripts/host_package_install.sh --install --yes
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
    NATIVELSBSTRING   = "Debian-8.1"
    DISTRO            = "wrlinux-small"
    DISTRO_VERSION    = "7.0.0.10"
    MACHINE           = "intel-corei7-64"
    DEFAULTTUNE       = "core2-64"
    TARGET_SYS        = "x86_64-wrs-linux"
    TUNE_FEATURES     = "m64 core2"
    TARGET_FPU        = ""
    wrlinux           = "(detachedfrom4ba70d8):4ba70d81b884270bf93e9911e11f952e3546b104"
    meta              = "(detachedfromd193de7):d193de73bec15ba6df488033367cc43e403cbffd"
    oe-meta-go        = "(detachedfromb29b384):b29b384eae4a40933d07cc64c51e890c289d9621"
    meta-virtualization = "(detachedfrom2f4211f):2f4211f3e9ae6ce78e8ccb8c46af2e929ed6fb33"
    meta-xfce         
    meta-webserver    
    meta-perl         
    meta-python       
    meta-oe           
    meta-gnome        
    meta-networking   
    meta-filesystems  = "(detachedfrom721a2ca):721a2cabf352085d34dd14c22e71914d3429ca59"
    meta-cube         = "(detachedfrom07c5d4f):07c5d4f7dcd0c2c10783646e43ac4e66c96470d0"
    wrll-hac          = "(detachedfromfd138eb):fd138ebdd5863b366cc71b6d9efe5223b4908e7b"
    wr-tools-debug    = "(detachedfrom76bf838):76bf838b043136e424502f015e4d414d03fc4df4"
    wr-fixes          = "(detachedfromae22cb9):ae22cb9d28e2c03ce8d7de264f96c9db2b4253a7"
    wr-base           = "(detachedfromb4d949a):b4d949a235d5a714250388556019ec4ff00f4cfc"
    meta-valleyisland 
    meta-intel        = "(detachedfromf9ee1b6):f9ee1b6139fbc8cadc72278f6ce5ec13c0e74c51"
    wr-kernel         = "(detachedfrom94a317e):94a317e4f8207a822b7e8dd1349016409295a75d"
    wrlabs-integration = "(detachedfrom7c356d3):7c356d33053641dee821b90d9539d6e29c58b854"
    
    NOTE: Preparing runqueue
    NOTE: Executing SetScene Tasks
    NOTE: Executing RunQueue Tasks
    WARNING: Failed to fetch URL http://zlib.net/pigz/pigz-2.3.1.tar.gz, attempting MIRRORS if available
    Currently 2 running tasks (320 of 8598):
    0: db-native-6.0.30-r0 do_fetch (pid 14452)
    1: libpcre-native-8.35-r0 do_configure (pid 30379)
    
    user@host:~$ sudo ../overc-installer/sbin/cubeit --force --config `pwd`/../install_templates/intel-x86/config-live.sh --artifacts `pwd`/tmp/deploy/images/intel-corei7-64 pulsar7-minnowboardmax.img
    
    user@host:~$ sudo ../overc-installer/sbin/cubeit --force --config `pwd`/../install_templates/intel-x86/config-live.sh --artifacts `pwd`/tmp/deploy/images/intel-corei7-64 $DEV
    user@host:~$ cd /opt/installer
    user@host:~$ ./sbin/cubeit-install -b images/cube-essential-* $DEV

    login: root
    password: incendia

    user@host:~$ kvm -drive file=pulsar7-minnowboardmax.img,if=virtio -m 2000 -nographic -vnc :3 -serial mon:stdio -vga vmware

    # Note: The terminal is your serial port, and you can access the
    #       grapics console by starting: vncviewer $YOUR_SERVER_IP:3


- http://linuxgizmos.com/wind-river-launches-helix-cloud-iot-platform-with-rocket-rtos-and-pulsar-linux/

## Building Blocks

bitbake

> BitBake is co-maintained by the Yocto Project and the OpenEmbedded project. BitBake recipes specify how a particular package is built. It includes all the package dependencies, source code locations, configuration, compilation, build, install and remove instructions. wikipedia

- layers/fslls10xx

> Freescale TWR-LS1021A Boards

- meta-intel
- meta-openembedded
- meta-overc
- meta-virtualization
- oe-core
- oe-meta-go
- qemuarm
- qemuarm9
- wr-base
- wr-fixes
- wr-kernel
- wr-tools-debug
- wrlabs-integration
- wrlinux
- layers/wrll-hac
- xilinx-zynq
- overc-installer
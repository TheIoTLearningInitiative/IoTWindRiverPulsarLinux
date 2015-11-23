Building
==

Quick start instructions to build Wind River Pulsar Linux

Intel Minnowboard MAX

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
    user@host:~$ ./scripts/host_package_install.sh --install --yes
    user@host:~$ . init-intel-x86-env
    user@host:~$ bitbake cube-domE cube-dom0 cube-essential

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

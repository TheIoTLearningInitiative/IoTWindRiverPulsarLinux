# Introduction

- [Wind River Pulsar Linux Homepage](http://www.windriver.com/products/operating-systems/pulsar/)
- [Wind River Pulsar Linux Product Overview](http://www.windriver.com/products/product-overviews/Pulsar-Linux-Product-Overview.pdf)
- [Wind River Support Network Knowledge Library](https://knowledge.windriver.com/en-us/000_Products/000/060)
- [Wind River Pulsar Linux Github](https://github.com/WindRiver-OpenSourceLabs/wr-core)
- [Binary Option](http://linuxgizmos.com/wind-river-linux-taps-yocto-1-7-and-adds-binary-option/)

1. Download
2. Load
3. Boot


Quick start instructions to build Wind River Pulsar Linux

Intel Minnowboard MAX

    git clone --recurse-submodules https://github.com/WindRiver-OpenSourceLabs/wr-core
    cd wr-core
    ./scripts/host_package_install.sh --install --yes
    . init-intel-x86-env
    bitbake cube-domE cube-dom0 cube-essential

    sudo ../overc-installer/sbin/cubeit --force --config `pwd`/../install_templates/intel-x86/config-live.sh --artifacts `pwd`/tmp/deploy/images/intel-corei7-64 pulsar7-minnowboardmax.img
    
    sudo ../overc-installer/sbin/cubeit --force --config `pwd`/../install_templates/intel-x86/config-live.sh --artifacts `pwd`/tmp/deploy/images/intel-corei7-64 $DEV
     cd /opt/installer
     ./sbin/cubeit-install -b images/cube-essential-* $DEV

    login: root
    password: incendia

    kvm -drive file=pulsar7-minnowboardmax.img,if=virtio -m 2000 -nographic -vnc :3 -serial mon:stdio -vga vmware

    # Note: The terminal is your serial port, and you can access the
    #       grapics console by starting: vncviewer $YOUR_SERVER_IP:3


http://linuxgizmos.com/wind-river-launches-helix-cloud-iot-platform-with-rocket-rtos-and-pulsar-linux/

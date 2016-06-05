# Running

# Flash

- [Quick start instructions to build Wind River Pulsar Linux for the Intel Minnow Board Max](https://github.com/WindRiver-OpenSourceLabs/wr-core/blob/pulsar-7.0/docs/README-intel-x86.TXT)

## Flash, Minnwboard MAX

### Build a self-bootable image

```sh
user@host:~$ sudo ../overc-installer/sbin/cubeit --force --config `pwd`/../install_templates/intel-x86/config-live.sh --artifacts `pwd`/tmp/deploy/images/intel-corei7-64 pulsar7-minnowboardmax.img
```

### Build an installer image or USB stick

```sh
user@host:~$ export DEV=/dev/NBD_DEVICE  # or a USB storage device
user@host:~$ sudo ../overc-installer/sbin/cubeit --force --config `pwd`/../install_templates/intel-x86/config-live.sh --artifacts `pwd`/tmp/deploy/images/intel-corei7-64 $DEV
user@host:~$ cd /opt/installer
user@host:~$ ./sbin/cubeit-install -b images/cube-essential-* $DEV
```

```sh
    login: root
    password: incendia
```

### Simulate the image with kvm/qemu

```sh
user@host:~$ kvm -drive file=pulsar7-minnowboardmax.img,if=virtio -m 2000 -nographic -vnc :3 -serial mon:stdio -vga vmware

# Note: The terminal is your serial port, and you can access the
#       grapics console by starting: vncviewer $YOUR_SERVER_IP:3
```


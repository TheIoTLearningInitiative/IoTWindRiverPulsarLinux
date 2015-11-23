Building Blocks
==

bitbake

> BitBake is co-maintained by the Yocto Project and the OpenEmbedded project. BitBake recipes specify how a particular package is built. It includes all the package dependencies, source code locations, configuration, compilation, build, install and remove instructions. wikipedia

layers/fslls10xx

> Freescale TWR-LS1021A Boards

- bootloader
- conf 	
- recipes-daemons/ptpd
- recipes-graphics/xorg-xserver
- recipes-kernel/linux

meta-intel

> Layer containing Intel hardware support metadata

- meta-crystalforest
- meta-haswell-wc
- meta-mohonpeak
- meta-valleyisland

meta-openembedded

> Collection of OpenEmbedded layers

- meta-efl
- meta-filesystems
- meta-gnome
- meta-gpe
- meta-initramfs
- meta-multimedia
- meta-networking
- meta-oe
- meta-perl
- meta-python
- meta-ruby
- meta-systemd
- meta-webserver
- meta-xfce

meta-overc

> The goal of these layers is to create a yocto build which can be deployed on a
modern server to provide a useable environment which in turn can build yocto
(and indeed the variant from this layer itself).  A lot of the heavy lifting
to achieve this has been done by the build-appliance image type of yocto, but
that is limited to virtual deployment, and does not have all the development
tools and/or man pages and things like tab completion that make a system
"useable".  This layer attempts to close that gap.

> Both meta-overc, and meta-overc/meta-cube should be added to your bblayers file.

meta-virtualization

> This layer provides support for building Xen, KVM, Libvirt, and associated
packages necessary for constructing OE-based virtualized solutions.

oe-core

> OpenEmbedded-Core is a layer containing the core metadata for current versions
of OpenEmbedded. It is distro-less (can build a functional image with
DISTRO = "nodistro") and contains only emulated machine support.

oe-meta-go
qemuarm
qemuarm9
wr-base
wr-fixes
wr-kernel
wr-tools-debug
wrlabs-integration
wrlinux
layers/wrll-hac
xilinx-zynq
overc-installer
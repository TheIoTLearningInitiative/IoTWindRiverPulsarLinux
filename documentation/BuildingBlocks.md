Building Blocks
==

## bitbake

> BitBake is co-maintained by the Yocto Project and the OpenEmbedded project. BitBake recipes specify how a particular package is built. It includes all the package dependencies, source code locations, configuration, compilation, build, install and remove instructions. wikipedia

https://github.com/WindRiver-OpenSourceLabs/bitbake

## layers/fslls10xx

> Freescale TWR-LS1021A Boards

- bootloader
- conf 	
- recipes-daemons/ptpd
- recipes-graphics/xorg-xserver
- recipes-kernel/linux

https://github.com/WindRiver-OpenSourceLabs/fsl-ls10xx

## meta-intel

> Layer containing Intel hardware support metadata

- meta-crystalforest
- meta-haswell-wc
- meta-mohonpeak
- meta-valleyisland

git://git.yoctoproject.org/meta-intel

## meta-openembedded

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

git://git.openembedded.org/meta-openembedded

## meta-overc

> The goal of these layers is to create a yocto build which can be deployed on a modern server to provide a useable environment which in turn can build yocto (and indeed the variant from this layer itself).  A lot of the heavy lifting to achieve this has been done by the build-appliance image type of yocto, but that is limited to virtual deployment, and does not have all the development tools and/or man pages and things like tab completion that make a system "useable".  This layer attempts to close that gap.

> Both meta-overc, and meta-overc/meta-cube should be added to your bblayers file.

https://github.com/WindRiver-OpenSourceLabs/meta-overc

## meta-virtualization

> This layer provides support for building Xen, KVM, Libvirt, and associated packages necessary for constructing OE-based virtualized solutions.

git://git.yoctoproject.org/meta-virtualization

## oe-core

> OpenEmbedded-Core is a layer containing the core metadata for current versions of OpenEmbedded. It is distro-less (can build a functional image with DISTRO = "nodistro") and contains only emulated machine support.

- recipes-bsp
- recipes-connectivity
- recipes-core
- recipes-devtools
- recipes-extended
- recipes-gnome
- recipes-graphics
- recipes-kernel
- recipes-lsb4
- recipes-multimedia
- recipes-qt
- recipes-rt
- recipes-sato
- recipes-support

https://github.com/WindRiver-OpenSourceLabs/oe-core

## oe-meta-go

> OpenEmbedded layer for the Go programming language

https://github.com/WindRiver-OpenSourceLabs/oe-meta-go

## qemuarm

> QEMU-ARM Board Support Package

https://github.com/WindRiver-OpenSourceLabs/qemuarm

## qemuarm9

>  QEMU-arma9 Board Support Package

https://github.com/WindRiver-OpenSourceLabs/qemuarma9

## wr-base

> This layer provides many of the base components for Wind River Linux.  It is required by most other layers provided by Wind River

- recipes-base
- recipes-benchmark
- recipes-bsp
- recipes-connectivity
- recipes-core
- recipes-devtools
- recipes-extended
- recipes-graphics
- recipes-installer-support
- recipes-kernel
- recipes-lsbtesting/qt3
- recipes-networking
- recipes-support

https://github.com/WindRiver-OpenSourceLabs/wr-base

## wr-fixes

> This layer provides the fixes to other components of the system
(oe-core, meta-yocto, meta-selinux, etc....)

https://github.com/WindRiver-OpenSourceLabs/wr-fixes

## wr-kernel

This layer:

- adds core kernel support on top of linux-yocto for boards supported by Wind River
- contains packages that are coupled to the kernel version
- contains task sets and configurations related to the kernel
- includes the nested 'kernel-dev' layer for local clones and externalsrc development

https://github.com/WindRiver-OpenSourceLabs/wr-kernel

## wr-tools-debug

> This layer provides target agents to support command line and Workbench debugging.  The tools provided include tcf-agent, agent-proxy and wrproxy.

https://github.com/WindRiver-OpenSourceLabs/wr-tools-debug

## wrlabs-integration

> This layer provides fixes to yocto project layers to allow unmodifed Wind River layers to work in the absence of the full Wind River toolchain.

https://github.com/WindRiver-OpenSourceLabs/wrlabs-integration

## wrlinux

> This layer provides the Wind River Linux distribution definitions, distribution-specific integration and bug fixes, and other wrlinux components.

https://github.com/WindRiver-OpenSourceLabs/wrlinux

## layers/wrll-hac
## xilinx-zynq
## overc-installer
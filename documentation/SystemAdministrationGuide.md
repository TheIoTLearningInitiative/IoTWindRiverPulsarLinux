# System Administration Guide

> Wind River Pulsar Linux is an application-ready Linux distribution that has been certified on select hardware. Pulsar Linux is designed to be simple to install so you can start developing in minutes. Pulsar Linux is a small, secure, high-performance, secure, and manageable image that is certified and bundled with COTS platforms. It includes select packages from the traditional Wind River Linux development environment and its market-specific profiles. [Wind River® Pulsar Linux Getting Started System Administration Guide](https://software.intel.com/en-us/articles/wind-river-pulsar-linux-getting-started-7-0)

- Introduction
- System Architecture Overview
- Container Management
- User Management
- Network Configuration
- Device Updates
- Package Management

## Introduction

### System Architecture Overview

> LXC (Linux Containers) is an operating-system-level virtualization environment for running multiple isolated Linux systems (containers) on a single Linux control host. Wikipedia

> A real-time operating system (RTOS) is an operating system (OS) intended to serve real-time application process data as it comes in, typically without buffering delays. Processing time requirements (including any OS delay) are measured in tenths of seconds or shorter. Wikipedia

> The GNU C Library (glibc) Any Unix-like operating system needs a C library: the library which defines the ``system calls'' and other basic facilities such as open, malloc, printf, exit... The GNU C Library is used as the C library in the GNU system and in GNU/Linux systems, as well as many other systems that use Linux as the kernel. [The GNU C Library (glibc)](https://www.gnu.org/software/libc/)

### Container Management

> The container infrastructure in the Pulsar Linux system is built using Linux containers and OverC, an open source project which provides a software framework for containerization.

### User Management

> Linux enables multiple users to use a single computer, through user accounts.

### Network Configuration

> To support containers and its access requirements, the Pulsar Linux system is configured with a Linux bridge, a virtual switch interface, by default.

### Device Updates

> By default, the Pulsar Linux system is configured to use the Wind River public repository for the most critical Linux updates.

### Package Management

#### Smart Package Manager (SmartPM)

> The Smart Package Manager project has the ambitious objective of creating smart and portable algorithms for solving adequately the problem of managing software upgrades and installation. This tool works in all major distributions and will bring notable advantages over native tools currently in use (APT, APT-RPM, YUM, URPMI, etc).

- [Smart Package Manager Homepage](https://labix.org/smart)

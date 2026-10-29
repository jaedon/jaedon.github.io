---
layout: default
title: "Jaedon Shin | Portfolio (en)"
description: "Senior Embedded Linux System Software Engineer"
locale: en_US
permalink: /en/
---

<style>
  .page-header { display: none !important; }
  .main-content { padding-top: 5rem !important; position: relative; }
  .lang-switcher {
    position: absolute;
    top: 1.5rem;
    right: 0;
    font-size: 1.1rem !important;
    color: #24292e !important;
    z-index: 999;
  }
  .lang-switcher a {
    color: #159957 !important;
    text-decoration: none !important;
    font-weight: bold;
  }
  .lang-switcher a:hover {
    text-decoration: underline !important;
  }
</style>

<div class="lang-switcher">
  <a href="/">ko</a> | <strong>en</strong>
</div>

# Jaedon Shin

Email: jaedon.shin@gmail.com

## Summary

Senior Embedded Linux System Software Engineer with more than 20 years of embedded Linux experience.

Led system software development for Wi-Fi Access Point (AP) and Set-Top Box (STB) platforms: hardware bring-up, bootloader, BSP, Linux kernel and device drivers, media and network stacks, productization, and maintenance.

- End-to-end software development: Built from scratch the hardware bring-up, bootloader, BSP, Linux kernel tuning, device drivers, platform design, large-scale open-source integration, and build infrastructure.

- Media platform development: Built Linux standard interfaces on the Broadcom SDK, tuned the kernel for network, storage, and DVB, and developed V4L2 mem2mem media drivers.

- Wi-Fi AP development: Migrated an RTOS platform to Linux on an Atheros (now Qualcomm) SoC, and optimized the bootloader, kernel, and network stack.

- Operator legacy defect support: For European cable and telecom operators, supported RDK-V integration, CAS integration, and major SDK migration, and analyzed long-standing defects to help stabilize the products. Operators: a European cable operator, a European/South American telecom operator (T), and a European telecom operator (B).

- Open-source contribution and platform extension: Integrated and optimized open-source software, and upstreamed SoC support and driver fixes to Mainline Linux, with kernel compatibility and long-term maintenance in mind.

- Development infrastructure: Introduced CVS, SVN + Trac, and Bazaar/Mercurial. Automated builds and releases with GitHub Actions. Standardized development environments with devcontainers and migrated projects to Git. Built SCM/CI infrastructure on Docker Swarm.

## Experience

Monotag / Founder & Independent Embedded Linux Engineer / 2009.08–Present

- 2021.11–Present: Contract with Humax. Maintenance and technical support of STBs for global broadcast and telecom operators.

- 2009.08–2021.11: Development and supply of open-source STBs for the European retail market.

TmaxCore (now S-Core) / Principal Research Engineer & Mobile OS Development Lead / 2008.06–2009.08

Humax / Assistant Manager & Linux STB Platform Engineer / 2006.08–2008.05

MMC Technology / Senior Research Engineer & Linux System Engineer / 2002.12–2006.08

## Linux Kernel Contributions

SoC support and driver fixes needed for commercial STB development, merged into Mainline Linux (2014–2020, 49 patches).

- Broadcom STB (BMIPS) platform: device nodes and support for UART, I2C, SPI, NAND, SDHCI, GPIO, PWM, SATA/PHY, power management, and watchdog.

- DVB core: unlocked_ioctl and compat_ioctl support in dvb_frontend.

- Driver fixes: ahci_brcmstb, phy_brcmstb_sata, bcmgenet, i2c-brcmstb, sdhci-brcmstb, bcm-qspi, USB 3.0 PHY.

- [Linux kernel commits](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/?qt=author&q=jaedon.shin%40gmail.com)

## Projects

### STB Maintenance and Technical Support for Broadcast and Telecom Operators

Provided software technical support and defect analysis for a European cable operator, a European/South American telecom operator (T), and a European telecom operator (B). Solved problems found during platform operation, and supported a major Broadcom SDK migration.

Analyzed long-standing legacy defects, fixed their root causes, and helped stabilize the services.

#### Expertise

RDK-V, OpenEmbedded (Yocto), HAL, Broadcom SDK, Linux Kernel, Networking (IPv4/IPv6 Dual Stack, DNS, DHCP), CAS, Mass Production

#### Key Achievements

- European cable operator: RDK-V technical support and recovery system networking

  - Optimized the RDK-V HAL layer and stabilized the architecture against hardware changes.

  - Built the networking software in the recovery system (IPv4/IPv6 Dual Stack, DNS, DHCP) to the operator requirements, and integrated it with the operator infrastructure.

  - Analyzed a legacy daemon crash of unknown cause during system boot, and fixed the root cause.

- European/South American telecom operator (T): Broadcom SDK major migration support

  - Supported the Broadcom SDK major version update and the migration of the upper platform software.

  - Modified the Quantenna (now Qualcomm) Wi-Fi driver for the newer Linux kernel that came with the SDK upgrade, and kept it compatible.

  - Handled periodic specification changes of the recovery system, and kept upgrade and downgrade compatible in all paths.

- European telecom operator (B): Audio DSP problem analysis and field reboot fix

  - Debugged an audio failure that was hard to diagnose, and the field reboots it caused, and found the root cause.

  - Showed technically that the cause was at the DSP level, and led the vendor to provide an official patch and the operator to apply it in the field.

  - Resolved a long-standing issue between the operator application software and the HAL.

- Technical support for global operators and factory production stabilization

  - European/Middle East pay-TV operator: Fixed an integration defect between the Opera browser and the network streaming engine.

  - Latin American pay-TV operator: Designed and supported a custom distribution system for stable firmware rollout.

  - Asian cable operator: Answered technical inquiries from the operations team, and supported root-cause analysis of field defects.

  - Production support: Updated production programs for software and hardware changes across many product lines.

- Standardization and migration of source control

  - Many model sources were spread across SVN, with no standard development environment. Built a reproducible build environment based on devcontainers.

  - Selected the projects with frequent maintenance and migrated them to Git.

- Self-built infrastructure and operation

  - As the existing infrastructure was reduced, built and ran SVN/Git mirrors, a file server, Jenkins, and several self-hosted runners on Docker Swarm.

### Open-Source STB Development and Supply for the European Retail Market

Designed an open-source STB platform for the European retail market from the architecture stage, and brought it to production.

Implemented the LinuxTV/DVB standard interfaces, contributed to the upstream kernel in parallel, and supplied a product line connected to the open-source community.

#### Expertise

OpenEmbedded (Yocto), Mainline Linux, Broadcom Magnum Layer, LinuxTV DVB Subsystem, V4L2 mem2mem, ALSA Audio, QtWebEngine, KODI, Realtek, Qualcomm, Wi-Fi, BlueZ

#### Key Achievements

- Linux standard drivers on the Broadcom Magnum layer

  - Used the low-level Magnum API instead of the Broadcom Nexus API, and designed and implemented the Linux standard driver interfaces from scratch.

  - Removed unnecessary upper abstraction layers, simplified the platform structure, and reduced resource usage.

- Media acceleration and standard decoding architecture based on the V4L2 mem2mem interface

  - Implemented HbbTV with a QtWebEngine WebView injection structure, instead of a binary plugin.

  - Designed and developed the kernel V4L2 mem2mem driver interface. This made a media pipeline in which hardware acceleration runs on the standard layer, for both the web environment and the KODI media platform.

- Open-sourced drivers for developer feedback

  - Published driver source code, so that developers can test the firmware and report bugs.

  - Used the technical assets of the community to improve product quality.

- Wireless network and multimedia ALSA audio integration

  - Integrated the Realtek and Qualcomm Wi-Fi drivers and the ALSA audio interface for Bluetooth at kernel level.

  - Built a multimedia environment that supports Wi-Fi and Bluetooth audio.

- OpenEmbedded (Yocto) build system design and operation

  - Designed custom meta layers that support many models, and maintained them for the product lifetime.

  - Automated the release of the product software, such as the kernel and bootloader, with GitHub Actions.

#### Responsibilities

- Linux kernel and BSP architecture: Developed platforms on many Broadcom SoCs, ported the kernel and drivers for kernel version migrations, and built an environment for peripheral optimization.

- Device driver development: DVB drivers on the LinuxTV standard API, and Flash, Network, USB, I2C, SPI, NAND, SDHCI, SATA, and Graphics drivers. Maintained the integration architecture for Wi-Fi/Bluetooth combo chipsets.

- System infrastructure and bootloader design: Designed a custom bootloader for each product, firmware upgrade, root-cause analysis of hardware initialization issues, OpenEmbedded (Yocto) meta layers, and production software.

### Next-Generation Linux STB Platform Development and Validation

Led a project to migrate an RTOS-based STB system fully to a Linux platform on Broadcom.

Designed an adapter layer for Linux, integrated graphics and media standard stacks (LinuxTV, DirectFB, UPnP), and contributed to the technical validation for the move to Linux.

#### Expertise

Broadcom SoC, Linux Kernel, BSP, Hardware Bring-up, Device Driver, Adapter Layer Design, LinuxTV Standard API, VDR, DirectFB UI Engine, UPnP Architecture, PCI/USB Wi-Fi Client Drivers, Wireless Media Streaming Stack

#### Key Achievements

- Legacy RTOS-to-Linux platform migration and adapter layer design

  - Designed an optimized layer and developed drivers, so that the existing RTOS middleware can run again on a standard Linux environment.

  - Built a custom build system for the new Linux platform, and prepared a stable migration and transition process.

- Source control setup: Built the SVN server and source control process right after joining the project. Then introduced the distributed tools Bazaar and Mercurial.

- Open-source media framework validation and system integration

  - Connected the LinuxTV standard API and the VDR runtime, and validated the standard open architecture technically.

  - Validated that various open-source multimedia software architectures can be commercialized on embedded Linux systems.

- DirectFB-based hardware-accelerated graphics UI and multimedia subsystem

  - Implemented a UI rendering pipeline with animation effects in the DirectFB environment.

  - Built a Plug & Play multimedia playback demo to verify the system interfaces.

- Wireless media streaming program for a CES exhibition

  - Ported PCI and USB Wi-Fi drivers to the Broadcom environment, and developed UPnP media server and renderer software.

  - Demonstrated wireless home streaming: the system receives media over a wireless link, and decodes and plays it in real time.

#### Responsibilities

- System infrastructure and integration: Linux kernel for Broadcom SoC-based STBs, cross-compile development environment, hardware initialization, and peripheral drivers.

- Device driver development: Flash, Ethernet, USB, PCI, and Graphics drivers.

- Media and network stack integration: Validated the LinuxTV media interface, and integrated open-source network software and the wireless network.

### Wi-Fi Access Point Development

Migrated an RTOS-based 802.11b AP to an embedded Linux platform, and contributed to the development of the first 802.11a/b/g AP in Korea based on an Atheros (now Qualcomm) single-chip SoC.

Designed and built the full stack, from the lowest hardware level to the bootloader, kernel, network drivers, and a custom build infrastructure. Supplied the product in volume to the service of a Korean telecom operator.

#### Expertise

Wi-Fi 802.11a/b/g, mac80211, madwifi, Ethernet Drivers, Network Subsystem Optimization, Embedded Linux, Samsung ARM SoC, Atheros Single-Chip SoC, Bootloader, Custom Build System, Firmware Upgrade Architecture

#### Key Achievements

- Linux platform setup

  - Developed the bootloader and was responsible for hardware initialization on various SoCs.

  - Developed from scratch the Linux kernel configuration, the Flash and Ethernet driver optimization, and the system software for the product specification. This made a solid embedded Linux system.

- Custom build infrastructure design

  - Built a custom build system and build tree on a cross toolchain, before open-source build frameworks such as Buildroot and Yocto were common.

  - Replaced archive-file version control with CVS, and then SVN. Built the servers, wrote the usage guides, and introduced Trac for issue tracking and a wiki.

  - Introduced source control for the product source code, and built the build pipeline for the whole development team.

- Performance improvement through network driver optimization

  - Ported the latest Atheros (now Qualcomm) reference Wi-Fi driver.

  - Tuned the packet processing of the Ethernet, Bridge, and Wi-Fi drivers and optimized the network connection. This improved wireless throughput and connection stability in the field network of a Korean telecom operator.

#### Responsibilities

- Hardware initialization and Linux platform development: Bootloader development, Linux kernel optimization for each product requirement, and a firmware development environment for each board.

- Wi-Fi driver optimization: Atheros (now Qualcomm) driver performance optimization, and fixes for wireless performance and network connection issues in the field.

- System integration and upgrade system development: A firmware upgrade engine for remote device management, A/B recovery system software, and a custom build system.

### Mobile OS Feasibility Study and Smartphone Platform PoC

In the feature-phone market that Symbian led at that time, proposed a mobile OS business based on a Samsung Mobile SoC, and led a proof-of-concept (PoC) project to validate the core functions.

Established the hardware bring-up base on an early mobile Linux environment, and validated modem stack integration, a touchscreen, and a WebKit-based interface. This confirmed that the product was feasible.

#### Key Achievements

- Mobile environment and OS bring-up base on a Samsung Mobile SoC

  - Ported the embedded Linux kernel and developed peripheral device drivers, optimized for the Samsung Mobile SoC specification.

  - Designed the runtime environment of the OS and the upper mobile applications for the limited resources of a mobile device.

  - Developed demos of the first required smartphone applications.

  - Integrated a 3G modem.

- WebKit-based full browsing and media integration

  - Cross-compiled the WebKit browser engine and ported it with memory optimization.

  - Built a full-browsing rendering environment for a touch display and optimized memory usage. This validated the web usability that a next-generation smartphone platform needs.

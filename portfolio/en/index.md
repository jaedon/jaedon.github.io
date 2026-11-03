---
layout: default
title: "Jaedon Shin | Portfolio (en)"
description: "Embedded Linux System Software Engineer"
locale: en_US
permalink: /portfolio/en/
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
  <a href="/portfolio/">ko</a> | <strong>en</strong>
</div>

# Jaedon Shin

Email: jaedon.shin@gmail.com

## Professional Summary

Embedded Linux systems software engineer with over 20 years of experience. Led system software development across Set-Top Box (STB) and Wi-Fi Access Point (AP) platforms, covering Board bring-up, Bootloaders, Board Support Packages (BSPs), Linux kernel, device drivers, networking and media stacks, build systems, CI/CD, and production software. Also managed the manufacturing process for retail STBs for the European market and contributed to the Linux kernel upstream.

- Hardware: Board bring-up and BSP development for new ARM/MIPS SoC-based boards using schematics and datasheets
- Bootloaders: Bootloader development using U-Boot, CFE, BOLT, and RedBoot; design of product-specific custom Bootloaders
- Linux kernel: Linux kernel and driver porting for various Broadcom SoCs, kernel upgrade support, and kernel configuration optimization
- Media: Design and implementation of Linux standard driver interfaces based on the Broadcom Magnum API (LinuxTV DVB, V4L2 mem2mem); HbbTV integration using QtWebEngine, KODI integration, and ALSA audio integration
- Wi-Fi: Bootloader, Linux kernel, and network stack optimization on Atheros (Qualcomm) SoCs; porting of Broadcom, Realtek, Qualcomm, and Quantenna Wi-Fi drivers
- Device drivers: Development of Ethernet, Wi-Fi, and peripheral drivers (Flash, NAND, USB, I2C, SPI, SDHCI, SATA); DMA and interrupt handling design; hardware issue analysis at register level
- Firmware updates: Firmware update engine, A/B partitioning and rollback, recovery software, and integration with operator OTA systems
- Platform migration: Migration from RTOS to Linux for Wi-Fi APs and next-generation STBs; adapter layer design
- Manufacturing: Manufacturer selection, production line visits, production software development, and software distribution and version management by production lot
- Technical support: RDK-V integration, CAS security solution support, major SDK upgrades, and root-cause analysis and fixes for long-standing issues
- Open-source contributions: Linux kernel upstream contributions, including updates to Broadcom BMIPS, bcmgenet, ahci_brcmstb, and sdhci-brcmstb
- Development infrastructure: Custom OpenEmbedded (Yocto) meta-layer development; introduction of SVN, Trac, Bazaar, and Mercurial; devcontainer-based reproducible build environments and migration to Git; CI implementation using GitHub Actions and Jenkins

## Professional Experience

- MONOTAG \| Independent Contractor (Humax outsourced development contract) \| STB development and technical support for global broadcast and telecommunications operators \| 2021.11–Present
- MONOTAG \| Independent Business Owner (Joint business) \| Development and manufacturing of retail STBs for the European market \| 2009.08–2021.11
- TmaxCore (now S-Core) \| Principal Research Engineer \| 2008.06–2009.08
- Humax \| Assistant Manager \| 2006.08–2008.05
- MMC Technology \| Senior Research Engineer \| 2002.12–2006.08

## Linux Kernel Contributions

Upstreamed changes to Broadcom SoCs and the DVB subsystem in the Linux kernel (2014–2020, 49 patches, [commit history](/linux/)).

- BMIPS: Power management, watchdog, Device Tree, and related areas
- Drivers: bcmgenet, ahci_brcmstb, sdhci-brcmstb, bcm-qspi, i2c-brcmstb, and others
- DVB core: Added `unlocked_ioctl` and `compat_ioctl` support to `dvb_frontend`

## Selected Projects

### STB Development and Technical Support for Broadcast and Telecommunications Operators

Core technologies: RDK-V, HAL, Embedded Linux, Linux kernel, OpenEmbedded (Yocto), Networking, IPv4/IPv6, Wi-Fi, OTA, CAS, Firmware Recovery, Broadcom SDK, Quantenna, CI/CD, Jenkins, GitHub Actions, Docker

Analyzed and fixed root causes of long-standing issues for broadcast and telecommunications operators, resolved field issues, and improved service stability. Also supported major SDK upgrades.

- European cable operator L
  - Stabilized RDK-V HAL and software in response to hardware changes
  - Implemented WPA3-SAE support on a Broadcom Wi-Fi chipset
  - Implemented IPv4/IPv6 dual-stack support, DNS, and DHCP in recovery software to meet operator requirements, and integrated it with the OTA infrastructure
  - Analyzed intermittent crashes that were difficult to reproduce and fixed their root causes
- European and South American telecommunications operator T
  - Supported a major SDK upgrade
  - Supported middleware migration
  - Ported the Quantenna (Qualcomm) Wi-Fi driver to accommodate Linux kernel changes
  - Addressed recurring specification changes in recovery software
  - Ensured compatibility during software rollback
- European telecommunications operator B
  - Modernized legacy build and CI/CD pipelines
  - Investigated a field reboot issue associated with an audio failure and identified its root cause
  - Resolved long-standing issues between the operator's application software and the HAL
- Technical support and production process stabilization
  - European/Middle Eastern pay-TV operator D: Fixed connectivity issues in the Opera browser and network streaming software
  - Central/South American pay-TV operator C: Designed a custom deployment system for reliable firmware rollouts
  - Asian cable operator J: Responded to technical inquiries and analyzed the root causes of field bugs
  - Production support: Developed production software to accommodate software and hardware changes across multiple products
- Build environment, version control, and CI/CD infrastructure
  - Built a reproducible devcontainer-based build environment when source code for multiple models was distributed across SVN repositories and no standardized development environment existed
  - Migrated selected projects with frequent development activity to Git
  - In response to reduced infrastructure, built and operated a Docker Swarm-based SVN/Git mirror, file server, Jenkins, and multiple self-hosted runners

### Retail STB Development and Manufacturing for the European Market

Core technologies: Embedded Linux, Linux kernel, BSP, Bootloader, Board bring-up, OpenEmbedded (Yocto), Broadcom SoC, Broadcom Magnum API, LinuxTV DVB, V4L2 mem2mem, ALSA, QtWebEngine, KODI, HbbTV, Wi-Fi, Bluetooth, device drivers, GitHub Actions

Designed and productized an open-source STB platform for the European retail market, starting at the architecture stage. Developed software based on standard Linux driver interfaces and supplied production software to manufacturing partners. In parallel with product development, contributed to the Linux kernel upstream. Also released various driver sources publicly and used community testing and bug reports to improve product quality.

- Board bring-up and Bootloader
  - Designed product-specific Bootloaders and developed BSPs for various Broadcom SoCs
  - Ported drivers for Linux kernel upgrades and analyzed Board bring-up issues
- Linux standard driver implementation based on Broadcom Magnum
  - Designed and implemented Linux standard driver interfaces using the Magnum API instead of the Nexus API
  - Simplified the architecture and reduced resource usage by removing redundant upper abstraction layers
- Hardware decoder architecture based on V4L2 mem2mem
  - Implemented HbbTV using a QtWebEngine WebView injection architecture instead of binary plugins
  - Designed and developed V4L2 mem2mem drivers to complete a media pipeline in which the hardware decoder operated through standard APIs in both web applications and KODI
- Driver source release and community feedback
  - Established a channel for developers to test firmware directly and report bugs, then incorporated reported issues into product quality improvements
- Wi-Fi and Bluetooth audio integration
  - Developed Realtek and Qualcomm Wi-Fi driver support and an ALSA audio interface for Bluetooth
- OpenEmbedded (Yocto)-based build system
  - Designed and maintained meta-layers supporting multiple product models
  - Automated product software releases—including the Linux kernel, Bootloader, device drivers, and production software—using GitHub Actions
- Manufacturing management and production
  - Managed manufacturing of retail STBs for the European market, visited production lines, developed production software, and managed software distribution and versions by production lot
  - Worked with manufacturing partners on shipment validation and defect analysis

### Next-Generation Linux STB Platform Development and Validation

Core technologies: Embedded Linux, Linux kernel, BSP, Board bring-up, device drivers, RTOS-to-Linux migration, adapter layer design, LinuxTV DVB, VDR, DirectFB, UPnP, Broadcom SoC, MIPS, cross-toolchain

Led a next-generation STB platform project to fully migrate an existing RTOS-based STB platform to Linux on Broadcom SoCs. Designed an adapter layer to reuse RTOS middleware on Linux and integrated graphics and media standards stacks, including LinuxTV, DirectFB, and UPnP, to validate the technical feasibility of the Linux platform.

- Linux kernel and driver development on Broadcom SoCs
  - Performed Board bring-up, established a cross-toolchain environment, and developed Flash, Ethernet, USB, PCI, and graphics drivers
- RTOS-to-Linux platform migration and adapter layer design
  - Designed the adapter layer and developed drivers to reuse RTOS middleware on Linux
  - Built a custom build system for the next-generation Linux platform
- Open-source media framework evaluation and integration
  - Validated an open architecture by integrating the LinuxTV DVB API with VDR
  - Evaluated the feasibility of commercializing open-source multimedia software on embedded Linux
- Hardware-accelerated graphics UI and multimedia subsystem based on DirectFB
  - Implemented a UI rendering pipeline with animation effects in a DirectFB environment
  - Developed a Plug & Play multimedia playback demo
- Wireless media streaming demo for CES
  - Ported PCI/USB Wi-Fi drivers to Broadcom SoCs and developed UPnP media server/renderer software
  - Successfully demonstrated home streaming with real-time decoding and playback of media received over a wireless connection
- Source code management (SCM)
  - Set up an SVN server shortly after joining the project, then introduced the distributed version control systems Bazaar and Mercurial

### Wi-Fi Access Point Development

Core technologies: Embedded Linux, Linux kernel, BSP, Bootloader, Board bring-up, Atheros (Qualcomm) SoC, Wi-Fi 802.11a/b/g, mac80211, network subsystem optimization, Ethernet, Bridge, firmware update, A/B recovery, custom build system

Developed 802.11a/b/g APs based on Atheros (Qualcomm) SoCs. Delivered products to a domestic telecommunications operator after developing the platform from Board bring-up and Bootloader through the Linux kernel, Ethernet/Wi-Fi drivers, and a custom build system.

- Linux platform development
  - Developed Bootloaders and took responsibility for Board bring-up across various SoCs
  - Optimized Linux kernel configuration, Flash and Ethernet drivers, and other system software for product requirements
- Custom build system and version control adoption
  - Developed a custom build system and build tree based on a cross-toolchain
  - Replaced archive-based version management with CVS and later SVN; set up servers, wrote user guides, and introduced the Trac issue tracker and wiki
  - Established build environments for the entire development team
- Network driver optimization
  - Ported reference Wi-Fi drivers from Atheros (Qualcomm)
  - Improved wireless throughput and connection stability in the field by optimizing packet-processing paths in Ethernet, Bridge, and Wi-Fi drivers
- Firmware update and recovery software
  - Developed a remote firmware update engine, A/B partitioning, and rollback functionality

### Mobile OS Technology Evaluation and Smartphone Platform PoC

Core technologies: Embedded Linux, Linux kernel, Samsung mobile SoC, Board bring-up, device drivers, WebKit, 3G modem, touchscreen, cross-compilation

Against the background of a mobile OS market led by Symbian, proposed an OS business based on Samsung mobile SoCs and led a PoC to validate its key functions. Evaluated product feasibility through Board bring-up, 3G modem integration, touchscreen support, and a WebKit-based UI.

- Linux mobile OS platform development
  - Ported the Linux kernel and developed peripheral drivers for Samsung mobile SoCs
  - Designed the OS and mobile application execution environment for memory-constrained systems
  - Developed basic application demos and integrated a 3G modem
- Full web browsing based on WebKit
  - Cross-compiled and optimized the WebKit engine for the target platform
  - Implemented full web browsing and rendering for touchscreen operation and evaluated web usability

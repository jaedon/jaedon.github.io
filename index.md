---
layout: default
title: "Jaedon Shin | Portfolio (ko)"
description: "Senior Embedded Linux System Software Engineer"
locale: ko_KR
permalink: /
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

# 신재돈

Email: jaedon.shin@gmail.com

## 경력요약

20년 이상의 임베디드 리눅스 개발 경험을 보유한 Senior Embedded Linux System Software Engineer입니다.

Wi-Fi Access Point (AP) 및 Set-Top Box (STB) 플랫폼의 하드웨어 초기화부터 부트로더, BSP, 리눅스 커널 및 디바이스 드라이버 개발, 미디어 및 네트워크 스택, 제품화와 유지보수까지 시스템 소프트웨어 전반을 리드했습니다.

- 엔드투엔드 소프트웨어 구축: 스크래치 단계부터 하드웨어 초기화, 부트로더, BSP, 리눅스 커널 최적화 및 디바이스 드라이버 개발, 플랫폼 설계, 대규모 오픈소스 소프트웨어 연동 및 빌드 인프라 구축

- 미디어 플랫폼 개발: Broadcom SDK 리눅스 표준 인터페이스 구축, 네트워크, 스토리지, DVB 등 커널 최적화, V4L2 mem2mem 기반 미디어 드라이버 개발

- Wi-Fi AP 개발: Atheros (현 Qualcomm) SoC 기반 RTOS-to-Linux 플랫폼 전환과 부트로더, 커널, 네트워크 스택 최적화

- 방송 통신 사업자 레거시 결함 대응: 유럽 케이블 사업자, 유럽/남미 통신 사업자 T, 유럽 통신 사업자 B 등 유럽 방송 통신 사업자 대상 RDK-V 연동, CAS 보안 솔루션 지원, 메이저 SDK 마이그레이션, 장기 미해결 결함 분석 및 안정화 지원

- 오픈소스 생태계 기여 및 플랫폼 확장: 오픈소스 소프트웨어 통합 및 최적화, 커널 호환성과 장기 유지보수를 고려한 설계 역량을 바탕으로 Mainline Linux에 SoC 지원 및 드라이버 수정 반영

- 개발 인프라 구축: CVS, SVN + Trac, Bazaar/Mercurial 도입, GitHub Actions 기반 빌드 및 릴리스 자동화, devcontainer 개발 환경 표준화 및 Git 이전, Docker Swarm 기반 SCM/CI 인프라 구축

## 주요경력

모노탁 / 대표 & Independent Embedded Linux Engineer / 2009.08-현재

- 2021.11-현재: 휴맥스 외주개발계약 - 글로벌 방송 통신 사업자 STB 유지보수 및 기술지원

- 2009.08-2021.11: 유럽 리테일 시장용 오픈소스 STB 개발 및 공급

티맥스코어 (현 에스코어) / 책임연구원 & Mobile OS Development Lead / 2008.06-2009.08

휴맥스 / 대리 & Linux STB Platform Engineer / 2006.08-2008.05

엠엠씨테크놀로지 / 선임연구원 & Linux System Engineer / 2002.12-2006.08

## 리눅스 커널 개발 기여

상용 STB 개발 중 필요한 SoC 지원과 드라이버 수정을 Mainline Linux에 반영 (2014~2020, 49개 패치)

- Broadcom STB (BMIPS) 플랫폼: UART, I2C, SPI, NAND, SDHCI, GPIO, PWM, SATA/PHY 장치 노드, 전원 관리, watchdog 지원

- DVB 코어: dvb_frontend의 unlocked_ioctl/compat_ioctl 지원

- 드라이버 수정: ahci_brcmstb, phy_brcmstb_sata, bcmgenet, i2c-brcmstb, sdhci-brcmstb, bcm-qspi, USB 3.0 PHY

- [리눅스 커널 커밋 내역](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/?qt=author&q=jaedon.shin%40gmail.com)

## 주요프로젝트

### 방송 통신 사업자용 STB 유지보수 및 기술지원

유럽 케이블 사업자, 유럽/남미 통신 사업자 T, 유럽 통신 사업자 B 등을 대상으로 소프트웨어 기술지원, 결함 분석 및 플랫폼의 운영 중 발생한 문제를 해결하고 Broadcom SDK의 메이저 마이그레이션을 지원했습니다.

장기간 해결되지 않았던 레거시 결함과 난제를 분석하여 근본 원인을 수정하고, 서비스 안정화에 기여했습니다.

#### 전문분야

RDK-V, OpenEmbedded (Yocto), HAL, Broadcom SDK, Linux Kernel, Networking (IPv4/IPv6 Dual Stack, DNS, DHCP), CAS, Mass Production

#### 핵심성과

- 유럽 케이블 사업자: RDK-V 기술지원 및 복구 시스템 네트워크 고도화

  - RDK-V HAL 레이어 최적화 및 하드웨어 변동에 맞춰 아키텍처 안정화 수행

  - 복구 시스템 내 IPv4/IPv6 Dual Stack, DNS, DHCP 등 네트워킹 소프트웨어를 요구사항에 맞춰 구축하여 사업자 인프라와 연동

  - 시스템 부팅 과정 중 발생하던 레거시 데몬의 원인 불명 크래시 결함을 분석하여 근본 원인 수정

- 유럽/남미 통신 사업자 T: Broadcom SDK 메이저 마이그레이션 지원

  - Broadcom SDK 메이저 버전 업데이트 및 상위 플랫폼 소프트웨어 전환 작업 지원

  - SDK 업그레이드에 따른 리눅스 커널 버전 상승에 맞춰 Quantenna (현 Qualcomm) Wi-Fi 드라이버를 수정하여 호환성 확보

  - 복구 시스템의 주기적인 사양 변경에 대응하고, 업그레이드 및 다운그레이드 전 과정에서 상호 호환성 확보

- 유럽 통신 사업자 B: 오디오 DSP 문제 분석 및 필드 리부팅 문제 해결

  - 원인 파악이 어려웠던 오디오 장애 현상과 이로 인한 필드 내 리부팅 문제를 디버깅하여 근본 원인 규명

  - 원인이 DSP 레벨의 문제임을 기술적으로 입증하여, 벤더의 공식 패치 제공 및 필드 적용 유도

  - 사업자의 애플리케이션 소프트웨어와 HAL 간의 장기 미결 이슈 해결

- 글로벌 사업자 기술 지원 및 공장 생산 프로세스 안정화

  - 유럽/중동 유료 방송 사업자: Opera 브라우저 및 네트워크 스트리밍 엔진 간 연동 결함 수정

  - 중남미 유료 방송 사업자: 안정적인 펌웨어 롤아웃을 위한 맞춤형 배포 시스템 설계 및 운영 지원

  - 아시아 케이블 사업자: 운영팀 기술 문의 대응 및 필드 결함 원인 분석 지원

  - 생산지원: 다양한 제품 라인업의 소프트웨어, 하드웨어 변경점에 따른 생산 프로그램 변경 지원

- 표준화 및 형상 관리 이전

  - 다수 모델의 소스가 SVN에 분산되고 표준 개발 환경이 없던 상태에서, devcontainer 기반 재현 가능한 빌드 환경을 구축

  - 유지보수 빈도가 높은 프로젝트를 선별하여 Git으로 이전

- 인프라 자체 구축 및 운영

  - 기존 인프라 축소에 대응하여 Docker Swarm 기반으로 SVN/Git 미러, 파일 서버, Jenkins, 다양한 Self-hosted Runner를 구축하고 운영

### 유럽 리테일 시장용 오픈소스 STB 개발 및 공급

유럽 리테일 시장을 타겟으로 오픈소스 STB 플랫폼을 아키텍처 단계부터 설계하고 제품화에 성공했습니다.

LinuxTV/DVB 표준 인터페이스를 구현하고 커널 업스트림 기여를 병행하며, 오픈소스 커뮤니티와 연계한 제품 라인업을 공급했습니다.

#### 전문분야

OpenEmbedded (Yocto), Mainline Linux, Broadcom Magnum Layer, LinuxTV DVB Subsystem, V4L2 mem2mem, ALSA Audio, QtWebEngine, KODI, Realtek, Qualcomm, Wi-Fi, BlueZ

#### 핵심성과

- Broadcom Magnum 레이어 기반 리눅스 표준 드라이버 구현

  - Broadcom Nexus API 대신 하위 로우레벨 레이어인 Magnum API를 이용하여 리눅스 표준 드라이버 인터페이스를 스크래치 단계부터 직접 설계 및 구현

  - 불필요한 상위 추상화 계층을 제거하고 플랫폼 구조를 단순화하여 리소스 사용량을 감소

- V4L2 mem2mem 인터페이스 기반 미디어 가속 및 표준 디코딩 아키텍처 구축

  - HbbTV를 바이너리 플러그인 방식 대신 QtWebEngine WebView 인젝션 구조로 구현

  - 커널 V4L2 mem2mem 드라이버 인터페이스 설계 및 개발하여 웹 환경과 KODI 미디어 플랫폼에서 하드웨어 가속이 표준 레이어 기반으로 구동되는 미디어 파이프라인 완성

- 드라이버 오픈소스화를 통한 개발자 피드백 채널 확보

  - 각종 드라이버 소스코드를 공개하여 개발자들이 직접 펌웨어를 테스트하고 버그 리포트를 공유할 수 있는 채널 확보

  - 커뮤니티의 기술 자산을 제품 품질 개선에 반영

- 무선 네트워크 및 멀티미디어 ALSA 오디오 시스템 통합

  - Realtek 및 Qualcomm의 Wi-Fi 드라이버와 Bluetooth용 ALSA 오디오 인터페이스를 커널 레벨에서 통합

  - Wi-Fi 및 Bluetooth 오디오를 지원하는 멀티미디어 환경 구현

- OpenEmbedded (Yocto) 기반 빌드 시스템 설계 및 운영

  - 다수 모델을 지원하는 자체 메타 레이어를 설계하고 제품 수명 기간 동안 유지보수

  - GitHub Actions 기반으로 커널, 부트로더 등 제품 소프트웨어 릴리스를 자동화

#### 담당업무

- 리눅스 커널 및 BSP 아키텍처: 다양한 Broadcom SoC 기반 플랫폼 개발, 커널 버전 마이그레이션에 따른 커널 및 드라이버 포팅, 주변장치 구동 최적화 환경 구축

- 디바이스 드라이버 개발: LinuxTV 표준 API 기반 DVB 드라이버, Flash, Network, USB, I2C, SPI, NAND, SDHCI, SATA, Graphics Driver 개발 및 Wi-Fi/Bluetooth 콤보 칩셋 연동 아키텍처 유지보수

- 시스템 인프라 및 부트로더 설계: 제품별 커스텀 부트로더 설계, 펌웨어 업그레이드, 하드웨어 초기화 이슈 원인 규명, OpenEmbedded (Yocto) 메타 레이어 및 생산 소프트웨어 개발

### 차세대 리눅스 STB 플랫폼 개발 및 검증

기존 RTOS 기반의 STB 시스템을 Broadcom 기반 리눅스 플랫폼으로 전면 마이그레이션하는 차세대 STB 플랫폼 개발 프로젝트를 주도했습니다.

리눅스를 위한 어댑터 레이어를 설계하고, LinuxTV, DirectFB, UPnP 등 그래픽 및 미디어 표준 스택을 통합하여 리눅스 플랫폼 전환에 필요한 기술 검증에 기여했습니다.

#### 전문분야

Broadcom SoC, Linux Kernel, BSP, Hardware Bring-up, Device Driver, Adapter Layer Design, LinuxTV Standard API, VDR, DirectFB UI Engine, UPnP Architecture, PCI/USB Wi-Fi Client Drivers, Wireless Media Streaming Stack

#### 핵심성과

- 레거시 RTOS-to-Linux 플랫폼 마이그레이션 및 어댑터 레이어 설계

  - 기존 RTOS 미들웨어를 표준 리눅스 환경 위에서 재사용할 수 있도록 최적화된 레이어 설계 및 드라이버 개발

  - 차세대 리눅스 플랫폼에 맞춰 독자 빌드시스템을 구축하여 안정적인 마이그레이션 및 전환 체계 마련

- 프로젝트 합류 직후 SVN 서버 구축 및 형상 관리 체계 구축, 이후 분산 관리 도구인 Bazaar와 Mercurial 도입

- 오픈소스 미디어 프레임워크 검증 및 시스템 통합

  - LinuxTV 표준 API 및 VDR 실행 환경을 연동하여 표준 개방형 아키텍처 환경에 대한 기술적 검증

  - 임베디드 리눅스 시스템에서 다양한 오픈소스 멀티미디어 소프트웨어 아키텍처의 상용화 가능성 검증

- DirectFB 기반 하드웨어 가속 그래픽 UI 및 멀티미디어 서브시스템 구현

  - DirectFB 환경에서 애니메이션 효과를 포함한 UI 렌더링 파이프라인 구현

  - Plug & Play 기반의 멀티미디어 재생 데모를 구축하여 시스템 인터페이스의 동작 검증

- CES 전시용 무선 미디어 스트리밍 프로그램 개발

  - PCI 및 USB 기반의 Wi-Fi 드라이버를 Broadcom 환경에 포팅하고, UPnP 미디어 서버 및 렌더러 소프트웨어 개발

  - 무선 환경에서 미디어를 전송받아 실시간 디코딩 및 재생하는 무선 홈 스트리밍 기술 시연에 성공

#### 담당업무

- 시스템 인프라 구축 및 통합: Broadcom SoC 기반 STB Linux 커널 개발, 크로스 컴파일 개발 환경 및 하드웨어 초기화, 주변장치 드라이버 개발

- 디바이스 드라이버 개발: Flash, Ethernet, USB, PCI 및 Graphics 드라이버 개발

- 미디어와 네트워크 스택 통합: LinuxTV 미디어 인터페이스 검증, 오픈소스 네트워크 소프트웨어 및 무선 네트워크 연동

### Wi-Fi Access Point 개발

기존 RTOS 802.11b AP 환경을 임베디드 리눅스 플랫폼으로 전환하고, 국내 최초의 Atheros(현 Qualcomm) 원칩 SoC 기반 802.11a/b/g AP 개발에 기여했습니다.

하드웨어 최하단부터 부트로더, 커널, 네트워크 드라이버 및 독자적인 빌드 인프라까지 전 과정을 설계하고 구축하여 국내 통신 사업자 서비스에 제품의 대량 공급을 진행했습니다.

#### 전문분야

Wi-Fi 802.11a/b/g, mac80211, madwifi, Ethernet Drivers, Network Subsystem Optimization, Embedded Linux, Samsung ARM SoC, Atheros Single-Chip SoC, Bootloader, Custom Build System, Firmware Upgrade Architecture

#### 핵심성과

- 리눅스 플랫폼 환경 구축

  - Bootloader 개발 및 다양한 SoC 기반의 하드웨어 초기화 전담

  - 제품 사양에 최적화된 Linux Kernel 설정, Flash 및 Ethernet Driver 최적화와 System Software를 직접 스크래치 단계부터 개발하여 임베디드 리눅스 기반 시스템 구축

- 독자적 커스텀 빌드 인프라 설계

  - 표준 Buildroot나 Yocto 등의 오픈소스 빌드 프레임워크가 보급되기 전, 크로스 툴체인 기반의 독자적인 빌드 시스템 및 빌드 트리 구축

  - 압축 파일 기반의 버전 관리를 CVS, 이어서 SVN으로 전환하고, 서버 구축 및 사용 가이드 작성, Trac 기반 이슈 트래킹과 위키 운영 체계 도입

  - 제품 소스코드 형상 관리를 도입하고 전체 개발 팀의 빌드 파이프라인 구축

- 네트워크 드라이버 최적화를 통한 성능 개선

  - Atheros (현 Qualcomm) 최신 레퍼런스 Wi-Fi 드라이버 이식

  - Ethernet, Bridge, Wi-Fi 드라이버의 패킷 처리 프로세스 튜닝 및 네트워크 연결 최적화를 통해, 국내 통신 사업자 필드 망에서 무선 전송 속도와 접속 안정성을 개선

#### 담당업무

- 하드웨어 초기화 및 리눅스 플랫폼 개발: 부트로더 개발 및 제품 요구사항별 리눅스 커널 최적화, 보드 맞춤형 펌웨어 개발 환경 구축

- Wi-Fi 드라이버 최적화: Atheros(현 Qualcomm) 드라이버 성능 최적화, 필드 환경에서의 무선 성능 및 네트워크 연결 이슈 해결

- 시스템 연동 및 업그레이드 체계 개발: 장비의 원격 관리를 위한 펌웨어 업그레이드 엔진, A/B 복구 시스템 소프트웨어, 독자 빌드 시스템 개발

### 모바일 OS 기술검증 및 스마트폰 플랫폼 PoC

Symbian이 주도하던 피처폰 시장 환경을 배경으로 Samsung Mobile SoC 기반 모바일 OS 사업을 제안하고, 핵심 기능의 타당성을 검증하는 PoC 프로젝트를 주도했습니다.

초기 모바일 리눅스 환경에서 하드웨어 구동 기반을 확보하고, 모뎀 스택 통합 및 터치스크린과 WebKit 기반 인터페이스를 검증하여 제품화 가능성을 확인했습니다.

#### 핵심성과

- Samsung Mobile SoC 기반 모바일 환경 및 OS 구동 기반 구축

  - Samsung Mobile SoC 사양에 최적화된 임베디드 리눅스 커널 포팅 및 주변장치 디바이스 드라이버 개발

  - 모바일 임베디드 리소스 환경에서 OS 및 상위 모바일 응용 소프트웨어의 실행 환경 설계

  - 스마트폰 초기 필요 애플리케이션 데모 개발

  - 3G 모뎀 통합

- WebKit 기반 풀 브라우징 및 미디어 연동

  - WebKit 브라우저 엔진을 크로스 컴파일 및 메모리 최적화 포팅 수행

  - 터치 디스플레이 환경에 맞춘 풀 브라우징 렌더링 환경을 구축하고 메모리 사용량을 최적화하여 차세대 스마트폰 플랫폼이 요구하는 웹 사용성 검증

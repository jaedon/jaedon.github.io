---
layout: default
title: "Jaedon Shin | Portfolio (ko)"
description: "Embedded Linux System Software Engineer"
locale: ko_KR
permalink: /portfolio/
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
  <strong>ko</strong> | <a href="/portfolio/en/">en</a>
</div>

# 신재돈

Email: jaedon.shin@gmail.com

## 경력 요약

20년 이상 Embedded Linux 시스템 소프트웨어를 개발해 온 엔지니어로, Set-Top Box(STB)와 Wi-Fi Access Point(AP) 플랫폼의 Board bring-up, Bootloader, Board Support Package(BSP), Linux kernel, Device drivers, 네트워크·미디어 스택, 빌드 시스템 및 CI/CD부터 양산 소프트웨어까지 시스템 소프트웨어 전반을 주도했습니다. 유럽 리테일향 STB의 개발부터 제조 관리까지 직접 수행했으며, Linux kernel upstream에도 기여했습니다.

- 하드웨어: 회로도와 데이터시트 기반 ARM/MIPS SoC 신규 보드의 Board bring-up 및 BSP 개발
- Bootloader: U-Boot, CFE, BOLT, RedBoot 등 Bootloader 개발, 제품별 커스텀 Bootloader 설계
- Linux kernel: 다양한 Broadcom SoC의 Linux kernel 및 드라이버 포팅, 업그레이드 대응 및 설정 최적화
- 미디어: Broadcom Magnum API 기반 Linux 표준 드라이버 인터페이스(LinuxTV DVB, V4L2 mem2mem) 설계 및 구현, HbbTV(QtWebEngine), KODI 연동, ALSA 오디오 통합
- Wi-Fi: Atheros(Qualcomm) SoC 기반 Bootloader, Linux kernel, 네트워크 스택 최적화, Broadcom/Realtek/Qualcomm/Quantenna Wi-Fi 드라이버 포팅
- 드라이버: Ethernet, Wi-Fi, 주변장치(Flash, NAND, USB, I2C, SPI, SDHCI, SATA) 드라이버 개발, DMA 및 인터럽트 처리 설계, 레지스터 수준의 하드웨어 이슈 해결
- 펌웨어 업데이트: 펌웨어 업데이트 엔진, A/B 파티션 이중화 및 롤백, 리커버리 소프트웨어, 사업자 OTA 연동
- 플랫폼 전환: RTOS에서 Linux로 마이그레이션(Wi-Fi AP, 차세대 STB), 어댑터 레이어 설계
- 제조 관리: 제조사 선정, 생산 라인 방문, 양산 소프트웨어 개발, 생산 로트별 소프트웨어 배포 및 버전 관리
- 기술 지원: RDK-V 연동, CAS 보안 솔루션 지원, SDK 메이저 업그레이드, 장기 미결 이슈 원인 분석 및 수정
- 오픈소스 기여: Linux kernel upstream 기여(Broadcom BMIPS, DVB subsystem, bcmgenet, ahci_brcmstb, sdhci-brcmstb 등 수정)
- 개발 인프라: OpenEmbedded(Yocto) 커스텀 메타 레이어, SVN, Trac, Bazaar, Mercurial 도입, devcontainer 기반 빌드 환경 구축 및 Git 이전, GitHub Actions와 Jenkins 기반 CI 구축

## 경력 사항

- 모노탁 \| 개인사업자(휴맥스 외주 개발 계약), 글로벌 방송 통신 사업자 STB 개발 및 기술 지원 \| 2021.11-현재
- 모노탁 \| 개인사업자(공동 사업), 유럽 리테일향 STB 개발 및 제조 \| 2009.08-2021.11
- 티맥스코어(현 에스코어) \| 책임연구원 \| 2008.06-2009.08
- 휴맥스 \| 대리 \| 2006.08-2008.05
- 엠엠씨테크놀로지 \| 선임연구원 \| 2002.12-2006.08

## Linux kernel 기여

Broadcom SoC 및 DVB subsystem 관련 수정 사항을 Linux kernel upstream에 반영(2014~2020, 49개 패치, [커밋 내역](/linux/))

- BMIPS: power management, watchdog, Device Tree 등
- 드라이버: bcmgenet, ahci_brcmstb, sdhci-brcmstb, bcm-qspi, i2c-brcmstb 등
- DVB core: dvb_frontend의 unlocked_ioctl/compat_ioctl 추가

## 주요 프로젝트

### 방송 통신 사업자용 STB 개발 및 기술 지원

전문분야: RDK-V, HAL, Embedded Linux, Linux kernel, OpenEmbedded(Yocto), Networking, IPv4/IPv6, Wi-Fi, OTA, CAS, Firmware Recovery, Broadcom SDK, Quantenna, CI/CD, Jenkins, GitHub Actions, Docker

방송 통신 사업자 대상으로 장기 미결 이슈의 근본 원인을 분석해 수정하고, 필드 이슈를 해결해 서비스를 안정화했습니다. SDK 메이저 업그레이드와 미들웨어 전환을 지원했습니다.

- 유럽 케이블 사업자 L
  - 하드웨어 변동에 맞춰 RDK-V HAL 및 소프트웨어 안정화 수행
  - Broadcom Wi-Fi 기반 WPA3-SAE 지원 기능 구현
  - 사업자 요구사항에 맞춰 리커버리 소프트웨어에 IPv4/IPv6 Dual Stack, DNS, DHCP를 구현하고 OTA 인프라와 연동
  - 2년 이상 해결되지 않던 간헐적 크래시를 투입 직후 원인 파악 및 수정
- 유럽/남미 통신 사업자 T
  - SDK 메이저 업그레이드 지원
  - 미들웨어 전환 작업 지원
  - Linux kernel 변경에 따라 Quantenna(Qualcomm) Wi-Fi 드라이버 포팅
  - 리커버리 소프트웨어의 주기적인 사양 변경에 대응
  - 소프트웨어 롤백 과정에서 상호 호환성 확보
- 유럽 통신 사업자 B
  - 레거시 빌드 및 CI/CD 파이프라인을 현대화
  - 원인 파악이 어려웠던 오디오 장애로 발생한 필드 리부트 이슈를 분석해 근본 원인을 규명
  - 사업자의 애플리케이션 소프트웨어와 HAL 간의 장기 미결 이슈 해결
- 기술 지원 및 공장 생산 프로세스 안정화
  - 유럽/중동 유료 방송 사업자 D: Opera 브라우저 및 Network 스트리밍 소프트웨어의 연결 이슈 수정
  - 중남미 유료 방송 사업자 C: 안정적인 펌웨어 롤아웃을 위한 커스텀 배포 시스템 설계
  - 아시아 케이블 사업자 J: 기술 문의 대응 및 필드 버그 원인 분석
  - 생산 지원: 다양한 제품의 소프트웨어 및 하드웨어 변경에 맞춰 양산 소프트웨어 개발
- 빌드 환경, 버전 관리, CI/CD 인프라
  - 다수 모델의 소스가 SVN에 분산되고 표준 개발 환경이 없던 상태에서, devcontainer 기반 재현 가능한 빌드 환경을 구축
  - 개발 빈도가 높은 프로젝트를 선별하여 Git으로 이전
  - 기존 인프라 축소에 대응하여 Docker Swarm 기반 SVN/Git 미러, 파일 서버, Jenkins, 다양한 self-hosted runner를 구축하고 운영

### 유럽 리테일향 STB 개발 및 제조

전문분야: Embedded Linux, Linux kernel, BSP, Bootloader, Board bring-up, OpenEmbedded(Yocto), Broadcom SoC, Broadcom Magnum API, LinuxTV DVB, V4L2 mem2mem, ALSA, QtWebEngine, KODI, HbbTV, Wi-Fi, Bluetooth, Device drivers, GitHub Actions

유럽 리테일향 오픈소스 STB 플랫폼을 아키텍처 단계부터 설계해 제품화했습니다. Linux 표준 드라이버 인터페이스를 기반으로 소프트웨어를 개발하고, 양산 소프트웨어를 제조 파트너에 공급했습니다. 개발과 병행해 Linux kernel 업스트림 기여를 했으며, 각종 드라이버 소스를 공개해 커뮤니티의 테스트와 버그 리포트를 품질 개선에 반영했습니다.

- Board bring-up 및 Bootloader
  - 제품별 Bootloader 설계, 다양한 Broadcom SoC의 BSP 개발
  - Linux kernel 업그레이드에 따른 드라이버 포팅, Board bring-up 이슈 분석
- Broadcom Magnum 기반 Linux 표준 드라이버 구현
  - Nexus API 대신 Magnum API를 사용해 Linux 표준 드라이버 인터페이스를 설계 및 구현
  - 중복되는 상위 추상화 계층을 제거해 구조를 단순화하고 리소스 사용량 절감
- V4L2 mem2mem 기반 하드웨어 디코더 아키텍처 설계
  - HbbTV를 바이너리 플러그인 대신 QtWebEngine WebView 인젝션 구조로 구현
  - V4L2 mem2mem 드라이버를 설계하고 개발해 웹 환경과 KODI에서 하드웨어 디코더가 표준 API로 동작하는 미디어 파이프라인 완성
- 드라이버 소스 공개 및 커뮤니티 피드백 확보
  - 개발자가 직접 펌웨어를 테스트하고 버그를 보고하는 채널을 확보하고, 접수된 버그를 제품 품질 개선에 반영
- Wi-Fi 및 Bluetooth 오디오 통합
  - Realtek 및 Qualcomm Wi-Fi 드라이버 포팅과 Bluetooth 오디오용 ALSA 인터페이스 개발
- OpenEmbedded(Yocto) 기반 빌드 시스템 운영
  - 다수 모델을 지원하는 메타 레이어를 설계하고 유지보수
  - GitHub Actions 기반으로 Linux kernel, Bootloader, Device drivers, 양산 소프트웨어 등 제품 소프트웨어 릴리스 자동화
- 제조 관리 및 양산
  - 유럽 리테일향 STB 제조, 생산 라인 방문, 양산 소프트웨어 개발, 생산 로트별 소프트웨어 배포 및 버전 관리
  - 제조 파트너와 협업해 출하 검증 및 불량 분석 수행

### 차세대 Linux STB 플랫폼 개발 및 검증

전문분야: Embedded Linux, Linux kernel, BSP, Board bring-up, Device drivers, RTOS-to-Linux Migration, Adapter Layer Design, LinuxTV DVB, VDR, DirectFB, UPnP, Broadcom SoC, MIPS, Cross Toolchain

기존 RTOS 기반 STB 플랫폼을 Broadcom SoC 기반 Linux로 전면 마이그레이션하는 차세대 STB 플랫폼 개발 프로젝트를 주도했습니다. RTOS 미들웨어를 Linux에서 재사용하는 어댑터 레이어를 설계하고, LinuxTV, DirectFB, UPnP 등 그래픽 및 미디어 표준 스택을 통합해 Linux 전환의 기술 검증을 수행했습니다.

- Broadcom SoC 기반 Linux kernel 및 드라이버 개발
  - Board bring-up, 크로스 툴체인 환경 구축, Flash, Ethernet, USB, PCI, Graphics 드라이버 개발
- RTOS에서 Linux로 플랫폼 마이그레이션 및 어댑터 레이어 설계
  - RTOS 미들웨어를 Linux에서 재사용하는 어댑터 레이어 설계 및 드라이버 개발
  - 차세대 Linux 플랫폼에 맞춰 자체 빌드 시스템 구축
- 오픈소스 미디어 프레임워크 검증 및 통합
  - LinuxTV DVB API와 VDR을 연동해 개방형 아키텍처의 기술 검증
  - 임베디드 Linux에서 오픈소스 멀티미디어 소프트웨어의 상용화 가능성 검증
- DirectFB 기반 하드웨어 가속 그래픽 UI 및 멀티미디어 서브시스템 구현
  - DirectFB 환경에서 애니메이션 효과를 포함한 UI 렌더링 파이프라인 구현
  - Plug & Play 멀티미디어 재생 데모 개발
- CES 전시용 무선 미디어 스트리밍 데모 개발
  - Broadcom SoC에 PCI/USB Wi-Fi 드라이버를 포팅하고 UPnP 미디어 서버/렌더러 소프트웨어 개발
  - 무선 환경에서 수신한 미디어를 실시간 디코딩 및 재생하는 홈 스트리밍 시연 성공
- SCM 체계 구축
  - 프로젝트 합류 직후 SVN 서버를 구축하고, 이후 분산 버전 관리 도구인 Bazaar와 Mercurial 도입

### Wi-Fi Access Point 개발

전문분야: Embedded Linux, Linux kernel, BSP, Bootloader, Board bring-up, Atheros(Qualcomm) SoC, Wi-Fi 802.11a/b/g, mac80211, Network Subsystem Optimization, Ethernet, Bridge, Firmware Update, A/B Recovery, Custom Build System

Atheros(Qualcomm) SoC 기반 802.11a/b/g AP를 개발했습니다. Board bring-up부터 Bootloader, Linux kernel, Ethernet/Wi-Fi 드라이버, 자체 빌드 시스템까지 개발하여 국내 통신 사업자에 공급했습니다.

- Linux 플랫폼 개발
  - Bootloader 개발 및 다양한 SoC의 Board bring-up 전담
  - 제품 사양에 맞춘 Linux kernel 설정 최적화, Flash 및 Ethernet 드라이버 최적화, 시스템 소프트웨어 신규 개발
- 자체 빌드 시스템 및 버전 관리 도입
  - 크로스 툴체인 기반 자체 빌드 시스템 및 빌드 트리 개발
  - 압축 파일 기반 버전 관리를 CVS, 이어서 SVN으로 전환하고, 서버 구축 및 사용 가이드 작성, Trac 이슈 트래커와 위키 도입
  - 전체 개발 팀의 빌드 환경 구축
- Network 드라이버 최적화
  - Atheros(Qualcomm) 레퍼런스 Wi-Fi 드라이버 포팅
  - Ethernet, Bridge, Wi-Fi 드라이버의 패킷 처리 경로 최적화로 필드에서 무선 전송 속도와 접속 안정성 개선
- 펌웨어 업데이트 및 리커버리 소프트웨어
  - 원격 관리용 펌웨어 업데이트 엔진 개발, A/B 파티션 이중화 및 롤백

### 모바일 OS 기술 검증 및 스마트폰 플랫폼 PoC

전문분야: Embedded Linux, Linux kernel, Samsung Mobile SoC, Board bring-up, Device drivers, WebKit, 3G Modem, Touchscreen, Cross Compilation

Symbian이 주도하던 모바일 OS 시장을 배경으로 Samsung 모바일 SoC 기반 OS 사업을 제안하고, 핵심 기능의 타당성을 검증하는 PoC를 주도했습니다. Board bring-up부터 3G 모뎀 통합, 터치스크린과 WebKit 기반 UI까지 검증해 제품화 가능성을 확인했습니다.

- Linux 모바일 OS 플랫폼 개발
  - Samsung 모바일 SoC용 Linux kernel 포팅 및 주변장치 드라이버 개발
  - 제한된 메모리 환경에서 OS 및 모바일 앱 실행 환경 설계
  - 기본 앱 데모 개발, 3G 모뎀 통합
- WebKit 기반 풀 브라우징
  - WebKit 엔진의 크로스 컴파일 및 최적화 포팅
  - 터치스크린 환경의 풀 브라우징 렌더링 구현 및 웹 사용성 검증

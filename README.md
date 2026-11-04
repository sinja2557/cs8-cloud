# MS8 Cloud

경기인력개발원 Microsoft Cyber Security 8회차 클라우드 학습 저장소입니다.

VMware 기반 가상화 실습 환경 구축부터 Linux·Windows Server 운영, 클라우드 취약점, 시큐어 코딩, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹까지 클라우드 보안과 관련된 학습 자료 및 실습 기록을 정리합니다.

## 📚 학습 과정

- **학습 기간:** 2026-11-02 ~ 2027-03-12
- **교육 과정:** 경기인력개발원 Microsoft Cyber Security 8회차
- **주요 학습 분야:** 클라우드 취약점, 시큐어 코딩, 클라우드 시스템 보안, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹
- **주요 학습 도구:** VMware Workstation, Rocky Linux 9, Windows Server 2022, Windows 10·11, Xshell

## 🗂️ 학습 목차

| 순서 | 학습 자료 | 주요 내용 |
|---|---|---|
| 1 | [12주차](./12주차/) | VMware 가상화 실습 환경 구축, Linux 기본 명령어 및 사용자·그룹 관리, Windows Server 구성 |

> 각 폴더의 세부 학습 내용은 해당 폴더에서 확인할 수 있습니다. 실제 실습 기록은 아래 날짜별 학습 기록에서도 확인할 수 있습니다.

## 🧭 권장 학습 순서

### 1. 가상화 실습 환경 구축

- VMware Workstation 설치와 가상 네트워크(Virtual Network Editor) 구성
- NAT(vmnet8), Host Only(vmnet1), Bridged(vmnet0) 네트워크 방식 구분
- Rocky Linux 9, Windows Server 2022, Windows 10·11 가상머신 구성
- 체계 구성도에 따른 IP 주소 계획과 VM 복제(Full Clone)

### 2. Linux 기본 명령어와 파일 권한

- 디렉토리·파일 관리 기본 명령어와 vi 편집기
- 파일 메타데이터 분석과 권한 설정(`chmod`, `umask`, `chown`)
- 하드링크와 심볼릭 링크 구분

### 3. Linux 사용자·그룹 관리

- `/etc/passwd`, `/etc/shadow`, `/etc/group` 설정 파일 분석
- `useradd`, `usermod`, `userdel`, `passwd`를 활용한 계정 관리
- 로그인 제한 쉘(`/sbin/nologin`, `/bin/false`)의 차이 확인

### 4. Windows Server 2022 구성

- 템플릿 VM 생성과 `sysprep` 일반화 후 복제
- AD 서버와 멤버 서버 구성
- 원격 데스크톱 서비스와 그룹 정책 설정

### 5. 클라우드 보안 학습 확장

- 클라우드 취약점 및 시큐어 코딩
- 클라우드 시스템 보안 및 하이브리드 클라우드 보안 구축
- Azure 클라우드 인프라, 데이터·앱 보안
- 행위 기반 보안 탐지 및 시스템 모의해킹

## 📅 날짜별 학습 기록

### 2026-11-02 (54일차)

**학습 주제: 가상화 실습 환경 구축**

<img width="800" alt="VMware 네트워크 구성도" src="./12주차/54일차/VMware%20네트워크%20구성도%20인포그래픽.png" />

- 과정 학습 로드맵 정리
  - Network(CCNA), Linux, Windows, MSA(Docker·Podman, Kubernetes)
  - Cloud: Private(vSphere, XenServer), Public(AWS, Azure, GCP, NCloud)
  - IaC(Terraform, Ansible), CI/CD(Git·GitHub, Jenkins, ArgoCD), Python
- VMware Workstation 가상 네트워크 구성
  - NAT(vmnet8), Host Only(vmnet1), Bridged(vmnet0)
- 체계 구성도 기반 실습 환경 구성
  - Rocky Linux 3대: `10.0.0.11` ~ `10.0.0.13`
  - Windows Server 2022 3대(AD, MEM1, MEM2): `10.0.0.21` ~ `10.0.0.23`
  - Windows 10, Windows 11: `10.0.0.101`, `10.0.0.201`
  - 서브넷 마스크 `255.255.255.0`, 게이트웨이 `10.0.0.254`, DNS `168.126.63.1`, `8.8.8.8`
  - VM 사양: 1 CPU 2 Core, 메모리 2GB(Windows 11은 4GB), 디스크 50GB, NAT 네트워크
- Rocky Linux 설정
  - `nmtui`로 네트워크를 Automatic에서 Manual로 변경, `nmcli` 활용
  - 재시작: `reboot`, `init 6`, `shutdown -r now` / 종료: `halt`, `poweroff`, `init 0`, `shutdown -h now`
  - 콘솔 접속(tty)과 원격 접속(pts) 구분
- Windows 10·11 설정
  - VMware Tools 설치, PC 이름 변경, 방화벽 ICMP 허용, 전원 옵션, IPv4 주소 설정
- 원격 접속 환경
  - Xshell, SSH 포트 포워딩(`60022`, `60122`, `60222`), 방화벽 인바운드 규칙

### 2026-11-03 (55일차)

**학습 주제: Linux 기본 명령어, 사용자·그룹 관리, Windows Server 원격 데스크톱**

- 기본 명령어
  - `ls`(`-a`, `-l`, `-h`, `-i`, `-R`), `mkdir`·`rmdir`(`-p`), `cd`, `touch`, `rm`(`-r`, `-f`), `cat`, `cp`, `mv`, `pwd`, `head`, `tail`
  - 리다이렉션(`>`, `>>`)과 파이프(`|`)
  - vi 편집기: `ESC` 입력 후 `:q!`로 강제 종료
- 파일 메타데이터와 권한
  - 파일 유형, 소유자·그룹·기타 사용자 권한(r 4, w 2, x 1)
  - `chmod`, `umask`, `chown`, `stat`(Modify·Access·Change Time)
- 하드링크와 심볼릭 링크(`ln -s`)
- 사용자·그룹 관리
  - 설정 파일: `/etc/passwd`, `/etc/shadow`, `/etc/group`, `/etc/login.defs`, `/etc/skel`
  - `useradd` 옵션: `-u`(UID), `-g`·`-G`(그룹), `-c`(설명), `-d`(홈 디렉토리), `-s`(쉘)
  - `usermod`, `userdel -r`, `passwd`
  - `/sbin/nologin`은 로그인 거부 사유를 안내하고, `/bin/false`는 사유를 안내하지 않음
  - `/etc/passwd`와 `/etc/shadow` 필드 분석: UID·GID, 암호화 방식(SHA-512), 마지막 수정일, 최소·최대 사용일, 만료 경고일
- Windows Server 2022 구성
  - 템플릿(`W2K22-TEM`)을 `sysprep`으로 일반화한 뒤 복제하여 SID 충돌 방지
  - `W2K22-AD`, `W2K22-MEM1`, `W2K22-MEM2` 구성
- 원격 데스크톱
  - `mstsc`, `rdcm`을 이용한 원격 접속
  - 원격 데스크톱 세션 호스트 역할 추가, 그룹 정책(`gpedit.msc`)으로 연결 수 100개 설정, `gpupdate /force`로 적용

## 🎯 학습 목표

- VMware 기반 가상화 실습 환경 구축
- Linux와 Windows Server 기본 운영 및 계정·권한 관리 이해
- 클라우드 환경의 취약점 이해와 보안 구축 능력 향상

## 🌐 이전 학습 과정: TCP/IP

TCP/IP 및 CSAP 학습 내용은 별도 저장소에서 관리합니다.

[MS8 TCP/IP 학습 저장소 바로가기](https://github.com/sinja2557/ms8-tcp-ip)

해당 저장소에서는 다음과 같은 학습 주제를 다룹니다.

- TCP/IP 네트워크 구조와 Cisco Packet Tracer 실습
- 실물 L2·L3 스위치, 정적 라우팅, RIP 라우팅
- Python 소켓 프로그래밍
- CSAP 클라우드 보안인증 학습 및 실습

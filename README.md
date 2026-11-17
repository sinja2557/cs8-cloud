# MS8 Cloud

경기인력개발원 Microsoft Cyber Security 8회차 클라우드 학습 저장소입니다.

VMware 기반 가상화 실습 환경 구축부터 Linux·Windows Server 운영과 접근권한 관리, 클라우드 취약점, 시큐어 코딩, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹까지 클라우드 보안과 관련된 학습 자료 및 실습 기록을 정리합니다.

## 📚 학습 과정

- **학습 기간:** 2026-11-02 ~ 2027-03-12
- **교육 과정:** 경기인력개발원 Microsoft Cyber Security 8회차
- **주요 학습 분야:** 클라우드 취약점, 시큐어 코딩, 클라우드 시스템 보안, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹
- **주요 학습 도구:** VMware Workstation, Rocky Linux 9, Windows Server 2022, Windows 10·11, Xshell, FileZilla, IIS, Apache httpd, hMailServer, sendmail, Dovecot, Thunderbird, BIND, Sysinternals(BGInfo), GNS3, VirtualBox

## 🗂️ 학습 목차

| 순서 | 학습 자료 | 주요 내용 |
|---|---|---|
| 1 | [12주차](./12주차/) | VMware 가상화 실습 환경 구축, Linux 기본 명령어, 사용자·그룹 관리, ACL, 압축·스토리지·LVM 관리, Windows Server 공유 권한 및 DHCP 구성 |
| 2 | [13주차](./13주차/) | Linux 패키지 관리(dnf, rpm, 소스 설치), vi 편집기, Linux DHCP 서버 구성, FTP 서버 구성(Linux vsftpd, Windows IIS, Passive 모드, 사용자 격리), DNS 서버(BIND) 주·보조 구성, Windows 계정 정책·보안 옵션, Windows IIS 웹·DNS 서버 구성, IIS 가상 호스트·접근 제어, Windows DNS 스텁 영역, GNS3 기반 라우터 실습 환경 구축 |
| 3 | [14주차](./14주차/) | Linux 웹 서버(Apache httpd) 구성, `httpd.conf` 주요 설정, 호스트 이름 기반 가상 호스트, IP 기반 접근 제어, `.htaccess` 기본 인증, DNS·웹 서버 복습, 메일 서버(SMTP·POP3·IMAP) 개념과 구성(hMailServer, sendmail, Dovecot) |

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
- 대용량 파일 생성으로 디스크 용량 테스트(`truncate`, `dd`, `fsutil`)
- 하드링크와 심볼릭 링크 구분

### 3. Linux 사용자·그룹 관리

- `/etc/passwd`, `/etc/shadow`, `/etc/group` 설정 파일 분석
- `useradd`, `usermod`, `userdel`, `passwd`를 활용한 계정 관리
- 로그인 제한 쉘(`/sbin/nologin`, `/bin/false`)의 차이 확인
- `chage`를 활용한 패스워드·계정 만료 정책 설정

### 4. Windows Server 2022 구성

- 템플릿 VM 생성과 `sysprep` 일반화 후 복제
- AD 서버와 멤버 서버 구성
- 원격 데스크톱 서비스와 그룹 정책 설정

### 5. 파일 접근권한 관리

- Linux ACL(`setfacl`)을 이용한 사용자별 세부 권한 부여
- 부서·직급 기준 폴더 접근 권한 설계 실습
- Windows 공유 권한과 보안 권한의 차이 이해, 네트워크 공유 폴더 구성

### 6. Linux 아카이브·압축 및 스토리지 관리

- `tar` 아카이브 생성·해제·추가·업데이트와 gzip, bzip2, xz, zip 압축 방식 비교
- 디스크 사용 순서(파티션 → 파일시스템 → 마운트) 이해
- `fdisk`, `mkfs`, `mount`로 파티션 생성부터 마운트까지 실습

### 7. Windows Server DHCP 서비스

- 서버·클라이언트 모델과 DHCP 동작 구조(DORA) 이해
- DHCP 서버 역할 설치, 범위 생성, 임대 기간·게이트웨이·DNS 옵션 설정
- MAC 주소 기반 IP 예약과 클라이언트 IP 할당 확인

### 8. Linux LVM 스토리지 관리

- 스토리지 유형(DAS, NAS, SAN)과 클라우드 스토리지(Block, Object) 비교
- LVM 구성 순서(파티션 → PV → VG → LV → 파일시스템 → 마운트) 이해
- 논리 볼륨 생성, 디스크 추가를 통한 용량 확장, 구성 초기화 실습

### 9. Linux 패키지 관리

- dnf, rpm, 소스 설치 방식의 차이와 의존성 문제 이해
- `dnf` 저장소 설정과 설치·삭제·이력 관리(`dnf history`)
- Apache httpd 소스 설치로 `configure` → `make` → `make install` 과정과 의존성 해결 순서 실습
- `rpm` 명령어로 패키지 설치·조회·삭제

### 10. vi 편집기와 Linux DHCP 서버

- vi 편집기의 입력, 이동, 복사, 치환, 검색, 저장 명령어
- `dhcp-server` 설치와 `dhcpd.conf` 설정, 임대 정보 확인, IP 예약

### 11. FTP 서버 구성

- FTP 동작 방식(제어 포트와 데이터 포트, Active·Passive 모드) 이해
- Linux `vsftpd` 설치와 설정(접속 제한, 타임아웃, 배너, chroot, 로그, 파일 제한)
- `firewall-cmd`로 방화벽 포트 허용, Windows 클라이언트 방화벽 설정
- Windows IIS로 FTP 사이트 구성(인증, 권한 부여 규칙, IP 제한, 요청 필터링, 사용자 격리)
- Linux·Windows FTP Passive 모드 구성(데이터 포트 범위 지정과 방화벽 규칙)

### 12. DNS 서버(BIND)

- DNS 개념(도메인과 IP 변환, UDP·TCP `53`번 포트, 루트 DNS 서버)
- `bind`, `bind-utils`, `bind-libs` 설치와 `named.conf`, `named.rfc1912.zones`, 존 파일 구성
- 정방향·역방향 존, A·CNAME·MX·PTR 레코드 작성, `nslookup`·`dig`로 질의 확인
- 주 DNS·보조 DNS 구성(슬레이브 존, 영역 전송)과 Windows 클라이언트 DNS 설정

### 13. Windows 계정 정책과 보안 옵션

- 로컬 보안 정책(`gpedit.msc`)의 암호 정책과 계정 잠금 정책 설정
- 보안 옵션: Administrator 계정 이름 변경, 마지막 로그온 사용자 이름 숨김, 로그온 경고 메시지
- `gpupdate /force`로 정책 즉시 적용, 정책 적용 결과 로그인 화면에서 확인

### 14. Windows 웹·DNS 서버

- IIS 웹 사이트 구성(기본 문서 우선순위, 익명 인증)과 Default Web Site 제거
- Windows DNS 서버의 정방향·역방향 주 영역, 보조 영역, 영역 전송 허용 구성
- Sysinternals(BGInfo, Autoruns, TCPView) 도구 확인

### 15. IIS 가상 호스트와 접근 제어

- 한 서버에서 여러 웹 사이트를 운영하는 3가지 방법(IP별, 포트별, 호스트 이름별 가상 호스트)
- IP 주소 및 도메인 제한, 기본 인증으로 사이트별 접근 제어
- HTTP 리디렉션, 기본 문서, 디렉터리 검색, 오류 페이지, 요청 필터링, HTTP 상태 코드와 메서드 이해
- Windows DNS 보조 영역과 스텁 영역 비교

### 16. 네트워크 장비와 GNS3 실습 환경

- 라우터와 스위치의 역할 비교, Cisco IOS 라우터 기본 구성(호스트 이름, 인터페이스 IP, 기본 경로)
- GNS3와 VirtualBox 기반 라우터·Linux 서버 연동 실습 환경 구축

### 17. Linux 웹 서버(Apache)와 가상 호스트

- `httpd` 설치와 `httpd.conf` 주요 설정 항목(서버 루트, 포트, 모듈, 사용자·그룹, 문서 루트, 로그) 이해
- 호스트 이름 기반 가상 호스트(`VirtualHost`)로 한 서버에서 `www`, `blog`, `intra` 사이트 운영
- `Order`·`Allow`·`Deny`를 이용한 IP 기반 접근 제어와 `.htaccess`·`htpasswd` 기반 기본 인증
- DNS(BIND)와 웹 서버를 처음부터 다시 구성하는 반복 학습

### 18. 메일 서버(SMTP·POP3·IMAP)

- 전자우편 서비스 개념(SMTP `25`, POP3 `110`, IMAP `143`, SSL 사용 시 `465`, `995`, `993`), MUA·MTA·MDA 동작 구조
- Windows 메일 서버: hMailServer 설치, 도메인·계정 생성, 프로토콜·로그·Auto-ban 설정, Thunderbird 클라이언트 연동
- Linux 메일 서버: `sendmail`(MTA)과 `dovecot`(POP3·IMAP) 구성, DNS `MX` 레코드 연동
- 서버 초기화 후 같은 순서로 다시 구성하는 반복 학습

### 19. 클라우드 보안 학습 확장

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
  - vi 편집기: `ESC` 입력 후 `:q!`로 강제 종료, `ZZ`로 저장 후 종료
- 파일 메타데이터와 권한
  - 파일 유형, 소유자·그룹·기타 사용자 권한(r 4, w 2, x 1)
  - `chmod`(`-R`: 하위 디렉토리까지), `umask`, `chown`, `stat`(수정·접근·권한 변경 시간)
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

### 2026-11-04 (56일차)

**학습 주제: 패스워드 정책, ACL, Windows 공유 권한**

- 대용량 파일 생성과 용량 테스트
  - Linux: `truncate -s 100M a.txt`, `dd if=/dev/zero of=./aa.txt bs=300M count=1`
  - Windows: `fsutil file createnew 1.txt 1024`, `dir`로 확인
- 패스워드 정책 관리(`chage`)
  - 옵션: `-l`(설정 확인), `-m`(최소 사용일), `-M`(최대 사용일), `-W`(만료 전 경고일), `-I`(유예 기간), `-E`(계정 만료일)
  - `date -s`로 날짜를 변경하고 `systemctl restart chronyd`로 시간 동기화
  - 패스워드를 바꿔도 계정 만료일은 연장되지 않음을 확인
  - `ssh a@10.0.0.11`로 접속하여 정책 적용 여부 테스트
- 그룹 관리
  - `groupadd`, `groupdel`, 삭제 오류 발생 시 `journalctl -xe`로 원인 확인
  - `useradd -N`: 사용자와 같은 번호의 그룹을 만들지 않음
  - 관련 설정 파일: `/etc/default/useradd`, `/etc/login.defs`
- Linux ACL 실습
  - 소유자·그룹·기타 사용자 권한만으로 설정하기 어려운 사용자별 권한을 ACL로 설정
  - `setfacl -m u:a:rx /PATH`, 여러 계정은 `u:a:rx,u:b:rw`처럼 쉼표로 연결
  - 실습 시나리오: 사용자 4명(a, b, c, d)을 admin·sales 부서로 나누고 회사 디렉토리 구성
  - 팀원은 본인 부서 폴더만 읽기, 팀장은 본인 부서 폴더 읽기·쓰기와 타 부서 폴더 읽기
  - 사용자를 삭제하면 ACL에 이름 대신 UID가 표시되는 현상 확인
- Windows 공유 권한 실습
  - 같은 시나리오를 Windows에서 구성: 컴퓨터 관리(`compmgmt.msc`)의 로컬 사용자 및 그룹에서 계정 생성
  - `\\10.0.0.21` 네트워크 공유 폴더 접속, 상위 대표 폴더만 공유하여 하위 권한 관리
  - 공유 권한의 읽기·쓰기·수정 차이: 쓰기는 파일 생성과 내용 변경만 가능, 수정은 권한 변경을 제외한 모든 작업 가능
  - 공유 권한과 보안 권한 중 더 제한적인 권한이 적용됨
  - 권한 변경 후 로그아웃·재로그인하여 적용
- 공유 권한 설정 실습 과제([공유권한실습.pdf](./12주차/56일차/공유권한실습.pdf))
  - 과제 1: Admin·Sales·Finance·Infra 4개 팀, 팀장은 전체 폴더 읽기, 팀원은 본인 팀 폴더만 읽기·실행, 일부 팀장에게 타 팀 폴더 쓰기 부여
  - 과제 2: 솔데스크 회사 폴더 구조(기획, 영업, 관리, 개발, 기술지원, 재경, Infra구축), 팀원·과장·팀장 직급별 권한과 CEO·Administrator 전체 권한 설계

### 2026-11-05 (57일차)

**학습 주제: Linux 압축·스토리지 관리, Windows Server DHCP**

- Windows 권한 복습
  - `System` 계정은 권한을 변경하지 않음
  - `Administrator`(사용자)와 `Administrators`(그룹) 양쪽 모두에서 권한 제거
- Linux 학습 로드맵
  - 학습 완료: 기본 명령어, 파일·디렉토리 관리, 사용자 관리
  - 학습 예정: 스토리지 관리, 패키지 관리, 프로세스 관리, 서버(DHCP, DNS, FTP, Web, Mail)
- 아카이브와 압축(`tar`)
  - 옵션: `c`(생성), `x`(해제), `t`(내용 확인), `r`(파일 추가), `u`(업데이트 파일 추가), `v`(과정 출력), `f`(파일명 지정), `-C`(디렉토리 변경)
  - 압축 연동 옵션: `z`(gzip), `j`(bzip2), `J`(xz), 압축 아카이브는 `t`만 가능하고 `u`, `r`은 불가
  - 압축 방식: gzip(기본 설치, `gz`), bzip2(별도 설치, `bz2`, gzip보다 압축률 약 30% 높음), xz(기본 설치), zip(Windows 호환용, 별도 설치)
  - 압축률은 1~9 단계로 지정 가능(`gzip -9`, `bzip2 -1`, `xz -6`)
  - 실습: 아카이브 생성·해제·내용 확인, 파일 추가·업데이트, 압축·해제 명령(`gunzip`, `bunzip2`, `unxz`)
- 스토리지 관리
  - VMware에 SCSI 디스크(10GB, 5GB) 추가 후 `lsblk`로 확인
  - 디스크 사용 순서: Windows는 파티션 → 파일시스템 → 드라이브명 할당, Linux는 파티션 → 파일시스템 → 마운트
  - 파티션: MBR은 주 파티션 4개까지, 확장 파티션 안에 논리 파티션 생성 가능 / UEFI는 주 파티션 128개까지
  - 파일시스템: Windows는 FAT16, FAT32, NTFS / Linux는 EXT2, EXT3, EXT4, XFS(EXT3, EXT4는 저널링 파일시스템)
  - 명령어: `fdisk`(`n` 생성, `d` 삭제, `p` 출력, `t` 타입 변경, `w` 저장, `q` 종료), `mkfs`, `blkid`, `mount`, `umount`, `wipefs`
  - 실습: 파티션 2개 생성(5GB EXT4를 `/p1`에, 나머지 XFS를 `/p2`에 마운트), `df -Th`로 확인 후 마운트 해제와 초기화
  - 과제: `/dev/sdb`에 3개 파티션 구성(EXT3 3GB `/p1`, EXT4 3GB `/p2`, XFS 나머지 `/p3`), `mount`와 `df -Th` 결과 및 초기화 후 `lsblk` 결과 제출
- Windows Server DHCP
  - 서버·클라이언트 모델: DHCP(IP 자동 할당), FTP(대용량 파일 전송), Web(콘텐츠 제공), DNS(URL을 IP로 변환), Mail(전자 우편)
  - 동작 구조(DORA): Discover(Broadcast) → Offer → Request → Ack, 임대 기간의 1/2 시점에 갱신 요청
  - 통신 방식: IPv4는 Unicast, Broadcast, Multicast / IPv6는 Anycast, Unicast, Multicast
  - 서버 관리자에서 DHCP 서버 역할 설치, 새 범위(`Test_DHCP`) 생성
  - 구성체계 실습: `10.0.0.0/24` 네트워크, 서버 고정 IP 순차 사용, DHCP 서버 `10.0.0.21`, 게이트웨이 `10.0.0.254`, DNS `168.126.63.1`, `8.8.8.8`, 임대 기간 24시간·12시간·4시간으로 변경하며 반복
  - MAC 주소 기반 IP 예약: W10-1은 101번, W11-1은 201번 IP 고정(MAC 앞 3바이트는 제조사 식별 코드 OUI)
  - VMware 가상 MAC 주소를 변경하여 예약 동작 확인, `ipconfig /all`로 할당 결과 확인
  - APIPA(Windows 전용): DHCP 서버가 없을 때 자동 할당되어 내부 네트워크 통신만 가능
  - 실습 후 DHCP 서버 역할 제거(범위 주소도 함께 삭제)
- 실습 명령어 이력(`2026-11-05 Linux history.docx`) 정리

### 2026-11-06 (58일차)

**학습 주제: 스토리지 유형, 포트, Linux 디렉토리 구조, LVM**

- 스토리지 유형
  - DAS(Direct Attached Storage): IDE, SATA, SCSI 직접 연결, 구성이 쉽고 빠르지만 원격 설치와 확장이 어려움
  - NAS(Network Attached Storage): 기존 네트워크에 구성, NFS·iSCSI 사용, 원격 설치와 확장이 쉽지만 속도가 낮고 병목 현상 발생 가능
  - SAN(Storage Area Network): SAN 스위치와 Fiber Channel(HBA 카드) 구성, 속도가 빠르고 확장이 쉽지만 네트워크를 새로 구성해야 하고 비용이 높음
  - 클라우드 스토리지: Block(디스크처럼 사용), Object(REST API, 객체별 URL과 ACL 설정, Azure Blob, AWS S3)
- 파일 공유 프로토콜
  - Windows는 CIFS(SMB)를 사용하며 Windows 10부터 NFS도 지원, `139`, `445` 포트
  - Linux는 CIFS를 지원하지 않아 Samba로 대체
- 포트 확인과 주요 포트
  - Windows `netstat -na -p tcp`, Linux는 `/etc/services` 확인
  - `20`·`21` FTP, `22` SSH, `23` Telnet, `25` SMTP, `53` DNS, `67`·`68` BOOTP(DHCP), `69` TFTP, `80` HTTP, `443` HTTPS
  - `110` POP3(메일을 내려받으면 서버에 남지 않음), `143` IMAP4(서버에 남음), `139` NetBIOS, `445` SMB
- Linux 복습
  - 디스크 사용 순서는 파티션 → 파일시스템 → 마운트, 해제는 역순
  - 설치 시 파티션 설정: swap(기본적으로 메모리의 2배), `/` 구성
- Linux 디렉토리 구조
  - `/dev`(장치 드라이버), `/boot`(부팅 파일), `/root`(root 홈), `/home`(일반 사용자 홈), `/bin`·`/sbin`(명령어), `/lib`·`/lib64`(라이브러리), `/var`(로그 등 가변 데이터), `/tmp`(임시), `/etc`(설정 파일), `/run`(실행 중 패키지의 pid), `/proc`(커널 메모리 상태)
  - `/home`, `/var`는 별도 파티션으로 분리하여 용량 확장 가능
- LVM(Logical Volume Manager)
  - 물리 디스크를 논리적으로 통합하여 파일시스템을 관리하는 중간 계층
  - 기존 구성: 파티션 → 파일시스템 → 마운트 / LVM 구성: 파티션 → PV → VG → LV → 파일시스템 → 마운트
  - PV: `pvcreate`, `pvscan`, `pvs`, `pvdisplay`, `pvremove`
  - VG: `vgcreate`, `vgscan`, `vgs`, `vgdisplay`, `vgextend`, `vgreduce`, `vgremove`
  - LV: `lvcreate -L 3G -n 이름 VG명`, `lvextend`, `lvreduce`(데이터 손상 위험으로 가급적 사용하지 않음), `lvremove`
  - 파티션 타입은 `fdisk`에서 `t` 선택 후 `8e`(Linux LVM)
- LVM 생성 실습
  - `/dev/sdb1`로 PV 생성, VG(`shkwon`)를 PE 크기 2MB(`-s 2M`)로 생성
  - LV 3개를 만들어 각각 ext3, ext4, xfs로 포맷 후 `/p1`, `/p2`, `/p3`에 마운트
  - 디스크(`/dev/sdc`) 추가 후 `pvcreate` → `vgextend` → `lvextend`로 확장, 파일시스템은 xfs는 `xfs_growfs`, ext3·ext4는 `resize2fs`로 확장
  - 초기화는 생성의 역순: `umount` → `wipefs` → `lvremove` → `vgremove` → `pvremove` → 파티션 삭제
- VMware 실습(`rocky9-lvm`)
  - 설치 시 SCSI 50GB 디스크에 LVM으로 `/`, `/home`, `/var` 구성
  - 10GB 디스크 추가 후 `pvcreate` → `vgextend` → `lvextend -l +2559` → `xfs_growfs`로 루트 볼륨 확장
- LVM 과제([lvm 구성체계.txt](./12주차/58일차/lvm%20구성체계.txt))
  - `/dev/sdb1` PV, 이니셜 VG, LV 3개(ext3 4GB `/p1`, ext4 4GB `/p2`, xfs 나머지 `/p3`) 구성 후 `mount`, `df -Th` 캡처
  - `/dev/sdc1` 추가 후 LV 크기를 5GB, 6GB, 3GB로 확장하여 `df -Th` 캡처
  - 초기화 후 `lsblk` 캡처
- 실습 명령어 이력(`LVM Command History.docx`) 정리

### 2026-11-09 (59일차)

**학습 주제: Linux 패키지 관리, vi 편집기, Linux DHCP 서버**

- 학습 흐름 정리
  - Linux 1주차 복습: 기본 명령어, 파일 및 디렉토리, 사용자, 스토리지 관리
  - Linux 2주차 학습 주제: 패키지 관리와 의존성 문제
- 패키지 관리 방식 비교
  - `dnf`(`yum`): 배포판 제작사가 제공하는 인터넷 저장소에서 내려받아 설치, 의존성 자동 해결, 커스터마이징 불가
  - `rpm`: RHEL 계열 패키지 확장자, 파일을 내려받아 설치, 소스 설치보다 쉽지만 의존성을 직접 해결
  - 소스 설치: 커스터마이징 가능, 의존성을 직접 해결, 환경 설정(`./configure`) → 컴파일(`make`) → 설치(`make install`)
- `dnf` 실습
  - 저장소 설정 파일 `/etc/yum.repos.d/rocky.repo`, 저장소 구성(BaseOS, AppStream, Extras)
  - `dnf install httpd`, 설치 시 확인 질문에 `N`으로 취소, `-y` 옵션으로 자동 승인
  - `dnf autoremove`로 삭제, `dnf history list`·`info`·`undo`·`redo`로 이력 조회와 되돌리기
- 소스 설치 실습: Apache httpd 2.4.70
  - 준비 패키지: `wget`, `tar`, `expat-devel`, `gcc`, `gcc-c++`
  - 의존성 설치 순서: apr 1.7.6 → apr-util 1.6.6 → pcre 8.45 → httpd
  - 각 단계에서 `./configure --prefix=경로`로 설치 위치를 지정하고 `--with-apr`, `--with-apr-util`, `--with-pcre`로 의존 패키지 경로 연결
  - 오류 해결 과정: apr 누락 → apr-util 누락 → `pcre-config` 누락 순으로 오류가 발생하여 해당 패키지를 먼저 설치
  - 명령어 연결: `&&`(앞 명령이 성공해야 실행), `||`(앞 명령이 실패해야 실행), `;`(성공·실패와 관계없이 실행)
  - 설치 후 `/root/.bashrc`에 `PATH` 등록, `apachectl start`, 방화벽 `80/tcp` 허용, `index.html` 수정으로 웹 페이지 확인
  - 스냅샷으로 되돌리고 초기화한 뒤 3회 반복 설치하여 순서 숙달, 과제 실습 후 `history` 제출
- `rpm` 실습
  - `dnf download --resolve`로 `createrepo` 패키지 내려받기
  - `rpm -Uvh`로 설치할 때 의존성 오류가 발생하여 `createrepo_c-libs`를 먼저 설치
  - 옵션: `-i`(설치), `-U`(업그레이드 설치), `-v`(과정 출력), `-h`(진행 표시), `-qa`(설치 확인), `-qi`(패키지 정보), `-ql`(관련 파일), `-qf`(파일이 속한 패키지), `-e`(삭제)
  - `dnf localinstall`로 내려받은 rpm 설치, `dnf history list`에 기록됨
- vi 편집기
  - 입력: `a`, `i`, `o`, `s`와 대문자 `A`, `I`, `O`, `S`, 이동: `$`, `gg`(맨 앞줄), `G`(맨 뒷줄)
  - 행 복사 `:3,4co12`, 치환 `:3s/무궁화/해당화/`, 전체 치환 `:%s/무궁화/해당화/g`
  - 검색 `/해당화`와 `n`, 행 번호 표시 `:se nu`, 파일명과 줄 번호 확인 `Ctrl + g`
  - 외부 명령 실행 `:!ls -la /`, 결과 삽입 `:$ r !ls -la /`, 파일 삽입 `:$ r /etc/passwd`
  - 삭제 `10dd`, `:1,51d`, 실행 취소 `u`와 다시 실행 `Ctrl + r`, 저장 `:w`와 `ZZ`
  - 참고 자료: [vi 명령어 정리표(vi.pdf)](./13주차/59일차/vi.pdf)
- Linux DHCP 서버
  - `dnf install -y dhcp-server` 설치 후 `/etc/dhcp/dhcpd.conf` 설정, 예제 파일 `/usr/share/doc/dhcp-server/dhcpd.conf.example` 참고
  - `systemctl start dhcpd`로 시작, 오류 발생 시 `journalctl -xe`로 확인
  - VMware의 Windows 10·11 가상머신을 켜서 IP 할당 확인, 임대 정보는 `/var/lib/dhcpd/dhcpd.leases`에서 확인
  - `host 이름 { }` 구문으로 IP 예약 설정
  - 삭제: `dnf autoremove`로 제거한 뒤 남은 `/etc/dhcp`, `/var/lib/dhcpd` 삭제
  - 교수님 정답지를 참고해 설정 복습 후 과제 진행

### 2026-11-10 (60일차)

**학습 주제: Linux DHCP 복습, FTP 서버(Linux vsftpd, Windows IIS)**

- 가상 네트워크 구성 정리(Host, NAT(vmnet8), Host Only(vmnet1))
- Linux DHCP 과제 복습
  - 방화벽 포트 삭제 `firewall-cmd --remove-port=80/tcp`, vi 실행 취소 `u`와 다시 실행 `Ctrl + r`
- Windows Server DHCP 복습(`W2K22-AD`)
  - DHCP 서버가 2대이면 먼저 도착한 Offer의 서버에서 IP 할당
  - 새 범위의 서브넷 지연(Offer 지연, 100ms)으로 서버 응답 우선순위 조절, Active·Standby 고가용성 구성
  - 임대 시간의 1/2 시점에 갱신(Request, ACK), 7/8 시점까지는 유니캐스트로 요청하고 이후 브로드캐스트
  - 범위 구성: `10.0.0.1` ~ `10.0.0.254`(`/24`), 제외 주소 `10.0.0.1` ~ `10.0.0.30`, `10.0.0.251` ~ `10.0.0.254`, 게이트웨이 `10.0.0.254`, 도메인 `이니셜.local`
- FTP(File Transfer Protocol) 개념
  - 대용량 파일 전송 서비스, Linux는 `vsftpd`, Windows는 IIS 사용
  - TCP `21`번은 인증·제어 포트, 데이터 전송은 모드에 따라 다름
  - Active 모드: 서버가 `20`번 포트로 클라이언트에 연결, 클라이언트 방화벽에서 차단되면 연결이 멈춤
  - Passive 모드: 서버가 데이터 포트를 알려 주고 관리자가 지정한 포트만 개방
- Linux FTP 실습(`vsftpd`, Rocky Linux)
  - 사용자 `a`, `b` 생성 후 `dd`로 홈 디렉토리에 대용량 파일 생성
  - `/etc/vsftpd/vsftpd.conf` 주요 설정
    - 접속·권한: `anonymous_enable=NO`, `local_enable=YES`, `write_enable=YES`, `local_umask=022`
    - 로그: `xferlog_enable=YES`, `xferlog_file` 경로 지정, `connect_from_port_20=YES`
    - 타임아웃: `idle_session_timeout` 600초를 300초로, `data_connection_timeout` 120초를 60초로 변경
    - 안내: `ftpd_banner` 문구 또는 `banner_file` 파일 지정
    - 제한: `chroot_list_enable=YES`와 `chroot_list_file`로 목록의 사용자만 홈 디렉토리를 최상위로 제한(chroot), `allow_writeable_chroot=YES`, `deny_file`로 특정 확장자 차단
  - anonymous는 비밀번호로 이메일 주소를 입력하는 방식
  - 방화벽: `firewall-cmd --list-all`, `--get-zones`, `--get-default-zone`(`public`), `--get-service`
    - `--permanent --add-port=21/tcp`, `20/tcp` 후 `--reload`(`--add-port`만 쓰면 재시작 시 사라짐)
  - `ss -natlp`로 `21`번 포트 LISTEN 상태(`vsftpd`) 확인, 오류 시 `journalctl -xe` 확인, `setenforce 0`으로 SELinux 임시 해제
  - Windows 10·11 클라이언트 접속(`ftp 10.0.0.11`)
    - 명령어: `pwd`, `dir`, `get`, `put`, `mget`, `mput`, `lcd`(로컬 디렉토리 이동), `!dir`(로컬 목록)
    - Windows Defender 방화벽 경고가 나오면 차단 규칙 2개를 삭제하고 `ftp.exe` 허용 인바운드 규칙 추가
    - chroot 확인: 목록 사용자는 `/`가 최상위, 그 외 사용자는 상위 디렉토리 이동 가능
    - FileZilla로 호스트 PC에서 접속(전송 모드는 능동형)
  - 전송 로그 `xferlog`: `o`는 서버에서 클라이언트(out), `i`는 클라이언트에서 서버(in)
  - 초기화(서비스 중지, `dnf autoremove`, 설정 디렉토리·사용자 삭제, 방화벽 포트 삭제)와 재설치를 4회 반복하여 숙달
- 실습 과제: FTP 서버 구성 요구사항 2건
  - 과제 1: 사용자 `a`, `b`와 500MB 파일, banner·chroot_list·xferlog를 별도 디렉토리에 저장, Active 모드, anonymous 차단, 접속 후 120초 무동작 시 종료, 데이터 전송 중 60초 경과 시 종료
  - 과제 2: 사용자 `aaa`, `bbb`와 `aaa.txt`, `bbb.sh`(500MB), `bbb`만 chroot 적용, 3분 무동작 시 종료, 1분 데이터 전송 제한, `*.sh` 업로드·다운로드 금지(`550 Permission denied` 확인)
  - 결과 확인: 본인 서버와 팀원 서버 3대에 `aaa`, `bbb`로 접속하여 `pwd` 결과 비교(`aaa`는 `/home/aaa`, chroot 적용된 `bbb`는 `/`)
  - 결과 화면: `13주차/60일차` 폴더의 `*_aaa.png`, `*_bbb.png` 파일에서 확인(아래는 본인 서버 접속 결과)

<img width="400" alt="본인 FTP 서버 aaa 접속 결과" src="./13주차/60일차/%EB%B3%B8%EC%9D%B8_aaa.png" /> <img width="400" alt="본인 FTP 서버 bbb 접속 결과" src="./13주차/60일차/%EB%B3%B8%EC%9D%B8_bbb.png" />

- Windows FTP 실습(IIS, `W2K22-AD`)
  - 서버 관리자에서 역할 추가: 웹 서버(IIS)의 FTP 서버(FTP 서비스)와 IIS 관리 콘솔 설치
  - `Default Web Site` 삭제, `C:\01_FTP` 폴더 생성, PowerShell에서 `fsutil file createnew ftp.txt 1024`로 파일 생성
  - `compmgmt.msc`의 로컬 사용자 및 그룹에서 사용자 `a`, `b` 생성
  - FTP 사이트 추가: 이름 `shkwon_ftp`, 경로 `C:\01_FTP`, 포트 `21`, SSL 사용 안 함
  - 인증과 권한: FTP 인증(기본 인증 사용, 익명 인증 사용 안 함)과 FTP 권한 부여 규칙(지정한 사용자 `a`, `b`의 읽기·쓰기)은 항상 함께 설정
  - 부가 설정
    - FTP IP 주소 및 도메인 제한: `10.0.0.101` 허용, 지정되지 않은 클라이언트는 거부
    - FTP 디렉터리 검색(UNIX 스타일), FTP 로깅, FTP 메시지(배너와 `%username%님 안녕하세요` 시작 메시지)
    - FTP 요청 필터링으로 `.sh` 확장자 거부, FTP 사용자 격리(FTP 루트 디렉터리), FTP 방화벽 지원
    - 고급 설정에서 연결 제한 시간 확인
  - 방화벽: 새 인바운드 규칙에서 포트 `20-21` 허용
  - Windows 간 접속(`user b`)으로 시작 메시지와 로그인 확인, 허용되지 않은 접근은 `550 Access is denied`
  - 초기화: 사이트 제거, DHCP 범위 제거, 사용자 제거, 기능 및 역할 제거, 스냅샷 복원
  - 복습 시 DHCP 구성 완료 후 FTP 사이트를 처음부터 다시 구성

### 2026-11-11 (61일차)

- 복습 전체 흐름 정리
  - Linux(기본 명령어, 파일·디렉토리, 사용자·그룹, 디스크, 패키지, 프로세스) → 서버(DHCP, FTP, DNS, WEB, MAIL, NFS) → Windows → Active Directory → 그룹 정책
- Linux FTP 복습 1: Active 모드 재구성(`vsftpd`, `rocky9-2`)과 Windows ↔ Linux 접속 확인
  - Linux DHCP(`dhcpd.conf`) 구성 후 FTP 서버 접속 확인
- Windows FTP 복습(`W2K22-AD`)
  - 사용자 `a`, `b` 생성, `C:\01_FTP\ftp.txt` 생성, DHCP 새 범위 구성, IIS FTP 사이트 구성, 방화벽 `20-21` 허용
  - Windows ↔ Windows 접속으로 탐색 확인
  - FTP 사용자 격리
    - 격리 미사용: 로그인 후 상위 폴더 탐색 가능
    - 격리 사용(`LocalUser` 폴더 아래 사용자별 폴더, 예: `a` 폴더에 `aa.txt`, `b` 폴더에 `bb.txt`): 자기 폴더 밖으로 탈출 불가
- 구성 복습: 1. DHCP, 2. FTP(사용자 격리)
- Linux FTP Passive 모드(`vsftpd`)
  - `/etc/vsftpd/vsftpd.conf` 설정: `pasv_enable=YES`, `pasv_min_port=65000`, `pasv_max_port=65010`, `allow_writeable_chroot=YES`, `deny_file={*.sh}`
  - 배너 파일(`/shkwon/ban`, `/shkwon/ch`)에 접속 경고 문구 작성
  - 방화벽: `firewall-cmd --permanent --add-port=21/tcp`, `--add-port=65000-65010/tcp` 후 `--reload`
  - FileZilla로 Guest PC(`w10`)에서 `a.txt` 다운로드, `w11`에서 접속 확인
  - `deny_file` 확인: `b.sh` 업로드는 거부되고 `b.txt`로 변경 시 정상 동작
  - `ss -nat`으로 `21`번 포트 LISTEN과 데이터 연결 상태 확인
- Windows FTP Passive 모드(IIS)
  - FTP 방화벽 지원의 전역 설정에서 데이터 채널 포트 범위 `60000-60010` 지정, 사이트 중지 후 시작
  - 방화벽 인바운드 규칙에 `60000-60010` 허용, `w10`에서 접속 확인
- DNS(Domain Name System) 개념
  - 도메인(URL)을 IP 주소로 변환하는 서비스
  - 기본 프로토콜은 UDP `53`번, 다음 두 경우에만 TCP 사용
    - 응답 데이터가 512 byte 초과
    - 영역 전송(Zone Transfer)
  - 전 세계 루트 DNS 서버는 13대로 제한
  - 설치: `dnf install -y bind bind-utils bind-libs`
  - 구성 파일: `/etc/named.conf` ← `/etc/named.rfc1912.zones` ← `/var/named/` 레코드 파일
  - `dig naver.com +trace`로 루트 DNS → `com` 도메인 DNS → `naver.com` 네임서버 순서의 질의 과정 확인(DNSSEC 레코드 `DS`, `RRSIG` 포함)
  - 한국인터넷진흥원(KISA) 인터넷 주소자원 사이트에서 IP 주소 체계, 도메인 네임 시스템, DNSSEC 자료 확인
  - 도메인 구매: 가비아에서 `shkwon.shop` 도메인 구입 완료(실습은 `shkwon.local` 사설 도메인 사용)
- 구성 체계도 확인(`구성체계_역할추가.png`)
  - 서버별 역할: `rocky9-1` DHCP, 주 DNS, WEB(Blog, Main), NFS 서버 / `rocky9-2` FTP, 보조 DNS, WEB(Blog, Main, Intra), NFS 클라이언트 / `rocky9-3` 보조 DNS, WEB(Main, Intra), Mail
  - Windows: `W2K22-AD`(DHCP, 주 DNS, WEB), `W2K22-MEM1`(FTP, 보조 DNS, WEB), `W2K22-MEM2`(보조 DNS, WEB, Mail), `w10-1`·`w11-1`(Mail, NFS 클라이언트)
  - 전체 NIC는 NAT, 서브넷 마스크 `255.255.255.0`, 기본 게이트웨이 `10.0.0.254`

<img width="700" alt="구성 체계도" src="./13주차/61일차/2026-11-11%20%EA%B5%AC%EC%84%B1%EC%B2%B4%EA%B3%84_%EC%97%AD%ED%95%A0%EC%B6%94%EA%B0%80.png" />

- DNS 구성 실습 1(`rocky9-1`, 주 DNS)
  - Windows 클라이언트의 기본 DNS 서버를 `rocky9-1`로 지정(`nslookup`은 주 DNS만 질의하고 보조 DNS는 확인하지 않음)
  - `/etc/named.conf`의 `options`에서 `listen-on port 53 { any; }`, `allow-query { any; }`로 변경
  - `/etc/named.rfc1912.zones`에 정방향 존 `shkwon.local`(`type master`, `file "1"`)과 역방향 존 `0.0.10.in-addr.arpa`(`file "2"`) 추가, 두 존 모두 `allow-update { none; }`(이 단계에서는 역방향 레코드 미작성)
  - `/var/named/named.localhost`를 복사해 존 파일 `1` 작성, 존 파일 권한 `chmod o+r` 부여
  - 존 파일 `1`: `$TTL 1D`, `SOA`(`ns1.shkwon.local.`), `NS`, `MX 10`, `A` 레코드(`www`, `ftp`, `ns1`, `mx1`), `CNAME` 레코드(`babo` → `ftp`)
  - 도메인으로 끝나는 이름은 반드시 끝에 `.`(점) 지정
  - `systemctl start named`, `firewall-cmd --permanent --add-port=53/udp` 후 `--reload`
  - 확인: Windows `nslookup`으로 `shkwon.local`, `www.shkwon.local`, `ftp.shkwon.local` 정방향 질의
  - FTP 서버 접속이 안 될 때는 보조 DNS 서버를 제외하고 확인
- DNS 구성 실습 2(`rocky9-2`)
  - `vsftpd` 설정을 다시 구성하고 `ftp.shkwon.local`로 FTP 접속, 배너와 로그인 성공 확인
  - 재귀(순환) 쿼리 개념 정리
- DNS 복습 2: 초기화 후 재구성
  - 초기화: 방화벽 `53/udp` 삭제, `dnf remove bind bind-utils bind-libs`, `named.conf.rpmsave`, `named.rfc1912.zones.rpmsave`, `/var/named/` 삭제
  - 재설치 후 `named.conf` 수정, `vi`의 `:23,27co$`, `:41,45co$` 명령으로 기존 존 설정 블록 복사 후 정방향·역방향 존 작성
  - 정방향 존 파일 `1`: `A` 레코드와 `MX` 레코드(`mx1`) 추가, 역방향 존 파일 `2`: `PTR` 레코드(`11` → `ns1.shkwon.local.`)
  - `rocky9-2`, `rocky9-3`에 `httpd` 설치 후 `systemctl start httpd`, 방화벽 `80/tcp` 허용
  - `nslookup` 확인: 하나의 이름(`www`)에 `10.0.0.11`, `10.0.0.12`, `10.0.0.13` 세 개의 `A` 레코드를 등록하면 모든 주소가 응답
- DNS 복습 3: 이전 데이터 삭제 후 재구성
  - `rocky9-1`의 `/var/www/html/index.html`에 `SHKWON-WEBSERVER-1` 작성, `bind`·`bind-utils`·`bind-libs` 재설치
  - `named.conf`, `named.rfc1912.zones`, 존 파일 `1`·`2` 재작성(`www`는 `10.0.0.11`, `10.0.0.12`, `10.0.0.13` 등록, `ftp`는 `10.0.0.12`, `mx1`은 `10.0.0.13`)
  - 존 파일 `1`·`2`에 `chmod o+r` 부여, `systemctl start named`, `53/udp` 허용
  - `ipconfig /flushdns` 후 `nslookup`으로 `www.shkwon.local`의 다중 주소 응답 확인
- 2026-11-11 과제 결과
  - `w10-1`의 브라우저에서 `shkwon.local`을 포함한 각 구성원의 `이니셜.local` 도메인으로 접속, 도메인별 WEB 서버 페이지 정상 출력

### 2026-11-12 (62일차)

- 주제 메모: OWASP Top 10 확인
- 1교시: Linux 서버 구성(`rocky9-1`, `rocky9-2`, `rocky9-3`)
  - DHCP(`rocky9-1`, `dhcp-server`)
    - `dhcpd.conf` 범위 `10.0.0.31` ~ `10.0.0.250`, 도메인 `shkwon.local`, 게이트웨이 `10.0.0.254`, 임대 시간 `7200`초
    - DNS 서버 주소를 `10.0.0.11`(자기 자신)로 변경, 대외 DNS는 `168.126.63.1` 추가
    - `w10`, `w11`은 MAC 주소 기준으로 `10.0.0.101`, `10.0.0.201` 예약
  - 주 DNS(`rocky9-1`, `bind`)
    - `named.conf`의 `options`에서 `listen-on port 53 { any; }`, `allow-query { any; }` 설정, DNSSEC 키 파일(`/etc/named.root.key`) include 확인
    - `named.rfc1912.zones`에 정방향 존 `shkwon.local`(파일 `1`), 역방향 존 `0.0.10.in-addr.arpa`(파일 `2`)를 `type master`로 추가, `allow-update`에 보조 DNS 주소 `10.0.0.12`, `10.0.0.13` 지정
    - `named.localhost`, `named.loopback`을 복사해 존 파일 `1`, `2` 작성 후 `chmod o+r` 부여
    - 존 파일 `1`: `NS`(`ns1`, `ns2`, `ns3`), `MX 10`(`mx1`), `@`와 `www`에 `10.0.0.11`, `10.0.0.12`, `10.0.0.13` 3개 `A` 레코드, `ftp`, `ns1` ~ `ns3`, `mx1`, `CNAME`(`babo` → `ftp`)
    - 존 파일 `2`: `PTR` 레코드 `11`, `12`, `13` → `ns1` ~ `ns3`
    - 방화벽 `53/{tcp,udp}` 허용 후 `systemctl restart named`
  - 웹 서버(3대 공통): `httpd` 설치, `/var/www/html/index.html`에 `SHKWON-WEBSERVER-1`, `-2`, `-3` 작성, 방화벽 `80/tcp` 허용 후 `systemctl start httpd`
  - FTP(`rocky9-2`, `vsftpd`)
    - 접속 거부 목록 파일 `/etc/vsftpd/user_list`와 `userlist_enable=YES` 옵션 확인
    - 사용자 `a`, `b` 생성 후 `dd`로 300M 파일(`a.txt`, `b.sh`) 생성, 배너 파일 `/shkwon/ban`, `/shkwon/ch` 작성
    - `pasv_min_port=65000`, `pasv_max_port=65010`, `deny_file={*.sh}` 설정, 방화벽 `21/tcp`, `65000-65010/tcp` 허용 후 `systemctl restart vsftpd`
  - `w10`, `w11`에서 `ipconfig /release`, `/renew`로 주소 재발급 후 `www.shkwon.local` 접속
    - 같은 이름에 `A` 레코드가 여러 개이면 접속할 때마다 `SHKWON-WEBSERVER-1`, `-2` 등 서로 다른 서버 화면 출력
- 2교시: 보조 DNS 구성
  - `rocky9-2`, `rocky9-3`: `bind` 설치, `named.conf`의 `options` 설정, 존을 `type slave`, `masters { 10.0.0.11; }`로 구성(zone 구성만 정확히 작성)
  - 주 DNS의 존 파일 수정 시 시리얼 번호를 올려 보조 DNS에 변경 사항 전파(`0` → `2` → `4` → `8`)
  - 보조 DNS의 `/var/named/`에 존 파일 `1`, `2`가 자동 생성되고 소유자가 `named`로 표시되는 것으로 영역 전송 확인
  - Windows 클라이언트의 DNS 서버를 `10.0.0.12`, `10.0.0.13`으로 바꿔 `nslookup` 해도 주 DNS와 같은 응답 확인
- 3, 4교시: 복습(전체 재구성)
  - `rocky9-1`: `dnf install -y dhcp-server bind bind-utils bind-libs httpd`로 DHCP, DNS, 웹 서버를 한 번에 설치
  - `rocky9-2`: `vsftpd`, `bind`, `httpd` / `rocky9-3`: `bind`, `httpd` 설치, `dnf history list`로 설치 이력 확인
  - DHCP, 주·보조 DNS, 웹, FTP를 처음부터 다시 구성하고 `w10`, `w11`에서 접속 확인
- 5교시: Windows 계정 정책과 보안 옵션(`W2K22-AD`, `W2K22-MEM2`)
  - 로컬 그룹 정책 편집기(`gpedit.msc`): 컴퓨터 구성 → Windows 설정 → 보안 설정 → 계정 정책
  - 암호 정책: 복잡성 사용, 최대 암호 사용 기간 42일, 최소 암호 길이 7문자 확인
    - 정책에 맞지 않는 암호로 `compmgmt.msc`에서 사용자를 만들면 오류 발생
  - 계정 잠금 정책: 잠금 임계값 5회, 잠금 기간 5분(`2`분에서 변경), 관리자 계정 잠금 허용은 사용 안 함
    - 비밀번호를 5회 틀리면 "참조된 계정이 현재 잠겨 있으므로 로그온할 수 없습니다" 메시지 출력
  - 보안 옵션
    - 시스템 종료: 로그온하지 않고 시스템 종료 허용, 로그인 화면에 종료 버튼 표시
    - 대화형 로그온: 마지막 로그온 사용자 이름 표시 안 함 → 기타 사용자 화면으로 변경
    - 대화형 로그온 메시지: 제목 `보안 경고!!`, 본문 `비인가자 무단 접근 시 형사 처벌 대상이 됩니다.`
    - 계정: Administrator 계정 이름 바꾸기
  - `gpupdate /force` 적용 후 로그아웃·재로그인으로 확인
  - 실습 후 `W2K22` 전체를 스냅샷으로 초기화, `W2K22-MEM1`, `W2K22-MEM2`는 원격 데스크톱 서비스 삭제 후 초기 설정 스냅샷 생성
  - `W2K22-AD`에 DHCP, DNS, 웹 서버(IIS) 역할 설치, DHCP에서 `w10`, `w11` 주소 예약(`10.0.0.101`, `10.0.0.201`)
- 6교시: Sysinternals와 Windows 서버 구성
  - Sysinternals 도구 다운로드(`Autoruns64`, `TCPView64`, `BGInfo64`)
    - `BGInfo`로 바탕화면에 Host Name, IP Address, Default Gateway 표시(`W2K22-AD` `10.0.0.21`, `W2K22-MEM1` `10.0.0.22`, `W2K22-MEM2` `10.0.0.23`)
  - `W2K22-MEM1`(FTP): 사용자 `a`, `b` 생성, PowerShell로 `C:\01_FTP\LocalUser\a\a.txt`, `b\b.txt` 생성
    - IIS 역할 서비스에서 FTP 서버와 관리 도구 설치, FTP 사이트 `shkwon_ftp`(경로 `C:\01_FTP`, 포트 `21`, SSL 사용 안 함, 기본 인증 사용, `a`, `b` 읽기·쓰기 허용)
    - FTP 메시지(배너 `Warning! SHKWON-W2K22-FTPSERVER`, 시작 메시지 `%username%님 안녕하세요`)
    - FTP 사용자 격리: 사용자 이름 실제 디렉터리 사용
    - FTP 방화벽 지원의 데이터 채널 포트 범위 `60000-60010`, 방화벽 규칙 `60000-60010`, `21` 허용 후 FTP 서비스 재시작
    - `w10`에서 `ftp 10.0.0.22` 접속, `a`와 `b` 모두 자기 폴더의 파일(`a.txt`, `b.txt`)만 조회
  - Default Web Site에 취약점이 있어 `W2K22-AD`, `MEM1`, `MEM2`에서 모두 삭제
  - 웹 사이트 구성(AD, MEM1, MEM2 공통)
    - `C:\11_web\index.html` 작성(`SHKWON-W2K22-WEBSERVER-번호`), 웹 사이트 `shkwon_main` 추가(포트 `80`)
    - 인증은 익명 인증 사용, 기본 문서에서 `index.html`을 맨 위로 이동
- 7교시: Windows DNS 서버
  - `W2K22-AD`(주 DNS)
    - 정방향 조회 영역 `shkwon.local` 추가: 주 영역, 파일 `shkwon.local.dns`, 동적 업데이트 허용 안 함
    - 이름 서버 탭에 `ns1.shkwon.local`(`10.0.0.21`) 등록, `ns2`, `ns3` 추가
    - 레코드: `@`, `www`에 `10.0.0.21`, `10.0.0.22`, `10.0.0.23`, `ftp`(`10.0.0.22`), `ns1` ~ `ns3`, `CNAME`(`babo` → `ftp.shkwon.local`), `wwww`
    - 역방향 조회 영역 `0.0.10.in-addr.arpa`(IPv4, 네트워크 ID `10.0.0`) 생성 후 `PTR` 레코드 `10.0.0.21` ~ `10.0.0.23` → `ns1` ~ `ns3`
    - 영역 전송 허용: 다음 서버로만(`10.0.0.22`, `10.0.0.23`)
  - `W2K22-MEM1`, `W2K22-MEM2`(보조 DNS)
    - 새 영역 마법사에서 보조 영역 선택, 영역 이름 `shkwon.local`, 마스터 서버 `10.0.0.21`, 역방향 영역도 같은 방식으로 생성
    - `F5`(새로고침) 후 보조 서버에 레코드 복제 확인
  - 확인: `w10`에서 `nslookup`(DNS 서버를 `10.0.0.21`, `10.0.0.22` 등으로 변경)으로 `shkwon.local`, `www`, `ftp` 질의, `ftp.shkwon.local` FTP 접속
  - `C:\Windows\System32\dns`의 `shkwon.local.dns`를 메모장으로 열어 SOA, NS 레코드 확인(Linux 존 파일과 같은 구조)
  - 복습 후 모든 VM을 스냅샷으로 초기 설정 복원

### 2026-11-13 (63일차)

- 1교시: 가상 호스트(Virtual Host) 개념과 구성 계획
  - 여러 웹 사이트 운영 방법: IP별로 다른 페이지, 포트별로 다른 페이지, 동일한 IP와 포트를 사용하는 가상 호스트(DNS 필수)
  - `blog`: IP 주소별 접근 제한(`w10`만 접속), `intra`: 내부 사용자(`a`, `b` 계정)만 접근 가능
  - 서버별 역할 정리: `AD`는 DHCP·DNS·웹, `MEM1`은 DNS·웹·FTP, `MEM2`는 DNS·웹
  - Cisco 장비 구조 개념 도식: Flash(IOS), CMOS, NVRAM(startup-config), RAM(running-config), 부팅 시 설정 불러오기 흐름
  - FTP 폴더 구조 확인: `C:\01_FTP\LocalUser` 아래 `a`, `b`, `public`
  - IIS 기능 복습(`W2K22-AD`, `shkwon_main` 사이트 대상)
    - 기본 문서: `C:\11_MAIN`에 `babo.html` 추가 후 기본 문서 목록 맨 위에 등록
    - HTTP 리디렉션: 요청을 `https://www.naver.com/`으로 리디렉션, 상태 코드 `302`(찾음)
    - HTTP 응답 헤더, MIME 형식(`.mp4` → `video/mp4` 등), IP 주소 및 도메인 제한(`10.0.0.100`만 허용, 지정되지 않은 클라이언트는 거부)
    - 디렉터리 검색: 시간, 크기, 확장명, 날짜 표시 옵션 설정, 사용 시 폴더 목록 노출(`10.0.0.21 - /1/`)
    - 모듈, 압축(동적·정적 콘텐츠), 오류 페이지(`401` ~ `502`), 요청 필터링(HTTP 동사, 규칙, URL), 인증은 기능 위치와 역할 확인(모듈은 가급적 수정하지 않기)
  - HTTP 상태 코드: `200`번대 정상, `300`번대 리디렉션, `400`번대 클라이언트 측 오류, `500`번대 서버 측 오류
  - 주요 HTTP 메서드: `GET`(조회), `POST`(생성·제출), `PUT`(전체 교체), `PATCH`(일부 수정), `DELETE`(삭제), `HEAD`, `OPTIONS`, `TRACE`, `CONNECT`
- 2교시: Windows DNS 서버 역할 분리
  - `AD`는 주 DNS, `MEM1`은 보조 DNS(영역 전송을 `10.0.0.22`에 허용), `MEM2`는 스텁(Stub) 영역
  - 스텁 영역: NS, SOA, 글루 호스트(A) 레코드만 복사하는 영역 유형(해당 영역에 대한 권한은 없음)
  - `MEM2`에 정방향·역방향 모두 스텁 영역으로 생성(마스터 서버 `10.0.0.21`), 스텁 영역에는 레코드를 직접 추가하지 않음
  - 레코드 생성 시 "연결된 PTR 레코드 업데이트"는 체크하지 않기
  - `w10-1`의 DNS 서버를 `10.0.0.23`(`MEM2`)으로 지정 후 `nslookup`으로 `shkwon.local` 조회, 권한 없는 응답으로 `10.0.0.21` ~ `10.0.0.23` 확인
- 3교시: IIS 가상 호스트 구성(호스트 이름 기반)
  - 사이트 폴더 생성: `C:\11_MAIN`, `C:\12_BLOG`, `C:\13_INTRA`(각 `index.html` 작성)
  - 페이지 문구: `AD`는 `SHKWON-W2K22-BLOG-1`, `MEM1`은 `BLOG-2`, `INTRA-2`, `MEM2`는 `INTRA-3`
  - 사이트 `shkwon_blog`(경로 `C:\12_BLOG`, 포트 `80`, 호스트 이름 `blog.shkwon.local`), `shkwon_intra`(`C:\13_INTRA`, `intra.shkwon.local`) 추가
    - `AD`, `MEM1`: `blog` / `MEM1`, `MEM2`: `intra`
  - DNS 레코드 추가: `blog`(`10.0.0.21`, `10.0.0.22`), `intra`(`10.0.0.22`, `10.0.0.23`)
  - `blog` 접근 제한: IP 주소 및 도메인 제한에서 `10.0.0.100`(`w10`)만 허용, 지정되지 않은 클라이언트는 거부
    - `w10`은 접속 가능, `w11`은 접속 불가
  - `intra` 접근 제한: 익명 인증 사용 안 함, 기본 인증 사용, 로컬 계정 `a`, `b` 생성
    - Chrome에서 `intra.shkwon.local` 접속 시 로그인 창 출력, 인증 후 `SHKWON-W2K22-INTRA-3` 페이지 확인
- 4교시: 팀원의 두 번째 서버에 도메인으로 접속하는 상호 점검
- 5교시: GNS3 실습 환경 구축
  - Cisco IOS 이미지(`c2691`, `c3745`)를 GNS3용 이미지 저장소에서 내려받아 준비
  - GNS3 `2.2.61` 설치: 구성 요소는 GNS3 Desktop, WinPcap, Dynamips, QEMU, VPCS, Cpulimit 선택, Solarwinds 도구 체험은 `No`
  - VirtualBox `7.2.22`와 Extension Pack 설치, 기본 머신 폴더 경로 수정
  - 가상 머신 `rocky9-tem` 생성(Rocky Linux 9.8 minimal ISO), VMware와 다른 방식의 NAT 구조를 확인하고 네트워크를 NAT에서 "연결되지 않음"으로 변경
  - GNS3 실행: 초기 마법사에서 로컬 컴퓨터 실행 선택, `Edit` → `Preferences` → `General` → `Console applications` 설정
  - `Dynamips` → `IOS routers`에 `c2691` 새 템플릿 등록(WIC `WIC-2T`, Idle-PC finder로 Idle-PC 값 확인), `c3745`도 같은 방식으로 추가
  - 프로젝트 `test` 생성
- 6교시: 라우터 2대와 Linux 서버 연동 실습
  - `rocky9-tem` 준비: `grubby --update-kernel ALL --args selinux=0` 실행 후 종료, 완전한 복제로 `rocky9-1`, `rocky9-2` 생성
  - 토폴로지(`test` 프로젝트): `R1`(Seoul) ↔ `R2`(Busan) 시리얼 연결, 각 라우터 아래 `Switch`와 `VPCS`(`PC1`, `PC2`) 연결
    - 서울 `10.0.0.0/24`(게이트웨이 `10.0.0.254`), 부산 `10.0.1.0/24`(게이트웨이 `10.0.1.254`), 라우터 간 `172.16.0.0/30`(`R1` `172.16.0.1`, `R2` `172.16.0.2`)
  - VPCS 설정: `ip 10.0.0.1/24 10.0.0.254`, `ip 10.0.1.1/24 10.0.1.254`, `ip dns 168.126.63.1 8.8.8.8`, `save`, `show ip`로 확인
  - 라우터 설정(`R1`, `R2` 공통 흐름)
    - `hostname`을 `Seoul_R1`, `Busan_R1`로 지정, `interface f0/0`에서 `ip add`, `no sh`, `do wr`로 저장
    - `interface s0/0`에 `172.16.0.1/30`, `172.16.0.2/30` 지정 후 `do ping`으로 라우터 간 통신 확인(성공률 100 percent)
    - 기본 경로 `ip route 0.0.0.0 0.0.0.0 상대 라우터 주소` 설정
  - `PC1`에서 `PC2`(`10.0.1.1`)로 `ping`: 초기 2회는 timeout 후 성공(`ttl=62`)하고, `PC2`에서 `PC1`으로도 성공
  - 개념 정리
    - 라우터: 서로 다른 네트워크의 통신을 연결, 라우팅 테이블 기반으로 패킷을 최적 경로로 전송
    - 스위치: 동일한 네트워크에서 노드를 확장, MAC 주소 기반으로 전송
  - GNS3에 VirtualBox VM 템플릿으로 `rocky9-1`, `rocky9-2` 등록 후 `test1` 프로젝트 생성
  - `rocky9-1`: `nmtui`로 `10.0.0.1/24`, 게이트웨이 `10.0.0.254`, DNS `168.126.63.1`, `8.8.8.8` 설정 후 `ip a`, `hostnamectl` 확인
  - `rocky9-2`: `10.0.1.1/24`, 게이트웨이 `10.0.1.254`로 같은 방식 구성
  - `R2`의 `f0/1`에 클라우드(이더넷) 노드를 연결하는 외부 통신 구성 시작(다음 주 진행)
- 7교시: 이번 주 학습 내용 정리

### 2026-11-16 (64일차)

> 14주차 시작. 주제: Linux 가상 호스트(Apache `httpd`)

- 1교시: Linux DHCP 서버 구성(`rocky9-1`)
  - `/etc/dhcp/dhcpd.conf` 작성: 범위 `10.0.0.31` ~ `10.0.0.250`, DNS `10.0.0.11`, `168.126.63.1`, 도메인 `shkwon.local`, 게이트웨이 `10.0.0.254`, 임대 시간 `7200`초
  - `w10`, `w11`은 MAC 주소 기준으로 `10.0.0.101`, `10.0.0.201` 고정 할당
  - `systemctl restart dhcpd`로 적용
- 2교시: Linux 서버 3대 구성(`rocky9-1` ~ `rocky9-3`)
  - `dnf history list`로 서버별 패키지 설치 이력 확인(`dhcp-server`, `bind`, `bind-utils`, `bind-libs`, `httpd`)
  - FTP(`rocky9-2`, `vsftpd`)
    - `/shkwon/ban`, `/shkwon/ch` 배너 파일 작성, `vsftpd.conf` 수정 후 `systemctl restart vsftpd`
    - 사용자 `a`, `b` 생성, `dd`로 300M 파일(`/home/a/a.txt`, `/home/b/b.sh`) 생성
    - 방화벽 `21/tcp`, `65000-65010/tcp` 허용
  - 주 DNS(`rocky9-1`)
    - `named.conf`: `listen-on port 53 { any; }`, `allow-query { any; }`
    - `named.rfc1912.zones`: 정방향 존 `shkwon.local`(파일 `1`), 역방향 존 `0.0.10.in-addr.arpa`(파일 `2`) `type master`, `allow-update`에 `10.0.0.12`, `10.0.0.13` 지정
    - `named.localhost`, `named.loopback`을 복사해 존 파일 작성, `chmod o+r` 부여
    - 정방향 존: `NS`(`ns1` ~ `ns3`), `MX 10`, `@`와 `www`에 `10.0.0.11` ~ `10.0.0.13`, `ftp`, `CNAME`(`babo` → `ftp`), `ns1` ~ `ns3`, `mx1`
    - 역방향 존: `PTR` 레코드 `11` ~ `13` → `ns1` ~ `ns3`
    - 방화벽 `53/{tcp,udp}`, `80/tcp` 허용
  - 보조 DNS(`rocky9-2`, `rocky9-3`)
    - 존을 `type slave`, `masters { 10.0.0.11; }`로 구성 후 `systemctl start named`
    - `/var/named/`에 존 파일 `1`, `2`가 자동 생성(소유자 `named`)되어 영역 전송 확인
- 2교시 후반: Apache 설정 파일 분석(`vi /etc/httpd/conf/httpd.conf`, `rocky9-1`)
  - 줄 번호별 주요 항목
    - `34` 서버 루트, `47` 네트워크 카드(리슨 주소·포트), `61` 모듈
    - `71`, `72` 실행 사용자·그룹, `91` 서버 관리자 메일 주소(`web@shkwon.local`)
    - `107` 디렉토리 경로 기본 접근 거부, `124` 웹 콘텐츠 디렉토리, `129` `/var/www` 디렉토리(`blog`, `intra` 페이지)
    - `136`(`149`, `156`) `/var/www/html` 디렉토리 옵션(`Options FollowSymLinks`, `AllowOverride None`, `Require all granted`), `168` 기본 문서(`DirectoryIndex`)
    - `176` 파일 접근 제어, `187` 에러 로그(`logs/error_log`), `194` 로그 레벨(`debug`, `info`, `notice`, `warn`, `error`, `crit`)
    - `201` 접속 클라이언트 정보(User-Agent) 로그, `222` 접속 로그(`combined`, `logs/access_log`)
    - `252` `ScriptAlias`, `271` `TypesConfig`, `358` `IncludeOptional`(`conf.d/*.conf` 로드)
- 3교시: 기본 웹 서버와 가상 호스트 구성
  - `rocky9-1` ~ `rocky9-3` 공통: `httpd` 설치, `ServerAdmin` 변경, `DirectoryIndex`에 `babo.html` 추가, 사이트 폴더 `/var/www/html`, `/var/www/blog`, `/var/www/intra` 생성 후 각 `index.html` 작성
  - `welcome.conf`를 `welcome.conf.bak`으로 이름 변경해 기본 테스트 페이지 비활성화(`index.html`이 없으면 `403 Forbidden` 출력), `index.html`을 `babo.html`로 바꿔 `DirectoryIndex` 우선순위 확인
  - 메모: 데스크톱 환경에 Firefox 설치, User-Agent Switcher 확장 설치(`httpd.conf`의 User-Agent 로그 항목 실습 관련)
  - 가상 호스트 설정(`httpd.conf` 맨 아래 또는 `conf.d/virtual.conf`)
    - `NameVirtualHost *:80`, `<VirtualHost *:80>`마다 `ServerName`, `DocumentRoot` 지정
    - `www.shkwon.local`(`ServerAlias shkwon.local`) → `/var/www/html`, `blog.shkwon.local` → `/var/www/blog`, `intra.shkwon.local` → `/var/www/intra`
    - 설정 파일을 서버 3대에 같은 내용으로 적용(`vi` 명령 모드 `Ctrl + V`로 줄 번호 열 선택 삭제 활용)
  - DNS에 `blog`(`10.0.0.11`, `10.0.0.12`), `intra`(`10.0.0.12`, `10.0.0.13`) `A` 레코드 추가, 서버 3대 모두 `systemctl restart httpd`
  - 결과: `w10`, `w11`에서 `www.shkwon.local`, `blog.shkwon.local`, `intra.shkwon.local` 접속 시 서버별 페이지 출력
    - `netstat -na -p tcp`로 클라이언트가 서버 3대(`10.0.0.11` ~ `10.0.0.13`)의 `80`번 포트에 연결된 상태 확인
- 4교시: 복습을 위한 초기화
  - DNS, `httpd`만 삭제: `dnf autoremove -y httpd bind bind-utils bind-libs`
  - 설정 잔여 파일 삭제: `rm -rf /etc/named.conf.rpmsave /etc/named.rfc1912.zones.rpmsave /etc/httpd/ /var/www/ /var/named/`
  - 방화벽 규칙 삭제: `80/tcp`, `53/{tcp,udp}` 제거 후 `firewall-cmd --reload`
  - 재설치: `dnf install -y httpd bind bind-utils bind-libs`(3대 모두)
- 5교시: DNS·`httpd` 복습(전체 재구성)
  - `rocky9-1`: `named.conf`, `named.rfc1912.zones`, 존 파일 `1`·`2` 작성(시리얼 증가), `chmod o+r`, 방화벽 허용 후 `systemctl enable --now named httpd`
  - `rocky9-2`, `rocky9-3`: 슬레이브 존 구성, `/var/www/{html,blog,intra}`와 `index.html` 작성, `welcome.conf` 비활성화
  - `/etc/httpd/conf.d/virtual.conf`에 가상 호스트 작성 후 `systemctl enable --now httpd`
- 6교시: 가상 호스트 접근 제어
  - 목표: `blog`는 `w10`만 접속 가능, `intra`는 등록된 계정만 접속 가능
  - IP 기반 접근 제어(`/etc/httpd/conf.d/virtual.conf`)
    - `<Directory "/var/www/blog">` 안에 `Order deny,allow`, `Allow from 10.0.0.101`, `Deny from all` 지정
    - `Order deny,allow`는 `Deny`를 먼저 평가한 뒤 `Allow`를 평가하므로 일치하는 `Allow`가 우선
    - 주소는 `10.0.0` 또는 `10.0.0.0/255.255.255.0` 형식도 사용 가능
  - 계정 기반 접근 제어
    - `<Directory "/var/www/intra">`에 `AllowOverride AuthConfig` 지정
    - `/var/www/intra/.htaccess`에 4줄 작성(반드시 기억할 항목)
      - `AuthName "Test_Auth"`
      - `AuthType Basic`(암호화 방식을 바꾸는 `Digest` 방식도 있음)
      - `AuthUserFile /web/.auth`
      - `Require user a b`
    - `mkdir /web` 후 `htpasswd -c /web/.auth a`(`-c`는 파일을 처음 만들 때만), `htpasswd /web/.auth b` 실행
    - `cat /web/.auth`에서 사용자별 암호가 해시(`$apr1$...`)로 저장된 것을 확인
    - 서버 3대 모두 적용 후 `systemctl restart httpd`
  - 결과
    - `blog.shkwon.local`: `w10`에서는 정상 출력, `w11`에서는 `403 Forbidden`
    - `intra.shkwon.local`: 접속 시 로그인 창 출력, `a`, `b` 계정으로 인증 후 페이지 출력
- 7교시: 과제
  - 팀원 도메인으로 접속하면 두 번째 서버(`rocky9-2`)로 접속되도록 구성
  - `blog`는 IP 제한, `intra`는 팀원별 이니셜 계정을 생성해 로그인
  - 결과 확인: `w10-1`에서 팀원 3명의 `blog` 도메인과 `blog.shkwon.local` 모두 `WEBSERVER-2` 페이지 출력
    - `w11-1`에서는 `intra` 도메인마다 로그인 창이 뜨고 인증 후 페이지 출력, `blog`는 허용 IP가 아니면 `403 Forbidden`

### 2026-11-17 (65일차)

> 주제: 메일 서버(Windows hMailServer, Linux sendmail·Dovecot)

- 1교시: 전자우편 서비스 개념
  - 프로토콜은 TCP 사용
  - 포트
    - 메일 송신: SMTP `25`(SSL 사용 시 `465`)
    - 메일 수신: POP3 `110`(SSL 사용 시 `995`), IMAP `143`(SSL 사용 시 `993`)
  - POP3: 메일 수신 시 클라이언트로 다운로드, 단말이 여러 대이면 메일 통합 작업 필요, 서버 사서함 용량 관리 불필요
  - IMAP: 메일 수신 후에도 서버에 메일이 남음, 단말이 여러 대여도 통합 작업 불필요, 서버 사서함 용량 관리 필요
  - SSL 사용 목적: 전송 데이터 암호화, 종단 간 신뢰성 확보(제3자 인증), 메모: 탈중앙화 블록체인
  - 오늘 사용 도구: 서버 `hMailServer`(Windows), 클라이언트 `Thunderbird`(`w10`, `w11`)
  - 서버 역할 확인: `W2K22-AD`는 DHCP·DNS·IIS, `W2K22-MEM1`은 DNS·IIS(+FTP), `W2K22-MEM2`는 DNS·IIS(+메일)
    - IIS 사이트 폴더: `C:\11_MAIN`, `C:\12_BLOG`, `C:\13_INTRA`
- 2교시: 메일 서버 준비(Windows)
  - DNS 역할 조정: `W2K22-MEM1`을 주 DNS로, `W2K22-AD`와 `W2K22-MEM2`를 서브 DNS로 설정
  - 메일 교환 레코드(`MX`) 추가: 메일 서버 FQDN `mx1.shkwon.local`, 우선 순위 `10`, 호스트 `mx1`은 `A` 레코드로 `W2K22-MEM2`(`10.0.0.23`) 등록
  - `blog` 사이트 IP 제한 확인: `10.0.0.100`만 허용, 지정되지 않은 클라이언트는 거부(거부 동작 "찾을 수 없음")
  - `W2K22-MEM1`, `W2K22-MEM2`에 사용자 `a`, `b` 생성
  - `W2K22-MEM2`에 `hMailServer` 설치(관리 비밀번호 설정), 실행 후 `Connect`로 관리 화면 접속
  - `w10`, `w11`에 `Thunderbird` 설치
- 3교시: 메일 동작 구조와 hMailServer 구성
  - 메일 동작 구조 용어
    - `MUA`(Mail User Agent): 사용자가 메일을 쓰고 읽는 프로그램
    - `MTA`(Mail Transfer Agent): 메일 서버끼리 메일을 전달하는 프로그램
    - `MDA`(Mail Delivery Agent): 사용자 사서함에 메일을 전달하는 프로그램
  - 메일 전달 흐름: `MUA` → `MTA`(SMTP `25`) → `MTA` → `MDA` → 사서함 → `MUA`(POP3·IMAP으로 수신)
    - Linux 구성: `sendmail`(MTA) + `dovecot`(POP3·IMAP)
  - hMailServer 설정
    - `Domains` → `Add domain`: `shkwon.local`(Enabled)
    - `Accounts` → `Add`: `a@shkwon.local`, `b@shkwon.local`(관리 수준 `User`)
    - `Settings` → `Protocols`: SMTP, POP3, IMAP 사용
    - `Logging`: Application, SMTP, POP3, IMAP, TCP/IP 로그 사용
    - `Advanced` → `Auto-ban`: 잘못된 로그온 5회, 30분 후 초기화, 60분 차단
      - 5회 오류 시 IP가 `IP Ranges`에 등록되어 접속이 막히므로, 사용하지 않을 때는 삭제
  - 방화벽 인바운드 규칙: TCP 로컬 포트 `25, 110, 143` 허용
  - Thunderbird 연동
    - `w10`: `a@shkwon.local`, IMAP(포트 `143`), 보내는 서버 포트 `25`, 서버 주소는 `mx1.shkwon.local` 또는 메일 서버 IP(`10.0.0.23`) 모두 사용 가능
    - `w11`: `b@shkwon.local`, POP3(포트 `110`), 보내는 서버 포트 `25`
    - 설정 검토에서 인증 방법 "일반 비밀번호", 연결 보안 "없음" 확인(SSL 미사용)
  - 메일 송수신 테스트: `w11`이 `a`, `b`에게 `mail test` 발송 → `w10`에서 수신 후 답장(`Re: mail test`) → `w11` 수신
  - Thunderbird 계정을 삭제하고 `a`, `b` 계정을 IMAP과 POP3로 다시 연결해 수신 방식 비교(메일 서버 주소는 IP `10.0.0.23`으로 입력)
  - 실습(점심시간까지): 팀원에게 메일 발송, 방화벽 열기, 포트 포워딩, DNS, 메일 계정 생성
- 5교시: Linux 메일 서버(`rocky9-3`)
  - 사전 준비: 모든 Rocky 서버의 DNS를 `10.0.0.11`로 변경, 사용자 `x`, `y` 생성
    - `/etc/group`의 `mail` 그룹에 `x`, `y` 추가(`mail:x:12:x,y`)
    - 패키지 설치: `dnf install -y sendmail sendmail-cf dovecot`
  - `sendmail` 구성(관련 파일: `access`, `sendmail.cf`, `sendmail.mc`, `local-host-names`)
    - `/etc/mail/sendmail.mc` 수정(`dnl`은 주석 표시이므로 지우면 활성화)
      - `21`번 줄: 로그 레벨 `confLOG_LEVEL` `14`
      - `56`, `57`번 줄: 인증 방식 `TRUST_AUTH_MECH`, `confAUTH_MECHANISMS` 활성화
      - `121`번 줄: `DAEMON_OPTIONS(`Port=smtp, Name=MTA')`(`Addr=127.0.0.1` 제한 제거로 외부 수신 허용)
    - `m4 /etc/mail/sendmail.mc > /etc/mail/sendmail.cf`로 설정 파일 생성(`sendmail.cf` 직접 수정은 `Cwlocalhost`, `Fw/etc/mail/local-host-names` 확인 정도)
    - `/etc/mail/local-host-names`: `mx1.shkwon.local`, `shkwon.local` 등록
    - `/etc/mail/access`: `localhost`, `127.0.0.1`, `mx1.shkwon.local`, `10.0.0`, `10.0.0.0/255.255.255.0`, `shkwon.local`에 `RELAY` 허용
    - `makemap hash /etc/mail/access < /etc/mail/access`로 `access.db` 생성
    - `systemctl enable --now sendmail` 후 `systemctl status sendmail`로 `active (running)` 확인
  - `dovecot` 구성(관련 파일: `10-auth`, `mail`, `master`, `ssl`)
    - `/etc/dovecot/dovecot.conf`: `protocols = imap pop3 lmtp submission`, `listen = *, ::`
    - `conf.d/10-auth.conf`: `disable_plaintext_auth = no`
    - `conf.d/10-ssl.conf`: `ssl = no`
    - `conf.d/10-mail.conf`: `mail_location = mbox:~/mail:INBOX=/var/mail/%u`
    - `conf.d/10-master.conf`: `pop3-login`의 `port = 110`, `imap-login`의 `port = 143` 활성화
    - `systemctl enable --now dovecot`, 방화벽 `firewall-cmd --permanent --add-port={25,110,143}/tcp` 후 `--reload`
  - Thunderbird 연동(보안 예외 확인 필요)
    - `w10`: `x@shkwon.local`, IMAP, 서버 `10.0.0.13`, 보내는 서버 `10.0.0.13`
    - `w11`: `y@shkwon.local`, POP3, 서버 `10.0.0.13`
    - 인증서 오류 창에서 보안 예외 추가 후 계정 설정 완료
  - 송수신 테스트: `x` → `y`로 `test_x` 발송, `y`가 `Re: test_y`로 답장
- 6교시: 복습(전체 재구성)
  - `w10`, `w11`의 Thunderbird 계정 삭제, `rocky9-1`, `rocky9-3` 스냅샷 초기화
  - `rocky9-1`: DHCP, DNS / `rocky9-3`: DNS, 메일(`sendmail`), `dovecot`
  - `rocky9-1`: DHCP 설정, 서비스 enable → DNS 설정, 서비스 enable
  - `rocky9-3`: 사용자 `aa`, `bb` 생성과 `mail` 그룹 추가 → 패키지 설치 → DNS 설정, 방화벽 허용, 서비스 enable → `sendmail.mc` 편집, `m4`로 `sendmail.cf` 생성, `local-host-names`, `access` 편집, `makemap hash` → 방화벽 허용, 서비스 enable → `dovecot.conf`, `10-auth`, `10-ssl`, `10-mail`, `10-master` 편집, 서비스 enable
  - 보충: `cat > 1.txt << eof` 형식의 here document로 여러 줄 파일 작성 연습
  - 메일 구성도 정리: 도메인마다 `NS`(DNS)가 있고, 메일 서버끼리 SMTP로 전달하며, 수신 사용자(`babo@babo.local`)는 자기 도메인의 메일 서버에서 메일 수신
- 7교시: 과제
  - 팀원에게 메일 보내기

## 🎯 학습 목표

- VMware 기반 가상화 실습 환경 구축
- Linux와 Windows Server 기본 운영 및 계정·권한 관리 이해
- ACL과 공유 권한을 활용한 부서·직급별 접근통제 설계
- 파티션·파일시스템·마운트 구조 이해와 DHCP 서버 구성
- LVM을 활용한 논리 볼륨 생성과 용량 확장
- dnf, rpm, 소스 설치 방식 비교와 Linux DHCP 서버 구성
- FTP 동작 방식 이해와 Linux·Windows FTP 서버 구성(Active·Passive 모드, 사용자 격리)
- DNS 동작 원리 이해와 BIND 기반 정방향·역방향, 주·보조 DNS 서버 구성
- Windows 암호·계정 잠금 정책과 보안 옵션을 활용한 계정 보호
- Windows IIS 웹 서버와 Windows DNS 서버(주·보조) 구성
- IIS 가상 호스트와 접근 제어(IP 제한, 기본 인증) 구성
- GNS3와 VirtualBox를 활용한 라우팅 실습 환경 구축과 서로 다른 네트워크 간 통신 확인
- Apache 가상 호스트, IP 기반 접근 제어, 기본 인증을 활용한 Linux 웹 서버 구성
- SMTP·POP3·IMAP 동작 원리 이해와 Windows(hMailServer)·Linux(sendmail, Dovecot) 메일 서버 구성
- 클라우드 환경의 취약점 이해와 보안 구축 능력 향상

## 🔗 참고 링크

- [끊임없이 노력하는 엔지니어를 꿈꾸며](https://virtualtech.tistory.com/): 교수님 블로그로, 네트워크, 리눅스, 가상화, 클라우드, 보안 등 학습 주제와 관련된 자료를 확인할 수 있습니다.

## 🌐 이전 학습 과정: TCP/IP

TCP/IP 및 CSAP 학습 내용은 별도 저장소에서 관리합니다.

[MS8 TCP/IP 학습 저장소 바로가기](https://github.com/sinja2557/ms8-tcp-ip)

해당 저장소에서는 다음과 같은 학습 주제를 다룹니다.

- TCP/IP 네트워크 구조와 Cisco Packet Tracer 실습
- 실물 L2·L3 스위치, 정적 라우팅, RIP 라우팅
- Python 소켓 프로그래밍
- CSAP 클라우드 보안인증 학습 및 실습

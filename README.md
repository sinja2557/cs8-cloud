# MS8 Cloud

경기인력개발원 Microsoft Cyber Security 8회차 클라우드 학습 저장소입니다.

VMware 기반 가상화 실습 환경 구축부터 Linux·Windows Server 운영과 접근권한 관리, 클라우드 취약점, 시큐어 코딩, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹까지 클라우드 보안과 관련된 학습 자료 및 실습 기록을 정리합니다.

## 📚 학습 과정

- **학습 기간:** 2026-11-02 ~ 2027-03-12
- **교육 과정:** 경기인력개발원 Microsoft Cyber Security 8회차
- **주요 학습 분야:** 클라우드 취약점, 시큐어 코딩, 클라우드 시스템 보안, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹
- **주요 학습 도구:** VMware Workstation, Rocky Linux 9, Windows Server 2022, Windows 10·11, Xshell

## 🗂️ 학습 목차

| 순서 | 학습 자료 | 주요 내용 |
|---|---|---|
| 1 | [12주차](./12주차/) | VMware 가상화 실습 환경 구축, Linux 기본 명령어, 사용자·그룹 관리, ACL, 압축·스토리지 관리, Windows Server 공유 권한 및 DHCP 구성 |

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

### 8. 클라우드 보안 학습 확장

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

## 🎯 학습 목표

- VMware 기반 가상화 실습 환경 구축
- Linux와 Windows Server 기본 운영 및 계정·권한 관리 이해
- ACL과 공유 권한을 활용한 부서·직급별 접근통제 설계
- 파티션·파일시스템·마운트 구조 이해와 DHCP 서버 구성
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

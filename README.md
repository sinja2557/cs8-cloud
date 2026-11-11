# MS8 Cloud

경기인력개발원 Microsoft Cyber Security 8회차 클라우드 학습 저장소입니다.

VMware 기반 가상화 실습 환경 구축부터 Linux·Windows Server 운영과 접근권한 관리, 클라우드 취약점, 시큐어 코딩, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹까지 클라우드 보안과 관련된 학습 자료 및 실습 기록을 정리합니다.

## 📚 학습 과정

- **학습 기간:** 2026-11-02 ~ 2027-03-12
- **교육 과정:** 경기인력개발원 Microsoft Cyber Security 8회차
- **주요 학습 분야:** 클라우드 취약점, 시큐어 코딩, 클라우드 시스템 보안, 하이브리드 클라우드 보안 구축, Azure 클라우드 인프라, 데이터·앱 보안, 행위 기반 보안 탐지, 시스템 모의해킹
- **주요 학습 도구:** VMware Workstation, Rocky Linux 9, Windows Server 2022, Windows 10·11, Xshell, FileZilla, IIS, BIND

## 🗂️ 학습 목차

| 순서 | 학습 자료 | 주요 내용 |
|---|---|---|
| 1 | [12주차](./12주차/) | VMware 가상화 실습 환경 구축, Linux 기본 명령어, 사용자·그룹 관리, ACL, 압축·스토리지·LVM 관리, Windows Server 공유 권한 및 DHCP 구성 |
| 2 | [13주차](./13주차/) | Linux 패키지 관리(dnf, rpm, 소스 설치), vi 편집기, Linux DHCP 서버 구성, FTP 서버 구성(Linux vsftpd, Windows IIS, Passive 모드, 사용자 격리), DNS 서버(BIND) 구성 |

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
- 주 DNS·보조 DNS 구성과 Windows 클라이언트 DNS 설정

### 13. 클라우드 보안 학습 확장

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

## 🎯 학습 목표

- VMware 기반 가상화 실습 환경 구축
- Linux와 Windows Server 기본 운영 및 계정·권한 관리 이해
- ACL과 공유 권한을 활용한 부서·직급별 접근통제 설계
- 파티션·파일시스템·마운트 구조 이해와 DHCP 서버 구성
- LVM을 활용한 논리 볼륨 생성과 용량 확장
- dnf, rpm, 소스 설치 방식 비교와 Linux DHCP 서버 구성
- FTP 동작 방식 이해와 Linux·Windows FTP 서버 구성(Active·Passive 모드, 사용자 격리)
- DNS 동작 원리 이해와 BIND 기반 정방향·역방향 DNS 서버 구성
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

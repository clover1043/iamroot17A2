# iamroot17차 A-2조

## links
- www.iamroot.org | IAMROOT 홈페이지
- jake.dothome.co.kr | 문c 블로그

## 1주차
- 2020.08.22, 온라인, zoom (7명: 강현우, 권오훈, 김홍석, 문영진, 이하은, 하재혁, 황보람)
- Orientation
- 조장 및 총무 선정 - 조장 권오훈, 총무 황보람
- 리눅스 커널 내부구조 (처음 ~ 86page)
- 실습은 정규 스터디시간 이외의 시간에 각자 또는 같이 할 수 있는 사람들끼리 진행 / 결과는 github에 공유해주시면 **매우 감사합니다**.

## 2주차
- 2020.08.29, 온라인, zoom (7명: 강현우, 권오훈, 김홍석, 이하은, 이호영, 하재혁, 황보람)
- 리눅스 커널 내부구조 (~143page)

## 3주차
- 2020.09.05, 온라인, zoom (3명: 강현우, 권오훈, 황보람)
- 리눅스 커널 내부구조 (~203page)

## 4주차
- 2020.09.12, 온라인, zoom (5명: 강현우, 권오훈, 김홍석, 하재혁, 황보람)
- 리눅스 커널 내부구조 (~247page)

## 5주차
- 2020.09.19, 온라인, zoom (6명: 강현우, 권오훈, 김홍석, 이하은, 하재혁, 황보람)
- 코드로 알아보는 ARM 리눅스 커널 (~55page)

## 6주차
- 2020.09.26, 온라인, zoom (4명: 강현우, 권오훈, 하재혁, 황보람)
- ARM System Developer's Guide (~364page: 4,5,6,7,8장 skip)

## 7주차
- 2020.10.10, 온라인 + 오프라인 (4명: 강현우, 권오훈, 하재혁, 황보람)
- ARM System Developer's Guide (~517page: 10,11장 skip)

## 8주차
- 2020.10.17, A조로 통합, 온라인
- head.S(1)
http://www.iamroot.org/xe/index.php?document_srl=212919&mid=Note#0

## 9주차
- 2020.10.24, A조, 온라인
- head.S(2)
http://www.iamroot.org/xe/index.php?document_srl=212973&mid=Note#0

## 10주차
- 2020.10.31, A_2조, 온라인
- head.S(3)
- __create_page_tables 시작 ~ idmap map_memory까지

## 11주차
- 2020.11.07, A_2조, 온라인
- head.S(4)
- ~ __cpu_setup 까지

## 12주차
- 2020.11.14, A_2조, 온라인
- arm64 memory management 문서
  
  (https://developer.arm.com/architectures/learn-the-architecture/memory-management)
  
  ~ 4.Address spaces in AArch64
- head.S(5)

  ~ __enable_mmu 까지

## 13주차
- 2020.11.21, A_2조, 온라인
- head.S(6) 完

  ~ start_kernel 직전까지


## 14주차
- 2020.11.28, A_2조, 온라인
- start_kernel

  ~ smp_setup_processor_id 까지.

## 15주차
- 2020.12.05, A_2조, 온라인
- start_kernel
  - debug_objects_early_init();
  - cgroup_init_early()
  ~ init_cgroup_root 안에 init_cgroup_housekeeping 까지.

## 16주차
- 2020.12.12, A_2조, 온라인
- start_kernel
  - cgroup_init_early()
  - ㄴ for_each_subsys
  - ㄴ cgroup_init_subsys
  - ㄴ init_and_link_css

## 17주차
- 2020.12.19, A_2조, 온라인
- atomic operations
  - arch/arm64/include/asm/atomic.h
  - arch/arm64/include/asm/lse.h
  - arch/arm64/include/asm/atomic_lse.h
  - arch/arm64/include/asm/atomic_ll_sc.h

## 18주차
- 2020.12.26, A_2조, 온라인
- start_kernel
  - cgroup_init_early() fin.
  - local_irq_disable() fin. ==> 이미 irq는 disable 되어 있는 것 같은데 다시 disable하는 이유를 확인하다가 kernel_ventry로 빠짐.
- kernel_ventry
- el0_irq ongoing

## 19주차
- 2021.1.2, A_2조, 온라인
- armv8 exception model: https://developer.arm.com/architectures/learn-the-architecture/exception-model
- kernel_ventry
  - kernel_entry
    - el0_irq

## 20주차
- 2021.1.9, A_2조, 온라인
- el0_irq
  - ret_to_user
    - kernel exit
- el0_svc

## 21주차
- 2021.1.16, A_2조, 온라인
- boot_cpu_init
- page_address_init
- early_security_init
- setup_arch
  - kaslr_require_kpti

## 22주차
- 2021.1.23, A_2조, 온라인
- setup_arch
  - early_fixmap_init
  http://jake.dothome.co.kr/fixmap/
  http://jake.dothome.co.kr/kmap/

## 23주차
- 2021.1.30, A_2조, 온라인
- setup_arch
  - setup_machine_fdt
    - fixmap_remap_fdt
  https://jamboard.google.com/u/0/d/1xDoyzjbikzI86vP4zu3idWlxlX8qYVKk5Wmmjs7swL8/viewer
- memblock_reserve & early_init_dt_scan 은 차주에 재개.

## 24주차
- 2021.02.06, A_2조, 온라인
- setup_arch
  - setup_machine_fdt

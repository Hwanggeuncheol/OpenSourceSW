# OpenSourceSW
OpenSourceSW task

# 오픈소스SW개론 과제

## top 

+ 실시간으로 CPU 사용률을 체크해주는 도구

+ 리눅스를 사용하는 서버의 성능이나 현재 돌아가고 있는 상황을 볼 때 사용

### 사용법

**top 라고 입력하여 사용**

![top](https://github.com/Hwanggeuncheol/OpenSourceSW/assets/133829778/30bb89cf-e9b4-449b-9b56-e1ff5cd04a3f)

### 나타내는 정보

1. 20:20:49 : 현재 서버의 시간
2. up 171days, 5:46 : uptime 켜져있는시간
3. 4users : 유저
4. load average : 현재 시스템이 얼마나 일을 하고 있는지 1분, 5분, 15분 단위로 실행|대기 중인 프로세스 수를 나타냄
5. Tasks : 프로세스 개수

***CPU***

| %us | 유저레벨에서 사용하고 있는 CPU 비중 |
|:--------:|:---------:|
| %sy | 시스템 레벨에서 사용하고 있는 CPU 비중 |
| %id | 유휴 상태의 CPU 비중|
| %wa | 시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중 |

MiB Mem, MiB Swap : 각 메모리의 상태 정보

***프로세스 상태 정보***

+ PID : 프로세스 ID(PID)
+ USER : 프로세스를 실행시킨 사용자 ID
+ PRI : 프로세스의 우선순위(priority)
+ NI : NICE 값. 일의 nice value 값이다. 마이너스를 가지는 nice value는 우선순위가 높다.
+ VIRT : 가상 메모리의 사용량(SWAP + RES)
+ RES : 현재 페이지가 상주하고 있는 크기(Resident Size)
+ SHR : 분할된 페이지, 프로세스에 의해 사용된 메모리를 나눈 메모리의 총합.
+ S : 프로세스의 상태 [S(sleeping), R(running), W(swapped out process), Z(zombies)]
+ %CPU : 프로세스가 사용하는 CPU의 사용률
+ %MEM : 프로세스가 사용하는 메모리의 사용률
+ COMMAND : 실행된 명령어

### Top 명령어 옵션(top 실행중 사용 가능)

1. **shift + p** : CPU 사용률이 높은 프로세스 순서대로 표시
2. **shift + m** : 메모리 사용률이 높은 프로세스 순서대로 표시
3. **shift + t** : 프로세스가 돌아가고 있는 시간 순서대로 표시
4. **k** : 프로세스 kill - k 입력 후 종료할 PID 입력 signal을 입력하라고 하면 kill signal인 9를 입력
5. **a** : 메모리 사용량에 따라 정렬
6. **b** : Batch 모드 작동
7. **c** : 명령행 / 프로그램 이름 토글
8. **d** : 지연 시간 간격은 다음과 같다. -d ss. tt(seconds.tenths)
9. **h** : 도움말
11. **H** : 스레드 토글
13. **i** : 유휴 프로세스 토글
14. **m** : VIRT/USED 토글
15. **M** : 메모리 유닛 탐지
16. **n** : 반복 횟수 제한 -n number
17. **p** : PID를 모니터 [-pN1 -pN2 ...] or [-pN1 N2 ...]
18. **s** : 보안 모드 작동
19. **S** : 누적 시간 모드 토글
20. **u** : 입력한 유저의 프로세스만 표시 which u
21. **숫자 1** : CPU Core별로 사용량을 보여준다.

***Top 명령어 페이지 이동***

Page Down : 프로세스의 다음페이지 목록

Page UP : 프로세스의 이전 페이지 목록

방향키 사용 가능


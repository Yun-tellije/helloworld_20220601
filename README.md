# 컴퓨터공학과 20213055 윤정은
***1) 리눅스 명령어***

- top

-시스템 프로세스/메모리 사용 현황을 실시간으로 출력하는 명령어

-옵션 없이 실행 시 기본 3초 간격으로 화면을 갱신하며 정보 출력


*top 실행 전 옵션*
| Command | Description |
| --- | --- |
| -b | 배치모드(순간의 정보 확인) |
| -n | top 실행 주기를 설정 |

*top 실행 후 옵션*
| Command | Description |
| --- | --- |
| shift + p | CPU 사용률 내림차순 |
| shift + m | 메모리 사용률 내림차순 |
| shift + t | 프로세스가 돌아가고 있는 시간 순 |
| a | 메모리 사용량에 따라 정렬 |
| 1 | CPU core별로 사용량 출력 |


---

- ps

-현재 실행중인 프로세스의 목록과 상태를 보여주는 명령어

*옵션*
| Command | Description |
| --- | --- |
| -e | 실행중인 모든 프로세스의 정보 출력 |
| -f | 프로세스에 대한 자세한 정보 출력 |
| -u [사용자이름] | 특정 사용자에 대한 모든 프로세스의 정보 출력 |
| -p pid | pid로 지정한 프로세스의 정보 출력 |
| u | 프로세스 소유자의 이름, CPU 사용량, 메모리 사용량 등 상세 정보 출력 |
| a | 터미널에서 실행한 프로세스의 정보 출력 |
| x | 실행 중인 모든 프로세스의 정보 출력 |

---

- jobs

-작업이 중지된 상태나 백그라운드로 진행 중인 상태를 표시하는 명령어
*옵션*
| Command | Description |
| --- | --- |
| -l | 프로세스 그룹 ID를 state 필드 앞에 출력 |
| -n | 프로세스 그룹 중에 대표 프로세스 ID를 출력 |
| -p | 각 프로세스 ID에 대해 한 행씩 출력 |

---

- kill

-특정 프로세스를 종료하거나 특정 프로세스에 특정 시그널을 보내는 명령어 

-시그널을 지정하지 않을 경우 기본 값인(15번) 정상 종료 시그널을 보냄

*옵션*
| Command | Description |
| --- | --- |
| -l | signal의 종류 출력 |

*주요 시그널*
| 시그널 번호 | 시그널 | 설명 |
| :---: | --- | --- |
| 1 | SIGHUP(HUP) | 종료(연결 끊기, 실행 종료) |
| 2 | SIGINT(INT) | 종료(CTRL + C, 인터럽트) |
| 3 | SIGQUIT(QUIT) | 종료+코어 덤프(CTRL+\) |
| 9 | SIGKILL(KILL) | 종료(강제 종료, 프로그램에서 핸들러를 만들 수 없는 시그널) |
| 15 | SIGTERM(TERM) | 종료(정상 종료) |
| 18 | SIGCONT(CONT) | 정지된 프로세스 재실행 |
| 19 | SIGSTOP(STOP) | 정지(프로그램에서 핸들러를 만들 수 없는 시그널) |
| 20 | SIGSTOP(TSTP) | 정지(CTRL+Z) |

---------

***2) vim 에디터***

- 매크로 사용방법

**매크로 저장**

명령모드에서 q<저장할 매크로 문자>  -> 매크로 내용 기록 -> esc 후 q

예시) qa -> 매크로 작성 -> q


**매크로 사용**

| 사용법 | 실행내용 |
| --- | --- |
| @<저장한 매크로 문자> | 매크로 실행 |
| 반복횟수@<저장한 매크로 문자> | 반복횟수만큼 매크로 실행 |
| @@ | 마지막으로 수행한 매크로 실행 |

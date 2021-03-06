# StudyTCPIP
Linux, Tcp/ip 학습을 위한 리포지토리

## Day 1
  - VMware Workstation 설치, 실행
  - Ubuntu 설치, 실행
  - Putty 설치, 실행
  - Linux의 기본명령어 학습
  - make 명령어, makefile 생성 실습

## Day 2
  - TCP / IP 기본내용 이해
  - TCP 기본 Server, Client code 구축
  
## Day 3
  - TCP Socket type, protocol
  - 주소정보의 표현(sockaddr_in, in_addr struct 분석)
  - Endian Conversions, inet_addr, inet_aton, inet ntoa
  - socket(), bind(), listen(), accept(), read() / write() 함수를 통한 TCP 통신 학습
  - TCP protocol stack(Link => IP => TCP / UDP => APPLICATION)
  - TCP Server, Client code 분석
  - lterative 기반의 Server, Client 구현

## Day 4
  - UDP Socket의 특성(Best effort, Tcp와 Flow control 차이)
  - sendto(), recvfrom() 함수를 통한 UDP 통신 학습, TCP와 차이 습득
  - UDP Server, Client code 분석

## Day 5
  - Socket Half close를 위한 Socket, Stream, shutdown() 함수 이해
  - Domain => Ip Address(gethostbyname() 함수)
  - Ip Address => Domain(gethostbyaddr() 함수)
  - Socket의 Option과 입출력(getsockopt(), setsockopt())
  - 주소할당 에러(Binding Error) => Tiem-wait, SO_REUSEADDR
  - Nagle Algorithm 이해

## Day 6
  - Process의 이해(fork() 함수)
  - Zombie Process 발생과 해결 => wait(), waitpid(), siganl handling(sigaction() 함수)
  - Multitasking 기반 Multiple access Server 구현
  - Pipe 기반의 Process간 통신 이해
  - Message를 저장하는 형태의 Echo server 구현

## Day 7
  - Multi Process의 단점 => 많은 양의 연산, 메모리 공간 큼, 복잡한 방법
  - Multiplexing의 개념과 원리
  - Select() 함수의 이해와 서버의 구현
  - send & recv 입/출력 함수, readv & writev 입/출력함수
  - MSG_OOB(긴급메세지, Urgent mode), MSG_PEEK/MSG_DONTWAIT(입력버퍼 검사)
  - Multicast(Routing, Time to Live(TTL)), BroadCast(Direct, Local) 
  - Socket과 표준 입/출력함수
  - 표준 입/출력함수 단점 => 1. 양방향 통신 어려움, 2. 때에 따라 빈번한 fflush함수, 3. fd를 FILE 구조체의 포인터로 변환
  
## Day 8
  - 표준 입/출력함수 사용 => fdopen(), fileno() 함수
  - Socket 기반에서의 표준 입/출력 함수 사용
  - 입력 스트림과 출력 스트림의 분리 => File 포인터의 Read/Write 분리로 인한 편의성 증대, 버퍼링 기능 향상
  - FD(File Descriptor) 복사와 Half-close
  - select() 함수의 단점 => IO Multiplexing이 상대적으로 느림 => epoll() 함수 사용
  - epoll() 함수의 이해와 활용 => epoll_create(), epoll_ctl(), epoll_wait() 함수
  - 레벨 트리거(Level Trigger)와 엣지 트리거(Edge Trigger)의 특성파악, 활용
  - Trigger 기반의 Echo server 구현

## Day 9
  - Mulit thread 기반의 Server 구현
  - Context Switching(컨텍스트 스위칭)
  - Thread의 장점 => 프로세스의 생성 및 컨텍스트 스위칭보다 빠르고, 데이터 교환시 특별한 기법 사용 x
  - Thread의 문제점과 Criticla Section(임계영역) => 하나의 전역변수에 두 개이상의 Thread가 동시접근해 원하는 값 x
  - Thread의 문제점(동일한 메모리 영역 동시접근 또는 실행순서를 지정해야 할 때)의 해결 => Mutex(Mutual Exclusion), Semaphore
  - Http Server Mini project 진행
  
## Day 10
  - Http Server Mini project 

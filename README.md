# opensouce-project
# 1. top(탑)

### **top**  명령어는 현재 OS의 상태를 나타내주는 CLI 어플리케이션입니다.


###### 메모리 사용량, CPU 사용량 등을 나타내주며 top를 실행하는 동안에는 주기적인 업데이트로 실시간에 근접한 내용을 보여줍니다. 리눅스에서 top 명령어를 실행하면 아래와 깉이 노출됩니다. 위에는 전체의 요약이 있으며 아래에는 각 프로세스마다 구체적인 내용을 포함하고 있습니다.
<img width="1280" height="375" alt="dhvmsthm" src="https://github.com/user-attachments/assets/6ffacee9-89dc-4ad3-ab38-1c73f243cf41" />


>  요약 영역은 top에서 상단에 위치하고 있습니다. 이 요약영역은 전체 프로세스가 OS에 대해서 리소스를 어느정도 차지하고 있는지를 알려줍니다. 요약 영역에 나타나는 대표적인 값은 시간, 유저, 로드 에버리지(Load Average), 테스크(Tasks), CPU, 메모리(memory)로 아래의 이미지 를 보시면 각 영역에 대해 나태내느 값이 어디에 위치하는지 알 수 있습니다.


## top(탑) 사용법

+  top
+  top -o %CPU
+  top -o %MEM
 
### top 명령어 실행 예시
''' 

bash
top - 15:22:41 up  2:11,  1 user,  load average: 0.12, 0.08, 0.06
Tasks: 184 total,   1 running, 183 sleeping,   0 stopped,   0 zombie
%Cpu(s):  5.3 us,  1.2 sy,  0.0 ni, 92.9 id,  0.4 wa,  0.0 hi,  0.1 si,  0.0 st
MiB Mem :   7856.0 total,   1250.3 free,   2203.7 used,   4401.9 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   5231.1 avail Mem 



'''

| PID  | USER | PR | NI |   VIRT   |  RES  |  SHR  | S | %CPU | %MEM |   TIME+   | COMMAND      |
|------|------|----|----|----------|-------|-------|---|------|------|-----------|---------------|
| 1421 | root | 20 |  0 |  414504  | 65728 | 50284 | S |  8.5 |  0.8 |  0:32.45 | Xorg          |
| 1864 | user | 20 |  0 | 1523040  |136924 | 89432 | S |  4.3 |  1.7 |  1:12.63 | gnome-shell   |
| 2542 | user | 20 |  0 | 1274528  | 64840 | 50128 | S |  2.0 |  0.8 |  0:18.21 | firefox       |
| 3678 | user | 20 |  0 |  245612  | 20348 | 16432 | R |  1.0 |  0.2 |  0:01.12 | top           |
| 1001 | root | 20 |  0 |  164892  | 12880 |  9984 | S |  0.0 |  0.2 |  0:03.22 | systemd       |



---

# 2.  ps(피에스)

**ps** 명령어는 현재 실행 중인 프로세스를 보여줍니다.


## ps 사용법
```
1 ps
2 ps aux
3 ps -ef
```


---

# 3. jobs

**jobs** 명령어는 현재 셸에서 실행 중인 작업 목록을 확인합니다.

## 🔧 사용법
```
jobs
fg %1
bg %1
```

---

# 4. kill

**kill** 명령어는 프로세스를 종료할 때 사용합니다.

## 🔧 사용법
```
kill <PID>
kill -9 <PID>
kill -15 <PID>
```

---

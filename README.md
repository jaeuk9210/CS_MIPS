# Computer Structure and Operation System IC-PBL Project

## MIPS Processor

본 프로젝트는 MIPS 명령어 집합 구조(ISA)를 기반으로 한 32비트 MIPS Processor 입니다. 

## 🔧 과제 3. Pipeline MIPS Processor (Prob.3 branch)

과제 2에서 사용자 정의 명령어가 추가된 Single Cycle MIPS를 Pipeline MIPS Processor 입니다.
<br/>Data hazard, Control hazard 해결을 위해 별도의 Hazard Unit을 설계하습니다.
<br/>Data hazard는 Forwarding 방식, Control hazard는 Branch stall(Early Branch) 방법을 통해서 해결하였습니다.
<br/>이 프로세서는 아래 명령어들을 지원합니다.

### 산술 연산 명령어

- **add**: 두 레지스터 값을 더하여 결과를 목적지 레지스터에 저장
- **addi**: 레지스터 값과 즉시값(immediate)을 더하여 결과 저장

### 논리 연산 명령어

- **and**: 두 레지스터 값의 비트별 AND 연산 수행
- **or**: 두 레지스터 값의 비트별 OR 연산 수행
- **slt**: 첫 번째 레지스터가 두 번째 레지스터보다 작으면 1, 아니면 0을 저장

### 메모리 접근 명령어

- **lw**: 메모리에서 워드를 읽어 레지스터에 로드
- **sw**: 레지스터의 값을 메모리에 저장

### 제어 흐름 명령어

- **beq**: 두 레지스터 값이 같으면 지정된 주소로 분기
- **j**: 무조건 지정된 주소로 점프

### 사용자 정의 명령어

- **popc**: 레지스터의 값에서 1로 설정된 비트의 개수를 카운트
- **popci**: 즉시값(immediate)에서 1로 설정된 비트의 개수를 카운트
- **avg**: 두 레지스터 값의 평균값을 계산

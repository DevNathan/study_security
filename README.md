# 보안

보안에 있어서 가장 중요한 것들은 네트워크와 시스템 보안이 제일 중요하다. 이는 모든 보안의 기본이 되기 때문이다.<br>
네트워크 보안과 시스템 보안은 마치 사회의 SOC와도 같은 개념이다.

### 목록
1. [정보보안](https://github.com/DevNathan/study_security/blob/main/README.md#%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88)
   > 1-1 ['정보보안'이란?](https://github.com/DevNathan/study_security/blob/main/README.md#1-1-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88%EC%9D%B4%EB%9E%80)<br>
   1-2 [정보보안 전문가가 갖춰야 할 것은 무엇인가?](https://github.com/DevNathan/study_security/blob/main/README.md#1-2-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88-%EC%A0%84%EB%AC%B8%EA%B0%80%EA%B0%80-%EA%B0%96%EC%B6%B0%EC%95%BC-%ED%95%A0-%EA%B2%83%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)<br>
   1-3 [보안의 종류](https://github.com/DevNathan/study_security/blob/main/README.md#1-3-%EB%B3%B4%EC%95%88%EC%9D%98-%EC%A2%85%EB%A5%98)<br>
   1-4 [정보보안의 3대 원칙, CIA](https://github.com/DevNathan/study_security/blob/main/README.md#1-4-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88%EC%9D%98-3%EB%8C%80-%EC%9B%90%EC%B9%99-cia)
3. 네트워크 보안
4. 웹 보안
5. 리버스 엔지니어링
6. 디지털 포렌식

***
## 1. 정보보안


### 1-1 '정보보안'이란?
**정보보안이란 기밀성, 무경성, 가용성(CIA)을 보장하는 것을 의미한다.**<br>
보안은 모든 접근을 차단하는 것이 목적이 아니라 권한이 없는 것을 차단하는 것이다.

### 1-2 정보보안 전문가가 갖춰야 할 것은 무엇인가?
#### I. 운영체제에 대한 이해
     1) Window Server
     2) Linux Server
        (이러한 운영체제들은 시스템 보안과 밀접한 관계가 있음)
  
#### II. 네트워크 + 시스템
     - 네트워크 구축

#### III. 서버
     - 정보와 데이터는 서버에 저장되기 때문에 서버 보안을 반드시 알아야 한다.

#### IV. 보안 솔루션
    1) Firewall(차단 시스템 / (구)방화벽) - 차단이 주 목적이나 무엇을 차단하였는지는 알 수 없음
    2) IDS(침입 탐지 시스템) - 침입 탐지만 하지만 차단을 하거나 행동하는 것은 없음. 마치 레이더와 같음
    3) IPS(침입 방지 시스템) - 탐지 및 차단이 가능한 능동 대응 시스템
    4) UTM(통합위협관리 / (현)방화벽) - 종합 보안 솔루션 시스템

#### V. 암호학
     1) 평문 : 누구나 쉽게 볼 수 있는 일반 텍스트 / 암호화 되지 않은 것
     2) 암호문 : 다른 숫자나 기호들을 통해 평문을 암호화 시킨 것
     3) 암호화 : 평문을 암호문으로 바꾸는 행위
     4) 복호화 : 암호문을 평문으로 해독하는 행위
     5) 암호 해독 : 복호화와 동일한 의미이나 비정상적 방법으로 암호문을 복호화한다라는 의미가 내포되어 있음
     6) 키 : 암호화/복호화 시 필요한 재료(허나 반드시 필요한 것은 아님[ex) Hash Function]
     7) 암호시스템(Cryptosystem)
  
#### VI. 암호 알고리즘
        알고리즘은 공개가 가능하나 키는 공개해서는 안됨.
        보안 강도는 키의 길이에 영향을 받으며 우리나라의 정보보호법에 따른 공식 최소 키 길이는 1024이다.
   암호 알고리즘에 관해서는 [이곳 참조](https://github.com/DevNathan/study_security/blob/main/README.md#%EC%95%94%ED%98%B8-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)

#### VII. 법률/정책(관리적 보안)
     1) 정보통신망 이용촉진 및 정보보호 등에 관한 법률(정보통신망법) ❗
     2) 개인정보보호법 ❗
     3) 정보통신기반보호법
     4) 전자서명법
     5) 전자정부법

#### VIII. 프로그래밍 언어
	1) C/C++
	2) JAVA
	3) Python
 	4) Assembly

### 1-3 보안의 종류
#### I. 관리적 보안
     물리적, 기술적 보안을 체계적으로 수행하기 위한 
     정보보호 체계 및 절차, 감시 조직, 사고 대책 등의 정보보호 활동

#### II. 물리적 보안
     건물, 설비와 같은 ㅁ물리적 정보 시스템 자산을 
     절도, 파괴, 화재 등과 같은 각종의 물리적인 위협으로부터 보호하는 방법

#### III. 기술적 보안
     전산 환경에서 정보 자산을 자산의 유출, 파괴 등으로부터 보호하기 위한 기술적 통제 방법.
     네트워크 보안 / PC 보안 / 서버 보안 / 접근제어

### 1-4 정보보안의 3대 원칙, CIA
	정보보안에는 3대 원칙이 있다. 이 3대 원칙을 통해, 
 	1)인가된 사용자만 정보에 접근이 가능하고, 
  	2)정보가 올바르게 유지되고, 
   	3)필요할 때 정보가 사용될 수 있게 된다.

<img width="459" alt="스크린샷 2023-11-10 201758" src="https://github.com/DevNathan/study_security/assets/142222091/1e1fca11-8b03-4e01-b42d-ad0296edcf73">

#### I.Confidentiality (기밀성)
	데이터 및 정보를 '필터링을 거친' '인가받은' 사용자에게 접근을 허용해주는 것이다. 
 	인가받지 못한 사용자에게는 접근을 거부한다.
- 위협 : Sniffing(스니핑), Eavesdropping(도청), 패킷분석
- 보안 솔루션 : Encryption(암호화)

#### II. Integrity (무결성)
	인가받은 사용자에게 데이터에대한 수정 및 삭제 권한을 보장하는 것을 의미한다.
 - 위협 : Malware(바이러스), Modification(변조)
 - 보안 솔루션 : Hash Function(해시함수)

#### III. Availability  (가용성)
	인가받은 사용자에게 한해 정보에 접근하고 사용하도록 허가하는 것을 의미한다.
 - 위협 : Dos(단일)/DDoS(단체) (공식 : 서비스 거부 공격 / 실제기능 : 서비스 방해 공격)
 - 보안 솔루션 : Firewall, IDS, IPS, UTM

## 네트워크 보안

## 시스템 보안

## 웹 보안

## 리버스 엔지니어링

## 악성코드 분석

## 디지털 포렌식

# 부록

## 암호 알고리즘
### 1. 양방향 암호 알고리즘
양방향 알고리즘은 평문과 암호문간의 '암호화' 및 '복호화'가 가능한 구조이다. 이 행위는 반드시 '키'를 통해 이뤄지게 되며 발신자가 암호문을 전달하기 위해서는 반드시 '키'를 먼저 수신자에게 보내야만 한다.

#### 1-1 대칭키 암호 알고리즘(관용암호)
     대칭키 암호 알고리즘은 키값을 송신할때 암호화하지 않고 네트워크를 통해 그대로 전달되기 때문에 
     스니핑위험에 그대로 노출되어있다. 해커는 키값을 탈취해낼 수 있으면 
     암호문을 간단히 복호화 해낼 수 있다는 큰 리스크가 있다. 
     
     하지만 단순한 구조로 인해 속도가 빠르다는 장점이 있다.
- 블록 암호 알고리즘 : 32/64비트 단위로 암호화.
  > DES, AES, IDEA, SEED, ARIA, LEA, HEIGHT
- 스트림 암호 알고리즘 - 비트 단위로 암호화(거의 사용하지 않음).
  > RC4, A6

#### 1-2 공개키(비대칭) 암호 알고리즘
     공개키 암호 알고리즘은 키값을 송신하기 이전에 키값 또한 암호화 시키는 알고리즘이다. 이때 키는 바로 이 '공개키'를 통해 암호화 되게 된다. 
     해커에게 필요한 것은 복호화 키 이기때문에 암호화 키인 이 '공개키'는 말그대로 공개가 되어도 상관 없기 때문이다. 
     반대로 복호화키는 반드시 비밀리에 관리 되어야 하기 때문에 '개인키'라고 불린다. 
     이 '공개키'와 '개인키'는 수학적으로 밀접한 관련이 있어 이 한쌍의 키는 '연관성'을 가졌다고 말할 수 있다. 
     공개키 암호 알고리즘은 개발된 후부터 지금까지 가장 안전한 암호 알고리즘이며 
     이 덕분에 오늘날 전자 상거래등 인터넷상 보안이 매우 중요한 일들이 가능캐 보안 위협 없이 가능캐 되었다.
     
     하지만 그만큼 복잡한 과정을 거치게 되므로 속도가 느려진다는 단점이 있다.
- 소인수분해 기반
  > RABIN, RSA
- 이산대수 기반
  > ECC, ElGamal, DSA, Diffie-Hellman

*공개키 암호 알고리즘에 대한 논문은 "Diffie-Hellman"이 써냈으며 이를 토대로 개발해낸 것은 "RSA" 세 사람이다.*

### 2. 단방향 암호 알고리즘
단방향 알고리즘은 '암호화'만 가능하고 '복호화'는 불가능한 구조이다. 로그인시 입력하는 비밀번호는 이런 단방향 암호 알고리즘의 대표 예시이다. 단방향 암호 알고리즘, '해시 함수'는 암호화시 한글자만 바뀌더라도 값이 크게 변하게 되므로 무결성을 보장한다. 하지만 동일한 입력값은 동일한 출력값을 가지게 되므로 시간을 들여 해독해내는 것이 가능하다. 해시함수는 다른 입력값을 넣었음에도 불구하고 동일한 출력값이 나올 수 있는 가능성이 있다. 이를 '충돌'이라 칭한다. 이 '충돌'을 최소화 시키고자 비트값을 계속해서 늘려왔으며 그 결과 현재는 SHA-512가 해시 함수의 최고 격이다.
#### 2-1 암호학적 해시함수
     > MD5(126), SHA-1(160), SHA-2(SHA-224, 256, 384, 512)
#### 2-2 비암호학적 해시함수
     > Checksum, CRC-32, FCS

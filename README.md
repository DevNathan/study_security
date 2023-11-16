조남호 | Nathan Cho<br>
수업 일수 11.08.23 ~ 진행중
<br><br>
수업 중 사용한 OS

	1) Kali linux -> www.kali.org
	2) CentOS 7 -> www.centos.org
	3) Windows 10
	4) Windows 2016 server

# 보안

보안에 있어서 가장 중요한 것들은 네트워크와 시스템 보안이 제일 중요하다. 이는 모든 보안의 기본이 되기 때문이다.<br>
네트워크 보안과 시스템 보안은 마치 사회의 SOC와도 같은 개념이다.

### 목록
1. [정보보안](https://github.com/DevNathan/study_security/blob/main/README.md#%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88)
   > 1-1 ['정보보안'이란?](https://github.com/DevNathan/study_security/blob/main/README.md#1-1-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88%EC%9D%B4%EB%9E%80)<br>
   > 1-2 [정보보안 전문가가 갖춰야 할 것은 무엇인가?](https://github.com/DevNathan/study_security/blob/main/README.md#1-2-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88-%EC%A0%84%EB%AC%B8%EA%B0%80%EA%B0%80-%EA%B0%96%EC%B6%B0%EC%95%BC-%ED%95%A0-%EA%B2%83%EC%9D%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)<br>
   > 1-3 [보안의 종류](https://github.com/DevNathan/study_security/blob/main/README.md#1-3-%EB%B3%B4%EC%95%88%EC%9D%98-%EC%A2%85%EB%A5%98)<br>
   > 1-4 [정보보안의 3대 원칙, CIA](https://github.com/DevNathan/study_security/blob/main/README.md#1-4-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88%EC%9D%98-3%EB%8C%80-%EC%9B%90%EC%B9%99-cia)<br>
   > 1-5 [정보보안의 5가지 핵심요소들](https://github.com/DevNathan/study_security/blob/main/README.md#1-5-%EC%A0%95%EB%B3%B4%EB%B3%B4%EC%95%88%EC%9D%98-5%EA%B0%80%EC%A7%80-%ED%95%B5%EC%8B%AC%EC%9A%94%EC%86%8C%EB%93%A4)<br>
   > 1-6 [(정보)자산과 위험성](https://github.com/DevNathan/study_security/blob/main/README.md#1-6-%EC%A0%95%EB%B3%B4%EC%9E%90%EC%82%B0%EA%B3%BC-%EC%9C%84%ED%97%98%EC%84%B1)<br>
   > 1-7 [공격(해킹)의 기초 단계](https://github.com/DevNathan/study_security/blob/main/README.md#1-7-%EA%B3%B5%EA%B2%A9%ED%95%B4%ED%82%B9%EC%9D%98-%EA%B8%B0%EC%B4%88-%EB%8B%A8%EA%B3%84)
   
2. [네트워크 보안](https://github.com/DevNathan/study_security/blob/main/README.md#2-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-%EB%B3%B4%EC%95%88)
3. 웹 보안
4. 리버스 엔지니어링
5. 디지털 포렌식

***
## 1. 정보보안

***
### 1-1 '정보보안'이란?
**정보보안이란 기밀성, 무경성, 가용성(CIA)을 보장하는 것을 의미한다.**<br>
보안은 모든 접근을 차단하는 것이 목적이 아니라 권한이 없는 것을 차단하는 것이다.

***
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

***
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

***
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

***
### 1-5 정보보안의 5가지 핵심요소들
#### Identification (식별)
	서버 및 시스템이 유저를 인정해주는 것을 의미한다.
 	식별에 대한 신청은 사용자가 하게 되고 인증은 시스템이 하게된다.
#### Authorization (권한부여/인가)
	사용자에게 접근하려는 대상에 대한 권한을 결정하는 것을 의미한다.
 	권한에 따라 사용자는 대상에 할 수 있는 것들이 제한될 수도 있다.
#### Authentication (인증)
	사용자의 신원을 증명하는 것을 의미한다.
	쉬운 예로 로그인시스템이 있다.
#### Access Controls (접근제어)
	위의 식별, 인증, 인가의 3가지 단계를 통해 주체의 접근을
 	허용하거나 거부하는 것을 의미한다.
#### Accounting (책임추적성)
	사용자의 접근행위를 기록하고 분석하는 것을 의미한다.


***
### 1-6 (정보)자산과 위험성
![images](https://github.com/DevNathan/study_security/assets/142222091/1a838f7c-5ebf-4f75-aaf8-871a616a14ac)

	정보 자산에 대한 위협이 커지면 위험성도 당연히 높아지게 된다.
 	이뿐만 아니라 정보보안의 취약점 또한 위험성을 높이게 되는 원인이 된다.
#### 1) Threat (위협)
	위험의 원인이다.
#### 2) Rist (위험)
	사건이 발생할 가능성을 의미한다.
#### 3) Vulnerability (취약점)
	보안의 취약점을 의미한다.
#### 4) Asset (자산, 정보자산)
	공격자로부터 지켜야하는 대상이며 이 자산이 커지면 커질 수록 위험성 또한 커진다.

<br>
<img width="455" alt="스크린샷 2023-11-10 201806" src="https://github.com/DevNathan/study_security/assets/142222091/b0c947c2-a98f-4d76-8964-69dd118ce19f">

	정보 자산은 지켜야 하는 대상이며 여러 위협들을 보안 기술들을 통해 자산을 보호할 수 있다.
 	하지만 보안에는 반드시 빈틈이 있기 마련이고 그것을 취약점이라 칭한다.
  	공격자들은 그 취약점을 파고들어 정보 자산에대한 공격을 하게 되니 이 취약점을 잘 방어하는 것이
   	정보보안에 있어 가장 중점이 되겠다.

***
### 1-7 공격(해킹)의 기초 단계
1. 정보 수집 ❗
	1) 정찰(reconnaissance)
	2) 스캐닝 및 취약점 분석(scanning and enumeration)
2. 침투 및 시스템 장악
3. 공격 전이
	1) 권한상승
	2) 백도어 관리
	3) 침투 흔적 지우기

***
## 2. 네트워크 보안

***
### 2-1 OSI 7 Layer Model
![osi-model-7-layers-1](https://github.com/DevNathan/study_security/assets/142222091/651a0a56-6644-4106-9019-a52cca011e90)

 	OSI 7 Layer Model은 네트워크에서 통신이 일어나는 과정을 7단계를 나눔으로서
  	통신이 이뤄지는 과정을 파악하기 쉽게 하기 위해 국제 표준화 기구(ISO)에서 정의한
   	네트워크 표준 모델이다.
   	하지만 실제 네트워크에서는 모든 상황이 유동적으로 이뤄지므로
    OSI모델은 단순 참조용으로만 사용하는 것이 좋다.

#### OSI 7 Layer Model과 네트워크 보안 시스템
1. Phisical Layer

		물리적단계의 보안 시스템은 사실상 존재하지 않는다

2. DataLink Layer

		VPN 기술이 사용되며 VPN의 터널링 기술을 통해 암호화가 가능하다.
		- PPTP : MicroSoft 개발
		- L2F : Cisco 개발
		- L2TP : IETF 개발

3. Network Layer

		VPN에서 IPSec 기술을 통해 암호화가 가능하다.

4. Transport Layer

		SSL/TLS 기술을 통해 암호화가 가능하다.
		SSL/TLS 기술은 전송 계층부터 어플리케이션 계층까지 수행한다.

5. Session Layer

		SSL

6. Presentation Layer

		데이터 표현 형식을 통해 암호화가 가능하다.
		예를 들어 JPG는 GIF를 통해 읽을 수 없으며 만약 이렇게 수행할 시 '깨져서' 읽지 못하게 된다.

7. Application Layer

		HTTPS, PGP, PEM과 같은 암호화 기술들이 있다.

***
### 네트워크 통신과정
#### 네트워크 데이터 단위
<img width="307" alt="스크린샷 2023-11-13 210251" src="https://github.com/DevNathan/study_security/assets/142222091/df8472ce-ee91-4feb-a064-d1e19edf8e30">

1. Phisical : Bits
2. Data Link : Frame
3. Network : Packet

		Packet은 항상 동일한 양으로 잘라진다는 특징이다 있다. ❗
4. Trasport : Segment
5. Application 및 나머지 : Message

#### 데이터 캡슐화(encapsulation) 과정 및 전송
	전송을 위해 계속해서 데이터를 헤더에 감싸게 되는 구조이다.

1. 응용단 - Message
2. 전송단 - TH(TrasportHeader) | Message
3. 네트워크단 - NH(NetworkHeader) | TH | Message
4. 데이터링크단 - DH(DataLinkHeader) | NH | TH | Trailer(데이터링크단에서는 헤더뿐만아니라 꼬리에 trailer가 더 붙는다.)
5. 피지컬단(NIC) - 데이터링크단의 Frame을 NIC(LAN)이 Bit단위로 변환시켜 전송한다.

#### 데이터 역캡슐화(decapsulation) 과정
1. Switch 혹은 Bridge를 통해 DH 제거, NH를 드러나게 함
2. Router/L3 Switch가 NH의 IP주소를 읽어내고 NH를 제거,
3. L4 Switch에서 TH 제거
4. 메시지만이 남게됨.
<br><br>
컴퓨터는 이모든 전과정을 수행할 수 있는 스위치, 라우터 등이 다 있다.

#### 헤더들의 구조
1. ARP
2. Ethernet
3. IP
4. TCP
5. UDP

#### 네트워크 토폴로지
<img width="436" alt="스크린샷 2023-11-13 210450" src="https://github.com/DevNathan/study_security/assets/142222091/84693499-ba8f-4497-8264-f814e57e8fc3">

	만약 내가 1.1.1.1 컴퓨터에서 4.4.4.1로 메시지를 보낸다고 가정하자.
	1. 내 메시지를 캡슐화를 하여 NIC가 광네트워크로 보내는 1.1.1.3 라우터까지 도착하게 되면
 	역캡슐화를 통해 NH를 읽어 IP주소를 확인한다.
  	2. 다시 캡슐화를 하여 광역 네트워크를 통해 4.4.4.3 라우터까지 전송,
   	역캡슐화를 통해 IP를 읽어낸다.
	3. 다시 캡슐화를 하여 읽어낸 IP를 토대로 맞는 주소로 전송한다.
	4. 4.4.4.1 컴퓨터에 도착하면 역캡슐화를 진행하고 
	소스IP(전송자IP)와 데스티네이션IP(송신자IP)를 읽어 맞는 주소인지 확인한다.
	맞는 주소일 시 역캡슐화를 지속 진행하여 TH에서 포트번호를 읽는다.
	5. 예를 들어 80번 포트로 보내져서 APACHE 서버에서 읽어내면 이를 토대로 화면에 출력되게 된다.

 	이와 같이 알맞은 IP로 보내질때까지 캡슐화/역캡슐화 과정이 계속 반복적으로 이뤄지게 된다.
  	하지만 네트워크 전송과정에서 결국 끝까지 존재하게 되는 것은 TH이다.
  	Data Link에서는 flow, Error, Link, Point to Point로 불리지만
   	Transport에서는 End to End로 불리게 되는 이유다.

***
### 네트워크 식별자
<img width="446" alt="스크린샷 2023-11-13 214957" src="https://github.com/DevNathan/study_security/assets/142222091/10e07fb2-b5ac-48d6-abc1-eceeb0517a1d">

1. MAC
2. IP
3. Port

#### 포트번호
	포트번호 총 65536개가 있다. 분류는 3개로 나뉜다.
 	1) Well-known Post : 0 ~ 1023
  	2) Registerd : 1024 ~ 49151
   	3) Dynamic : 49152 ~ 65535

#### 알아야할 포트 번호들
	FTP - 21/20(C/D)
	SSH - 22
	TELNET 23
	HTTP - 80
	POP3 - 110
	IMAP - 143

	DHCP 67,68
	TFTP 69
	DNS - 53
	SNMP - 161,162

	SSL/TLS - 443

***
### 이더넷 프레임
1. 이더넷 헤더 (총 14바이트)
	1) MAC Address (맥 주소) (총 12바이트)

			- Destination MAC Address : 수신자의 맥 주소이다.
			- Source MAC Address : 송신자의 맥 주소이다.

			이더넷 프레임에서는 MAC 주소 중 수신자의 맥주소가 송신자 주소 보다 앞에 위치한다는 특이점이 있다.

	2) Ether Type (2 바이트)

   			뒤에 따라오는 페이로드(데이터)의 내용물 타입을 알려준다.

2. 페이로드/데이터 (46바이트 ~ 1500바이트)
	1) IP (Network) (20바이트)
 	2) TCP (총 20바이트)
  	3) 옵션

3. Trailer (4 바이트)

		오류 검출을 위한 필드

※ 데이터를 읽기 위해서는 최소 56바이트가 필요하다.

		맥주소(14바이트), 타입(2바이트), TCP/IP(40바이트) = 56바이트

※ 데이터의 최대 크기는 1500바이트이다. 여기서 실질적으로 보낼 수 있는 내용물의 양은 IP와 TCP, 40바이트를 제외한 총 1460바이트이다.

#### ARP HEADER
	IP주소를 통해서 MAC주소를 알아내는 프로토콜이다. 반대 개념은 RARP이다.

1. H/W Type (2바이트)

		사용중인 하드웨어 주소(MAC)의 타입을 나타내는 필드이다.
2. Protocol Type (2바이트)

		상위 프로토콜(IP)을 정의한다.
3. H/W Length (1바이트)

		하드웨어 주소(MAC)의 길이를 정의한다(나타낸다).
4. Protocol Length (1바이트)
	
		상위 프로토콜(IP)의 길이를 정의한다(나타낸다).
5. Operation (2바이트)

		요청 패킷인지 응답 패킷인지 확인한다.
6. Source Hardware Address 

		송신자의 하드웨어 주소(MAC) 주소를 나타내는 필드이다.
7. Source Protocol Address

		송신자의 IP주소를 나타내는 필드.
8. Target Hardware Address

		목적지의 하드웨어 주소를 정의한다.
		요청일 시, 송신자는 목적지의 MAC주소를 알 수 없으므로 이 경우 모두 0으로 설정 되어 있다.
10. Target Protocol Address

		목적지의 IP 주소를 정의한다.

#### IPv4 Header
	IP 헤더는 IP패킷의 앞부분에 위치하며 IP 주소를 비롯한 각종 제어정보를 담고 있다. 
	IPv4 헤더는 고정 20바이트, 옵션 0~40바이트이다. 즉, 최소 용량 20바이트이다.

1. Version

		IP의 종류를 알려준다. (IPv4, IPv6)
2. IHL(IP Header Length)

		IP 헤더의 길이를 나타낸다.
3. TOS(Type of Service)

		Service 타입을 알려준다.
4. Total Length

   		헤더와 데이터를 합한 IP 패킷 전체 길이를 바이트 단위로 나타낸다. (최대 65,535바이트)
5. Identification(식별자)

   		IP 패킷을 식별하기 위해 사용한다. 분할 되어 전송된 데이터를 식별할 수 있다.
6. Flags

		패킷의 분할 여부에 대한 정보를 나타내는 영역이다
   		예비 / DF(Don't Fragment) / MF(More Fragment) 가 있으며
   		DF는 패킷의 마지막임을 알려 다음에 전송될 데이터가 없다는 것을 나타낸다.
   		MF는 패킷이 잘라져있어서 다음에 전송될 데이터가 있다는 것을 나타낸다.
7. Fragment Offset

   		분할된 패킷을 재조립할 수 있도록 원래 위치를 알려준다. 이때 위치를 알려주는 방식은
   		항상 처음시작점으로부터의 상대적 주소를 나타낸다.
8. TTL(Time to Live)

		전송된 패킷이 수신지에 도착하지 못하게 될시 계속해서 떠돌게 되므로 제거되지 않으면 네트워크는 반드시 부하가 일어난다.
		이것을 방지하기 위해 TTL이 있으며 라우터를 거칠 때마다 1씩 차감하는 형태가 된다.
		TTL이 0이 될시 라우터에서 패킷을 폐기하게 되고 이 사실을 전송지에 알리게 된다.
9. Protocol Type(ID)

   		어떤 상위 계층 프로토콜이 포함되어 있는지를 나타낸다.
10. Header Checksum

		네트워크를 통해 패킷이 전송될 때 헤더의 오류를 검출한다.
		오류 검출시 해당 패킷은 폐기된다.
11. Source IP Address

		전송지 IP 주소
13. Destination IP Address

		수신지 IP 주소

***
### TCP와 UDP의 차이점
- TCP
	- 32바이트
 	- 패킷로스(패킷손실) 발생시 재요청을 한다.
	- 전송속도가 느리다(헤더의 크기).
 	- 스트리밍 서비스에 부적합
- UDP
	- 8바이트
 	- 패킷로스 발생시 무시한다(비신뢰성).
  	- 전송속도가 빠르다(헤더의 크기).
  	- 스트리밍 서비스에 적합
 
*** 
### TCP 3-Way Handshake(빠름)

### TCP 4-way Handshake(신뢰성)

### TCP 3-WAY Handshake + SSL/TLS

***
## 공격과 방어
### 공격
#### 1단계, 정보 수집(Information Gathering)
	ping - 상대방의 IP주소를 알아낼 수 있다.
 	traceroute - 목적지 까지 거치게 되는 모든 라우터들의 IP를 알아낼 수 있다(총 3번 시도).

## 3. 시스템 보안

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

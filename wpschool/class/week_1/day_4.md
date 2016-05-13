#Day - 4
##네트워크 및 암호화
###네트워크

- LAN (Local Area Network) : 근거리 통신망
- MAN(Metropolitan Area Network) : 도시권 통신망
- WAN(Wide Area Network) : 광역통신망

-Server
-Client

- Internet
     컴퓨터로 연결하여 TCP/IP 프로토콜을 이용해 정보를 주고받는 컴퓨터 네트워크
     네트워크의 네트워크
- TCP/IP : 통신규약
     TCP(Transmission Control Protocol):전송제어 프로토콜
     IP(Internet Protocol):인터넷 프로토콜

- WWW(World Wide Wep)
     문서(웹페이지)들이 있는 정보의 저장소
     분산과 연결
- URL
     Unoform Resource Locator

- Protocol(프로토콜) : 통신규약
     장비 사이에서 메시지를 주고 받는 양식과 규칙의 체계 즉, 통신(네트워킹) 할 때 정해진 메세지 규칙

- HTTP(Hyper Text Transfer Protocol)
- FTP(File Transfer Protocol)
- TELNET(TErmonal NETwork) - 원격 로그인을 위한 프로토콜
- SSH(Secure Shell) - 네트워크 상의 다른 컴퓨터에 로그인 하거나 원격 시스템에서 명령을 실행하고 다른 시스템으로 파일을 복사할 수 있도록 해 주는 응용 프로크램 또는 그 프로토콜, Telnet의 대용 목적으로 설계(보안강화)
- SSL(Secure Socket Layer) : 웹서버와 브라우저 사이의 보안을 위한 프로토콜
- SMTP(Simple mail Transfer Protocol) : 전자메일 발송 프로토콜

*Hostname : 네트워크에 연결된 장치에 부여되는 고유한 이름 예)IP주소, 도메인 주소, MAC주소 등등

- IP Address (Internet Protocol Address) - 고유번호
- Domain Address - 네트워크상에서 컴퓨터를 식별하는 호스트 이름
- DNS(Domain Name System) : 호스트의 도메인 이름을 호스트의 네트워크 주소로 바꾸거나 그 반대의 변환을 수행
- MAC Address(Media Access Control Address) : 네트워크 어댑터에 부착된 식별자

*Port - 가상의 논리적 통신 연결단, 번호로 구분(65535개의 문, 특정 사황에 맞게 열어놓음, 번호에 따라 기능이 다름.ex - 80번포트 http통신을 위한 포트)

     GET
     PUT
     POST
     DELETE
     FTP
     TELNET
     SSH
     SSL
     IP
     DNS
     MAC Adderss
     
###OSI 7 계층 모형

응용계층
표현계층
세션계층
전송계층
네트워크 계층
데이터링크 계층
물리계층

HTML :
XML :
JSON :

- HTTP
     GET - 주소에 파라메타를 함께 보내는 방식
     PUT -
     POST - BODY에 정보를 담아 보내는 방식
     DELETE -

###암호화 기법
- 대칭키 암호화 - 암호화와 복호화에 같은 암호키를 쓰는 알고리즘.(DES,AES,SEED 등)
--하나의 키 형태를 보내는 사람과 받는 사람이 사용하는(교환일기, 집 현관문)
--문제점 : 키값을 알고있으면 모든 정보를 알수 있다.
- 공개키(비대칭키) 암호화 - 사전에 비밀 키를 나눠가지지 않은 사용자들이 안전하게 통신할 수 있도록 하는 암호화 알고리즘.(RSA 등)
--공개키로 잠그고 다른 키(프라이빗 키)로 연다(?)
- 암호화 해시 함수 - 임의의 데이터(함호 등)를 고정된 길이의 데이터로 매핑하여 원래의 입력값과의 관계를 찾기 어렵게 만든것(SHA, MS5등)
--웹페이지 비밀번호
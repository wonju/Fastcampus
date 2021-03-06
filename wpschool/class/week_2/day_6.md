#Day_6
##프로그래밍 용어, 각종 실무 용어, 현업에서의 프로그래머

###프로그래밍 언어

* 1950년대 포트란(fortran)시작
  64베이직,
  69 B(bell연구소 에서 만든 통신관련 언어), 71 C,78년 C(K&R): 최초 표준화된 C

- 프로그래밍 언어 - 어떤 동작을 주기위해 만든 언어. 어셈블리어, 천공카드(?),

- 프로그래밍 언어의 종류 - 고급언어에서 저급언어로 변환되는 과정에 따른 분류

	1. 컴파일 언어 : C,C++, Go, Swift
     -- 사용자들이 프로그램 파일을 전달하기 전에 컴퓨터언어(0,1)로 배포( ****.exe), 바로 메모리. 용량이 큰 경우 대부분 컴파일 언어를 사용. 플렛폼(운영체제)에 종속적
	
	2. 바이트코드 언어 : Java, C#
     -- 컴파일러 언어와 인터프리티어 중간단계, 가상머신을 OS위에서 중간역할을 함.JVM에 도달하기 전까지는 컴파일 하고 OS에 따라 인터프리터 언어 사용. 범용성을 얻고 속도를 잃어.
	
	3. 인터프리터 언어 : BASIC, JavaScript, Python
     -- 사용자가 실행시키기 전까지 아님, 실행시 인터프리터(통역기)가 변환. 실시간 반영시 유리, 서버 운용시 많이 사용.

#####프로그래밍 패러다임에 따른 분류

-프로그래밍의 관점 :

- 객체지향 프로그래밍 패러다임(Objective-C, Python, Swift, C++, C#, Smalltalk,) : 프로그램을 상호작용하는 객체들의 집합으로 표현, 프로그램 동작시 객체들이 움직임으로써 표현

- 함수형 프로그래밍 패러디임 : 프로그램을 상태값을 지니지 않는 함수값들의 연속으로 표현. 프로그램 동작시 함수값에 따라 표현. 다중처리 작업에 용이. 멀티스레드 환경에 용이

		<객체지향 프로그래밍 패러다임>
		-프로그래밍 패러다임 중 하나
		-기존 시각은 (명령어) 순차적 프로그램 실행으로 보고 있었으나, 우리가 사는 모습과 프로그램과 똑같았으면 좋겠다 하는 생각으로 만들어진. 개개인(객체)의 상호작용으로 프로그램의 동작을 구현하고자 하는것.
		- 클래스 —> 객체 : 실질적인 형태(클래스의 객체화)
		- 객체(Object) : 의식과 행위를 가지는 형체
		- 클래스(class) : 객체가 가질 수 있는 속성과 행위를 정하는 틀(템플릿, 플렛폼) , 속성(변수)+기능(함수)

캡슐화, 상속, 다형성에 관해 꼭 알아보아요~~~

*개발자 - Developer
     프로그래머 + 디자이너 + 기획자 + …….

*서버(server)/클라이언트(Client)
     서버 ———데이터제공-—>클라이언트

*프론트엔드 백엔드

*Thread
     프로세스 내에서 작업이 실행되는 흐름의 단위

*Multi Thread - 다중 스레드
     멀티 스레드(프로그램 안에서 번갈아 실행) vs 멀티 테스크(음악+검색+영화)

*Livrary - 특정 기능을 수행할 수 있는 클래스 또는 함수의 집합체
     수학 라이브러리
     애니메이션 라이브러리
     문자열 라이브러리

*API(Application programming Interface)
     응용 소프트 웨어 프로그래밍 접합부
     응용 소프트웨어와 프레임워크 사이의 중간매체(방법)
     소프트웨어 간의 통신을 위해 메시지를 전달하는 방식 등이 결정된 것

###Framework
     구조적으로 고정된 부분을 재사용할 수 있도록 하고, 응용별 특정 기능을 추가적인 사용자 작성 코드에 의해 선택적으로 구현 가능하도록 하는 포괄적인 추상 구조, 그리고 이를 지원하는 소프트웨어 플랫폼.
     소프트웨어 플랫폼 - 소프트웨어가 동작할 수 있는 기반시설 또는 체계(세계?)
     비유해 보자면
          프레임워크 - 국가(정부)
          프레임워크의 하위 프레임워크 - 정부부처
          API - 국가기관
          라이브러리 - 직무전문가
          프로그래밍 언어 - 국가 통용 언어
          레퍼런스 문서 - 국가 조직도 및 기능 설명서

* 디자인 패턴
     프로그램 개발에서 자주 나타나는 과제를 해결하기 위한 방법 중 하나
     과거의 소프트웨어 개발 과정에서 발견딘 설계의 노하우에 이름을 붙여 이후에 재이용하기 좋은 형태로 묶어 정리한 것 - MVC, Singleton 등

*레퍼런스 문서(Reference Document) - API에 대해 서술해 놓은 문서

* IDE - 통합 개발 환경(하나의 소프트웨어)

*SDK - 소프트웨어 개발에 필요한 도구의 모음 IDE + Framework + Tools…...

*웹 프로그래머
     퍼블리셔
     프론트엔드 프로그래머
     백엔드 프로그래머
     DB
     디자이너
     기획자
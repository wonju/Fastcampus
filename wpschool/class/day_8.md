#Day _ 8
## Python 기초
###자료형(Data type)

- Number (**int**)
	- 정수, 실수, 복소수, 8진수, 16진수 등
	- a = a + 1  => a += 1
	- 2 * 2 = 2 ** 2
	- a x a x a = a ** 3

- 문자형 (**str**)
	- name = "원주"
 		name + "님 안녕하세요."
        원주님 안녕하세요.
	- {0}님 안녕하세요.".format(원주)
	- {name}님 안녕하세요.".format(name="원주")
	- print(name[0]) => 원
	- pritn(name[0:])=> 원주

- List : 순서가 있는 여러 집합의 모음
	- animals = ["강아지", "고양이", "이구아나"]
	- animals.append("물고기") => 물고기 삽입
	- animals.pop(0) => 강아지 삭제
	- 현재상태에서 animals[0][0] => 고 (0의 자리(고양이)의 0의 자리(고))

- Tuple : 순서가 있는 여러 집합의 모음이지만 값이 변하지 않는
	- width_and_height = (120,240)
	- width, height = width_and_height
	- width => 120
	- heigh => 240
	
- Dict : 키와 연결되어 있는 자료
	- detail_dict = {"name" : "황원주", "age" : 24, "phone_number" : "010 - 3144 - 8845}
	- del detail_dict["age"] => 나이(24) 삭제
	- detail_dict["name"] => '황원주'

- Set : 순서가 없는 자료
	- name_set = set(["원주", "원주", "지훈", "정원"])
	- name_set => {'원주', '정원', '지훈'}
	- name_list = {"원주", "원주", "원주", "정원", "정원"}
name_list = list(set(name_list))
name_list => ['원주', '정원']

- Boolean : "참" 또는 "거짓"
	- True or False
	
###제어문
##### 대부분의 프로그래밍 언어에서는 특정 조건에 대해서만 실행하거나, 반복적으로 특정 파이썬 코드를 실항하는 제어문을 제공한다.
- if
	
	- a = 13
b = 12
if a > b:
   print("a는 b보다 크다")
else:
   print("a는 b보다 작다") ==> a는 b보다 크다  

    - animals = ["강아지", "고양이", "이구아나"]
if "이구아나" in animals:
    print("이구아나를 키우고 있습니다.")
else:
    print("이구아나를 키우고 있지 않습니다.")

- while

	- age = 20
	while age < 30:
    print("20대에 나이를 먹었습니다. 현재나이:{age}".format(age=age))
    age += 1

- for

	- animals = ["강아지", "고양이"]
for animal in animals:
    print("{animal}".format(animal=animal))
    
    - for _ in range(10):
    print("Hello World")
    
###입력과 출력
- 사용자
	- 작업 자동화
 우리가 반복적으로 사용할 어떤 특정 기능들에 대해서 => "재사용 가능한 코드 덩어리"
	- def greeting():
    username = input()
    print("{username}님, 가입을 축하드립니다.".format(username=username))
    - greeting()

- 파일
	- ./ => 현재폴더
	- ../ ==> 상위폴더

	- ./test.txt => 상위폴더 test.txt
	- ../test.txt => 상위 폴더에 있는 test.txt
	- ../../test.txt => 상위폴더의 상위폴더에 있는 test.txt

	- f = open("../animals.txt", "r") # mode => "w", "r", "a" (append)
	
	- read, readline, readlins
	- f.read()
	- f.readline()
	- f.readlines()
 
- stsin/stdout
	- 입력과 출력은 Python 내장 함수 ( Built-in Function ) 를 이용해서 할 수 있다.
		- print
		- input
	- Python 2.X 에서는 다르게 동작합니다. ( raw_input 를 사용합니다. )

- print
	- print 를 이용함으로써 외부로 출력할 수 있습니다. 
	- print("hello world")
	• Python 2에서 print 는 statement 이지만, Python 3 에서는 print가 function 으로 변경되었 습니다.
    
- input
	- input 이라는 함수를 실행함으로써 사용자로부터 입력을 받을수있습니다.(Python 2에서는raw_input을사 용합니다. )
	- input()

- 인코딩 : 입력과 출력에서의 가장 큰 문제


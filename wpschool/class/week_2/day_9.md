#Day_9
##Python 기초
###Lists, Tuples, Dictionaries and Sets

```python
# List, Dict

animals = ["강아지", "고양이", "거북이", "토끼", "참새"]
my_informations = {
    "name": "wonju", 
    "phone": "01031448845", 
    "email": "ga@gmail.com", 
    "age": 24
}
```


```python
# List for loop(1)

for animal in animals:
    print(animal)
```

    강아지
    고양이
    거북이
    토끼
    참새



```python
# Dict for loop(2)

for my_information in my_informations:
    print(my_information)
    print(my_informations[my_information])
    print(my_informations)
```

    age
    24
    {'age': 24, 'name': 'wonju', 'email': 'ga@gmail.com', 'phone': '01031448845'}
    name
    wonju
    {'age': 24, 'name': 'wonju', 'email': 'ga@gmail.com', 'phone': '01031448845'}
    email
    ga@gmail.com
    {'age': 24, 'name': 'wonju', 'email': 'ga@gmail.com', 'phone': '01031448845'}
    phone
    01031448845
    {'age': 24, 'name': 'wonju', 'email': 'ga@gmail.com', 'phone': '01031448845'}



```python
my_informations["name"]
```




    'wonju'




```python
# Dict for loop(3)

for my_information in my_informations.items():
    print(my_information)
    key, value = my_information
    print(key)
    print(value)
```

    ('age', 24)
    age
    24
    ('name', 'wonju')
    name
    wonju
    ('email', 'ga@gmail.com')
    email
    ga@gmail.com
    ('phone', '01031448845')
    phone
    01031448845



```python
# Dict for loop(3)

for key, value in my_informations.items():
    print(key)
    print(value)
```

    age
    24
    name
    wonju
    email
    ga@gmail.com
    phone
    01031448845



```python
my_informations.keys()
my_informations.values()
my_informations.items()
```




    dict_items([('age', 24), ('name', 'wonju'), ('email', 'ga@gmail.com'), ('phone', '01031448845')])




```python
animals = ["강아지", "고양이", "거북이", "토끼", "참새"]

# 하나씩 출력을 하는데,
# index 가 2번인 애는 "파이썬" 으로 변경하자.
```


```python
for i in range(len(animals)):
    if i == 2:
        animals[i] = "파이썬"    
    print(animals[i])
```

    강아지
    고양이
    파이썬
    토끼
    참새



```python
animals.index("강아지")
```




    0




```python
for animal in animals:
    if animals.index(animal) == 2:
        animal = "거북이"
    print(animal)
    
```

    강아지
    고양이
    거북이
    토끼
    참새



```python
for number, animal in enumerate(animals):
    if number == 2:
        animal = "코끼리"
    print(animal)    
```

    강아지
    고양이
    코끼리
    토끼
    참새



```python
for something in enumerate(animals):
    number, animal = something
    if number == 2:
        animal = "다람쥐" 
    print(animal)    
```

    강아지
    고양이
    다람쥐
    토끼
    참새



```python
# 소수 구하기 ( prime nimber)
```


```python
def get_prime_numbers(number):
    # number 만큼 for 문을 돌면서,
    # 각각의 숫자가 소수인지 아닌지를 체크
    # 빈 리스트 만들어서
    # 소수면 리스트에 추가하고
    # for 끝나는 시점에 빈 리스트를
    
    prims_numbers = []
    for i in range(2, number):
        #소수인지 아닌지 체크하는 함수
        pass
```


```python
def is_prime(number):
    # 2부터 number-1 까지의 숫자로 각각 나눠서 체크해본다.
    for i in range(2, number):
        if (number % i == 0):
            return False
    return True
```


```python
def get_prime_numbers(number):
    # number 만큼 for 문을 돌면서,
    # 각각의 숫자가 소수인지 아닌지를 체크
    # 빈 리스트 만들어서
    # 소수면 리스트에 추가하고
    # for 끝나는 시점에 빈 리스트를
    
    prime_numbers = []
    for i in range(2, number):
        #소수인지 아닌지 체크하는 함수
        if is_prime(i):
            prime_numbers.append(i)
    return prime_numbers
```


```python
get_prime_numbers(11)
```




    [2, 3, 5, 7]




```python
def sum(a,b):
    print("sum: {result}".format(result = a + b))
```


```python
print(sum(1,3))
```

    sum: 4
    None



```python
sum(1, 3)
```

    sum: 4



```python
def sum(a,b):
    return a + b
```


```python
sum(10,20)
```




    30




```python
# sum = > funtion
# a, b => parameter
# 10, 20 => argument
```


```python
# 입력받은 모든 숫자를 더해주는 'sum'이라는 함수를 만들어라

def sum(number_list): 
    total = 0
    for number in number_list:
        total = number + total
    return total
```


```python
sum([1,2,3,4,5])
```




    15




```python
def sum(*args):
    total = 0
    for arg in args:
        total += arg
    return total
```


```python
sum(1,2,3,4,5)
```




    15




```python
def greeting(name, course):
    print("{name}님, {course} 등록을 축하 드립니다.".format(name = name, course = course))
   
greeting("황원주", "웹프스")
```

    황원주님, 웹프스 등록을 축하 드립니다.



```python
values = ("황원주", "웹프스")
greeting(values)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-30-e4821951cc6a> in <module>()
          1 values = ("황원주", "웹프스")
    ----> 2 greeting(values)
    

    TypeError: greeting() missing 1 required positional argument: 'course'



```python
# unpack / unpacking
greeting(*values) # => greetig("황원주","웹프스")
```

    황원주님, 웹프스 등록을 축하 드립니다.



```python
def greeting(name, course, happy):
    print("{name}님, {course} 등록을 {happy} 드립니다.".format(name = name, course = course, happy = happy))
```


```python
value = ("황원주", "웹프스", "축하")
```


```python
greeting(*value)
```

    황원주님, 웹프스 등록을 축하 드립니다.



```python
# unnamed => *args
# named => **kwargs
```


```python
def greeting(name, course):
    print("{name}님, {course} 등록을 축하 드립니다.".format(name = name, course = course))
   
```


```python
greeting(name = "황원주", course = "웹프스")
```

    황원주님, 웹프스 등록을 축하 드립니다.



```python
values = {"name": "황원주", "course": "웹프스"}
```


```python
greeting(**values)
```

    황원주님, 웹프스 등록을 축하 드립니다.



```python
def print_all_informations(**kwargs):
    for key, value in kwargs.items():
        print("{key} => {value}".format(key = key, value = value))
```


```python
informations = {
    "name" : "황원주",
    "이메일" : "가후",
    "전화" : "010-3144-8845"
}
```


```python
print_all_informations(**informations)
```

    name => 황원주
    이메일 => 가후
    전화 => 010-3144-8845



```python
print_all_informations(a = "b", d = "e")
```

    d => e
    a => b



```python
def 누가만들어논함수(이건필수값1, 이건필수값2, *args, **kwargs):
    pass
```


```python
# Lambda
# 이름이 없는 함수 (익명 함수)
```


```python
def increment(x):
    return x + 1
```


```python
increment(55)
```




    56




```python
lambda x: x+1
```




    <function __main__.<lambda>>




```python
incerment_lambda = lambda x: x+1
```


```python
incerment_lambda(33)
```




    34




```python
(lambda x: x+1)(34)
```




    35




```python
(lambda x, y: x+y)(10, 20)
```




    30




```python
# 리스트를 입력받아 그 값을 제곱한 값이 출력되도록 함수 만들기
# ex) [1, 2, 3] = [1, 4, 9]
```


```python
def square_list_elements(*argus):
    list = []
    for argu in argus:
        list.append(argu ** 2)
    return list
```


```python
def get_square_list(numbers):
    square_list = []
    for number in numbers:
        square_list.append(number ** 2)
    return square_list
```


```python
get_square_list([1,2,3])
```




    [1, 4, 9]




```python
square_list_elements(1,2,3)
```




    [1, 4, 9]




```python
# [1, 2, 3] => [2, 3, 4]

def get_increment_list(numbers):
    incerment_list = []
    for number in numbers:
        incerment_list.append(number + 1)
    return incerment_list
```


```python
get_increment_list([1, 2, 3])
```




    [2, 3, 4]




```python
def square(x):
    return x ** 2
```


```python
list(map(square, [1, 2, 3]))
```




    [1, 4, 9]




```python
list(map(lambda x: x**2, [1, 2, 3]))
```




    [1, 4, 9]




```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```


```python
list(filter(lambda x: x>5, numbers))
```




    [6, 7, 8, 9]




```python
a = map(lambda x: x**8, numbers)
list(a)
```




    [0, 1, 256, 6561, 65536, 390625, 1679616, 5764801, 16777216, 43046721]




```python
import time

def sleeping_numbers(x):
    time.sleep(1)
    return x ** 2
```


```python
sleeping_numbers(1)
```




    1




```python
a = map(sleeping_numbers, [1, 2, 3, 4, 5])
```


```python
for i in a:
    print(i)
```

    1
    4
    9
    16
    25



```python
list(a)
```




    []




```python
# Map => 모든 Element => 새로운 List
# Filter => 모든 Element => Ture 인 Element 만 새로운 List
```


```python
# Reduce => import functools 해야됨(파이썬 3)
# 줄이는 애
# 하나만 남기는 애
```


```python
import functools
```


```python
# functools.reduce
```


```python
functools.reduce(lambda x, y: x + y, [10, 20, 30, 40])
```




    100




```python
def sum(x, y):
    print((x, y))
    return x + y
```


```python
functools.reduce(sum,[10, 20, 30, 40, 50])
```

    (10, 20)
    (30, 30)
    (60, 40)
    (100, 50)





    150




```python
#리스트에서 최대값을 뽑는 함수
 
def max(numbers):
    i = 0
    for number in numbers:
        if number >= i:
            i = number
    print(i)
```


```python
list_a = [2,3,76,4,3,5,7,4,57]
```


```python
max(list_a)
```

    76



```python
functools.reduce(lambda x, y: x if x>y else y, list_a)
```




    76




```python
3 if True else 5
```




    3




```python
3 if False else 5
```




    5




```python
# [참일때의 값] if [조건문] else [거짓일때의 값]
```


```python
awesome_list = [1, 2, "안수찬", {}, [], 4, 5]
```


```python
# Lamvda Operator => awesome_list 에서 숫자값만 제곱해서나오게
# [1, 4, 16, 25]

isinstance(1, int)  
```




    True




```python
def choose_number(groups):
    i = []
    for group in groups:
        if isinstance(group, int):
            i.append(group**2)
    print(i)        
```


```python
choose_number(awesome_list)
```

    [1, 4, 16, 25]



```python
list(map(
    lambda x: x**2, 
    filter(
        lambda x: isinstance(x, int),
        awesome_list
    )
))
```




    [1, 4, 16, 25]




```python
[i for i in range(10)]
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
[i ** 2 for i in range(10)]
```




    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]




```python
list(map(lambda x: x ** 2, range(10)))
```




    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]




```python
[i ** 2 for i in range(10) if i > 5]
```




    [36, 49, 64, 81]




```python
# 1-100 까지 숫자 중에서 짝수인 애들의 제곱 리스트
```


```python
def result_list(numbers):
    i = []
    for number in numbers:
        if number%2 == 0:
            i.append(number ** 2)
    return i
```


```python
a = list(map(lambda x: x, range(1,101)))
```


```python
print(result_list(a))
```

    [4, 16, 36, 64, 100, 144, 196, 256, 324, 400, 484, 576, 676, 784, 900, 1024, 1156, 1296, 1444, 1600, 1764, 1936, 2116, 2304, 2500, 2704, 2916, 3136, 3364, 3600, 3844, 4096, 4356, 4624, 4900, 5184, 5476, 5776, 6084, 6400, 6724, 7056, 7396, 7744, 8100, 8464, 8836, 9216, 9604, 10000]



```python
print([i ** 2 for i in range(1,101) if i % 2 == 0])
```

    [4, 16, 36, 64, 100, 144, 196, 256, 324, 400, 484, 576, 676, 784, 900, 1024, 1156, 1296, 1444, 1600, 1764, 1936, 2116, 2304, 2500, 2704, 2916, 3136, 3364, 3600, 3844, 4096, 4356, 4624, 4900, 5184, 5476, 5776, 6084, 6400, 6724, 7056, 7396, 7744, 8100, 8464, 8836, 9216, 9604, 10000]



```python
# 소수 구하기
# 소수가 아닌 애들 먼저 찾고
# 범위 안에서 소수가 아닌 애들을 제거
```


```python
def a(i):
    if 40%i == 0:
        print(2)
        
a(4)
```

    2



```python
def is_prime(number):
    for i in range(2, number):
        if number%i == 0 :
            return False
        else:
            return True
```


```python
print(list(filter(lambda x: is_prime(x), range(2,101))))
```

    [3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99]



```python
print([i for i in range(2,100) if is_prime(i)])
```

    [3, 5, 7, 9, 11, 13, 15, 17, 19, 21, 23, 25, 27, 29, 31, 33, 35, 37, 39, 41, 43, 45, 47, 49, 51, 53, 55, 57, 59, 61, 63, 65, 67, 69, 71, 73, 75, 77, 79, 81, 83, 85, 87, 89, 91, 93, 95, 97, 99]



```python
awesome_list = [(i, j) 
    for i in range(8) 
    for j in range(4)
]
```


```python
print(awesome_list)
```

    [(0, 0), (0, 1), (0, 2), (0, 3), (1, 0), (1, 1), (1, 2), (1, 3), (2, 0), (2, 1), (2, 2), (2, 3), (3, 0), (3, 1), (3, 2), (3, 3), (4, 0), (4, 1), (4, 2), (4, 3), (5, 0), (5, 1), (5, 2), (5, 3), (6, 0), (6, 1), (6, 2), (6, 3), (7, 0), (7, 1), (7, 2), (7, 3)]




```python
# Decorator => 람다와 성질이 비슷
#           => 함수를 입력 받아 새로운 함수를 리턴하는 함수

# 여러개를 함께 쓸 수도 있다
```


```python
import time

def get_timer(function):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = function(*args, **kwargs)
        end_time = time.time()
        print("{time}s 초 걸렸습니다.".format(time=end_time-start_time))
        return result
    return wrapper
```


```python
memo = [0, 1]
```


```python
@get_timer

def fibonacci_dp(x):
    if x <= 0:
        return 0
    if x == 1:
        return 1
    if len(memo)-1 >= x:
        return memo[x]
    if len(memo)-1 < x:
        new_number = fibonacci_dp(x-1) + fibonacci_dp(x-2)
        memo.append(new_number)
        return new_number
```


```python
fibonacci_dp(20)
```

    2.384185791015625e-06s 초 걸렸습니다.





    6765




```python
def fridge(function):
    def wrapper(*args, **kwargs):
        print("냉장고를 연다.")
        function(*args, **kwargs)
        print("냉장고를 닫는다.")
    return wrapper
```


```python
@fridge
def put_fridge(food):
    print("{food}를 냉장고에 넣는다.".format(food=food))
```


```python
put_fridge("족발")
```

    냉장고를 연다.
    족발를 냉장고에 넣는다.
    냉장고를 닫는다.



```python
# @before_enecute => "_____ 함수를 실행 시작합니다."
# @after_execute => "______ 함수 실행을 종료합니다."
# @timer =>_____ s 초 걸렸습니다."

# something(....)

# something 함수를 실행합니다.
# ....
# something 함수를 종료합니다.
# something 함수를 실행하는데 ____s  걸렸습니다.

# @log_to_csv => csv 파이르을 읽어서, 함수의 실행 순서에 대해서 기록해주는 애
```


```python
# decorator function =>
```


```python
def before_execute(function):
    def wrapper(*args, **kwargs):
        print("@before_execute")
        print("{function} 을 실행합니다.".format(function=function))
        return function(*args, **kwargs)
    return wrapper


def after_execute(function):
    def wrapper(*args, **kwargs):
        print("@after_execute")
        result = function(*args, **kwargs)
        print("{function} 를 종료합니다.".format(function=function))
        return result
    return wrapper


def timer(function):
    def wrapper(*args, **kwargs):
        print("@timer")
        start_time = time.time()
        result = function(*args, **kwargs)
        end_time = time.time()
        print("{time}s 가 소요되었습니다.".format(time=end_time-start_time))
        return result
    return wrapper
```


```python
@timer
@after_execute
@before_execute
def something():
    print("something")
    return "This is something"
```


```python
something()
```

    @timer
    @after_execute
    @before_execute
    <function something at 0x7f6c90719598> 을 실행합니다.
    something
    <function before_execute.<locals>.wrapper at 0x7f6c90719268> 를 종료합니다.
    3.24249267578125e-05s 가 소요되었습니다.





    'This is something'




```python
# 데코레이터 역순으로 결과가 나온다. 레핑의 개념이기 때문
```


```python

# def introduce(name, course):
#     return("안녕하세요, 저는 {name} 입니다. {course} 에서 공부하고 있습니다.".format(
#         name=name,
#         course=course,
#     ))

```


```python
# @bold
# @italic
# => <b><i>...</i></b>

# @phonenumber
# 010-둘둘둘영-오칠삼육 = > 01022005736
```


```python
def bold(function):
    def wrapper(*args, **kwargs):
        return "<b>{text}</b>".format(
            text=function(*args, **kwargs)
        )
    return wrapper
```


```python
def italic(function):
    def wrapper(*args, **kwargs):
        return "<i>{text}</i>".format(
            text=function(*args, **kwargs)
        )
    return wrapper
```


```python
@bold
@italic
def introduce(name, course):
    return("안녕하세요, 저는 {name} 입니다. {course} 에서 공부하고 있습니다.".format(
        name=name,
        course=course,
    ))
```


```python
introduce("원주", "패캠")
```




    '<b><i>안녕하세요, 저는 원주 입니다. 패캠 에서 공부하고 있습니다.</i></b>'




```python
def prettify(function):
    def wrapper(*args, **kwargs):
        result = function(*args, **kwargs)
        return result.replace("오", "5").replace("칠", "7").replace("삼", "3").replace("육", "6")
    return wrapper
```


```python
def crawl_phonenumber(naver_cafe_name, naver_cafe_post_id):
    # 어떤 식으로 크롤링 되어서....
    return "010-2220-오칠삼육"

crawl_phonenumber("중고나라", "35782")
```




    '010-2220-오칠삼육'




```python

```

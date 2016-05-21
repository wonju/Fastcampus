

```python
# ---------------------------------
# enumerate(리스트) => (index, value)
# ---------------------------------
```


```python
list(enumerate([1,2]))
```




    [(0, 1), (1, 2)]




```python
# ---------------------------------
# List Comperhersion 
# ---------------------------------
# => [계산식 또는 결과형 for i in 리스트 또는 range] 하면 리스트가 만들어져용
```


```python
[{i, j} for i,j in enumerate([1,2])]
```




    [{0, 1}, {1, 2}]




```python
# ---------------------------------
# Lambda(익명함수)
# ---------------------------------
```


```python
(lambda x,y: x + y)(2,3)
```




    5




```python
# ---------------------------------
# Lambda Operator
# ---------------------------------
# map, filter, reduce 등에 들어가는 함수에 람다를 많이 사용

# map    =>   map(함수, 리스트) : 리스트값을 함수로 계산
# filter =>   filter(블리언, 리스트) : 리스트중 참의 값으로 정리
# reduce =>   functools.reduce(함수(블리언포함), 리스트) : 둘중 하나만 남기는
```


```python
a = [1, 2, 3, 4]
print(list(map(lambda x: x**2, a)))
print(list(filter(lambda x: x>2, a)))
import functools
functools.reduce(lambda x, y: x + y, a)
```

    [1, 4, 9, 16]
    [3, 4]





    10




```python
# ---------------------------------
# *args, **kwargs
# ---------------------------------

# packing, unpacking을 이용해 정해지지 않은 argument또는 keyword argument를 받음
# packing => 패킹을 함 ex) a = 2, 3
# unpacking => 패킹을 풀음 ex) a, b = 2, 3 ==> 즉 a = 2, b = 3 이 된다능
```


```python
# ---------------------------------
# spilt, join, replace
# ---------------------------------

# spilt => 문장.spilt("") => 구분자("")를 중심으로 문장을 나눔
# join  => 구분자.join(리스트) => 구분자를 넣어 문장을 붙임
# replace => 문장.replace(변경 전 단어, 변경 후 단어) => 변경전 단어를 후 단어로 고침
```


```python
"#".join('새로운 도전은 즐겁다'.split(" "))
```




    '새로운#도전은#즐겁다'




```python
'새로운 도전은 즐겁다'.replace(" ","#")
```




    '새로운#도전은#즐겁다'




```python

```

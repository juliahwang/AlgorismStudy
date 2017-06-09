## 서울에서 김서방 찾기 

findKim 함수(메소드)는 String형 배열 seoul을 매개변수로 받습니다.

seoul의 element중 "Kim"의 위치 x를 찾아, "김서방은 x에 있다"는 String을 반환하세요.
seoul에 "Kim"은 오직 한 번만 나타나며 잘못된 값이 입력되는 경우는 없습니다.

### 내 코드

```
def findKim(seoul):
    kimIdx = 0
    while kimIdx < len(seoul):
        if seoul[kimIdx]=="Kim":
            return "김서방은 {}에 있다".format(kimIdx)
        kimIdx += 1

# 실행을 위한 테스트코드입니다.
print(findKim(["Queen", "Tod", "Kim"]))
```


### 타인의 코드 

```python
def findKim(seoul):
    return "김서방은 {}에 있다".format(seoul.index('Kim'))


# 실행을 위한 테스트코드입니다.
print(findKim(["Queen", "Tod", "Kim"]))
```

```python
def findKim(seoul):

    for i,v in enumerate(seoul):
        if v == 'Kim':
            kimIdx = i


    return "김서방은 {}에 있다".format(kimIdx)


# 실행을 위한 테스트코드입니다.
print(findKim(["Queen", "Tod", "Kim"]))
```

<br>

## 삼각형 출력하기 

printTriangle 메소드는 양의 정수 num을 매개변수로 입력받습니다.
다음을 참고해 *(별)로 높이가 num인 삼각형을 문자열로 리턴하는 printTriangle 메소드를 완성하세요
printTriangle이 return하는 String은 개행문자('\n')로 끝나야 합니다.

높이가 3일때

	*
	**
	***
	
### 내코드 

```python
def printTriangle(num):
    s = ""
    for row in range(1, num+1):
        s += ('*' * row + '\n')
    return s

# 아래는 테스트로 출력해 보기 위한 코드입니다.
print( printTriangle(3) )
```


### 타인의 코드 

```python
def printTriangle(num):
    return ''.join(['*'*i + '\n' for i in range(1,num+1)])


# 아래는 테스트로 출력해 보기 위한 코드입니다.
print( printTriangle(3))
```
---
layout: post
title: CodingTest Tip (Python)
date: 2022-06-13 13:56 +0800
last_modified_at: 2022-06-02 13:56 +0800
tags: [코딩테스트, 프로그래머스]
toc:  true
---

# 코딩테스트
### 성장과정의 기록

```python
# 꾸준히 풀기
# 복습하고 풀이를 내 것으로 만들기

# 막힐 땐 다음을 생각하자

# 1. 예외처리
# 2. type
# 3. 조건
# 4. 초기화 (for문)

# 변수 선언은 for문 밖에 하기 (for문 특징 이해)
```

# 문자열

## lv1. 문자열 바꾸기

```python
def solution(phone_numbers):
    return "*" * (len(phone_numbers)-4) + phone_numbers[-4:]

# 문자열은 곱셈이 된다는 점을 기억하자

# list slicing 방법
# [a:b] = a는 포함, b는 포함 x
# [:-4] = 0부터 -4까지
# [-4:] = -4부터 끝까지

```

## lv1. 없는 숫자 더하기
```python
def solution(numbers):
    return sum(range(10)) - sum(numbers)

# sum(range(10)) : 1부터 9까지의 숫자를 더한다
```

## lv1. 문자열 가운데 출력
```python
def solution(s):
    answer = s[(len(s) - 1) // 2 : len(s) // 2 + 1]
    return answer

# 홀수일때와 짝수일때의 가운데가 다를때 응용할 수 있다
# 홀수일 경우 범위(ex: 5) = [2:3]
# 짝수일 경우 범위(ex: 6) = [2:4], 2-3번째 인덱스 출력
# // 몫, / 나누기, % 나머지
```

## lv1. 문자열 정렬하기
```python
def solution(strings, n):
    
    strings.sort(key=lambda x: (x[n], x))
    
    return strings

# 2차원 배열일 때, 내 마음대로 정렬
# strings의 배열을 lambda에 맞춰 sort
# key=lambda x: (x[n], x)
# x[n]에 맞춰 정렬하고, 중복일 땐 x(string)에 맞추기
```

## lv1. 문자열 내 알파벳 개수
```python
def solution(s):
    answer = True
    if s.count('P') + s.count('p') != s.count('Y') + s.count('y'):
        answer = False

    return answer

# 기본 출력값을 True로 두고, 조건에 False를 걸기
# 대문자와 소문자를 같게 취급하니까 합이 같지 않을 때 False
# s.lower().count('p) 로 한꺼번에 바꿔도 됨
```

## lv1. 문자열 숫자 구성 확인
```python
def solution(s):
    if (len(s)==4 or len(s)==6) and s.isdigit():
        answer = True
    else:
        answer = False

# 주의할 점: 조건문을 잘 읽자
# 길이가 4 혹은 6이면서 숫자일 때 True 반환
# s.isdigit() : 문자열의 숫자 확인 함수
```

## lv1. 문자열 내림차순 배열
```python
def solutions(s):
    return ''.join(sorted(s,reverse=True))

# 문자열도 sort 정렬 가능 : sorted(s)
# reverse=True : 내림차순 정렬

# join 활용 : ''.join
# 혹은 answer = answer.join 해줘도 됨
```

## lv1. K번째 수
```python
def solution(array, commands):
    answer = []
    for i in commands:
        answer.append(sort(array(i[0]-1:i[1])[i[2]-1]))
    return answer

# array의 i[0]-1 부터 i[1]까지를 sort
# sort한 리스트의 i[2]-1 뽑아내기
# answer에 append

# range의 경우 a:b에서 b는 포함이 안되므로 1을 안빼지만 a와 인덱스는 1 빼주기
```

## lv1. 숫자 문자열과 영단어
```python
def solution(s):
    num_dict = {"zero":"0", "one":"1", "two":"2", "three":"3", "four":"4", "five":"5", "six":"6", "seven":"7", "eight":"8", "nine":"9"}

    answer = s

    for key, val in num_dict.items():
        answer = answer.replace(key,val)
    
    return int(answer)

# dictionary 특징 이해하기
# dictionary = {key, val} key는 중복되면 안됨
# dict.items() : dictionary의 아이템들 꺼내기

# replace(key, val) : key가 있으면 val로 replace
# int(a), str(a) : type 변환 (int 혹은 str) 
```
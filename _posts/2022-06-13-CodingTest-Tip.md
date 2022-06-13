---
layout: post
title: CodingTest Tip (Python)
date: 2022-06-13 13:56 +0800
last_modified_at: 2022-06-02 13:56 +0800
tags: [jekyll theme, jekyll, tutorial]
toc:  true
---

## 코딩테스트

## 문자열 바꾸기

```python
def solution(phone_numbers):
    return "*" * (len(phone_numbers)-4) + phone_numbers[-4:]

# 문자열은 곱셈이 된다는 점을 기억하자

# list slicing 방법
# [a:b] = a는 포함, b는 포함 x
# [:-4] = 0부터 -4까지
# [-4:] = -4부터 끝까지

```

## 없는 숫자 더하기
```python
def solution(numbers):
    return sum(range(10)) - sum(numbers)

# sum(range(10)) : 1부터 9까지의 숫자를 더한다
```

## 문자열 가운데 출력
```python
def solution(s):
    answer = s[(len(s) - 1) // 2 : len(s) // 2 + 1]
    return answer

# 홀수일때와 짝수일때의 가운데가 다를때 응용할 수 있다
# 홀수일 경우 범위(ex: 5) = [2:3]
# 짝수일 경우 범위(ex: 6) = [2:4], 2-3번째 인덱스 출력
# // 몫, / 나누기, % 나머지
```
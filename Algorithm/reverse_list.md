# 리스트를 역순으로 정렬하기

## Python

1. 파이썬 표준 라이브러리 사용
```
x.reverse()
```
2. 역순으로 정렬한 리스트 생성
```
y = list(reversed(x))
```
reversed는 x의 원소를 역순으로 정렬하는 이터러블 객체를 생성한다. 엄밀히 말하자면 x의 원소를 역순으로 꺼내는 이터레이터(반복자)를 반환한다. 따라서 어떤 리스트의 원소를 역순으로 정렬한다면, reversed() 함수가 반환하는 이터러블 객체를 list() 함수에 넘기고 새로운 리스트를 생성한 후 대입해야 한다.
# 기수 변환하기 (n진수 구하기)

10진수 정수를 n진수로 변환하려면 정수를 n으로 나눈 나머지를 구하는 동시에 몫을 반복해서 나누어야 한다. 몫이 0이 될 때까지 이 과정을 반복하고 나머지를 역순으로 늘어놓으면 기수로 변환한 수가 된다.

## Python
10진수 정숫값을 입력받아 2~36진수로 변환하여 출력하기

### 도입부
```
def card_conv(x: int, r: int) -> str:
    
    d = ''
    dchar = '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ'

    while x > 0:
        d += dchar[x % r]
        x //= r

    return d[::-1]
```

### 메인부

```
if __name__ == '__main__':
    print('10진수를 n진수로 변환합니다.')

    while True :
        While True :
            no = int(input('변환할 값으로 음이 아닌 정수를 입력하세요.: '))
            if no > 0:
                break
        
        while True :
            cd = int(input('어떤 진수로 변환할 까요?: '))
            if 2 <= cd <= 36:
                break
        
        print(f'{cd}진수로는 {card_conv(no, cd)}입니다.')

        retry = input("한 번 더 변환할까요?(Y ... 예 / N ... 아니요): ")
        if retry in {'N', 'n'}:
            break
```
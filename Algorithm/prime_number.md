# n 이하의 소수 나열하기

어떤 정수 이하의 소수를 모두 나열하는 알고리즘 <br> 다음의 조건을 만족하면 소수이다.
```
2부터 n-1까지 어떤 정수로도 나누어 떨어지지 않는다.
```

## Python

### 1~n 을 돌며 2~n-1로 나뉘는 지 확인
```
counter = 0

for n in range(2, 1001):
    for i in range(2, n): #2부터 n-1까지를 도는 i
        counter += 1
        if n % i == 0 : #나누어 떨어지면 소수가 아님
            break
    else : #for ~ else 문
        print(n)

print(f'나눗셈을 실행한 횟수: {counter}')
```

> for ~ else문은 for문이 break이 되지 않고 마지막까지 실행되었을 때 else문이 실행된다. 

### 알고리즘 개선 1

어떤 수가 소수인지 확인할 때, 2나 3으로 안나눠지는지 확인했다면 당연히 2 X 2인 4나 2 X 3인 6으로도 안나누어진다는 것을 알 수 있다. 즉, 위 프로그램은 불필요한 연산을 계속 실행하고 있다. <br> 결국 정수 n이 소수인지 여부는 다음 조건을 만족하면 된다.
```
2부터 n-1까지 어떤 소수로도 나누어 떨어지지 않는다.
```
```
counter = 0
ptr = 0
prime = [None] * 500

prime[ptr] = 2
ptr += 1

for n in range(3, 1001, 2) #짝수는 소수 X
    for i in range(1, ptr): 
        counter += 1
        if n % prime[i] == 0:
            break
    else:
        prime[ptr] = n
        ptr += 1

for i in range(ptr):
    print(prime[i])

print(f'나눗셈을 실행한 횟수: {counter}')
```
> 처음 ptr은 1이기 때문에 range(1, 1)은 실행되지 않는다. 이 for 문이 실행되지 않아도 그 다음의 else 문은 실행된다. 따라서 n은 소수로 판단되어 prime[1]에 n 값, 곧 3을 대입하고 ptr을 증가시킨다.

> 안쪽 for문이 0이 아니라 1부터 반복되는 이유는 판단 대상인 n이 홀수이므로 prime[0]에 저장된 2로는 나눌 필요가 없기 때문이다.

### 알고리즘 개선 2

<img src="https://user-images.githubusercontent.com/76716519/149663108-15483651-a87c-4f79-aaef-806672b423a5.png" width="480px">

넓이가 100인 직사각형의 가로, 세로 변의 길이를 생각해보면, 5 X 20과 20 X 5는 가로, 세로 변의 길이는 다르지만 같은 직사각형이다. 따라서 모든 직사각형은 정사각형인 10 X 10을 경계로 대칭 구조를 이룬다.

만약 100이 5로 나누어 떨어지지 않는다면 20으로도 나누어 떨어지지 않는다. 이것은 직사각형 한 변의 길이만 나눗셈을 시도하고, 그 과정에서 한 번도 나누어 떨어지지 않으면 소수라고 판단할 수 있는 근거가 된다. 즉, 다음의 조건을 만족하는 정수 n은 소수이다.

```
n의 제곱근 이하의 어떤 소수로도 나누어 떨어지지 않는다.
```

```
counter = 0
ptr = 0
prime = [None] * 500

prime[ptr] = 2
ptr += 1

prime[ptr] = 3
ptr += 1

for n in range(5, 1001, 2):
    i = 1
    while prime[i] * prime[i] <= n:
        counter += 2
        if n % prime[i] == 0:
            break
        i += 1
    
    else:
        prime[ptr] = n
        ptr += 1
        counter += 1

for i in range(ptr):
    print(prime[i])
print(f'곱셈과 나눗셈을 실행한 횟수 : {counter}')
```
> counter는 연산을 얼마나 하는지 저장하는 변수이므로, 곱셈과 나눗셈을 하는 횟수를 저장한다. 즉, counter는 이 알고리즘이 계산 비용을 얼마나 요구하는지 나타낸다.

> while 문을 반복할 때마다 counter를 2씩 증가시키는 것은 prime[i] * prime[i]의 곱셈과 n % prime[i]의 나눗셈의 횟수를 세기 때문이다.

> prime[i] * prime[i] <= n 이 성립하지 않는 경우 while이 실행되지 않으므로 counter를 더할 수 없다. 따라서 else문에서 곱셈치 1을 더해준다.

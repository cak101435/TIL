# ��� ��ȯ�ϱ� (n���� ���ϱ�)

10���� ������ n������ ��ȯ�Ϸ��� ������ n���� ���� �������� ���ϴ� ���ÿ� ���� �ݺ��ؼ� ������� �Ѵ�. ���� 0�� �� ������ �� ������ �ݺ��ϰ� �������� �������� �þ������ ����� ��ȯ�� ���� �ȴ�.

## Python
10���� �������� �Է¹޾� 2~36������ ��ȯ�Ͽ� ����ϱ�

### ���Ժ�
```
def card_conv(x: int, r: int) -> str:
    
    d = ''
    dchar = '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ'

    while x > 0:
        d += dchar[x % r]
        x //= r

    return d[::-1]
```

### ���κ�

```
if __name__ == '__main__':
    print('10������ n������ ��ȯ�մϴ�.')

    while True :
        While True :
            no = int(input('��ȯ�� ������ ���� �ƴ� ������ �Է��ϼ���.: '))
            if no > 0:
                break
        
        while True :
            cd = int(input('� ������ ��ȯ�� ���?: '))
            if 2 <= cd <= 36:
                break
        
        print(f'{cd}�����δ� {card_conv(no, cd)}�Դϴ�.')

        retry = input("�� �� �� ��ȯ�ұ��?(Y ... �� / N ... �ƴϿ�): ")
        if retry in {'N', 'n'}:
            break
```
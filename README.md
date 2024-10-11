# SWE_2021_41_2024_2_week_6
---
### Week 4 Assignment<br/>
- [My repository link](https://github.com/chlrudtlr/SWE_2021_41_2024_2_week_4/tree/main)<br/>

```python
def isHappy(n):
    sum = 0
    while n>0:
        digit = n%10
        n = n//10
        sum += digit*digit
    if sum == 1:
        return True
    elif sum > 1 and sum < 10:
        return False
    else:
        return isHappy(sum)
```
- 입력된 숫자의 각 자릿수의 제곱의 합을 반복적으로 계산하면서, 그 값이 최종적으로 1이 되는지(Happy number인지)를 확인하는 함수
- While문을 이용해 숫자의 각 자릿수(digit)를 구하고, 그 자릿수의 제곱을 더하여 sum에 저장.
- 반복문이 끝난 후에 sum이 1이면 True를 반환.
- sum이 1보다 크고 10보다 작은 경우는 1이 아닌 한자리 수에서 계산이 완료된 것이므로 False를 반환
- 그 외의 경우(sum이 두자리 수인 경우)는 계산이 완료되지 않았으므로 재귀적으로 계산 반복
---
### Week 5 Assignment<br/> 

> ```bash
> $ docker exec new-container cat /etc/os-release
> ```
>- 컨테이너의 '/etc/os-release' 파일을 읽어 운영 체제(OS)의 정보를 출력하는 command.
>- 주로 리눅스 배포판의 이름, 버전, ID 등의 정보를 포함하고 있음.
>- Output<br/> 
> ![image](https://github.com/chlrudtlr/SWE_2021_41_2024_2_week_6/blob/main/week5_1.png)

> ```bash
> $ docker exec new-container git --version
> ```
>- 설치된 git의 버전을 출력하는 command.<br/> 
>- Output<br/> 
> ![image](https://github.com/chlrudtlr/SWE_2021_41_2024_2_week_6/blob/main/week5_2.png)

> ```bash
> $ docker exec new-container python3 --version
> ```
>- 설치된 python 3의 버전을 출력하는 command.<br/>
>- Output<br/> 
> ![image](https://github.com/chlrudtlr/SWE_2021_41_2024_2_week_6/blob/main/week5_3.png)

> ```bash
> $ docker inspect --format="{{ .HostConfig.Binds }}" new-container
> ```
>- 호스트 시스템에서 해당 컨테이너의 바인드 마운트 설정을 조회하는 command.
>- 주로 컨테이너가 호스트 시스템의 디렉터리를 잘 마운트하고 있는지를 확인하기 위해 사용
>- Output<br/> 
> ![image](https://github.com/chlrudtlr/SWE_2021_41_2024_2_week_6/blob/main/week5_4.png)

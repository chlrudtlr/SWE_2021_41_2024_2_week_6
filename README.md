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
- Description of my code
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

---
layout: single
title: "프로젝트"
---

[문제 상황]
==
일어날 때 한번에 못일어나기도 하고 일어나도 다시 잠듦

[작업 조건]
==
정해진 시간에 알람 울림.  
알람을 끄려고 하면 문제가 나옴(덧셈) 문제 틀리면 다른 수로 다른 문제가 나옴.  
알람을 끄려고 하지 않으면 5분후 다시 울림

[설계]
==
알람이 울리면서 단순 연산 문제가 나옴.
맞추면 기상
틀리면 알람이 다시 울림

[구현]
==
~~~python
time=int(input('시: '))
minute=int(input('분: '))
from datetime import datetime
now = datetime.now()
h = now.hour
m = now.minute
import random
num1=random.randint(1,9999)
num2=random.randint(1,9999)
if time==h and minute==m:
  print('@@@@@@@@@@')
  print(num1)
  print(num2)
  a=int(input('답: '))
  if a==(int(num1)+int(num2)):
    print('기상')
  else:
    print('@@@@@@@@@@')
~~~

[테스트]
==
1) 현재 시각 3:03  
시: 3  
분: 3  
@@@@@@@@@@  
5552  
613  
답: 6165  
기상  

2) 현재시각 3:06  
시: 3  
분: 6  
@@@@@@@@@@  
2905  
5816  
답: 99  
@@@@@@@@@@

[프로젝트 후 소감]
==
이러한 알람은 이미 앱으로 나와있지만 이렇게 모방함으로서 또 하나의 새롭고 좋은 아이디어가 나올 수 있다고 생각한다. 처음에 계획한대로 만들지 못해 아쉬웠지만 공부를 좀더 한뒤 다음번엔 더 잘 만들어보고싶다.

# aicontrol1

### 내가 만든 첫 마크다운 파일입니다

---
title: "[Python]연습문제: 문자열, 리스트, 튜플"
excerpt: "[Python]문자열, 리스트, 튜플"
categories: [Python]
tags: [python, study]
toc: true
toc_sticky: true
---

## ✏️1번

- 문제  
![문제 이미지-불러오기 실패](/assets/Image/python_assign_02_2_1.png)  
- 입력  
  
  ```python
    s1= "spam"
    s2= "ni!"

    print("The Knights who say, " + s2)
    print(3*s1 + 2*s2)
    print(s1[1])
    print(s1[1:3])
    print(s1[2] + s2[:2])
    print(s1 + s2[-1])
    print(s1.upper())
    print(s2.upper().ljust(4)*3)
    ```  
- 결과  
    ```python
    The Knights who say, ni!
    spamspamspamni!ni!
    p
    pa
    ani
    spam!
    SPAM
    NI! NI! NI!
    ```
      
## ✏️2번

- 문제  


![문제 이미지-불러오기 실패](/assets/Image/python_assign_02_2_2.png)  

- 답안  

```python
#(a) 슬라이싱을 이용해 앞 두글자'ni'를 띄어내고 .upper()함수를 사용해 소문자를 대문자로 만들어줌
print('"'+ s2[:2].upper()+'"')

#(b) format()함수를 사용하여 {0}과{1}을 "ni!"와 "spam"으로 지정해주고 원하는 출력값을 출력함 
print('"'+'{0}{1}{0}'.format(s2,s1)+'"')

#(c) capitalize() 함수를 이용해 첫 글자를 대문자로 만들어준 문자열을 a,b로 지정하고 콤마로 띄어써줌 
a = s1.capitalize()
b = s2.capitalize()
print('"'+a,b,a,b,a,b+'"')

#(d) 쌍따옴표를 출력하기 위해 작은따옴표를 사용함 
print('"'+s1+'"')

#(e) split() 함수를 사용해 a를 기준으로 문자열을 'sp','m'으로 나누어 출력함 
print(s1.split('a'))

#(f) 슬라이싱을 이용해 문자열에서 앞 두 글자 'sp'와 뒤 한 글자'm'을 띄어내어 출력함 
print('"'+s1[:2]+s1[-1]+'"')
```
  

## ✏️3번

- 문제  
![문제 이미지-불러오기 실패](/assets/Image/python_assign_02_2_3.png)  

- 답안  

```python
#(a) 문자열이 차례대로 ch에 대입되어 출력하는 것을 반복한 것 같음   
for ch in "aardvark":
    print(ch)

#(b) split함수가 사용되었으므로 문자열이 공백을 기준으로 나누어졌고, 나누어진 문자열이 차례대로 w에 대입되어 출력하는 것을 반복한 것 같음.
for w in "Now is the winter of our discontent...".split():
    print(w)

#(c) i를 기준으로 문자열이 M,ss,ss,pp 로 나뉘었고, 차례대로 w에 대입되어 출력되었으며, 그 끝이 공백이 하나 추가되어 끝남.
#   따라서 end=는 맨 나중에 끝으로 올 문자나 값을 지정하는 역할을 하는 것 같음.
for w in "Mississippi".split("i"):
    print(w,end=" ")

#(d) 문자열을 e를 기준으로 s, cr, t로 나누었고, 그 문자열을 s에 대입하여 msg와 합쳐 저장하는 과정을 반복한 것 같음
    #따라서 처음엔 msg가 아무것도 없으므로 s, 두번째엔 scr이 msg로 저장되고, 마지막으로 scr에 t가 합쳐져 msg로 저장되어 출력됨.
msg = ""
for s in "secret".split("e"):
    msg = msg +s
print(msg)

#(e) 구글링 결과 chr은 숫자를 문자로, ord는 문자를 숫자로 변환시켜주는 함수임. 따라서 secret 문자열에서
#  차례대로 ch에 대입한 후 그것을 숫자로 변환시켜 1을 더하고 다시 문자로 변환시켜 계속 합쳐서 그 결과를 출력함.
msg = ""
for ch in "secret":
    msg = msg + chr(ord(ch)+1)
print(msg)
```  


## ✏️4번

- 문제  
![문제 이미지-불러오기 실패](/assets/Image/python_assign_02_2_4.png)  

- 답안  

```python
#(a) format함수를 사용하여 {0}{1}에 각각 "eggs", "spam" 문자열을 대입함.
print("Looks like {1} and {0} for breakfast".format("eggs","spam"))


#(b) format함수를   차례대로 문자열을 대입함.
print("There is {0} {1} {2} {3}".format(1,"spam",4,"you"))


#(c) format함수를 사용하여 {0}에 해당하는 문자열"Susan"을 대입함. "computewell"은 {1}이므로 사용할 일이 없음.
print("Hello {0}".format("Susan", "Computewell"))


#(d) {0:0.2f}는 2.3을 소수점 둘째자리까지 나타내라는 뜻이므로 출력값이 2.30이 됨. 이때 2.3468은 사용할 일이 없으므로
#   두번째{0:0.2f}대신 {1:0.2f}을 써야함. 따라서 2.3468이 소수점 둘째자리까지 반올림되어 출력이 됨.
print("{0:0.2f} {0:0.2f}".format(2.3,2.3468))

#(e) {7.5f}는 문법오류이므로 앞에 0: 이나 1: 을 써 어떤 숫자열에 해당하는지 입력해야함.
# 따라서 {0:7.5f}, {1:7.5f}로 바꿔쓰면 각각의 숫자열이 전체 일곱자리 소수점 다섯자리까지 이렇게 '2.30000 2.34680'가 출력됨. 
print("{7.5f} {7.5f}".format(2.3,2.3468))

#(f) 출력 결과가 Time left 01:37.37 가 나오는걸 보아 {0:02}는 {0}에 해당하는 값이 1을 전체 두자리로 출력해야하므로 01로출력됨.
# {1}에 해당하는 값인 2를 소수점 두자리까지 포함하여 전체 다섯자리로 출력해야하므로 37.37이 출력됨.
print("Time left {0:02}:{1:05.2f}".format(1, 37.374))

#(g) format함수에 {1}에 해당하는 숫자가 없으므로 오류가 발생함. 따라서 1을 0으로 바꾸어야함.
print("{1:3}".format("14"))
```


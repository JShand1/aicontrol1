# aicontrol1

### 내가 만든 첫 마크다운 파일입니다

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


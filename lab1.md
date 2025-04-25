https://github.com/nurcan06/lab1/blob/main/lab1

import math as m
a=(m.log(5,2)*(5**1/2)-(5**1/3)*m.log(5,3))
b=m.exp(-2)*m.acos(1/2*m.cos(-4/7))
if a*b<0.1:
    print(abs(a*b)**1/2)
else:
    print(abs(a+b)**1/2)


-----------------------------------------------------
import math as m

# Verilmiş ifadələrin hesablanması
a = (m.log(5,2) * (5**(1/2)) - (5**(1/3)) * m.log(5,3))
b = m.exp(-2) * m.acos((1/2) * m.cos(-4/7))

# Şərtin yoxlanması və nəticənin hesablanması
if a * b < 0.1:
    result = abs(a * b) ** (1/2)
else:
    result = abs(a + b) ** (1/2)

result



                                                    lab 2



                                                    🥇 1-ci Funksiya
Funksiya:
𝑥
∈
[
0
;
5
]
x∈[0;5], 
Δ
𝑥
=
0.5
Δx=0.5

𝑦
=
{
𝑎
+
𝑏
𝑥
,
𝑥
≥
1
2
𝑎
−
3
𝑏
,
𝑥
<
1
y={ 
a+bx,
2a−3b,
​
  
x≥1
x<1
​
 
Algoritm:
Başla

x = 0 təyin et

x <= 5 olana qədər:

Əgər 
𝑥
≥
1
x≥1 → 
𝑦
=
𝑎
+
𝑏
𝑥
y=a+bx

Əgər 
𝑥
<
1
x<1 → 
𝑦
=
2
𝑎
−
3
𝑏
y=2a−3b

x = x + 0.5 artır

Bitir

Python kodu:
python
Copy
Edit
import numpy as np
import matplotlib.pyplot as plt

a = 2  # istədiyin qiymətləri verə bilərsən
b = 3

x = np.arange(0, 5.5, 0.5)
y = []

for xi in x:
    if xi >= 1:
        yi = a + b * xi
    else:
        yi = 2 * a - 3 * b
    y.append(yi)

plt.plot(x, y, marker='o')
plt.title('1-ci Funksiya')
plt.xlabel('x')
plt.ylabel('y')
plt.grid()
plt.show()
🥈 2-ci Funksiya
Funksiya:
𝑥
∈
[
−
1
;
6
]
x∈[−1;6], 
Δ
𝑥
=
1
Δx=1

𝑦
=
{
6
𝑥
2
+
1
,
𝑥
=
2
8
𝑥
−
3
,
𝑥
>
2
4
𝑥
+
8
,
𝑥
<
2
y= 
⎩
⎨
⎧
​
  
6x 
2
 +1,
8x−3,
4x+8,
​
  
x=2
x>2
x<2
​
 
Algoritm:
Başla

x = -1 təyin et

x <= 6 olana qədər:

Əgər 
𝑥
=
2
x=2 → 
𝑦
=
6
𝑥
2
+
1
y=6x 
2
 +1

Əgər 
𝑥
>
2
x>2 → 
𝑦
=
8
𝑥
−
3
y=8x−3

Əgər 
𝑥
<
2
x<2 → 
𝑦
=
4
𝑥
+
8
y=4x+8

x = x + 1 artır

Bitir

Python kodu:
python
Copy
Edit
x = np.arange(-1, 7, 1)
y = []

for xi in x:
    if xi == 2:
        yi = 6 * xi**2 + 1
    elif xi > 2:
        yi = 8 * xi - 3
    else:
        yi = 4 * xi + 8
    y.append(yi)

plt.plot(x, y, marker='o', color='green')
plt.title('2-ci Funksiya')
plt.xlabel('x')
plt.ylabel('y')
plt.grid()
plt.show()
🥉 3-cü Funksiya
Funksiya:
𝑥
∈
[
1
;
7
]
x∈[1;7], 
Δ
𝑥
=
0.5
Δx=0.5

𝑦
=
{
𝑎
𝑥
2
+
𝑏
𝑥
+
𝑐
,
𝑥
<
3
2
𝑥
+
𝑐
𝑥
+
𝑏
,
𝑥
=
3
3
𝑥
2
−
𝑥
−
1
,
𝑥
>
3
y= 
⎩
⎨
⎧
​
  
ax 
2
 +bx+c,
2x+cx+b,
3x 
2
 −x−1,
​
  
x<3
x=3
x>3
​
 
Algoritm:
Başla

x = 1 təyin et

x <= 7 olana qədər:

Əgər 
𝑥
<
3
x<3 → 
𝑦
=
𝑎
𝑥
2
+
𝑏
𝑥
+
𝑐
y=ax 
2
 +bx+c

Əgər 
𝑥
=
3
x=3 → 
𝑦
=
2
𝑥
+
𝑐
𝑥
+
𝑏
y=2x+cx+b

Əgər 
𝑥
>
3
x>3 → 
𝑦
=
3
𝑥
2
−
𝑥
−
1
y=3x 
2
 −x−1

x = x + 0.5 artır

Bitir

Python kodu:
python
Copy
Edit
a = 1
b = 2
c = 3

x = np.arange(1, 7.5, 0.5)
y = []

for xi in x:
    if xi < 3:
        yi = a * xi**2 + b * xi + c
    elif xi == 3:
        yi = 2 * xi + c * xi + b
    else:
        yi = 3 * xi**2 - xi - 1
    y.append(yi)

plt.plot(x, y, marker='o', color='red')
plt.title('3-cü Funksiya')
plt.xlabel('x')
plt.ylabel('y')
plt.grid()
plt.show()
🏅 4-cü Funksiya
Funksiya:
𝑥
∈
[
1
;
4
]
x∈[1;4], 
Δ
𝑥
=
0.5
Δx=0.5

𝑦
=
{
2
𝑎
2
+
𝑏
𝑥
,
𝑥
≤
2
3
𝑎
−
2
𝑏
,
𝑥
>
2
y={ 
2a 
2
 +bx,
3a−2b,
​
  
x≤2
x>2
​
 
Algoritm:
Başla

x = 1 təyin et

x <= 4 olana qədər:

Əgər 
𝑥
≤
2
x≤2 → 
𝑦
=
2
𝑎
2
+
𝑏
𝑥
y=2a 
2
 +bx

Əgər 
𝑥
>
2
x>2 → 
𝑦
=
3
𝑎
−
2
𝑏
y=3a−2b

x = x + 0.5 artır

Bitir

Python kodu:
python
Copy
Edit
a = 2
b = 3

x = np.arange(1, 4.5, 0.5)
y = []

for xi in x:
    if xi <= 2:
        yi = 2 * a**2 + b * xi
    else:
        yi = 3 * a - 2 * b
    y.append(yi)

plt.plot(x, y, marker='o', color='purple')
plt.title('4-cü Funksiya')
plt.xlabel('x')
plt.ylabel('y')
plt.grid()
plt.show()
🏆 5-ci Funksiya
Funksiya:
𝑥
∈
[
1
;
4
]
x∈[1;4], 
Δ
𝑥
=
0.5
Δx=0.5

𝑦
=
{
9
𝑥
2
+
3
,
𝑥
=
2
8
𝑥
+
5
,
𝑥
<
2
3
𝑥
−
2
,
𝑥
>
2
y= 
⎩
⎨
⎧
​
  
9x 
2
 +3,
8x+5,
3x−2,
​
  
x=2
x<2
x>2
​
 
Algoritm:
Başla

x = 1 təyin et

x <= 4 olana qədər:

Əgər 
𝑥
=
2
x=2 → 
𝑦
=
9
𝑥
2
+
3
y=9x 
2
 +3

Əgər 
𝑥
<
2
x<2 → 
𝑦
=
8
𝑥
+
5
y=8x+5

Əgər 
𝑥
>
2
x>2 → 
𝑦
=
3
𝑥
−
2
y=3x−2

x = x + 0.5 artır

Bitir

Python kodu:
python
Copy
Edit
x = np.arange(1, 4.5, 0.5)
y = []

for xi in x:
    if xi == 2:
        yi = 9 * xi**2 + 3
    elif xi < 2:
        yi = 8 * xi + 5
    else:
        yi = 3 * xi - 2
    y.append(yi)

plt.plot(x, y, marker='o', color='orange')
plt.title('5-ci Funksiya')
plt.xlabel('x')
plt.ylabel('y')
plt.grid()
plt.show()

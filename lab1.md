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

                                                           lab 3

                                                           🥇 1-ci Tapşırıq
Verilmiş:
𝑆
=
1
+
1
2
+
1
3
+
1
4
+
⋯
S=1+ 
2
1
​
 + 
3
1
​
 + 
4
1
​
 +⋯
𝜀
=
0.01
ε=0.01
Algoritm:
Başla

𝑆
=
1
S=1, 
𝑖
=
2
i=2

Əlavə
=
1
𝑖
Əlavə= 
i
1
​
 

Əlavəni 
𝑆
S-ə əlavə et

Əgər 
Əlavə
≥
𝜀
Əlavə≥ε, onda 
𝑖
=
𝑖
+
1
i=i+1 və 3-cü addıma qayıt

Bitir

Python Kodu:
python
Copy
Edit
epsilon = 0.01
S = 1
i = 2

while True:
    term = 1 / i
    if term < epsilon:
        break
    S += term
    i += 1

print(f"S = {S}")
Qrafik:
python
Copy
Edit
import matplotlib.pyplot as plt

epsilon = 0.01
S = 1
i = 2

terms = [S]

while True:
    term = 1 / i
    if term < epsilon:
        break
    S += term
    terms.append(S)
    i += 1

plt.plot(range(1, len(terms)+1), terms, marker='o')
plt.title('1-ci Tapşırıq üçün S cəmi')
plt.xlabel('İterasiya')
plt.ylabel('Cəm S')
plt.grid()
plt.show()
🥈 2-ci Tapşırıq
Verilmiş:
𝑃
=
𝑥
−
𝑥
2
2
+
𝑥
3
3
−
𝑥
4
4
+
⋯
P=x− 
2
x 
2
 
​
 + 
3
x 
3
 
​
 − 
4
x 
4
 
​
 +⋯
𝑥
=
0.5
,
𝜀
=
0.01
x=0.5,ε=0.01
Algoritm:
Başla

𝑃
=
𝑥
P=x, 
𝑖
=
2
i=2

Əlavə
=
(
−
1
)
𝑖
+
1
⋅
𝑥
𝑖
𝑖
Əlavə=(−1) 
i+1
 ⋅ 
i
x 
i
 
​
 

Əlavəni 
𝑃
P-yə əlavə et

Əgər 
∣
Əlavə
∣
≥
𝜀
∣Əlavə∣≥ε, onda 
𝑖
=
𝑖
+
1
i=i+1 və 3-cü addıma qayıt

Bitir

Python Kodu:
python
Copy
Edit
x = 0.5
epsilon = 0.01
P = x
i = 2

while True:
    term = (-1)**(i+1) * (x**i) / i
    if abs(term) < epsilon:
        break
    P += term
    i += 1

print(f"P = {P}")
Qrafik:
python
Copy
Edit
x = 0.5
epsilon = 0.01
P = x
i = 2

terms = [P]

while True:
    term = (-1)**(i+1) * (x**i) / i
    if abs(term) < epsilon:
        break
    P += term
    terms.append(P)
    i += 1

plt.plot(range(1, len(terms)+1), terms, marker='o', color='green')
plt.title('2-ci Tapşırıq üçün P cəmi')
plt.xlabel('İterasiya')
plt.ylabel('Cəm P')
plt.grid()
plt.show()
🥉 3-cü Tapşırıq
Verilmiş:
𝑃
=
−
𝑥
−
𝑥
2
2
−
𝑥
3
3
−
𝑥
4
4
−
⋯
P=−x− 
2
x 
2
 
​
 − 
3
x 
3
 
​
 − 
4
x 
4
 
​
 −⋯
𝑥
=
0.7
,
𝜀
=
0.01
x=0.7,ε=0.01
Algoritm:
Başla

𝑃
=
−
𝑥
P=−x, 
𝑖
=
2
i=2

Əlavə
=
−
𝑥
𝑖
𝑖
Əlavə=− 
i
x 
i
 
​
 

Əlavəni 
𝑃
P-yə əlavə et

Əgər 
∣
Əlavə
∣
≥
𝜀
∣Əlavə∣≥ε, onda 
𝑖
=
𝑖
+
1
i=i+1 və 3-cü addıma qayıt

Bitir

Python Kodu:
python
Copy
Edit
x = 0.7
epsilon = 0.01
P = -x
i = 2

while True:
    term = -(x**i) / i
    if abs(term) < epsilon:
        break
    P += term
    i += 1

print(f"P = {P}")
Qrafik:
python
Copy
Edit
x = 0.7
epsilon = 0.01
P = -x
i = 2

terms = [P]

while True:
    term = -(x**i) / i
    if abs(term) < epsilon:
        break
    P += term
    terms.append(P)
    i += 1

plt.plot(range(1, len(terms)+1), terms, marker='o', color='red')
plt.title('3-cü Tapşırıq üçün P cəmi')
plt.xlabel('İterasiya')
plt.ylabel('Cəm P')
plt.grid()
plt.show()
🏅 4-cü Tapşırıq
Verilmiş:
𝑆
=
sin
⁡
𝑥
1
+
sin
⁡
2
𝑥
2
+
sin
⁡
3
𝑥
3
+
⋯
S= 
1
sinx
​
 + 
2
sin 
2
 x
​
 + 
3
sin 
3
 x
​
 +⋯
𝑥
=
0.9
,
𝜀
=
0.001
x=0.9,ε=0.001
Algoritm:
Başla

\sinx
=
sin
⁡
(
𝑥
)
\sinx=sin(x)

𝑆
=
sin
⁡
𝑥
1
S= 
1
sinx
​
 , 
𝑖
=
2
i=2

Əlavə
=
sin
⁡
𝑖
(
𝑥
)
𝑖
Əlavə= 
i
sin 
i
 (x)
​
 

Əlavəni 
𝑆
S-ə əlavə et

Əgər 
∣
Əlavə
∣
≥
𝜀
∣Əlavə∣≥ε, onda 
𝑖
=
𝑖
+
1
i=i+1 və 4-cü addıma qayıt

Bitir

Python Kodu:
python
Copy
Edit
import math

x = 0.9
epsilon = 0.001
sinx = math.sin(x)
S = sinx
i = 2

while True:
    term = sinx**i / i
    if abs(term) < epsilon:
        break
    S += term
    i += 1

print(f"S = {S}")
Qrafik:
python
Copy
Edit
import math
import matplotlib.pyplot as plt

x = 0.9
epsilon = 0.001
sinx = math.sin(x)
S = sinx
i = 2

terms = [S]

while True:
    term = sinx**i / i
    if abs(term) < epsilon:
        break
    S += term
    terms.append(S)
    i += 1

plt.plot(range(1, len(terms)+1), terms, marker='o', color='purple')
plt.title('4-cü Tapşırıq üçün S cəmi')
plt.xlabel('İterasiya')
plt.ylabel('Cəm S')
plt.grid()
plt.show()
🏆 5-ci Tapşırıq
Verilmiş:
𝑆
=
1
+
1
4
+
1
9
+
1
16
+
⋯
S=1+ 
4
1
​
 + 
9
1
​
 + 
16
1
​
 +⋯
𝜀
=
0.001
ε=0.001
Algoritm:
Başla

𝑆
=
1
S=1, 
𝑖
=
2
i=2

Əlavə
=
1
𝑖
2
Əlavə= 
i 
2
 
1
​
 

Əlavəni 
𝑆
S-ə əlavə et

Əgər 
Əlavə
≥
𝜀
Əlavə≥ε, onda 
𝑖
=
𝑖
+
1
i=i+1 və 3-cü addıma qayıt

Bitir

Python Kodu:
python
Copy
Edit
epsilon = 0.001
S = 1
i = 2

while True:
    term = 1 / i**2
    if term < epsilon:
        break
    S += term
    i += 1

print(f"S = {S}")
Qrafik:
python
Copy
Edit
import matplotlib.pyplot as plt

epsilon = 0.001
S = 1
i = 2

terms = [S]

while True:
    term = 1 / i**2
    if term < epsilon:
        break
    S += term
    terms.append(S)
    i += 1

plt.plot(range(1, len(terms)+1), terms, marker='o', color='orange')
plt.title('5-ci Tapşırıq üçün S cəmi')
plt.xlabel('İterasiya')
plt.ylabel('Cəm S')
plt.grid()
plt.show()

plt.plot(x, y, marker='o', color='orange')
plt.title('5-ci Funksiya')
plt.xlabel('x')
plt.ylabel('y')
plt.grid()
plt.show()

 
                                                                   lab 4

                                                                   1) [0;1] intervalında təsadüfi həqiqi ədədlərdən ibarət siyahı:
python
Copy
Edit
from random import random

n = 10
a = [0] * n

for i in range(n):
    a[i] = random()  # [0;1) intervalında

print(a)
2) [1;5] intervalında təsadüfi həqiqi ədədlərdən ibarət siyahı:
python
Copy
Edit
from random import uniform

n = 10
a = [0] * n

for i in range(n):
    a[i] = uniform(1, 5)  # [1;5] intervalında

print(a)
3) [0;7] intervalında təsadüfi tam ədədlərdən ibarət siyahı:
python
Copy
Edit
from random import randint

n = 10
a = [0] * n

for i in range(n):
    a[i] = randint(0, 7)  # [0;7] intervalında tam ədədlər

print(a)
4) [7;25] intervalında təsadüfi həqiqi ədədlərdən ibarət siyahı:
python
Copy
Edit
from random import uniform

n = 10
a = [0] * n

for i in range(n):
    a[i] = uniform(7, 25)  # [7;25] intervalında həqiqi ədədlər

print(a)
5) [0;25] intervalında təsadüfi həqiqi ədədlərdən ibarət siyahı:
python
Copy
Edit
from random import uniform

n = 10
a = [0] * n

for i in range(n):
    a[i] = uniform(0, 25)  # [0;25] intervalında həqiqi ədədlər

print(a)


                    LAb 5 



                    1. [0;1) intervalında dəyişən n sayda təsadüfi həqiqi ədəddən ibarət siyahının (massivin) elementlərinin cəmini hesablayan alqoritm:

funksiya siyahıElementlərininCəminiHesabla(siyahı):
  cəm = 0
  üçün hər bir element siyahıda:
    cəm = cəm + element
  return cəm
2. [0;7) intervalında dəyişən n sayda təsadüfi həqiqi ədəddən ibarət siyahının (massivin) elementlərinin hasilini hesablayan alqoritm:

funksiya siyahıElementlərininHasiliniHesabla(siyahı):
  hasil = 1
  üçün hər bir element siyahıda:
    hasil = hasil * element
  return hasil
3. C(n) ədədi massivinin (siyahısının) müsbət elementlərinin cəmini hesablayan alqoritm:

funksiya müsbətElementlərinCəminiHesabla(siyahı):
  cəm = 0
  üçün hər bir element siyahıda:
    əgər element > 0 onda:
      cəm = cəm + element
  return cəm
4. A(n) ədədi massivinin (siyahısının) müsbət elementlərinin hasilini hesablayan alqoritm:

funksiya müsbətElementlərinHasiliniHesabla(siyahı):
  hasil = 1
  üçün hər bir element siyahıda:
    əgər element > 0 onda:
      hasil = hasil * element
  return hasil
5. B(n) ədədi massivinin (siyahısının) mənfi elementlərinin cəmini hesablayan alqoritm:

funksiya mənfiElementlərinCəminiHesabla(siyahı):
  cəm = 0
  üçün hər bir element siyahıda:
    əgər element < 0 onda:
      cəm = cəm + element
  return cəm
6. [−3;10) intervalında dəyişən n sayda təsadüfi tam ədəddən ibarət siyahının (massivin) birinci mənfi elementindən əvvəlki elementlərinin ədədi ortasını hesablayan alqoritm:

funksiya birinciMənfidənƏvvəlkiElementlərinOrtasınıHesabla(siyahı):
  cəm = 0
  say = 0
  üçün hər bir element siyahıda:
    əgər element < 0 onda:
      qır döngüdən
    cəm = cəm + element
    say = say + 1

  əgər say > 0 onda:
    orta = cəm / say
  başqa:
    orta = 0
  return orta
Bu alqoritmlər verilən tələblərə uyğun olaraq siyahılardakı elementlərlə müxtəlif əməliyyatları yerinə yetirir. Hər bir alqoritm funksiya şəklində təqdim olunmuşdur ki, bu da onların istifadəsini asanlaşdırır.


                       lab 6 



                       Gəlin bu laboratoriya işindəki tapşırıqların alqoritmlərini tərtib edək. Hər bir tapşırıq üçün alqoritmi sadə və anlaşıqlı şəkildə izah edəcəyəm.

Qeyd: Nümunələrdə Python sintaksisinə yaxın psevdokoddan istifadə olunacaq.

Tapşırıq 1: İki ölçülü A(n,m) ədədi massivinin bütün elementlərinin cəmini hesablayan alqoritm.

funksiya bütünElementlərinCəminiHesabla(A, n, m):
  ümumi_cəm = 0
  üçün i 0-dan n-1-ə qədər:
    üçün j 0-dan m-1-ə qədər:
      ümumi_cəm = ümumi_cəm + A[i][j]
  return ümumi_cəm
Tapşırıq 2: İki ölçülü A(n,m) ədədi massivinin hər bir sətrindəki elementlərinin cəmini hesablayan alqoritm.

funksiya hərSətrinCəminiHesabla(A, n, m):
  sətr_cəmləri = []
  üçün i 0-dan n-1-ə qədər:
    sətr_cəmi = 0
    üçün j 0-dan m-1-ə qədər:
      sətr_cəmi = sətr_cəmi + A[i][j]
    sətr_cəmləri.əlavəEt(sətr_cəmi)
  return sətr_cəmləri
Tapşırıq 3: İki ölçülü A(n,n) ədədi massivinin baş dioqanaldan yuxarıda yerləşən müsbət elementlərinin cəmini hesablayan alqoritm.

funksiya başDioqonaldanYuxarıMüsbətlərinCəminiHesabla(A, n):
  cəm = 0
  üçün i 0-dan n-1-ə qədər:
    üçün j i+1-dən n-1-ə qədər:
      əgər A[i][j] > 0 onda:
        cəm = cəm + A[i][j]
  return cəm
Tapşırıq 4: İki ölçülü A(n,n) ədədi massivinin baş dioqonalda yerləşən elementlərinin kvadratları cəmini hesablayan alqoritm.

funksiya başDioqonalKvadratlarıCəminiHesabla(A, n):
  cəm = 0
  üçün i 0-dan n-1-ə qədər:
    cəm = cəm + A[i][i] * A[i][i]
  return cəm
Tapşırıq 5: İki ölçülü A(n,n) ədədi massivinin baş dioqonalda yerləşən elementlərinin kvadrat kökləri cəmini hesablayan alqoritm.

funksiya başDioqonalKvadratKökləriCəminiHesabla(A, n):
  cəm = 0
  üçün i 0-dan n-1-ə qədər:
    əgər A[i][i] >= 0 onda:
      cəm = cəm + sqrt(A[i][i])
  return cəm
Qeyd: sqrt() kvadrat kök funksiyasını təmsil edir.

Tapşırıq 6: İki ölçülü A(n,m) ədədi massivinin hər bir sütunundakı elementlərinin hasilini hesablayan alqoritm.

funksiya hərSütununHasiliniHesabla(A, n, m):
  sütun_hasilləri = []
  üçün j 0-dan m-1-ə qədər:
    sütun_hasili = 1
    üçün i 0-dan n-1-ə qədər:
      sütun_hasili = sütun_hasili * A[i][j]
    sütun_hasilləri.əlavəEt(sütun_hasili)
  return sütun_hasilləri
Tapşırıq 7: İki ölçülü A(n,m) ədədi massivinin hər bir cüt sətrindəki elementlərinin cəmini hesablayan alqoritm.

funksiya cütSətirlərinCəminiHesabla(A, n, m):
  cüt_sətr_cəmləri = []
  üçün i 0-dan n-1-ə qədər addım 2 ilə:
    sətr_cəmi = 0
    üçün j 0-dan m-1-ə qədər:
      sətr_cəmi = sətr_cəmi + A[i][j]
    cüt_sətr_cəmləri.əlavəEt(sətr_cəmi)
  return cüt_sətr_cəmləri
Tapşırıq 8: İki ölçülü A(n,m) ədədi massivinin hər bir tək sütunundakı elementlərinin kvadrat köklərinin cəmini hesablayan alqoritm.

funksiya təkSütunKvadratKökləriCəminiHesabla(A, n, m):
  tək_sütun_kvadrat_kökləri_cəmləri = []
  üçün j 1-dən m-1-ə qədər addım 2 ilə:
    sütun_kvadrat_kökləri_cəmi = 0
    üçün i 0-dan n-1-ə qədər:
      əgər A[i][j] >= 0 onda:
        sütun_kvadrat_kökləri_cəmi = sütun_kvadrat_kökləri_cəmi + sqrt(A[i][j])
    tək_sütun_kvadrat_kökləri_cəmləri.əlavəEt(sütun_kvadrat_kökləri_cəmi)
  return tək_sütun_kvadrat_kökləri_cəmləri
Tapşırıq 9: İki ölçülü A(n,m) ədədi massivinin hər bir tək sətrindəki elementlərinin hasilini hesablayan alqoritm.

funksiya təkSətirlərinHasiliniHesabla(A, n, m):
  tək_sətr_hasilləri = []
  üçün i 1-dən n-1-ə qədər addım 2 ilə:
    sətr_hasili = 1
    üçün j 0-dan m-1-ə qədər:
      sətr_hasili = sətr_hasili * A[i][j]
    tək_sətr_hasilləri.əlavəEt(sətr_hasili)
  return tək_sətr_hasilləri
Tapşırıq 10: İki ölçülü A(n,m) ədədi massivində elementləri cəmi mənfi olan sütunun nömrəsini təyin etməli.

funksiya mənfiCəmliSütunNömrəsiniTəyinEt(A, n, m):
  üçün j 0-dan m-1-ə qədər:
    sütun_cəmi = 0
    üçün i 0-dan n-1-ə qədər:
      sütun_cəmi = sütun_cəmi + A[i][j]
    əgər sütun_cəmi < 0 onda:
      return j + 1  // Sütun nömrəsi 1-dən başlayır
  return -1 // Əgər mənfi cəmli sütun tapılmazsa
Tapşırıq 11: x dəyişəni iki ölçülü X(n,m) ədədi massivinin elementi olduğunu nəzərə alaraq, hər bir element üçün y=sin(x) funksiyasının qiymətini hesablayan alqoritm.

funksiya sinusuHesabla(X, n, m):
  Y = yeni n x m ölçülü massiv
  üçün i 0-dan n-1-ə qədər:
    üçün j 0-dan m-1-ə qədər:
      Y[i][j] = sin(X[i][j])
  return Y
Qeyd: sin() sinus funksiyasını təmsil edir.

Tapşırıq 12: İki ölçülü A(n,n) ədədi massivinin baş dioqonal elementlərinin cəmini hesablayan alqoritm.

funksiya başDioqonalElementlərininCəminiHesabla(A, n):
  cəm = 0
  üçün i 0-dan n-1-ə qədər:
    cəm = cəm + A[i][i]
  return cəm
Tapşırıq 13: İki ölçülü A(n,m) ədədi massivinin hər bir tək sətrindəki elementlərinin kvadratları cəmini hesablayan alqoritm.

funksiya təkSətirlərinKvadratlarıCəminiHesabla(A, n, m):
  tək_sətr_kvadrat_cəmləri = []
  üçün i 1-dən n-1-ə qədər addım 2 ilə:
    sətr_kvadrat_cəmi = 0
    üçün j 0-dan m-1-ə qədər:
      sətr_kvadrat_cəmi = sətr_kvadrat_cəmi + A[i][j] * A[i][j]
    tək_sətr_kvadrat_cəmləri.əlavəEt(sətr_kvadrat_cəmi)
  return tək_sətr_kvadrat_cəmləri
Tapşırıq 14: İki ölçülü A(n,n) ədədi massivinin baş dioqonalda yerləşən elementlərinin həndəsi ortasını hesablayan alqoritm.

funksiya başDioqonalHəndəsiOrtasınıHesabla(A, n):
  hasil = 1
  say = 0
  üçün i 0-dan n-1-ə qədər:
    hasil = hasil * A[i][i]
    say = say + 1
  əgər say > 0 onda:
    həndəsi_orta = hasil ** (1/say)
  başqa:
    həndəsi_orta = 0
  return həndəsi_orta
Tapşırıq 15: İki ölçülü A(n,m) ədədi massivinin hər bir sütunundakı mənfi elementlərinin hasilini hesablayan alqoritm.

funksiya hərSütununMənfiElementləriHasiliniHesabla(A, n, m):
  sütun_mənfi_hasilləri = []
  üçün j 0-dan m-1-ə qədər:
    sütun_mənfi_hasili = 1
    mənfi_element_var = yalan
    üçün i 0-dan n-1-ə qədər:
      əgər A[i][j] < 0 onda:
        sütun_mənfi_hasili = sütun_mənfi_hasili * A[i][j]
        mənfi_element_var = doğru
    əgər mənfi_element_var onda:
      sütun_mənfi_hasilləri.əlavəEt(sütun_mənfi_hasili)
    başqa:
      sütun_mənfi_hasilləri.əlavəEt(1) // Mənfi element yoxdursa, hasil 1 olur
  return sütun_mənfi_hasilləri
Tapşırıq 16: İki ölçülü A(n,n) ədədi massivinin baş dioqonaldan aşağıda yerləşən elementlərinin hasilini hesablayan alqoritm.

funksiya başDioqonaldanAşağıElementlərinHasiliniHesabla(A, n):
  hasil = 1
  üçün i 1-dən n-1-ə qədər:
    üçün j 0-dan i-1-ə qədər:
      hasil = hasil * A[i][j]
  return hasil
Tapşırıq 17: İki ölçülü A(n,m) ədədi massivindən bir ölçülü B massivi qurmalı. Beləki, B massivinin hər bir elementi A massivinin uyğun sütun elementləri cəminə bərabərdir.

funksiya sütunCəmlərindənBirÖlçülüMassivQur(A, n, m):
  B = yeni m ölçülü massiv
  üçün j 0-dan m-1-ə qədər:
    sütun_cəmi = 0
    üçün i 0-dan n-1-ə qədər:
      sütun_cəmi = sütun_cəmi + A[i][j]
    B[j] = sütun_cəmi
  return B
Tapşırıq 18: İki ölçülü A(n,m) ədədi massivində elementləri cəmi mənfi olan sətrin nömrəsini təyin etməli.

funksiya mənfiCəmliSətrNömrəsiniTəyinEt(A, n, m):
  üçün i 0-dan n-1-ə qədər:
    sətr_cəmi = 0
    üçün j 0-dan m-1-ə qədər:
      sətr_cəmi = sətr_cəmi + A[i][j]
    əgər sətr_cəmi < 0 onda:
      return i + 1 // Sətr nömrəsi 1-dən başlayır
  return -1 // Əgər mənfi cəmli sətr tapılmazsa
Tapşırıq 19: İki ölçülü A(n,n) ədədi massivin mənfi elementlərinin yerinə sıfırlar yazıb, matrisi qəbul olunmuş formada çap edin.

funksiya mənfiləriSıfırla(A, n):
  üçün i 0-dan n-1-ə qədər:
    üçün j 0-dan n-1-ə qədər:
      əgər A[i][j] < 0 onda:
        A[i][j] = 0
  çapEtMassivi(A, n, n) // Massivi çap edən funksiya
funksiya çapEtMassivi(massiv, n, m):
  üçün i 0-dan n-1-ə qədər:
    üçün j 0-dan m-1-ə qədər:
      çap et(massiv[i][j], boşluqla ayıraraq)
    yeni sətir çap et
Tapşırıq 20: Elementləri tam ədədlər olan iki ölçülü A(n,n) ədədi massivinin hər sətrindəki 3-ə bölünən elementlərin cəmini həmin sətrdəki baş diaqonal elementi ilə əvəz edin. Matrisi qəbul olunmuş formada çap edin.

funksiya üçəBölünənlərinCəminiDioqonalaYaz(A, n):
  üçün i 0-dan n-1-ə qədər:
    cəm_3ə_bölünənlər = 0
    üçün j 0-dan n-1-ə qədər:
      əgər A[i][j] % 3 == 0 onda:
        cəm_3ə_bölünənlər = cəm_3ə_bölünənlər + A[i][j]
    A[i][i] = cəm_3ə_bölünənlər
  çapEtMassivi(A, n, n)

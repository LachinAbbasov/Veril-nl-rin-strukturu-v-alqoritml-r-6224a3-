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


                                                   lab 7

                                                   Laboratoriya işi № 7-də verilən tapşırıqların alqoritmlərini təqdim edirəm. Hər bir tapşırıq üçün alqoritmi sadə və anlaşıqlı şəkildə izah edəcəyəm.

**Qeyd:** Nümunələrdə Python sintaksisinə yaxın psevdokoddan istifadə olunacaq.

**Tapşırıq 1: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək cüt ədədləri yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya cutEdedleriFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, cüt ədədləri tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  cüt_ədədlərin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  üçün ədəd simvol ədədlərdə:
    ədəd = tam_ədədə_çevir(ədəd_simvol)
    əgər ədəd % 2 == 0 onda:
      faylı_yaz(çıxış_faylı, ədəd + " ")
      cüt_ədədlərin_cəmi = cüt_ədədlərin_cəmi + ədəd
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return cüt_ədədlərin_cəmi
```

**Tapşırıq 2: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək tək ədədləri yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya tekEdedleriFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, tək ədədləri tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  tək_ədədlərin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  üçün ədəd simvol ədədlərdə:
    ədəd = tam_ədədə_çevir(ədəd_simvol)
    əgər ədəd % 2 != 0 onda:
      faylı_yaz(çıxış_faylı, ədəd + " ")
      tək_ədədlərin_cəmi = tək_ədədlərin_cəmi + ədəd
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return tək_ədədlərin_cəmi
```

**Tapşırıq 3: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək cüt nömrəsi olan ədədləri yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya cutNomreliEdedleriFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, cüt indeksli ədədləri tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  cüt_indeksli_ədədlərin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  üçün indeks, ədəd_simvol enumerate(ədədlər):
    əgər indeks % 2 == 0 onda:
      ədəd = tam_ədədə_çevir(ədəd_simvol)
      faylı_yaz(çıxış_faylı, ədəd + " ")
      cüt_indeksli_ədədlərin_cəmi = cüt_indeksli_ədədlərin_cəmi + ədəd
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return cüt_indeksli_ədədlərin_cəmi
```

**Tapşırıq 4: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək tək nömrəsi olan ədədləri yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya tekNomreliEdedleriFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, tək indeksli ədədləri tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  tək_indeksli_ədədlərin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  üçün indeks, ədəd_simvol enumerate(ədədlər):
    əgər indeks % 2 != 0 onda:
      ədəd = tam_ədədə_çevir(ədəd_simvol)
      faylı_yaz(çıxış_faylı, ədəd + " ")
      tək_indeksli_ədədlərin_cəmi = tək_indeksli_ədədlərin_cəmi + ədəd
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return tək_indeksli_ədədlərin_cəmi
```

**Tapşırıq 5: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək ilk 5 ədədi yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya ilkBesEdediFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, ilk 5 ədədi tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  ilk_beş_ədədin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  sayğac = 0
  üçün ədəd_simvol ədədlərdə:
    əgər sayğac < 5 onda:
      ədəd = tam_ədədə_çevir(ədəd_simvol)
      faylı_yaz(çıxış_faylı, ədəd + " ")
      ilk_beş_ədədin_cəmi = ilk_beş_ədədin_cəmi + ədəd
      sayğac = sayğac + 1
    başqa:
      qır döngüdən
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return ilk_beş_ədədin_cəmi
```

**Tapşırıq 6: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək son 3 ədədi yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya sonUcEdediFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, son 3 ədədi tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  son_üç_ədədin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  başlanğıc_indeks = uzunluq(ədədlər) - 3
  əgər başlanğıc_indeks < 0 onda:
    başlanğıc_indeks = 0
  üçün i başlanğıc_indeksdən uzunluq(ədədlər)-1-ə qədər:
    ədəd = tam_ədədə_çevir(ədədlər[i])
    faylı_yaz(çıxış_faylı, ədəd + " ")
    son_üç_ədədin_cəmi = son_üç_ədədin_cəmi + ədəd
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return son_üç_ədədin_cəmi
```

**Tapşırıq 7: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək 4<X<12 şərtinə uyğun ədədləri yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya aralıqdakıEdedleriFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, 4<ədəd<12 şərtinə uyğun ədədləri tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  şərtə_uyğun_ədədlərin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  üçün ədəd_simvol ədədlərdə:
    ədəd = tam_ədədə_çevir(ədəd_simvol)
    əgər ədəd > 4 və ədəd < 12 onda:
      faylı_yaz(çıxış_faylı, ədəd + " ")
      şərtə_uyğun_ədədlərin_cəmi = şərtə_uyğun_ədədlərin_cəmi + ədəd
  faylı_bağla(giriş_faylı)
  faylı_bağla(çıxış_faylı)
  return şərtə_uyğun_ədədlərin_cəmi
```

**Tapşırıq 8: Ədədi massiv əsasında fayl yaradın. Faylı daxil edərək X<12 şərtinə uyğun ədədləri yeni fayla yazın və əlavə olaraq onların cəmini hesablayın.**

```
funksiya onİkidənKiçikEdedleriFaylaYazCeminiHesabla(massiv, giriş_fayl_adı, çıxış_fayl_adı):
  # Massivi giriş faylına yaz
  giriş_faylı = faylı_aç(giriş_fayl_adı, "w")
  üçün element massivdə:
    faylı_yaz(giriş_faylı, element + " ")
  faylı_bağla(giriş_faylı)

  # Giriş faylından oxu, ədəd<12 şərtinə uyğun ədədləri tap, yeni fayla yaz və cəmini hesabla
  çıxış_faylı = faylı_aç(çıxış_fayl_adı, "w")
  şərtə_uyğun_ədədlərin_cəmi = 0
  giriş_faylı = faylı_aç(giriş_fayl_adı, "r")
  ədədlər_sətiri = faylı_oxu(giriş_faylı)
  ədədlər = ədədlər_sətiri.split()
  üçün ədəd_simvol ədədlərdə:
    ədəd = tam_ədədə_



                                                      lab 8

  Laboratoriya işi № 8-də verilən tapşırıqların alqoritmlərini təqdim edirəm. Hər bir tapşırıq üçün alqoritmi parçanı yarıya bölmə üsuluna əsasən tərtib edəcəyəm. Alqoritmlərdə f(x) verilmiş tənliyi, [a, b] isə axtarılan kökün yerləşdiyi intervalı bildirir. Təqribi hesablamalar üçün müəyyən bir dəqiqlik təyin olunmalıdır (məsələn, ϵ=0.0001).

Ümumi Alqoritm (Parçanı Yarıya Bölmə Üsulu):

funksiya parçanıYarıyaBölmə(f, a, b, dəqiqlik):
  əgər f(a) * f(b) >= 0 onda:
    çıxış et("Verilmiş intervalda kök ola bilər və ya çoxlu kök var.")
    return NaN // Kök tapılmadı

  dövr et:
    c = (a + b) / 2
    əgər f(c) == 0 və ya (b - a) / 2 < dəqiqlik onda:
      return c

    əgər f(a) * f(c) < 0 onda:
      b = c
    başqa:
      a = c
İndi isə hər bir tapşırıq üçün f(x) funksiyasını və verilmiş intervalı nəzərə alaraq alqoritmi tətbiq edək.

Tapşırıqlar:

f(x) = x * arctan(x) - 1, [0.0, 2.0]

funksiya f1(x):
  return x * arctan(x) - 1

kök1 = parçanıYarıyaBölmə(f1, 0.0, 2.0, 0.0001)
f(x) =  
1+x 
2
 

​
 −2, [0.0, 2.0]

funksiya f2(x):
  return sqrt(1 + x*x) - 2

kök2 = parçanıYarıyaBölmə(f2, 0.0, 2.0, 0.0001)
f(x) = 2 
x
 −x−2, [-2.0, -1.0]

funksiya f3(x):
  return 2**x - x - 2

kök3 = parçanıYarıyaBölmə(f3, -2.0, -1.0, 0.0001)
f(x) = x 
3
 −2x−5, [2.0, 3.0]

funksiya f4(x):
  return x**3 - 2*x - 5

kök4 = parçanıYarıyaBölmə(f4, 2.0, 3.0, 0.0001)
f(x) = e 
x
 −2, [0.0, 1.0]

funksiya f5(x):
  return exp(x) - 2

kök5 = parçanıYarıyaBölmə(f5, 0.0, 1.0, 0.0001)
f(x) = ln(x)−1, [2.0, 3.0]

funksiya f6(x):
  return log(x) - 1

kök6 = parçanıYarıyaBölmə(f6, 2.0, 3.0, 0.0001)
f(x) = x 
2
 −0.2, [0.0, 0.2]

funksiya f7(x):
  return x*x - 0.2

kök7 = parçanıYarıyaBölmə(f7, 0.0, 0.2, 0.0001)
f(x) = cos(x)−x, [0.0, 0.2]

funksiya f8(x):
  return cos(x) - x

kök8 = parçanıYarıyaBölmə(f8, 0.0, 0.2, 0.0001)
f(x) = x 
3
 −2, [0.8, 1.0]

funksiya f9(x):
  return x**3 - 2

kök9 = parçanıYarıyaBölmə(f9, 0.8, 1.0, 0.0001)
f(x) = x−cos(x), [2.6, 3.0]

funksiya f10(x):
  return x - cos(x)

kök10 = parçanıYarıyaBölmə(f10, 2.6, 3.0, 0.0001)
f(x) = x 
2
 −3, [1.0, 1.5]

funksiya f11(x):
  return x*x - 3

kök11 = parçanıYarıyaBölmə(f11, 1.0, 1.5, 0.0001)
f(x) = x 
3
 −5, [1.0, 2.0]

funksiya f12(x):
  return x**3 - 5

kök12 = parçanıYarıyaBölmə(f12, 1.0, 2.0, 0.0001)
f(x) = e 
x
 −1.5, [0.0, 1.0]

funksiya f13(x):
  return exp(x) - 1.5

kök13 = parçanıYarıyaBölmə(f13, 0.0, 1.0, 0.0001)
f(x) = sin(x)−0.5, [0.0, 1.0]

funksiya f14(x):
  return sin(x) - 0.5

kök14 = parçanıYarıyaBölmə(f14, 0.0, 1.0, 0.0001)
f(x) = x 
2
 −10, [3.0, 4.0]

funksiya f15(x):
  return x*x - 10

kök15 = parçanıYarıyaBölmə(f15, 3.0, 4.0, 0.0001)
f(x) = x 
4
 −2, [1.0, 1.2]

funksiya f16(x):
  return x**4 - 2

kök16 = parçanıYarıyaBölmə(f16, 1.0, 1.2, 0.0001)
f(x) = tan(x)−1, [1.0, 2.0]

funksiya f17(x):
  return tan(x) - 1

kök17 = parçanıYarıyaBölmə(f17, 1.0, 2.0, 0.0001)
f(x) = x 
2
 −e, [0.0, 1.0]

funksiya f18(x):
  return x*x - exp(1)

kök18 = parçanıYarıyaBölmə(f18, 0.0, 1.0, 0.0001)
f(x) = x+cos(x), [-0.2, -0.1]

funksiya f19(x):
  return x + cos(x)

kök19 = parçanıYarıyaBölmə(f19, -0.2, -0.1, 0.0001)
f(x) = x−sin(x)−0.2, [0.1, 0.9]

funksiya f20(x):
  return x - sin(x) - 0.2

kök20 = parçanıYarıyaBölmə(f20, 0.1, 0.9, 0.0001)
f(x) = ln(x)−0.5, [1.0, 1.4]

funksiya f21(x):
  return log(x) - 0.5

kök21 = parçanıYarıyaBölmə(f21, 1.0, 1.4, 0.0001)
f(x) = x 
3
 −12, [3.0, 4.0]

funksiya f22(x):
  return x**3 - 12

kök22 = parçanıYarıyaBölmə(f22, 3.0, 4.0, 0.0001)
f(x) = e 
−x
 −x, [0.0, 1.5]

funksiya f23(x):
  return exp(-x) - x

kök23 = parçanıYarıyaBölmə(f23, 0.0, 1.5, 0.0001)
f(x) = x 
2
 −sin(x)−1, [0.0, 1.0]

funksiya f24(x):
  return x*x - sin(x) - 1

kök24 = parçanıYarıyaBölmə(f24, 0.0, 1.0, 0.0001)
f(x) = cos(x)−e 
−x
 , [0.1, 1.0]

funksiya f25(x):
  return cos(x) - exp(-x)

kök25 = parçanıYarıyaBölmə(f25, 0.1, 1.0, 0.0001)
f(x) = x 
2
 −0.3, [0.4, 0.6]

funksiya f26(x):
  return x*x - 0.3

kök26 = parçanıYarıyaBölmə(f26, 0.4, 0.6, 0.0001)
f(x) = x−ln(x)−2, [3.0, 4.0]

funksiya f27(x):
  return x - log(x) - 2

kök27 = parçanıYarıyaBölmə(f27, 3.0, 4.0, 0.0001)
f(x) = x 
2
 −20, [4.0, 5.0]

funksiya f28(x):
  return x*x - 20

kök28 = parçanıYarıyaBölmə(f28, 4.0, 5.0, 0.0001)
f(x) = x 
3
 −7, [2.0, 3.0]

funksiya f29(x):
  return x**3 - 7

kök29 = parçanıYarıyaBölmə(f29, 2.0, 3.0, 0.0001)
f(x) = sin(x)−x 
2
 +0.5, [0.0, 0.48]

funksiya f30(x):
  return sin(x) - x*x + 0.5

kök30 = parçanıYarıyaBölmə(f30, 0.0, 0.48, 0.0001)
f(x) = x 
2
 −4, [1.0, 2.0]

funksiya f31(x):
  return x*x - 4

kök31 = parçanıYarıyaBölmə(f31, 1.0, 2.0, 0.0001)
f(x) = e 
x
 −x−2, [0.0, 2.0]

funksiya f32(x):
  return exp(x) - x - 2

kök32 = parçanıYarıyaBölmə(f32, 0.0, 2.0, 0.0001)
f(x) = ln(x+1)−x 
2
 +0.5, [1.0, 4.0]

funksiya f33(x):
  return log(x + 1) - x*x + 0.5

kök33 = parçanıYarıyaBölmə(f33, 1.0, 4.0, 0.0001)
f(x) = x 
2
 −cos(x)−2, [1.0, 3.0]

funksiya f34(x):
  return x*x - cos(x) - 2

kök34 = parçanıYarıyaBölmə(f34, 1.0, 3.0, 0.0001)
f(x) = x 
3
 −x−1, [0.0, 1.0]

funksiya f35(x):
  return x**3 - x - 1

kök35 = parçanıYarıyaBölmə(f35, 0.0, 1.0, 0.0001)
Qeyd: Yuxarıdakı alqoritmlərdə arctan, sqrt, exp, log, sin, cos, tan riyazi funksiyaları, ** qüvvətə yüksəltmə operatoru, * vurma operatoru, - çıxma operatoru, / bölmə operatoru, + toplama operatoru, % modul operatoru, ==, <, > müqayisə operatorları, NaN isə "Not a Number" mənasını bildirir. Hər bir tapşırıq üçün parçanıYarıyaBölmə funksiyasını müvafiq f(x) funksiyası və interval ilə çağıraraq təqribi kökü tapmaq mümkündür.

SUALLARIN CAVABLARI:

Yarıya bölmə üsulu (dixotomiya metodu) verilmiş bir [a,b] intervalında kəsilməz olan f(x) funksiyasının f(a)⋅f(b)<0


 
                                             lab 9


Laboratoriya işi № 9-da verilən tapşırıqların alqoritmlərini təqdim edirəm. Hər bir tapşırıq üçün alqoritmi sadə iterasiya üsuluna əsasən tərtib edəcəyəm. Əvvəlcə, verilmiş f(x)=0 tənliyini x=ϕ(x) ekvivalent formasına gətirməli, sonra isə iterasiya prosesini x 
n+1
​
 =ϕ(x 
n
​
 ) şəklində qurmalıyıq. Iterasiya prosesinin yığılması üçün ∣ϕ 
′
 (x)∣<1 şərti verilmiş [a,b] intervalında ödənməlidir. Təqribi hesablamalar üçün müəyyən bir dəqiqlik təyin olunmalıdır (məsələn, ϵ=0.0001) və iterasiya prosesinə başlamaq üçün bir başlanğıc_qiymət seçilməlidir (adətən intervalın daxilindən).

Ümumi Alqoritm (Sadə İterasiya Üsulu):

funksiya sadəİterasiya(phi, başlanğıc_qiymət, dəqiqlik, maksimum_iterasiya):
  əvvəlki_x = başlanğıc_qiymət
  üçün iterasiya 1-dən maksimum_iterasiyaya qədər:
    yeni_x = phi(əvvəlki_x)
    əgər |yeni_x - əvvəlki_x| < dəqiqlik onda:
      return yeni_x
    əvvəlki_x = yeni_x
  çıxış et("Maksimum iterasiya sayına çatıldı, həll tapılmadı.")
  return NaN // Həll tapılmadı
İndi isə hər bir tapşırıq üçün f(x)=0 tənliyini x=ϕ(x) formasına gətirək və verilmiş intervalı nəzərə alaraq alqoritmi tətbiq edək. Başlanğıc qiymət olaraq intervalın orta nöqtəsini seçəcəyik.

Tapşırıqlar:

x⋅arctan(x)−1=0, [0.0,2.0]
ϕ(x)= 
arctan(x)
1
​
 

funksiya phi1(x):
  əgər arctan(x) == 0 onda:
    return NaN
  return 1 / arctan(x)

başlanğıc1 = (0.0 + 2.0) / 2
kök1 = sadəİterasiya(phi1, başlanğıc1, 0.0001, 100)
1+x 
2
 

​
 −2=0, [0.0,2.0]
x= 
3

​
  (analitik həll)
ϕ(x)= 
4−x 
2
 

​
 

funksiya phi2(x):
  əgər 4 - x*x < 0 onda:
    return NaN
  return sqrt(4 - x*x)

başlanğıc2 = (0.0 + 2.0) / 2
kök2 = sadəİterasiya(phi2, başlanğıc2, 0.0001, 100)
2 
x
 −x−2=0, [−2.0,−1.0]
ϕ(x)=2 
x
 −2

funksiya phi3(x):
  return 2**x - 2

başlanğıc3 = (-2.0 + -1.0) / 2
kök3 = sadəİterasiya(phi3, başlanğıc3, 0.0001, 100)
x 
3
 −2x−5=0, [2.0,3.0]
ϕ(x)= 
3
  
2x+5

​
 

funksiya phi4(x):
  return (2*x + 5)**(1/3)

başlanğıc4 = (2.0 + 3.0) / 2
kök4 = sadəİterasiya(phi4, başlanğıc4, 0.0001, 100)
e 
x
 −2=0, [0.0,1.0]
x=ln(2) (analitik həll)
ϕ(x)=ln(2)

funksiya phi5(x):
  return log(2)

başlanğıc5 = (0.0 + 1.0) / 2
kök5 = sadəİterasiya(phi5, başlanğıc5, 0.0001, 100)
ln(x)−1=0, [2.0,3.0]
x=e (analitik həll)
ϕ(x)=e

funksiya phi6(x):
  return exp(1)

başlanğıc6 = (2.0 + 3.0) / 2
kök6 = sadəİterasiya(phi6, başlanğıc6, 0.0001, 100)
x 
2
 −0.2=0, [0.0,0.2]
x= 
0.2

​
  (analitik həll)
ϕ(x)= 
0.2

​
 

funksiya phi7(x):
  return sqrt(0.2)

başlanğıc7 = (0.0 + 0.2) / 2
kök7 = sadəİterasiya(phi7, başlanğıc7, 0.0001, 100)
cos(x)−x=0, [0.0,0.2]
ϕ(x)=cos(x)

funksiya phi8(x):
  return cos(x)

başlanğıc8 = (0.0 + 0.2) / 2
kök8 = sadəİterasiya(phi8, başlanğıc8, 0.0001, 100)
x 
3
 −2=0, [0.8,1.0]
x= 
3
  
2

​
  (analitik həll)
ϕ(x)= 
3
  
2

​
 

funksiya phi9(x):
  return 2**(1/3)

başlanğıc9 = (0.8 + 1.0) / 2
kök9 = sadəİterasiya(phi9, başlanğıc9, 0.0001, 100)
x−cos(x)=0, [2.6,3.0]
ϕ(x)=cos(x)

funksiya phi10(x):
  return cos(x)

başlanğıc10 = (2.6 + 3.0) / 2
kök10 = sadəİterasiya(phi10, başlanğıc10, 0.0001, 100)
x 
2
 −3=0, [1.0,1.5]
x= 
3

​
  (analitik həll)
ϕ(x)= 
3

​
 

funksiya phi11(x):
  return sqrt(3)

başlanğıc11 = (1.0 + 1.5) / 2
kök11 = sadəİterasiya(phi11, başlanğıc11, 0.0001, 100)
x 
3
 −5=0, [1.0,2.0]
x= 
3
  
5

​
  (analitik həll)
ϕ(x)= 
3
  
5

​
 

funksiya phi12(x):
  return 5**(1/3)

başlanğıc12 = (1.0 + 2.0) / 2
kök12 = sadəİterasiya(phi12, başlanğıc12, 0.0001, 100)
e 
x
 −1.5=0, [0.0,1.0]
x=ln(1.5) (analitik həll)
ϕ(x)=ln(1.5)

funksiya phi13(x):
  return log(1.5)

başlanğıc13 = (0.0 + 1.0) / 2
kök13 = sadəİterasiya(phi13, başlanğıc13, 0.0001, 100)
sin(x)−0.5=0, [0.0,1.0]
ϕ(x)=arcsin(0.5)

funksiya phi14(x):
  return asin(0.5)

başlanğıc14 = (0.0 + 1.0) / 2
kök14 = sadəİterasiya(phi14, başlanğıc14, 0.0001, 100)
x 
2
 −10=0, [3.0,4.0]
x= 
10

​
  (analitik həll)
ϕ(x)= 
10

​
 

funksiya phi15(x):
  return sqrt(10)

başlanğıc15 = (3.0 + 4.0) / 2
kök15 = sadəİterasiya(phi15, başlanğıc15, 0.0001, 100)
x 
4
 −2=0, [1.0,1.2]
x= 
4
  
2

​
  (analitik həll)
ϕ(x)= 
4
  
2

​
 

funksiya phi16(x):
  return 2**(1/4)

başlanğıc16 = (1.0 + 1.2) / 2
kök16 = sadəİterasiya(phi16, başlanğıc16, 0.0001, 100)
tan(x)−1=0, [1.0,2.0]
ϕ(x)=arctan(1)+π⋅k
ϕ(x)=x−(tan(x)−1)⋅ 
sec 
2
 (x)
1
​
  (Nyuton üsuluna yaxın)
ϕ(x)=arctan(1) (intervala uyğun kök)

funksiya phi17(x):
  return atan(1)

başlanğıc17 = (1.0 + 2.0) / 2
kök17 = sadəİterasiya(phi17, başlanğıc17, 0.0001, 100)
x 
2
 −e=0, [0.0,1.0]
x= 
e

​
  (analitik həll, intervala daxil deyil)
ϕ(x)= 
e

​
 

funksiya phi18(x):
  return sqrt(exp(1))

başlanğıc18 = (0.0 + 1.0) / 2
kök18 = sadəİterasiya(phi18, başlanğıc18, 0.0001, 100)
x+cos(x)=0, [−0.2,−0.1]
ϕ(x)=−cos(x)

funksiya phi19(x):
  return -cos(x)

başlanğıc19 = (-0.2 + -0.1) / 2
kök19 = sadəİterasiya(phi19, başlanğıc19, 0.0001, 100)
x−sin(x)−0.2=0, [0.1,0.9]
ϕ(x)=sin(x)+0.2

funksiya phi20(x):
  return sin(x) + 0.2

başlanğıc20 = (0.1 + 0.9) / 2
kök20 = sadəİterasiya(phi20, başlanğıc20, 0.0001, 100)
ln(x)−0.5=0, [1.0,1.4]
x=e 
0.5
 = 
e

​
  (analitik həll)
ϕ(x)=e 
0.5
 

funksiya phi21(x):
  return exp(0.5)

başlanğıc21 = (1.0 + 1.4) / 2
kök21 = sadəİterasiya(phi21, başlanğıc21, 0.0001, 100)
x 
3
 −12=0, [3.0,4.0]
x= 
3
  
12

​
  (analitik həll)
ϕ(x)= 
3
  
12

​
 

funksiya phi22(x):
  return 12**(1/3)

başlanğıc22 = (3.0 + 4.0) / 2
kök22 = sadəİterasiya(phi22, başlanğıc22, 0.0001, 100)
e 
−x
 −x=0, [0.0,1.5]
ϕ(x)=e 
−x
 

funksiya phi23(x):
  return exp(-x)

başlanğıc23 = (0.0 + 1.5) / 2
kök23 = sadəİterasiya(phi23, başlanğıc23, 0.0001, 100)
x 
2
 −sin(x)−1=0, [0.0,1.0]
ϕ(x)= 
1+sin(x)

​
 

funksiya phi24(x):
  əgər 1 + sin(x) < 0 onda:
    return NaN
  return sqrt(1 + sin(x))

başlanğıc24 = (0.0 + 1.0) / 2
kök24 = sadəİterasiya(phi24, başlanğıc24, 0.0001, 100)
cos(x)−e 
−x
 =0, [0.1,1.0]
ϕ(x)=arccos(e 
−x
 )

funksiya phi25(x):
  əgər e**(-x) > 1 və ya e




                                                                        lab 10

Laboratoriya işi № 10-da verilən tapşırıqların alqoritmlərini təqdim edirəm. Hər bir tapşırıq üçün alqoritmi Nyuton üsuluna əsasən tərtib edəcəyəm. Nyuton üsulu f(x)=0 tənliyinin təqribi kökünü tapmaq üçün aşağıdakı iterasiya düsturundan istifadə edir:

x 
n+1
​
 =x 
n
​
 − 
f 
′
 (x 
n
​
 )
f(x 
n
​
 )
​
 

Burada f 
′
 (x 
n
​
 ) funksiyanın x 
n
​
  nöqtəsindəki birinci tərtib törəməsidir. Təqribi hesablamalar üçün müəyyən bir dəqiqlik (ϵ) təyin olunmalı və iterasiya prosesinə başlamaq üçün bir başlanğıc_qiymət (x 
0
​
 ) seçilməlidir (adətən verilmiş intervalın daxilindən).

Ümumi Alqoritm (Nyuton Üsulu):

funksiya nyutonÜsulu(f, f_törəmə, başlanğıc_qiymət, dəqiqlik, maksimum_iterasiya):
  əvvəlki_x = başlanğıc_qiymət
  üçün iterasiya 1-dən maksimum_iterasiyaya qədər:
    törəmə_qiyməti = f_törəmə(əvvəlki_x)
    əgər törəmə_qiyməti == 0 onda:
      çıxış et("Törəmə sıfıra bərabərdir, üsul tətbiq oluna bilməz.")
      return NaN // Həll tapılmadı
    yeni_x = əvvəlki_x - f(əvvəlki_x) / törəmə_qiyməti
    əgər |yeni_x - əvvəlki_x| < dəqiqlik onda:
      return yeni_x
    əvvəlki_x = yeni_x
  çıxış et("Maksimum iterasiya sayına çatıldı, həll tapılmadı.")
  return NaN // Həll tapılmadı
İndi isə hər bir tapşırıq üçün f(x) funksiyasını, onun f 
′
 (x) törəməsini və verilmiş intervalı nəzərə alaraq alqoritmi tətbiq edək. Başlanğıc qiymət olaraq intervalın orta nöqtəsini seçəcəyik.

Tapşırıqlar:

f(x)=x⋅arctan(x)−1, [0.0,2.0]
f 
′
 (x)=arctan(x)+ 
1+x 
2
 
x
​
 

funksiya f1(x):
  return x * atan(x) - 1

funksiya f1_törəmə(x):
  return atan(x) + x / (1 + x*x)

başlanğıc1 = (0.0 + 2.0) / 2
kök1 = nyutonÜsulu(f1, f1_törəmə, başlanğıc1, 0.0001, 100)
f(x)= 
1+x 
2
 

​
 −2, [0.0,2.0]
f 
′
 (x)= 
1+x 
2
 

​
 
x
​
 

funksiya f2(x):
  return sqrt(1 + x*x) - 2

funksiya f2_törəmə(x):
  return x / sqrt(1 + x*x)

başlanğıc2 = (0.0 + 2.0) / 2
kök2 = nyutonÜsulu(f2, f2_törəmə, başlanğıc2, 0.0001, 100)
f(x)=2 
x
 −x−2, [−2.0,−1.0]
f 
′
 (x)=2 
x
 ln(2)−1

funksiya f3(x):
  return 2**x - x - 2

funksiya f3_törəmə(x):
  return 2**x * log(2) - 1

başlanğıc3 = (-2.0 + -1.0) / 2
kök3 = nyutonÜsulu(f3, f3_törəmə, başlanğıc3, 0.0001, 100)
f(x)=x 
3
 −2x−5, [2.0,3.0]
f 
′
 (x)=3x 
2
 −2

funksiya f4(x):
  return x**3 - 2*x - 5

funksiya f4_törəmə(x):
  return 3*x*x - 2

başlanğıc4 = (2.0 + 3.0) / 2
kök4 = nyutonÜsulu(f4, f4_törəmə, başlanğıc4, 0.0001, 100)
f(x)=e 
x
 −2, [0.0,1.0]
f 
′
 (x)=e 
x
 

funksiya f5(x):
  return exp(x) - 2

funksiya f5_törəmə(x):
  return exp(x)

başlanğıc5 = (0.0 + 1.0) / 2
kök5 = nyutonÜsulu(f5, f5_törəmə, başlanğıc5, 0.0001, 100)
f(x)=ln(x)−1, [2.0,3.0]
f 
′
 (x)= 
x
1
​
 

funksiya f6(x):
  return log(x) - 1

funksiya f6_törəmə(x):
  return 1 / x

başlanğıc6 = (2.0 + 3.0) / 2
kök6 = nyutonÜsulu(f6, f6_törəmə, başlanğıc6, 0.0001, 100)
f(x)=x 
2
 −0.2, [0.0,0.2]
f 
′
 (x)=2x

funksiya f7(x):
  return x*x - 0.2

funksiya f7_törəmə(x):
  return 2*x

başlanğıc7 = (0.0 + 0.2) / 2
kök7 = nyutonÜsulu(f7, f7_törəmə, başlanğıc7, 0.0001, 100)
f(x)=cos(x)−x, [0.0,0.2]
f 
′
 (x)=−sin(x)−1

funksiya f8(x):
  return cos(x) - x

funksiya f8_törəmə(x):
  return -sin(x) - 1

başlanğıc8 = (0.0 + 0.2) / 2
kök8 = nyutonÜsulu(f8, f8_törəmə, başlanğıc8, 0.0001, 100)
f(x)=x 
3
 −2, [0.8,1.0]
f 
′
 (x)=3x 
2
 

funksiya f9(x):
  return x**3 - 2

funksiya f9_törəmə(x):
  return 3*x*x

başlanğıc9 = (0.8 + 1.0) / 2
kök9 = nyutonÜsulu(f9, f9_törəmə, başlanğıc9, 0.0001, 100)
f(x)=x−cos(x), [2.6,3.0]
f 
′
 (x)=1+sin(x)

funksiya f10(x):
  return x - cos(x)

funksiya f10_törəmə(x):
  return 1 + sin(x)

başlanğıc10 = (2.6 + 3.0) / 2
kök10 = nyutonÜsulu(f10, f10_törəmə, başlanğıc10, 0.0001, 100)
f(x)=x 
2
 −3, [1.0,1.5]
f 
′
 (x)=2x

funksiya f11(x):
  return x*x - 3

funksiya f11_törəmə(x):
  return 2*x

başlanğıc11 = (1.0 + 1.5) / 2
kök11 = nyutonÜsulu(f11, f11_törəmə, başlanğıc11, 0.0001, 100)
f(x)=x 
3
 −5, [1.0,2.0]
f 
′
 (x)=3x 
2
 

funksiya f12(x):
  return x**3 - 5

funksiya f12_törəmə(x):
  return 3*x*x

başlanğıc12 = (1.0 + 2.0) / 2
kök12 = nyutonÜsulu(f12, f12_törəmə, başlanğıc12, 0.0001, 100)
f(x)=e 
x
 −1.5, [0.0,1.0]
f 
′
 (x)=e 
x
 

funksiya f13(x):
  return exp(x) - 1.5

funksiya f13_törəmə(x):
  return exp(x)

başlanğıc13 = (0.0 + 1.0) / 2
kök13 = nyutonÜsulu(f13, f13_törəmə, başlanğıc13, 0.0001, 100)
f(x)=sin(x)−0.5, [0.0,1.0]
f 
′
 (x)=cos(x)

funksiya f14(x):
  return sin(x) - 0.5

funksiya f14_törəmə(x):
  return cos(x)

başlanğıc14 = (0.0 + 1.0) / 2
kök14 = nyutonÜsulu(f14, f14_törəmə, başlanğıc14, 0.0001, 100)
f(x)=x 
2
 −10, [3.0,4.0]
f 
′
 (x)=2x

funksiya f15(x):
  return x*x - 10

funksiya f15_törəmə(x):
  return 2*x

başlanğıc15 = (3.0 + 4.0) / 2
kök15 = nyutonÜsulu(f15, f15_törəmə, başlanğıc15, 0.0001, 100)
f(x)=x 
4
 −2, [1.0,1.2]
f 
′
 (x)=4x 
3
 

funksiya f16(x):
  return x**4 - 2

funksiya f16_törəmə(x):
  return 4*x**3

başlanğıc16 = (1.0 + 1.2) / 2
kök16 = nyutonÜsulu(f16, f16_törəmə, başlanğıc16, 0.0001, 100)
f(x)=tan(x)−1, [1.0,2.0]
f 
′
 (x)=sec 
2
 (x)=1+tan 
2
 (x)

funksiya f17(x):
  return tan(x) - 1

funksiya f17_törəmə(x):
  return 1 + tan(x)**2

başlanğıc17 = (1.0 + 2.0) / 2
kök17 = nyutonÜsulu(f17, f17_törəmə, başlanğıc17, 0.0001, 100)
f(x)=x 
2
 −e, [0.0,1.0]
f 
′
 (x)=2x

funksiya f18(x):
  return x*x - exp(1)

funksiya f18_törəmə(x):
  return 2*x

başlanğıc18 = (0.0 + 1.0) / 2
kök18 = nyutonÜsulu(f18, f18_törəmə, başlanğıc18, 0.0001, 100)
f(x)=x+cos(x), [−0.2,−0.1]
f 
′
 (x)=1−sin(x)

funksiya f19(x):
  return x + cos(x)

funksiya f19_törəmə(x):
  return 1 - sin(x)

başlanğıc19 = (-0.2 + -0.1) / 2
kök19 = nyutonÜsulu(f19, f19_törəmə, başlanğıc19, 0.0001, 100)
f(x)=x−sin(x)−0.2, [0.1,0.9]
f 
′
 (x)=1−cos(x)

funksiya f20(x):
  return x - sin(x) - 0.2

funksiya f20_törəmə(x):
  return 1 - cos(x)

başlanğıc20 = (0.1 + 0.9) / 2
kök20 = nyutonÜsulu(f20, f20_törəmə, başlanğıc20, 0.0001, 100)

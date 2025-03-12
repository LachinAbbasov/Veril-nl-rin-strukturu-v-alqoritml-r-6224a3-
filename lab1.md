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

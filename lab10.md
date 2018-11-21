# 用 python 做计算器，做数学题

## 1.安装winpython


尽管python有很多发行版本，作业使用winpython。它是windows环境下最易于使用、最强大的科学计算工具之一。
下载网站“ https://sourceforge.net/projects/winpython/files/ ” 下载提供的最新版本，并安装！例如：WinPython-64bit-3.6.3.0Qt5.exe (409.0 MB)

## 2.高数

- 1 解方程组

```
from sympy import *    
x,y,z = symbols('x y z ') 
f1 = 2*x - y + z - 10 
f2 = 3*x + 2*y - z - 16 
f3 = x + 6*y - z - 28 
print(solve([f1, f2, f3])) 
结果： {x: 46/11, z: 74/11, y: 56/11}
```

- 2 求极限

求n趋近于0时sin（x）/x的值

```
from sympy import *
n = Symbol('n') 
f = sin(x)/x 
print(limit(f, x, 0))
结果：1
```

### 3.线代

- 1 求矩阵的逆

```
import numpy as np 
a = np.array([[0,1,2],[1,1,4],[2,-1,0]])
np.linalg.inv(a)

matrix([[2,-1,1],[4,-2,1],[-3/2,1,-1/2]])

```

- 2 求矩阵的det

```
import numpy as np 
a = np.array([[1, 2, 3],[4, 5, 6],[7, 8, 9]])
np.linalg.det(E)

6.6613381477509402e-16
```
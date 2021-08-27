# Python_DeepLearning

<h6>라이브러리 다운로드</h6>
<pre>
<code>
pip install matplotlib 
<br />
pip install numpy
</code>
</pre>

## 넘파이
우선 딥러닝을 공부하다보면 배열이나 행렬 계산이 종종 나오는데요. 넘파이의 배열 클래스를 사용한다면 그러한 계산을 편리하게 사용할수 있기에<br />
넘파이를 사용합니다.

넘파이를 improt 할때는 밑에 코드처럼 쓰면 됩니다.

~~~python
import numpy as np
~~~

이렇게 쓰고나면 이제 넘파이를 불러오는것은 성공한것인데요. 
이후부터는 넘파이를 활용해보겟습니다.

### 넘파이 배열 생성
**넘파이 배열**을 생성할때는 **np.array()** 메서드를 사용합니다. <br />
**np.array()** 는 파이썬의 list를 argument로 받아서 넘파이에서 제공하는 특수한 형태의 배열(numpy.ndarray)을 반환합니다.<br />
코드를 하나 예로 들어보겟습니다. 밑에 코드를 봐주세요.
~~~python 
x = np.array([1.0, 2.0 , 3.0])
print(x)
~~~
우선 출력값을 보시면 뒤에 0을 없애서 출력값으로 나옵니다.
그후 **type(x)** 를 해보시면 class가 **numpy.ndarray** 로 출력이 됩니다.

### 넘파이의 산술 연산
파이썬 넘파이에서 산술연산을 하는 코드부터 보여드리겟습니다.
~~~python
import numpy as np

x = np.array([1.0, 2.0, 3.0])
y = np.array([2.0, 4.0, 6.0])

print(x + y)

출력값>>> [3. , 6. , 9.]
~~~
산술연산에서 주의해야할것은 일단 **x와y의 원소 수가 값다는 것입니다.(둘다 수를 3개 가진다는 의미)**  <br />
원소 수가 같다면 산술연산은 각 원소에 대해서 실행되기때문에 **두 배열다 원소 즉 수를 3개를 쓰는것이** 중요합니다. <br />

## 넘파이의 N차원 배열
넘파이는 1차원 배열(1줄로 쓴 배열)뿐 **다차원 배열** 예를 들어 2차원 배열은 밑에 코드처럼 작성합니다.<br />
~~~python
import numpy as np

A = np.array([[1, 2], [3, 4]])
print(A)

print(A.shape)
출력값>>>(2, 2) 
print(A.dtype)
>>> int 64
~~~
위에 코드는 2X2의 A라는 행렬을 작성했습니다<br />
행렬의 형상은 **shape** 로 행렬에 담긴 원소의 자료형은 dtype으로 알 수 있습니다.<br />

## Broadcast
넘파이에서는 형상이 다른 배열끼리도 계산이 가능합니다.<br />
예를들어보자면 10이라는 **스칼라값**이 2X2 행렬로 연산이 가능합니다.
~~~python
import numpy as np

A = np.array([[1, 2],[3, 4]])
B = np.array([10, 20])

print(A * B)
~~~

## 원소접근

원소의 인덱스는 0부터 시작합니다. <br />
그리고 각 원소에 접근하려면 밑에 코드처럼 작성해야합니다.<br />

~~~python
import numpy as np

X = np.array([[51, 55], [14, 19], [0, 4]])
print(X)
~~~
이렇게 쓰면 결과값에서 **0번째(첫번째)** 인 51,55를 출력하려면 이런 코드를 작성해야합니다.

~~~python
X = np.array([[51, 55], [14, 19], [0, 4]])
print(X)

print(X[0])
print(X[0][1])
~~~
우선 코드를 해석해보자면 print문에서 첫번째는 X라는 variable에 0번째 즉 첫번째를 출력시켜달라는 뜻이구요. <br />
그후 밑에 print문은 X라는 variabel에 0번째에서 1번을 출력해달라는데 0부터 인덱스는 시작하니 일반 숫자로 세면 2번이겠군요 <br />

# 여러가지로 응용하기
~~~python
#for 원소 접근

for row in X:
    print(row)

X = X.flatten()
print(X)

print(X[np.array([0, 2, 4])])

# Boolean

print(X > 15)
print(X[X > 15])
~~~








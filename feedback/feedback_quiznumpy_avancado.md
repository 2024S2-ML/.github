
```markdown
# Relatório de Feedback sobre Questões Avançadas de NumPy

## Questão 1
**Pergunta:** Qual função do NumPy é usada para calcular a decomposição de valores singulares (SVD)?
**Resposta Correta:** B. np.linalg.svd()

**Feedback:** A função `np.linalg.svd()` é usada para calcular a decomposição de valores singulares de uma matriz. Esta função retorna três matrizes: U, S e V, onde A = U*S*V.T.

**Exemplo de Uso:**
```python
import numpy as np
A = np.array([[1, 2], [3, 4], [5, 6]])
U, S, V = np.linalg.svd(A)
print("U:", U)
print("S:", S)
print("V:", V)
```

## Questão 2
**Pergunta:** Como você pode calcular o determinante de uma matriz em NumPy?
**Resposta Correta:** A. np.linalg.det(matrix)

**Feedback:** A função `np.linalg.det()` calcula o determinante de uma matriz quadrada.

**Exemplo de Uso:**
```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
det = np.linalg.det(A)
print("Determinante:", det)
```

## Questão 3
**Pergunta:** Qual função do NumPy é usada para resolver sistemas de equações lineares?
**Resposta Correta:** A. np.linalg.solve(A, b)

**Feedback:** A função `np.linalg.solve()` resolve um sistema de equações lineares da forma Ax = b, onde A é a matriz dos coeficientes e b é o vetor das constantes.

**Exemplo de Uso:**
```python
import numpy as np
A = np.array([[3, 1], [1, 2]])
b = np.array([9, 8])
x = np.linalg.solve(A, b)
print("Solução:", x)
```

## Questão 4
**Pergunta:** Como você pode calcular a norma de um vetor em NumPy?
**Resposta Correta:** A. np.linalg.norm(vector)

**Feedback:** A função `np.linalg.norm()` calcula a norma (magnitude) de um vetor.

**Exemplo de Uso:**
```python
import numpy as np
vector = np.array([3, 4])
norm = np.linalg.norm(vector)
print("Norma:", norm)
```

## Questão 5
**Pergunta:** Qual função do NumPy retorna os autovalores e autovetores de uma matriz quadrada?
**Resposta Correta:** A. np.linalg.eig(matrix)

**Feedback:** A função `np.linalg.eig()` calcula os autovalores e autovetores de uma matriz quadrada.

**Exemplo de Uso:**
```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
eigenvalues, eigenvectors = np.linalg.eig(A)
print("Autovalores:", eigenvalues)
print("Autovetores:", eigenvectors)
```

## Questão 6
**Pergunta:** Como você pode realizar a multiplicação de matrizes em NumPy?
**Resposta Correta:** A. np.matmul(A, B)

**Feedback:** A função `np.matmul()` realiza a multiplicação de matrizes. Alternativamente, o operador `@` pode ser usado para a multiplicação de matrizes.

**Exemplo de Uso:**
```python
import numpy as np
A = np.array([[1, 2], [3, 4]])
B = np.array([[5, 6], [7, 8]])
C = np.matmul(A, B)
print("Resultado da multiplicação de matrizes:", C)
```

## Questão 7
**Pergunta:** Qual função do NumPy é usada para calcular a transformada de Fourier de um array?
**Resposta Correta:** A. np.fft.fft(array)

**Feedback:** A função `np.fft.fft()` calcula a transformada rápida de Fourier de um array.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([1, 2, 3, 4])
fft_x = np.fft.fft(x)
print("Transformada de Fourier:", fft_x)
```

## Questão 8
**Pergunta:** Como você pode calcular a convolução de dois arrays em NumPy?
**Resposta Correta:** A. np.convolve(a, b)

**Feedback:** A função `np.convolve()` calcula a convolução de dois arrays unidimensionais.

**Exemplo de Uso:**
```python
import numpy as np
a = np.array([1, 2, 3])
b = np.array([0, 1, 0.5])
convolution = np.convolve(a, b)
print("Convolução:", convolution)
```

## Questão 9
**Pergunta:** Qual função do NumPy é usada para calcular a diferença discreta ao longo de um eixo?
**Resposta Correta:** A. np.diff(array)

**Feedback:** A função `np.diff()` calcula a diferença discreta entre elementos consecutivos ao longo de um eixo especificado.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([1, 2, 4, 7, 0])
diff_x = np.diff(x)
print("Diferença discreta:", diff_x)
```

## Questão 10
**Pergunta:** Como você pode ordenar os elementos de um array NumPy ao longo de um eixo específico?
**Resposta Correta:** A. np.sort(array, axis=0)

**Feedback:** A função `np.sort()` ordena os elementos de um array ao longo de um eixo especificado. O padrão é ordenar ao longo do último eixo.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([[3, 2], [1, 4]])
sorted_x = np.sort(x, axis=0)
print("Array ordenado ao longo do eixo 0:", sorted_x)
```

## Questão 11
**Pergunta:** Qual função do NumPy retorna índices que ordenariam um array?
**Resposta Correta:** A. np.argsort(array)

**Feedback:** A função `np.argsort()` retorna os índices que ordenariam um array.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([3, 1, 2])
indices = np.argsort(x)
print("Índices que ordenam o array:", indices)
```

## Questão 12
**Pergunta:** Como você pode calcular a correlação cruzada de dois arrays em NumPy?
**Resposta Correta:** A. np.correlate(a, b)

**Feedback:** A função `np.correlate()` calcula a correlação cruzada de dois arrays unidimensionais.

**Exemplo de Uso:**
```python
import numpy as np
a = np.array([1, 2, 3])
b = np.array([0, 1, 0.5])
correlation = np.correlate(a, b, mode='full')
print("Correlação cruzada:", correlation)
```

## Questão 13
**Pergunta:** Qual função do NumPy é usada para empilhar arrays ao longo de um novo eixo?
**Resposta Correta:** A. np.stack((a, b))

**Feedback:** A função `np.stack()` empilha arrays ao longo de um novo eixo.

**Exemplo de Uso:**
```python
import numpy as np
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
stacked = np.stack((a, b))
print("Arrays empilhados:", stacked)
```

## Questão 14
**Pergunta:** Como você pode dividir um array em vários sub-arrays horizontalmente?
**Resposta Correta:** A. np.hsplit(array, indices)

**Feedback:** A função `np.hsplit()` divide um array em vários sub-arrays horizontalmente (ao longo do eixo 1).

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])
subarrays = np.hsplit(x, 2)
print("Sub-arrays:", subarrays)
```

## Questão 15
**Pergunta:** Qual função do NumPy é usada para criar uma matriz diagonal a partir de um array?
**Resposta Correta:** A. np.diag(array)

**Feedback:** A função `np.diag()` cria uma matriz diagonal a partir de um array ou extrai a diagonal de uma matriz.

**Exemplo de Uso:**
```python
import numpy as np
a = np.array([1, 2, 3])
diagonal_matrix = np.diag(a)
print("Matriz diagonal:", diagonal_matrix)
```

## Questão 16
**Pergunta:** Como você pode calcular a integral cumulativa de um array em NumPy?
**Resposta Correta:** A. np.cumtrapz(array)

**Feedback:** A função `np.cumtrapz()` calcula a integral cumulativa de um array usando a regra do trapézio.

**Exemplo de Uso:**
```python
import numpy as np
from scipy.integrate import cumtrapz
x = np.array([0, 1, 2, 3])
y = np.array([0, 1,

 4, 9])
cumulative_integral = cumtrapz(y, x, initial=0)
print("Integral cumulativa:", cumulative_integral)
```

## Questão 17
**Pergunta:** Qual função do NumPy é usada para calcular a transformada rápida de Fourier inversa?
**Resposta Correta:** A. np.fft.ifft(array)

**Feedback:** A função `np.fft.ifft()` calcula a transformada rápida de Fourier inversa de um array.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([1, 2, 3, 4])
ifft_x = np.fft.ifft(x)
print("Transformada de Fourier inversa:", ifft_x)
```

## Questão 18
**Pergunta:** Como você pode calcular a matriz de covariância de um array em NumPy?
**Resposta Correta:** A. np.cov(array)

**Feedback:** A função `np.cov()` calcula a matriz de covariância de um array.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([[1, 2, 3], [4, 5, 6]])
cov_matrix = np.cov(x)
print("Matriz de covariância:", cov_matrix)
```

## Questão 19
**Pergunta:** Qual função do NumPy é usada para gerar números aleatórios a partir de uma distribuição binomial?
**Resposta Correta:** A. np.random.binomial(n, p, size)

**Feedback:** A função `np.random.binomial()` gera números aleatórios a partir de uma distribuição binomial com parâmetros n (número de ensaios), p (probabilidade de sucesso) e size (tamanho do array de saída).

**Exemplo de Uso:**
```python
import numpy as np
binomial_samples = np.random.binomial(n=10, p=0.5, size=100)
print("Amostras binomiais:", binomial_samples)
```

## Questão 20
**Pergunta:** Como você pode encontrar os índices dos elementos que atendem a uma condição em um array NumPy?
**Resposta Correta:** A. np.where(condition)

**Feedback:** A função `np.where()` retorna os índices dos elementos em um array que atendem a uma condição especificada.

**Exemplo de Uso:**
```python
import numpy as np
x = np.array([1, 2, 3, 4, 5])
indices = np.where(x > 3)
print("Índices dos elementos maiores que 3:", indices)
```
```


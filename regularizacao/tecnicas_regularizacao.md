# Técnicas de Regularização L1 e L2

## Introdução

A regularização é uma técnica fundamental em machine learning utilizada para prevenir overfitting. As duas formas mais comuns de regularização são L1 (lasso) e L2 (ridge). Ambas adicionam um termo de penalização à função de custo, ajudando a controlar a complexidade do modelo e, assim, melhorar sua capacidade de generalização.

### Regularização L1 (Lasso)

A regularização L1 adiciona a soma dos valores absolutos dos coeficientes do modelo à função de custo. Isso incentiva a criação de modelos esparsos, onde muitos coeficientes são reduzidos a zero. Como resultado, L1 pode ser útil tanto para a seleção de features quanto para a prevenção de overfitting.

### Regularização L2 (Ridge)

A regularização L2 adiciona a soma dos quadrados dos coeficientes do modelo à função de custo. Em vez de definir os coeficientes a zero, L2 tende a distribuir a penalização uniformemente, encolhendo todos os coeficientes, mas sem necessariamente eliminá-los.

## Matemática por Trás da Regularização

### Função de Custo

Para um problema de regressão linear, a função de custo sem regularização é a soma dos erros quadráticos:

\[ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} \left( h_{\theta}(x^{(i)}) - y^{(i)} \right)^2 \]

onde \( h_{\theta}(x) \) é a função de hipótese, \( \theta \) são os parâmetros do modelo, \( x^{(i)} \) são os exemplos de treinamento e \( y^{(i)} \) são os rótulos.

### Regularização L1

A função de custo com regularização L1 é dada por:

\[ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} \left( h_{\theta}(x^{(i)}) - y^{(i)} \right)^2 + \lambda \sum_{j=1}^{n} |\theta_j| \]

onde \( \lambda \) é o parâmetro de regularização que controla a força da penalização.

### Regularização L2

A função de custo com regularização L2 é dada por:

\[ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} \left( h_{\theta}(x^{(i)}) - y^{(i)} \right)^2 + \lambda \sum_{j=1}^{n} \theta_j^2 \]

## Aplicação Prática

### Implementação com Scikit-Learn

Vamos aplicar a regularização L1 e L2 usando a biblioteca Scikit-Learn em um exemplo de regressão linear.

```python
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import Lasso, Ridge
from sklearn.metrics import mean_squared_error
import matplotlib.pyplot as plt

# Dados simulados
np.random.seed(0)
X = np.random.randn(100, 5)
y = np.dot(X, np.array([1.5, -2, 0, 0, 3])) + np.random.randn(100)

# Divisão dos dados
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=0)

# Modelo Lasso (L1)
lasso = Lasso(alpha=0.1)
lasso.fit(X_train, y_train)
y_pred_lasso = lasso.predict(X_test)

# Modelo Ridge (L2)
ridge = Ridge(alpha=0.1)
ridge.fit(X_train, y_train)
y_pred_ridge = ridge.predict(X_test)

# Avaliação
print("Lasso MSE:", mean_squared_error(y_test, y_pred_lasso))
print("Ridge MSE:", mean_squared_error(y_test, y_pred_ridge))

# Coeficientes
plt.figure(figsize=(12, 6))
plt.plot(lasso.coef_, label='Lasso coefficients')
plt.plot(ridge.coef_, label='Ridge coefficients')
plt.legend()
plt.show()
```

### Comparação Visual

No gráfico acima, podemos observar a diferença nos coeficientes aprendidos pelos modelos Lasso e Ridge. O Lasso força alguns coeficientes a zero, enquanto o Ridge tende a encolher todos os coeficientes, mas sem eliminá-los completamente.

## Vantagens e Desvantagens

### L1 (Lasso)

**Vantagens:**
- **Seleção de Features**: Pode eliminar completamente features irrelevantes.
- **Simplicidade**: Produz modelos esparsos e interpretáveis.

**Desvantagens:**
- **Estabilidade**: Pode ser instável quando há alta correlação entre features.
- **Bias**: Pode introduzir um viés maior nos coeficientes devido à penalização.

### L2 (Ridge)

**Vantagens:**
- **Estabilidade**: Mais estável em presença de features altamente correlacionadas.
- **Generalização**: Pode melhorar a performance em modelos com muitas features.

**Desvantagens:**
- **Complexidade**: Não elimina completamente features irrelevantes.
- **Interpretação**: Pode ser menos interpretável devido à retenção de todas as features.

## Combinação: Elastic Net

Elastic Net combina as penalizações L1 e L2 para aproveitar os benefícios de ambas as técnicas. A função de custo do Elastic Net é dada por:

\[ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m} \left( h_{\theta}(x^{(i)}) - y^{(i)} \right)^2 + \lambda_1 \sum_{j=1}^{n} |\theta_j| + \lambda_2 \sum_{j=1}^{n} \theta_j^2 \]

```python
from sklearn.linear_model import ElasticNet

# Modelo Elastic Net
elastic_net = ElasticNet(alpha=0.1, l1_ratio=0.5)
elastic_net.fit(X_train, y_train)
y_pred_elastic_net = elastic_net.predict(X_test)

# Avaliação
print("Elastic Net MSE:", mean_squared_error(y_test, y_pred_elastic_net))

# Coeficientes
plt.figure(figsize=(12, 6))
plt.plot(elastic_net.coef_, label='Elastic Net coefficients')
plt.legend()
plt.show()
```

## Considerações Finais

A regularização é uma ferramenta poderosa para melhorar a generalização dos modelos de machine learning, prevenindo o overfitting. A escolha entre L1, L2 ou uma combinação de ambas depende das características específicas do problema e dos dados. Experimentar com diferentes técnicas de regularização e ajustar os parâmetros de penalização é essencial para encontrar o equilíbrio certo para cada aplicação.

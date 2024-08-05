### Gradiente Descendente: Teoria, Prática e Exercícios

#### Teoria

**1. Introdução ao Gradiente Descendente:**
   - **Definição:** O gradiente descendente é um algoritmo de otimização usado para minimizar funções de custo em modelos de aprendizado de máquina. Ele é fundamental para o treinamento de modelos de regressão e redes neurais.
   - **Objetivo:** Encontrar o conjunto de parâmetros que minimiza a função de custo, que mede a diferença entre as previsões do modelo e os valores reais.

**2. Conceito de Gradiente:**
   - **Gradiente:** O gradiente de uma função é um vetor que aponta na direção do maior aumento da função. Para minimizar uma função, movemos na direção oposta ao gradiente.
   - **Cálculo do Gradiente:** Em um espaço multidimensional, o gradiente é um vetor de derivadas parciais em relação a cada parâmetro.

**3. Algoritmo do Gradiente Descendente:**
   - **Passos do Algoritmo:**
     1. **Inicialização:** Começar com valores iniciais para os parâmetros $\theta$.
     2. **Cálculo do Gradiente:** Calcular o gradiente da função de custo em relação aos parâmetros.
     3. **Atualização dos Parâmetros:** Atualizar os parâmetros na direção oposta ao gradiente:
        \[
        $\theta$ := $\theta$ - $\alpha$ $\nabla$ J($\theta$)
        \]
        onde \($\alpha$) é a taxa de aprendizado e \($\nabla$ J($\theta$)\) é o gradiente da função de custo.
     4. **Iteração:** Repetir os passos 2 e 3 até a convergência.

**4. Tipos de Gradiente Descendente:**
   - **Gradiente Descendente Batch (BGD):**
     - Calcula o gradiente usando todo o conjunto de dados.
     - Vantagem: Atualizações estáveis.
     - Desvantagem: Computacionalmente caro para grandes datasets.
   - **Gradiente Descendente Estocástico (SGD):**
     - Calcula o gradiente usando uma única amostra por vez.
     - Vantagem: Mais rápido e pode escapar de mínimos locais.
     - Desvantagem: Atualizações ruidosas.
   - **Gradiente Descendente Mini-Batch:**
     - Calcula o gradiente usando pequenos lotes de amostras.
     - Combina as vantagens de BGD e SGD.

**5. Taxa de Aprendizado \($\alpha$\):**
   - **Definição:** Controla o tamanho dos passos dados na direção do gradiente.
   - **Escolha da Taxa de Aprendizado:**
     - Taxa de aprendizado muito alta pode fazer o algoritmo divergir.
     - Taxa de aprendizado muito baixa pode tornar a convergência muito lenta.
   - **Métodos de Ajuste da Taxa de Aprendizado:**
     - **Constante:** Um valor fixo durante todo o treinamento.
     - **Decay:** Diminui a taxa de aprendizado ao longo do tempo.
     - **Adaptive:** Ajusta a taxa de aprendizado com base no histórico de atualizações (ex. Adagrad, RMSprop, Adam).

**6. Convergência do Gradiente Descendente:**
   - **Critério de Convergência:** Quando as mudanças nos valores dos parâmetros são menores que um determinado limiar ou quando a função de custo não diminui significativamente.
   - **Desafios:**
     - **Mínimos Locais:** Pode convergir para um mínimo local, especialmente em funções não convexas.
     - **Platôs e Saddle Points:** Pode ficar preso em regiões onde o gradiente é zero, mas não é um mínimo global.

**7. Melhorias e Variações do Gradiente Descendente:**
   - **Momentum:** Acelera o gradiente descendente em direções relevantes e suaviza as oscilações.
     \[
     $v_t$ = $\gamma$ $v_{t-1}$ + $\alpha$ $\nabla$ $J(\theta)$
     \]
     \[
     $\theta$ := $\theta$ - $v_t$
     \]
     onde \($\gamma$\) é o fator de momentum.
   - **Adagrad:** Ajusta a taxa de aprendizado para cada parâmetro com base na magnitude dos gradientes passados.
   - **RMSprop:** Modifica o Adagrad para reduzir a diminuição da taxa de aprendizado.
   - **Adam:** Combina as ideias do momentum e RMSprop, ajustando a taxa de aprendizado com base nos momentos de primeira e segunda ordem dos gradientes.

#### Prática

**1. Importação de Bibliotecas:**
   ```python
   import numpy as np
   import matplotlib.pyplot as plt
   ```

**2. Função de Custo de Exemplo:**
   ```python
   def cost_function(X, y, theta):
       m = len(y)
       predictions = X.dot(theta)
       cost = (1/2*m) * np.sum(np.square(predictions - y))
       return cost
   ```

**3. Implementação do Gradiente Descendente:**
   ```python
   def gradient_descent(X, y, theta, learning_rate, iterations):
       m = len(y)
       cost_history = np.zeros(iterations)
       theta_history = np.zeros((iterations, len(theta)))
       
       for i in range(iterations):
           predictions = X.dot(theta)
           errors = np.subtract(predictions, y)
           sum_delta = (learning_rate/m) * X.transpose().dot(errors)
           theta = theta - sum_delta
           theta_history[i,:] = theta.transpose()
           cost_history[i] = cost_function(X, y, theta)
           
       return theta, cost_history, theta_history
   ```

**4. Exemplo de Uso:**
   ```python
   # Dados de exemplo
   X = 2 * np.random.rand(100,1)
   y = 4 + 3 * X + np.random.randn(100,1)

   # Adicionando intercepto
   X_b = np.c_[np.ones((100, 1)), X]

   # Parâmetros iniciais
   theta = np.random.randn(2,1)

   # Configurações do Gradiente Descendente
   learning_rate = 0.01
   iterations = 1000

   theta, cost_history, theta_history = gradient_descent(X_b, y, theta, learning_rate, iterations)

   print(f'Parâmetros finais: {theta}')
   print(f'Custo final: {cost_history[-1]}')

   plt.plot(cost_history)
   plt.xlabel('Iterações')
   plt.ylabel('Custo')
   plt.title('Histórico do Custo durante o Gradiente Descendente')
   plt.show()
   ```

#### Exercícios






**1. Implementação Básica:**
   - Implemente o algoritmo de gradiente descendente para uma função de custo quadrática simples.
   - Visualize a convergência da função de custo ao longo das iterações.

**2. Análise de Taxa de Aprendizado:**
   - Experimente diferentes valores de taxa de aprendizado e observe como isso afeta a convergência do algoritmo.
   - Plote a função de custo ao longo das iterações para cada taxa de aprendizado.

**3. Comparação de Métodos de Gradiente Descendente:**
   - Implemente e compare o desempenho do gradiente descendente batch, estocástico e mini-batch.
   - Avalie a convergência e o tempo de execução de cada método.

**4. Implementação de Melhorias:**
   - Implemente o gradiente descendente com momentum, Adagrad, RMSprop e Adam.
   - Compare a velocidade de convergência e a precisão dos diferentes métodos em um problema de regressão linear.

**5. Projeto Final:**
   - Escolha um problema de aprendizado de máquina, como a regressão linear ou a classificação com redes neurais.
   - Treine o modelo usando diferentes variantes do gradiente descendente.
   - Documente as observações sobre a convergência, tempo de execução e precisão dos modelos.

Este conteúdo oferece uma visão aprofundada sobre o gradiente descendente, combinando teoria com prática e exercícios para consolidar o aprendizado.
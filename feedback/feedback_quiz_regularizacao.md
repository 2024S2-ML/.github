### Regularização L1 e L2

#### 1. Qual é o principal objetivo da regularização em machine learning?
**Resposta correta: B) Prevenir overfitting**
- Feedback: A regularização é utilizada principalmente para prevenir o overfitting, que ocorre quando o modelo se ajusta muito bem aos dados de treinamento, mas não generaliza bem para novos dados.

#### 2. Qual função de custo é usada na regularização L1?
**Resposta correta: A) Soma dos valores absolutos dos coeficientes**
- Feedback: A regularização L1 usa a soma dos valores absolutos dos coeficientes para adicionar uma penalidade ao modelo.

#### 3. A regularização L1 é também conhecida como:
**Resposta correta: B) Lasso**
- Feedback: A regularização L1 é conhecida como Lasso (Least Absolute Shrinkage and Selection Operator), que ajuda na seleção de features eliminando alguns coeficientes completamente.

#### 4. Qual função de custo é usada na regularização L2?
**Resposta correta: B) Soma dos quadrados dos coeficientes**
- Feedback: A regularização L2 usa a soma dos quadrados dos coeficientes para adicionar uma penalidade ao modelo.

#### 5. A regularização L2 é também conhecida como:
**Resposta correta: A) Ridge**
- Feedback: A regularização L2 é conhecida como Ridge, que reduz todos os coeficientes de forma proporcional.

#### 6. Qual é o efeito principal da regularização L1 nos coeficientes do modelo?
**Resposta correta: B) Elimina alguns coeficientes completamente**
- Feedback: A regularização L1 pode resultar em coeficientes exatamente zero, efetivamente eliminando algumas features do modelo.

#### 7. Qual é o efeito principal da regularização L2 nos coeficientes do modelo?
**Resposta correta: A) Reduz todos os coeficientes igualmente**
- Feedback: A regularização L2 reduz todos os coeficientes de forma proporcional, mas não os elimina completamente.

#### 8. A função de custo da regularização L1 é dada por:
**Resposta correta: B) \(\frac{1}{2m} \sum_{i=1}^{m} (h_{\theta}(x^{(i)}) - y^{(i)})^2 + \lambda \sum_{j=1}^{n} |\theta_j|\)**
- Feedback: A função de custo da regularização L1 inclui uma penalidade que é a soma dos valores absolutos dos coeficientes dos parâmetros do modelo.

#### 9. A função de custo da regularização L2 é dada por:
**Resposta correta: A) \(\frac{1}{2m} \sum_{i=1}^{m} (h_{\theta}(x^{(i)}) - y^{(i)})^2 + \lambda \sum_{j=1}^{n} \theta_j^2\)**
- Feedback: A função de custo da regularização L2 inclui uma penalidade que é a soma dos quadrados dos coeficientes dos parâmetros do modelo.

#### 10. Elastic Net combina:
**Resposta correta: A) Penalizações L1 e L2**
- Feedback: Elastic Net é uma técnica de regularização que combina as penalidades de L1 (Lasso) e L2 (Ridge), oferecendo os benefícios de ambas.

#### 11. Qual biblioteca Python é comumente usada para implementar regularização L1 e L2?
**Resposta correta: C) Scikit-Learn**
- Feedback: Scikit-Learn é uma biblioteca popular em Python para machine learning, que inclui implementações de regularização L1 e L2.

#### 12. A regularização L1 é útil para:
**Resposta correta: A) Seleção de features**
- Feedback: A regularização L1 pode eliminar completamente alguns coeficientes, tornando-se útil para a seleção de features importantes no modelo.

#### 13. O parâmetro de regularização \(\lambda\) controla:
**Resposta correta: B) A quantidade de penalização aplicada**
- Feedback: O parâmetro \(\lambda\) controla a intensidade da penalização aplicada aos coeficientes, ajustando o balanceamento entre ajuste do modelo e regularização.

#### 14. Qual das seguintes é uma desvantagem da regularização L1?
**Resposta correta: B) Pode ser instável quando há alta correlação entre features**
- Feedback: A regularização L1 pode ser instável e apresentar variabilidade nos coeficientes quando há alta correlação entre as features do modelo.

#### 15. Qual das seguintes é uma vantagem da regularização L2?
**Resposta correta: C) Mais estável em presença de features altamente correlacionadas**
- Feedback: A regularização L2 tende a ser mais estável e menos sensível a alta correlação entre features, distribuindo a penalização de forma mais uniforme.

### Funções de Custo

#### 16. Qual é a função de custo mais comum em problemas de regressão?
**Resposta correta: C) Erro Quadrático Médio (MSE)**
- Feedback: O Erro Quadrático Médio (MSE) é a função de custo mais comum em problemas de regressão, pois penaliza mais severamente os erros maiores.

#### 17. A função de custo MSE é calculada como:
**Resposta correta: B) Média dos quadrados das diferenças entre previsões e valores reais**
- Feedback: O MSE calcula a média dos quadrados das diferenças entre as previsões do modelo e os valores reais, enfatizando grandes erros.

#### 18. O que caracteriza o Erro Absoluto Médio (MAE)?
**Resposta correta: C) Usa os valores absolutos das diferenças entre previsões e valores reais**
- Feedback: O MAE usa os valores absolutos das diferenças entre as previsões do modelo e os valores reais, sendo menos sensível a outliers comparado ao MSE.

#### 19. Qual é a principal desvantagem do MSE?
**Resposta correta: B) Sensível a outliers**
- Feedback: O MSE é muito sensível a outliers, pois os erros são elevados ao quadrado, amplificando a penalização de grandes desvios.

#### 20. A Huber Loss combina:
**Resposta correta: C) MSE e MAE**
- Feedback: A Huber Loss combina os benefícios do MSE e do MAE, sendo menos sensível a outliers enquanto ainda penaliza severamente grandes erros.

#### 21. Qual função de custo é mais utilizada em problemas de classificação?
**Resposta correta: C) Entropia Cruzada**
- Feedback: A Entropia Cruzada é amplamente utilizada em problemas de classificação, especialmente em classificação binária e multi-classe.

#### 22. A Entropia Cruzada é calculada como:
**Resposta correta: D) Média da soma dos produtos entre valores reais e o log das previsões**
- Feedback: A Entropia Cruzada calcula a média da soma dos produtos entre os valores reais e o log das previsões, medindo a diferença entre as distribuições de probabilidade predita e real.

#### 23. A Hinge Loss é usada principalmente em:
**Resposta correta: B) Máquinas de Vetores de Suporte (SVMs)**
- Feedback: A Hinge Loss é comumente utilizada em Máquinas de Vetores de Suporte (SVMs) para problemas de classificação binária.

#### 24. A Logistic Loss é utilizada em:
**Resposta correta: B) Regressão Logística**
- Feedback: A Logistic Loss é utilizada em regressão logística para medir a diferença entre as previsões probabilísticas e os valores reais.

#### 25. A Softmax Loss é utilizada em:
**Resposta correta: C) Classificação Multi-Classe**
- Feedback: A Softmax Loss é usada em problemas de classificação multi-classe para converter scores de logits em probabilidades.

#### 26. A divergência Kullback-Leibler mede:
**Resposta correta: A) A diferença entre duas distribuições de probabilidade**
- Feedback: A divergência Kullback-Leibler mede a diferença entre duas distribuições de probabilidade, quantificando quão uma distribuição diverge da outra.

#### 27. Qual função de custo é menos sensível a outliers que MSE?
**Resposta correta: A) MAE**
- Feedback: O MAE é menos sensível a outliers que o MSE, pois não eleva os erros ao quadrado, resultando em uma penalização mais uniforme.

#### 28. Qual função de custo é mais sensível a previsões erradas com alta confiança?
**Resposta correta: C) Entropia Cruzada**
- Feedback: A Entropia Cruzada penaliza severamente as previsões erradas feitas com alta confiança, tornando-se uma escolha eficaz para modelos de classificação.

#### 29. Qual das seguintes é uma desvantagem da Entropia Cruzada?
**Resposta correta: B) Pode ser sensível a previsões extremamente erradas**
- Feedback: A Entropia Cruzada pode ser sensível a previsões extremamente erradas, o que pode resultar em altos valores de perda.

#### 30. Em qual problema é mais adequado usar MAE em vez de MSE?
**Resposta correta: B) Quando há muitos outliers nos dados**
- Feedback: O MAE é mais adequado quando há muitos outliers nos dados, pois trata os erros de forma mais uniforme sem amplificar a penalização de grandes desvios.

#### 31. Qual função de custo combina os benefícios do MSE e MAE?
**Resposta correta: C) Huber Loss**
- Feedback: A Huber Loss combina os benefícios do MSE e MAE, proporcionando uma abordagem equilibrada que é menos sensível a outliers enquanto ainda penaliza grandes erros.


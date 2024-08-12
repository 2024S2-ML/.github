### Questões Básicas

1. **Qual é a primeira etapa no ciclo de vida de um modelo de Machine Learning?**  
   **Feedback:** A definição do problema é crucial, pois orienta todas as etapas subsequentes do projeto de Machine Learning. Compreender o problema ajuda a definir quais dados são necessários e quais métricas serão usadas para avaliar o sucesso.

2. **O que é utilizado para ajustar os hiperparâmetros de um modelo?**  
   **Feedback:** O dataset de validação é usado para ajustar os hiperparâmetros, ajudando a otimizar o desempenho do modelo sem introduzir viés, pois não é usado diretamente no treinamento.

3. **Qual técnica de divisão de dataset é essencial para séries temporais?**  
   **Feedback:** A divisão por séries temporais é essencial para manter a sequência temporal dos dados, evitando vazamento de informações futuras no treinamento e garantindo uma avaliação mais realista do modelo.

4. **Qual é o principal objetivo da etapa de Feature Selection?**  
   **Feedback:** A seleção de features visa identificar e reter as variáveis mais relevantes para o modelo, o que pode melhorar a performance e reduzir o overfitting.

5. **Qual métrica é comumente usada para avaliar modelos de classificação?**  
   **Feedback:** O F1-Score é uma métrica importante para avaliar a performance de modelos de classificação, especialmente em cenários com classes desbalanceadas, pois considera tanto a precisão quanto o recall.

6. **Qual é a principal função do dataset de teste?**  
   **Feedback:** O dataset de teste avalia a capacidade do modelo de generalizar para dados novos e não vistos, fornecendo uma medida final do desempenho do modelo.

7. **Qual técnica de split assegura que a distribuição das classes seja preservada em cada conjunto?**  
   **Feedback:** A divisão estratificada mantém a distribuição das classes consistente entre os conjuntos de treino e teste, o que é crucial para evitar viés e garantir uma avaliação precisa.

8. **Em qual etapa do ciclo de vida do Machine Learning ocorre a escolha das métricas de avaliação?**  
   **Feedback:** A escolha das métricas de avaliação é feita na etapa de avaliação do modelo para garantir que a performance seja medida de acordo com os objetivos definidos inicialmente.

9. **O que é model drift e por que deve ser monitorado?**  
   **Feedback:** O model drift refere-se a mudanças na distribuição dos dados ao longo do tempo, o que pode afetar a performance do modelo. Monitorar o drift ajuda a manter a eficácia do modelo e a atualizar ou re-treinar conforme necessário.

10. **Qual é a principal vantagem da técnica K-Fold Cross-Validation?**  
    **Feedback:** O K-Fold Cross-Validation permite que todos os dados sejam usados tanto para treinamento quanto para validação, fornecendo uma estimativa mais robusta do desempenho do modelo.

### Questões Avançadas

1. **Durante a etapa de Feature Selection, qual técnica pode ser usada para identificar a importância de cada variável no modelo?**  
   **Feedback:** A importância das features pode ser avaliada usando modelos como Random Forests, que fornecem uma medida direta da contribuição de cada variável para a previsão.

2. **Qual abordagem de validação é mais indicada para problemas de classificação multiclasse com classes extremamente desbalanceadas?**  
   **Feedback:** A validação estratificada (Stratified K-Fold) garante que a distribuição das classes seja mantida em cada fold, o que é crucial para obter uma avaliação justa em problemas com classes desbalanceadas.

3. **Em um problema de Machine Learning, o modelo apresentou alta acurácia no conjunto de treino, mas baixo desempenho no conjunto de teste. Qual técnica seria mais adequada para resolver este problema?**  
   **Feedback:** A regularização ajuda a reduzir o overfitting ao penalizar a complexidade do modelo, melhorando a generalização para dados novos.

4. **Ao trabalhar com séries temporais, por que o método de divisão aleatória do dataset pode levar a resultados enganosos?**  
   **Feedback:** A divisão aleatória ignora a ordem temporal dos dados, o que pode resultar em vazamento de informações e avaliações incorretas do desempenho do modelo.

5. **Como o conceito de Bias-Variance Tradeoff influencia a escolha do modelo durante o ciclo de vida do Machine Learning?**  
   **Feedback:** O Bias-Variance Tradeoff é essencial para balancear a complexidade do modelo e a capacidade de generalização. Modelos muito complexos podem ter baixa bias e alta variance, enquanto modelos simples podem ter alta bias e baixa variance.

6. **No contexto de validação cruzada, qual é a principal vantagem do método Nested Cross-Validation em relação ao K-Fold Cross-Validation simples?**  
   **Feedback:** O Nested Cross-Validation oferece uma estimativa imparcial do desempenho ao ajustar os hiperparâmetros e avaliar o modelo em um processo separado, o que é mais robusto para modelos complexos.

7. **Quando se utiliza a técnica de Dropout durante o treinamento de um modelo de rede neural, qual é o efeito esperado no comportamento do modelo?**  
   **Feedback:** O Dropout ajuda a evitar o overfitting ao desativar aleatoriamente neurônios durante o treinamento, promovendo uma maior generalização do modelo.

8. **Em uma pipeline de Machine Learning, onde você colocaria a normalização dos dados e por quê?**  
   **Feedback:** A normalização deve ser feita após a divisão dos dados para evitar vazamento de informações do conjunto de teste e garantir que a transformação seja aplicada de maneira consistente.

9. **Qual técnica de avaliação de modelo seria mais apropriada ao lidar com um conjunto de dados altamente desbalanceado, onde a classe positiva é de particular interesse?**  
   **Feedback:** O F1-Score é uma métrica adequada para conjuntos de dados desbalanceados, pois considera tanto a precisão quanto o recall, fornecendo uma visão equilibrada do desempenho do modelo.

10. **Ao operacionalizar um modelo de Machine Learning em produção, qual é uma prática recomendada para monitorar a saúde do modelo ao longo do tempo?**  
    **Feedback:** Monitorar métricas de desempenho regularmente ajuda a identificar mudanças no comportamento do modelo, possibilitando ajustes ou re-treinamento para manter a eficácia ao longo do tempo.
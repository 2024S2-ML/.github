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
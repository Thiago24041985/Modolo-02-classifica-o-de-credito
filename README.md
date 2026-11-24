adiciona projeto de previsao de inadimplencia em cartoes de credito

- Implementa fluxo completo seguindo a metodologia CRISP-DM
- Realiza analise exploratoria univariada e bivariada (idade e tempo de emprego)
- Prepara dados categoricos com variaveis dummy
- Treina e avalia modelo Random Forest ajustando hiperparametros (n_estimators)

- ## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python 3**
* **Pandas:** Manipulação e limpeza de dados.
* **Seaborn & Matplotlib:** Visualização de dados e análise exploratória.
* **Scikit-Learn:** Divisão de treino/teste, modelagem (*Random Forest*) e métricas de avaliação.

## 📊 Etapas Desenvolvidas (CRISP-DM)
1. **Entendimento do Negócio:** Definição do problema de risco de crédito e da variável resposta (`mau`).
2. **Entendimento dos Dados:** 
   * Análise univariada (distribuição da variável alvo, posse de imóvel, posse de veículo e histograma de idade).
   * Análise bivariada avaliando a taxa de inadimplência por faixas de `idade` e `tempo_emprego`, identificando que clientes com menor tempo de emprego apresentam maior risco.
3. **Preparação dos Dados:** Tratamento de valores anômalos em `tempo_emprego` e transformação de variáveis categóricas em variáveis *dummy* (`pd.get_dummies`).
4. **Modelagem:** Treinamento do algoritmo `RandomForestClassifier`, testando diferentes quantidades de árvores (`n_estimators`) para otimizar o desempenho.
5. **Avaliação:** Análise de acurácia (atingindo **~97,79%**) e matriz de confusão, incluindo uma simulação de impacto financeiro na aprovação/reprovação de crédito.
6. **Implantação (Conceitual):** Estruturação de como o modelo atuaria em um motor de decisão de crédito.

## 📈 Principais Conclusões
* A base apresenta um forte desbalanceamento (cerca de 2,34% de inadimplentes).
* Variáveis comportamentais e de estabilidade, como o **tempo de emprego**, mostraram forte poder de discriminação de risco na análise bivariada.
* O ajuste no número de estimadores da *Random Forest* permitiu melhorar a 

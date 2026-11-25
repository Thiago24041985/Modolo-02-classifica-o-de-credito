 # 💳 Projeto 01 - Concessão de Cartões de Crédito (CRISP-DM)

Projeto desenvolvido durante o curso **Profissão: Cientista de Dados (EBAC)** com o objetivo de construir uma análise exploratória e preditiva para avaliar o risco de inadimplência na concessão de cartões de crédito.

## 💡 Como elaborei este projeto

Estruturei o desenvolvimento seguindo as etapas da metodologia **CRISP-DM**, partindo da compreensão do problema de negócio até a análise visual das variáveis que influenciam o risco de crédito:

1. **Entendimento do Negócio e dos Dados:** Comecei mapeando o objetivo principal — identificar clientes com risco de atraso igual ou superior a 90 dias em 12 meses (`mau`) — e inspecionando o dicionário de dados e as 16 variáveis disponíveis na base (`demo01.csv`, com 16.650 registros).
2. **Preparação do Ambiente:** Importei e organizei as bibliotecas essenciais para manipulação de dados, visualização e modelagem (`pandas`, `seaborn`, `matplotlib` e `scikit-learn`).
3. **Análise Univariada:**
   * Verifiquei a proporção da variável resposta (`mau`), identificando uma taxa base de aproximadamente **2,34% de inadimplentes**.
   * Construí **gráficos de barras** para variáveis categóricas (`posse_de_veiculo` e `posse_de_imovel`) para entender o perfil patrimonial dos proponentes.
   * Criei **histogramas** para variáveis contínuas (`tempo_emprego` e `idade`), realizando ajustes de escala (tratando valores negativos extremos em `tempo_emprego`) para melhorar a visualização da distribuição.
4. **Análise Bivariada:** Segmentei variáveis numéricas em quartis (`pd.qcut`) para cruzar com a taxa média de inadimplência, avaliando visualmente como `idade` e `tempo_emprego` discriminam o risco de crédito ao longo das faixas.

## 🛠️ Tecnologias Utilizadas
* **Python 3**
* **Pandas** (manipulação, agrupamento e discretização de dados)
* **Matplotlib & Seaborn** (visualização univariada e bivariada)
* **Scikit-Learn** (preparação para modelagem preditiva com Random Forest)

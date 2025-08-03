# Estudo de Previsão de Evasão de Clientes (Churn) - parte 2

Este projeto foca na análise dos fatores que influenciam a evasão de clientes (Churn) e no desenvolvimento de um modelo preditivo para identificar clientes em risco. O objetivo é fornecer insights acionáveis para estratégias de retenção.

📌 **Objetivo**
O principal objetivo deste estudo é:
- Identificar os principais fatores e padrões de comportamento que levam os clientes a evadir.
- Desenvolver e comparar modelos de Machine Learning para prever a probabilidade de Churn.
- Propor estratégias de retenção de clientes baseadas nos insights obtidos da análise e do modelo.

🛠️ **Tecnologias e Bibliotecas Utilizadas**
- Python 3.x
- Pandas (para manipulação e análise de dados)
- NumPy (para operações numéricas)
- Matplotlib e Seaborn (para visualização de dados)
- Scikit-learn (para pré-processamento, modelagem e avaliação de Machine Learning)
- Imbalanced-learn (para técnicas de balanceamento de classes como SMOTE e NearMiss)

📂 **Estrutura do Projeto**
- `[Nome do seu Notebook].ipynb`: O notebook principal contendo todas as etapas do estudo, desde a preparação dos dados até a modelagem e interpretação.
- `README.md`: Este arquivo de apresentação do projeto.
- `/content/dados_tratados.csv`: O arquivo de dados utilizado para a análise (presumindo que este é o caminho no ambiente Colab).

🧪 **Etapas Realizadas**
1.  **Carregamento e Limpeza dos Dados:** Inclusão e limpeza inicial do conjunto de dados, remoção de colunas identificadas como irrelevantes ('ID_Cliente') ou redundantes ('Contas_Diarias' devido a multicolinearidade perfeita).
2.  **Pré-processamento:** Tratamento de variáveis categóricas usando One-Hot Encoding.
3.  **Análise de Desequilíbrio de Classes:** Identificação e tratamento do desequilíbrio na variável alvo ('Churn') criando três bases de dados: Original, Undersampling (NearMiss) e Oversampling (SMOTE).
4.  **Divisão e Normalização:** Separação de cada base em conjuntos de treino e teste e normalização das features numéricas.
5.  **Modelagem Preditiva:** Treinamento de modelos de Regressão Logística e Random Forest nas três bases de dados.
6.  **Avaliação Comparativa:** Avaliação do desempenho dos modelos com métricas apropriadas para dados desequilibrados (Precisão, Recall, F1-score, Matriz de Confusão), identificando o modelo Random Forest treinado com SMOTE como o de melhor performance.
7.  **Interpretação do Modelo:** Análise da importância das features no melhor modelo para identificar os principais fatores que influenciam o Churn.
8.  **Experimentação (Seleção de Features):** Teste do modelo Random Forest com SMOTE utilizando apenas as top 10 features mais importantes, comparando o desempenho com o modelo completo.

📈 **Resultados e Insights**
- O desequilíbrio de classes é um fator importante a ser considerado na modelagem de Churn.
- Técnicas de balanceamento, especialmente o Oversampling (SMOTE), foram eficazes em melhorar o desempenho dos modelos na identificação da classe minoritária (Churn).
- O modelo **Random Forest treinado com Oversampling (SMOTE)** demonstrou o melhor equilíbrio entre Precisão e Recall para a previsão de Churn.
- Os principais fatores que mais influenciam a evasão de clientes incluem: **Valor Mensal**, **Tempo de Cliente**, **Valor Total**, **Tipo de Contrato (principalmente contratos mensais)**, **Uso de Serviços Adicionais (como Suporte Técnico e Segurança Online)**, e **Tipo de Internet (Fibra Óptica)**.

**Estratégias de Retenção Sugeridas:**
- Implementar programas de engajamento para clientes novos.
- Incentivar a adesão a contratos de longo prazo.
- Focar na proposta de valor de serviços adicionais.
- Desenvolver abordagens específicas para segmentos de clientes em risco, como aqueles com contratos mensais ou serviço de fibra óptica.

👨‍💻 **Autor**
Este projeto foi desenvolvido por Jorge Fernandes.

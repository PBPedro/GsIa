# 📊 Previsão do Nível de Estresse em Abrigos

Este projeto de IA tem como objetivo prever o **nível médio de estresse** em abrigos para pessoas em situações vulneráveis. Ele utiliza **Machine Learning (Random Forest)** para identificar quais fatores contribuem mais para o estresse e gerar previsões baseadas em novos dados.

---

## 🟩 Descrição do Problema

A gestão de abrigos é desafiadora: níveis elevados de estresse afetam tanto a equipe quanto os abrigados.  
Este projeto visa fornecer uma ferramenta de **análise preditiva** para prever o nível de estresse médio, considerando fatores como:

- **Temperatura interna do abrigo (°C)**
- **Nível de ruído (dB)**
- **Total de pessoas no abrigo**
- **Número de pessoas sendo atendidas**

---

## 🟩 Metodologia Utilizada

O projeto foi dividido nas seguintes etapas:

1️⃣ **Exploração de Dados:**  
- Leitura do dataset `dados_abrigo.xlsx`  
- Visualização simples da relação entre temperatura e estresse médio  

2️⃣ **Levantamento de Hipótese:**  
- Hipótese: **temperatura** e **ruído** aumentam o estresse médio, enquanto o número de pessoas atendidas pode ajudar a reduzi-lo.

3️⃣ **Preparação e Treinamento do Modelo:**  
- Separação das variáveis de entrada (X) e alvo (y).  
- Normalização dos dados usando `StandardScaler`.  
- Divisão dos dados em **treino (80%)** e **teste (20%)**.  
- Treinamento com o algoritmo **Random Forest Regressor**.

4️⃣ **Avaliação do Modelo:**  
- Avaliação pelo coeficiente de determinação (**R²**).  
- Armazenamento do modelo e scaler com **Joblib**.

5️⃣ **Previsão com Dados Reais:**  
- Pergunta de dados reais ao usuário via input.  
- Normalização e previsão do nível médio de estresse.

6️⃣ **Explicabilidade com SHAP:**  
- Cálculo da contribuição real de cada variável para o estresse previsto.

7️⃣ **Visualização Final:**  
- Gráfico de evolução do estresse médio nos últimos 5 períodos + o período atual previsto.

---

## 🟩 Resultados Obtidos

- O modelo obteve um desempenho de **R² = {valor dinâmico}** (exemplo: `0.80`).  
- Ele foi capaz de prever níveis médios de estresse entre **1 e 5** para novos dados reais inseridos.  
- As variáveis de maior contribuição para o estresse foram destacadas com SHAP, trazendo insights relevantes para melhorar a gestão do abrigo.

---

## 🟩 Conclusões

- O modelo **Random Forest** mostrou-se eficaz para prever o estresse médio em abrigos com as variáveis analisadas.  
- A ferramenta permite aos gestores identificar fatores de maior impacto e atuar para **reduzir o estresse coletivo**.  
- Para ganhos adicionais, recomenda-se:  
  - Coletar mais dados (ampliar a base de treinamento).  
  - Ajustar hiperparâmetros ou testar outros modelos (p.ex.: Gradient Boosting).  

---

## 🟩 Justificativa da Escolha do Modelo e Técnica Aplicada

- **Modelo Escolhido:** **Random Forest Regressor**  
- **Por quê?**  
  - É um modelo **robusto e versátil** para problemas de regressão, especialmente com dados que possuem **relações não-lineares**.  
  - Suporta facilmente múltiplas variáveis e lida bem com **pequenas amostras**.  
  - Possui **mecanismo de ensemble** que reduz o risco de overfitting em relação a árvores de decisão simples.  
  - Além disso, foi possível integrar o SHAP para interpretar as contribuições de cada variável de forma **explicável**.

---

## 📦 Tecnologias Utilizadas

- **Bibliotecas:**  
  - pandas  
  - matplotlib  
  - scikit-learn  
  - shap  
  - joblib  
  - openpyxl  

---

## ⚙️ Como Executar o Script

1️⃣ Instale as dependências:  
```bash
pip install pandas scikit-learn joblib shap matplotlib openpyxl

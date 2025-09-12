# 📊 Pós-graduação em Ciência de Dados (2025/2026)  

**Escola Superior de Tecnologia da Universidade Estadual do Amazonas - EST/UEA**  
**Disciplina:** Fundamentos de Machine Learning  
**Professor:** Prof. Me. Mario Bessa  

📂 **Repositório do Projeto Acadêmico no GitHub:** [e-SUS_Sinan_Mpox_ML-Workflow](https://github.com/Cristie-Lima/e-SUS_Sinan_Mpox_ML-Workflow)  
📂 **Apresentação**: [apresentacao_cristie_mod6_proj_final](https://notebooksharing.space/view/030aed325c8e09961eb80bfe1b2bde6ad5e306ada46882d009ed90773ff9b449#displayOptions=show-linenos)

👩‍🎓 **Aluna:**  
- A. Cristiane R. Lima (Cristie)  

📅 **Data:** 03 de setembro de 2025  

---

## 📌 Contextualização do Projeto

A **Mpox (Monkeypox)** é uma doença infecciosa emergente que ganhou atenção internacional devido ao seu potencial de disseminação e impacto na saúde pública.  

No Brasil, o **sistema e-SUS Sinan** tem sido fundamental para o registro e monitoramento dos casos, permitindo a construção de bases de dados estruturadas para análise epidemiológica.  

Este projeto tem como objetivo aplicar **técnicas de aprendizado de máquina** para explorar, tratar e modelar os dados disponíveis, com foco na geração de **insights preditivos** que possam apoiar estratégias de vigilância e resposta.  

A abordagem contempla desde o **pré-processamento e análise exploratória (EDA)** até a **engenharia de atributos, balanceamento e modelagem supervisionada**, seguindo diretrizes metodológicas discutidas em ambiente acadêmico.  

---

## ✅ Objetivos Gerais
- Estruturar um **workflow completo de Machine Learning aplicado à saúde pública**.  
- Validar diferentes estratégias de **pré-processamento, codificação e balanceamento**.  
- Comparar modelos supervisionados para **classificação binária** em múltiplos targets.  
- Gerar insights que possam **auxiliar vigilância epidemiológica** e apoiar políticas públicas.  

📌 **Observação:** Este projeto é de caráter acadêmico e não substitui protocolos médicos ou epidemiológicos oficiais.  

---

## ⚙️ Estrutura dos Notebooks

### 🔹 Parte 1 – Pré-processamento & EDA  
Arquivo: `cristie_mod6_proj_final_parte_1.ipynb`  

1. **Aquisição, limpeza e imputação de dados**  
   - Correção de tipos, remoção/correção de registros inválidos.  
   - Imputação de valores ausentes com média/moda.  

2. **Visualizações exploratórias (EDA)**  
   - Histogramas e boxplots (NU_IDADE_N, CONTAG_CD4).  
   - Identificação e interpretação de outliers.  
   - Síntese interpretativa consolidada.  

3. **Codificação de variáveis categóricas**  
   - Uso de `OneHotEncoder` (não há variáveis ordinais).  
   - Auditoria dimensional (85 → 1392 colunas).  

4. **Escalonamento de variáveis numéricas**  
   - Teste com `StandardScaler` e `MinMaxScaler`.  
   - Registro de impacto gráfico/estatístico.  

5. **Seleção de atributos**  
   - Auditoria pós-correlação (1392 → 1019 colunas).  

6. **Persistência do dataset pré-processado**  
   - Serialização do `df_prep` em `.parquet`.  

---

### 🔹 Parte 2 – Engenharia de Atributos & Modelagem  
Arquivo: `cristie_mod6_proj_final_parte_2.ipynb`  

1. **Carregamento dos dados**  
   - Desserialização do `df_prep`.  

2. **Engenharia de Atributos**  
   - Criação dos targets binários:  
     - `target_hosp` (hospitalização).  
     - `target_obito_any` (óbito por qualquer causa).  
     - `target_obito_mpx` (óbito por Mpox).  

3. **Análise de classes**  
   - Distribuição dos targets binários (barras horizontais com percentuais).  

4. **Balanceamento dos dados**  
   - Aplicação sequencial: `Tomek Links → SMOTE`.  
   - Justificativa metodológica (sensibilidade de métricas).  

5. **Treinamento e Validação de Modelos**  
   - Classificação binária com múltiplos algoritmos:  
     - Naive Bayes, Árvore de Decisão, Random Forest, kNN, Regressão Logística, SVM, Redes Neurais.  
   - Comparação de desempenho com diferentes escalonadores.  
   - Validação cruzada estratificada.  
   - Métricas robustas: **F1-score, AUC-PR**.  

6. **Persistência e Uso do Modelo Final**  
   - Serialização do pipeline completo (`pré-processamento + balanceamento + modelo`) em `.pkl`.  
   - Predição em novos dados.  

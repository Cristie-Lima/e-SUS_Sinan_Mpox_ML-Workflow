# 📊 Pós-graduação em Ciência de Dados (2025/2026)  

**Escola Superior de Tecnologia da Universidade Estadual do Amazonas - EST/UEA**  
**Disciplina:** Fundamentos de Machine Learning  
**Professor:** Prof. Me. Mario Bessa  

📂 **Repositório do Projeto Acadêmico no GitHub:** [e-SUS_Sinan_Mpox_ML-Workflow](https://github.com/Cristie-Lima/e-SUS_Sinan_Mpox_ML-Workflow)  

👩‍🎓 **Alunos:**  
- A. Cristiane R. Lima (Cristie)  
- José Henrique Santos Cavalcante (Henrique)  

📅 **Data:** 03?? de setembro de 2025  

---

## 📌 Contextualização do Projeto

A **Mpox (Monkeypox)** é uma doença infecciosa emergente que ganhou atenção internacional devido ao seu potencial de disseminação e impacto na saúde pública.  

No Brasil, o **sistema e-SUS Sinan** tem sido fundamental para o registro e monitoramento dos casos, permitindo a construção de bases de dados estruturadas para análise epidemiológica.  

Este projeto tem como objetivo aplicar **técnicas de aprendizado de máquina** para explorar, tratar e modelar os dados disponíveis, com foco na geração de **insights preditivos** que possam apoiar estratégias de vigilância e resposta.  

A abordagem contempla desde o **pré-processamento e imputação de dados** até a **construção e uso de modelos supervisionados**, seguindo diretrizes metodológicas discutidas em ambiente acadêmico.

---

## ⚙️ Estrutura dos Notebooks

🔹 **Parte 1 – Pré-processamento (`cristie_mod6_proj_final_parte_1.ipynb`)**  
1. **Limpeza de dados incorretos**  
   - Identificação de valores inválidos (ex.: idades < 0, datas futuras, preços absurdos).  
   - Correção ou remoção das entradas inconsistentes.  

2. **Imputação de valores faltantes**  
   - Identificação de valores ausentes (`NaN`, `?`).  
   - Aplicação de técnicas de imputação: média e moda.  

3. **Codificação de variáveis categóricas**  
   - Uso de `OrdinalEncoder` e `OneHotEncoder`.  

4. **Escalonamento de variáveis numéricas**  
   - Uso de `StandardScaler` e `MinMaxScaler`.  

---

🔹 **Parte 2 – Modelagem (`cristie_mod6_proj_final_parte_2.ipynb`)**  
5. **Balanceamento dos dados**  
   - Verificação de desbalanceamento da variável alvo.  
   - Aplicação dos algoritmos `Tomek` e `SMOTE`.  
   - Avaliação do impacto no desempenho dos modelos.  

6. **Treinamento de Modelos de Machine Learning**  
   - Tarefas: classificação binária.  
   - Modelos avaliados:  
     - Naive Bayes  
     - Árvore de Decisão  
     - Random Forest  
     - kNN (K-Nearest Neighbors)  
     - Regressão Logística  
     - SVM (Support Vector Machine)  
     - Redes Neurais Artificiais  
   - Estratégias:  
     - Avaliar impacto das técnicas de imputação e codificação.  
     - Ajustar hiperparâmetros via GridSearch e Validação Cruzada.  
     - Evitar overfitting.  

7. **Uso do modelo treinado**  
   - Serialização dos transformadores e do modelo.  
   - Predição em novos dados.  

---

## ✅ Objetivos Gerais
- Estruturar um **workflow completo de Machine Learning aplicado à saúde pública**.  
- Validar diferentes estratégias de **pré-processamento e balanceamento de dados**.  
- Comparar modelos supervisionados para **classificação binária**.  
- Gerar insights que possam **auxiliar vigilância epidemiológica** e políticas públicas.  

---

📌 **Observação:** Este projeto é de caráter acadêmico e não substitui protocolos médicos ou epidemiológicos oficiais.  


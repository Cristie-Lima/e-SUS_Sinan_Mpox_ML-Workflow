---
# **Ciência de Dados: Fundamentos de Machine Learning**

---
## **Pós-graduação em Ciência de Dados (2025/2026)**


**Escola Superior de Tecnologia da Universidade Estadual do Amazonas - EST/UEA**
    
**Disciplina:** Fundamentos de Machine Learning

**Prof. Me.:** Mario Bessa

_**Projeto Acadêmico no Github:** e-SUS_Sinan_Mpox_ML-Workflow_



# **Machine Learning Workflow**
Este notebook contém o fluxo completo de pré-processamento e modelagem para o dataset [e-SUS Sinan/Mpox](https://opendatasus.saude.gov.br/ne/dataset/mpox), seguindo uma estrutura padronizada.
Foi desenvolvido a partir do notebook-base apresentado e explicado ao longo as aulas teórico-práticas em laboratório do Professor.


**Instruções:**
Realizar os preprocessamentos abaixo:

---
**Atividade 1: Limpar dados incorretos**
- Identificar valores numéricos inválidos, por exemplo, idades em < 0, data acima da data atual ou zero, preços absurdos etc
- Remover ou corrigir essas entradas
---
**Atividade 2: Imputação de valores faltantes**
- Identificar valores faltantes: NaN e ?
- Usar as técnicas: média e moda
---
**Atividade 3: Codificação de variáveis categóricas (OrdinalEncoder e OneHotEncoder)**

---

**Atividade 4: Escalonamento de variáveis numéricas (StandardScaler e MinMaxScaler)**

---

**Atividade 5: Balanceamento dos dados (Tomek e Smote)**
- Checar se os dados estão desbalanceados
- Aplicar os algoritmos Tomek e Smote
- Avaliar impacto no desempenho dos modelos treinados
---
**Atividade 6: Treinamento dos modelos de Machine Learning**
- Comparar modelos: testar diferentes classificadores
    - Classificação binária
    - Modelos: Naive Bayes, Árvore de Decisão, Random Forest, Aprendizagem baseada em instâncias - kNN, Regressão logística, SVM, Redes Neurais Artificiais 
- Medir desempenho com métricas adequadas e evitar overfitting
- Investigar como técnicas de imputação e codificação impactam os resultados
- Escolher e ajustar modelos (gridsearch/validação cruzada)
---
**Atividade 7: Usar o modelo treinado**
- Salvar os transformadores
- Salvar o modelo
- Fazer predição usando dados novos
---




## 📌 Resultados das etapas cumpridas na primeira fase  do Projeto. 

Ref. Notebook: [cristie_mod6_proj_final_parte_1.ipynb](https://github.com/Cristie-Lima/e-SUS_Sinan_Mpox_ML-Workflow/blob/main/cristie_mod6_proj_final_parte_1.ipynb)

## 📌 Fluxo de Persistência de Dados e Modelos
```mermaid
flowchart TD

    A["Dataset bruto: df_raw"] --> B["Pré-processamento: df_prep"]
    B --> C["Engenharia de atributos: df_feateng"]
    C --> D["Codificação categóricas: df_eng_ohe"]
    D --> |Persistência| E["💾 Salvar em .parquet"]

    D --> F["Escalonamento: StandardScaler / MinMaxScaler"]
    F --> |Persistência| G["💾 Salvar escalonadores em .pkl"]
    F --> H["Modelagem"]

    E --> H
    G --> H

    H["Modelagem supervisionada"] --> I["Modelos treinados"]
    I --> |Persistência| J["💾 Salvar modelos em .pkl"]

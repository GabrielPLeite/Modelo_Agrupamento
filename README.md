# Análise Socioeconômica para Alocação de Auxílio Internacional
![naom_624c15a5a0453](https://github.com/user-attachments/assets/4ee10b5c-d3cf-4312-b65d-320895875ece)

## Descrição
Projeto de identificação de países em situação crítica que precisam de auxílio econômico, com base em dados socioeconômicos. A análise usa clustering para priorizar países que apresentam baixa expectativa de vida, alta mortalidade infantil e baixo PIB per capita.

## Estrutura do Projeto

- **Dataset**: Contém indicadores de saúde, economia e desenvolvimento para vários países.
  - **Principais indicadores**:
    - `child_mort`: Taxa de mortalidade infantil.
    - `life_expec`: Expectativa de vida.
    - `gdpp`: PIB per capita.

## Metodologia

1. **Critérios de Seleção**:
   - Países com baixa expectativa de vida, alta mortalidade infantil e baixo PIB per capita foram priorizados.

2. **Análise e Clusterização**:
   - Dividimos os países em clusters com base nos indicadores para identificar os mais frágeis (Cluster 1).

3. **Cálculo do Índice de Fragilidade**:
   - Com base nos indicadores, foi criado um índice de fragilidade com pesos:
     - Mortalidade Infantil: 40%
     - Expectativa de Vida: 30%
     - PIB per Capita: 20%
     - Renda per Capita: 10%

4. **Distribuição do Auxílio**:
   - O auxílio foi alocado para países do Cluster 1, proporcional ao índice de fragilidade.

## Requisitos de Instalação

```python
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Observações Finais

Este projeto é uma aplicação de ciência de dados para auxiliar na alocação justa de auxílio internacional, priorizando os países em maior necessidade.

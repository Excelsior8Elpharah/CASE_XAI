# Decifrando a Caixa Preta: Tornando Modelos de IA Explicáveis com LIME

## Contextualização e Objetivos

O desafio deste projeto foi desenvolver um modelo preditivo para aprovação de crédito bancário, utilizando um dataset real (como o Statlog - German Credit Data ou similar). Embora modelos preditivos como Random Forest atinjam alta precisão, suas decisões são frequentemente questionadas por clientes, gerentes e órgãos regulatórios, que demandam explicações claras e transparentes para as decisões, especialmente em casos de negação.

Este projeto foca na aplicação da técnica Explainable AI (XAI) usando a biblioteca **LIME (Local Interpretable Model-agnostic Explanations)** para gerar explicações locais detalhadas. O objetivo principal é mostrar, para cada cliente, quais características financeiras (idade, renda, score, histórico de inadimplência, etc.) mais influenciaram a decisão do modelo, permitindo maior transparência e compliance.

---

## Modelo Preditivo Utilizado

- **Algoritmo:** Random Forest Classifier
- **Motivação:** Alta performance em classificação binária, robustez e capacidade de capturar interações não-lineares entre variáveis.
- **Features Utilizadas:**  
  - Renda Mensal  
  - Score de Crédito  
  - Endividamento (%)  
  - Tempo no Emprego (meses)  
  - Histórico de Inadimplência (binário)  
  - Razão Valor Solicitado / Renda (feature criada para contextualizar o valor pedido no crédito)

- **Divisão dos Dados:** 80% treino, 20% teste  
- **Pré-processamento:** Padronização (StandardScaler) aplicada via pipeline

---

## Aplicação do LIME para Explicação Local

Utilizamos o **LIME** para gerar explicações individuais das previsões feitas pelo modelo para cada cliente, mostrando quais variáveis mais impactaram a decisão. Esse processo ajuda a:

- Interpretar decisões complexas do modelo.
- Comunicar os motivos da aprovação ou negação de crédito de forma compreensível para stakeholders.
- Auxiliar em processos de compliance regulatório.
- Identificar possíveis vieses ou inconsistências nas decisões.

As explicações são apresentadas em gráficos de barras que indicam o peso de cada feature na decisão para o caso específico.

---

## Reflexões e Discussão

- A interpretabilidade é crucial para modelos financeiros, pois decisões automáticas impactam diretamente a vida das pessoas.
- LIME possibilita explicações locais, complementando análises globais (ex: importância geral das features).
- Limitações do LIME incluem a aproximação local que pode não refletir o comportamento global do modelo, além de sensibilidade ao ponto de explicação escolhido.
- Explicações claras aumentam a confiança no uso de IA em decisões críticas e reduzem riscos de contestação.

---

## Estrutura do Projeto no GitHub

- **Código-fonte:**  
  - Treinamento do modelo Random Forest  
  - Pré-processamento e criação das features  
  - Implementação do LIME para explicação local  
  - Visualizações exploratórias e análise dos dados  
  - Simulações manuais e em lote para clientes  
- **Outputs:**  
  - Prints e imagens dos gráficos gerados (LIME, matrizes de confusão, distribuições, etc.)  
- **Dataset:** Link para o dataset Statlog (German Credit Data) da UCI ou arquivo CSV utilizado.  
- **requirements.txt:** lista das dependências do projeto para fácil instalação.  
- **README.md:** este arquivo com todas as instruções, contextualização e explicações.

---



# Decifrando a Caixa Preta: Tornando Modelos de IA Explicáveis com LIME

## 📋 Descrição do Projeto

Este projeto visa construir um modelo preditivo para aprovação de crédito bancário utilizando o algoritmo **Random Forest** e aplicar técnicas de Explainable AI (XAI) para tornar as decisões do modelo transparentes e compreensíveis.

Embora modelos de machine learning como Random Forest ofereçam alta performance, suas decisões são frequentemente vistas como uma "caixa preta". A explicação local por meio da biblioteca **LIME (Local Interpretable Model-agnostic Explanations)** permite entender, para cada cliente, quais características mais influenciaram a aprovação ou negação do crédito.

---

## 🎯 Objetivos

- Desenvolver um modelo preditivo robusto para aprovação de crédito.
- Aplicar pré-processamento e engenharia de features para melhorar a qualidade dos dados.
- Usar LIME para gerar explicações locais, facilitando a interpretação das decisões.
- Proporcionar visualizações exploratórias para melhor compreensão do perfil dos clientes.
- Criar funcionalidades para simulação manual e em lote, permitindo análise detalhada para um ou múltiplos clientes.

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Python 3.8+**
- [scikit-learn](https://scikit-learn.org/stable/) — Treinamento e avaliação do modelo Random Forest.
- [LIME](https://github.com/marcotcr/lime) — Geração de explicações locais das previsões.
- [pandas](https://pandas.pydata.org/) e [numpy](https://numpy.org/) — Manipulação e análise dos dados.
- [matplotlib](https://matplotlib.org/) e [seaborn](https://seaborn.pydata.org/) — Visualização dos dados e resultados.
- (Opcional) Google Colab para execução e upload de arquivos CSV.

---

## 📂 Estrutura do Projeto

├── data/
│ └── german_credit_data.csv # Dataset utilizado (Statlog German Credit Data ou similar)
├── notebooks/
│ └── credit_approval_lime.ipynb # Notebook com código completo, análise, treino e explicações
├── requirements.txt # Lista de dependências para instalação rápida
├── README.md # Documentação do projeto
└── outputs/
├── lime_explanations/ # Gráficos e imagens gerados pelo LIME
├── confusion_matrix.png # Matriz de confusão do modelo
├── feature_importance.png # Importância das variáveis
└── exploratory_plots/ # Visualizações exploratórias

yaml
Copiar
Editar

---

## ⚙️ Como Executar

1. **Clone o repositório:**
```bash
git clone https://github.com/seuusuario/seuprojeto-lime-credit.git
cd seuprojeto-lime-credit
Instale as dependências:

bash
Copiar
Editar
pip install -r requirements.txt
Execute o notebook no Jupyter ou Google Colab:

No notebook você poderá:

Fazer upload de um CSV com dados dos clientes.

Realizar pré-processamento e engenharia de features.

Treinar e avaliar o modelo Random Forest.

Gerar explicações locais para cada cliente via LIME.

Visualizar gráficos para análise exploratória e resultados.

📊 Detalhes do Modelo
Algoritmo: Random Forest Classifier

Features principais:

Renda Mensal

Score de Crédito

Endividamento (%)

Tempo no Emprego (meses)

Histórico de Inadimplência (binário)

Razão Valor Solicitado / Renda (feature criada)

Pré-processamento: Padronização via StandardScaler no pipeline

Divisão dos dados: 80% treino / 20% teste

Métricas de avaliação: Acurácia e Matriz de Confusão

🔍 Explicabilidade com LIME
Gera explicações locais para cada previsão individual, identificando as features mais impactantes na decisão.

Facilita a comunicação dos motivos de aprovação ou rejeição do crédito para clientes, gerentes e órgãos reguladores.

Permite simulações manuais e em lote para múltiplos clientes.

Apresenta gráficos de barras com os pesos das variáveis influentes.

📈 Visualizações e Análises Exploratório
Gráficos de dispersão, boxplots, histogramas e pairplots para entender a distribuição dos dados e perfil dos clientes.

Análise comparativa entre clientes aprovados e negados.

Importância das features no modelo global.

Distribuição das probabilidades previstas.

Mapa de correlação entre variáveis.

Explicação global do modelo com SHAP (complementar ao LIME).

📖 Como Usar as Funcionalidades
Opção 1: Simulação Manual
Insira dados financeiros do cliente (renda, score, parcelas, etc.).

O modelo prediz aprovação ou negação.

LIME gera explicação local detalhada.

Simulação de diferentes prazos para financiamento com cálculo de parcelas e endividamento.

Opção 2: Simulação em Lote via CSV
Faça upload de um arquivo CSV com dados de vários clientes.

O pipeline processa as informações e gera previsões.

Relatório com aprovações, probabilidades e explicações médias via LIME.

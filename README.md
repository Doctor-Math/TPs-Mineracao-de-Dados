```markdown
# 📊 Mineração de Dados — Trabalhos Práticos (UFMG)

[![Python Version](https://img.shields.io/badge/python-3.10%2B-blue.svg)](https://www.python.org/)
[![Data Science](https://img.shields.io/badge/UFMG-Ci%C3%AAncia%20de%20Dados-red)](https://dcc.ufmg.br/)
[![Framework](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-111111?logo=xgboost)](https://xgboost.readthedocs.io/)

Este repositório centraliza o desenvolvimento dos Trabalhos Práticos (TPs) e do Projeto Final desenvolvidos para a disciplina de **Mineração de Dados** do curso de graduação em **Ciência de Dados** da Universidade Federal de Minas Gerais (UFMG). 

O repositório está estruturado de forma modular para garantir a reprodutibilidade das análises, cobrindo desde a extração de padrões frequentes e agrupamentos até pipelines complexos de classificação e auditoria ética de algoritmos.

---

## 📂 Organização do Repositório

A estrutura de diretórios do projeto é padronizada seguindo boas práticas de reprodutibilidade científica:

```text
.
├── data/               # Bases de dados brutas e tratadas segregadas por etapa
│   ├── data_tp1/
│   ├── data_tp2/
│   └── data_tp3/
├── docs/               # Relatórios técnicos finais em formato Markdown/PDF
│   ├── project/
│   ├── tp1/
│   ├── tp2/
│   └── tp3/
├── notebooks/          # Jupyter Notebooks contendo os experimentos funcionais
│   ├── tp1/
│   ├── tp2/
│   └── tp3/
└── README.md           # Sumário executivo do repositório

```

---

## 🛠️ Visão Geral dos Trabalhos Práticos

### 🔹 TP1: Mineração de Padrões Frequentes & Regras de Associação

* **Dataset:** MovieLens (Filmes e Avaliações).
* **Foco:** Engenharia de Atributos via Padrões de Consumo.
* **Abordagem:** Implementação e comparação de performance computacional entre os algoritmos **Apriori** e **FP-Growth**. Extração de regras de associação baseadas em métricas de suporte, confiança e *lift* para mapear dependências comportamentais ocultas e otimizar representações matriciais (*feature engineering*).

### 🔹 TP2: Aprendizado Não Supervisionado — Análise de Agrupamento

* **Dataset:** Dados Socioeconômicos e Demográficos.
* **Foco:** Segmentação de Instâncias e Detecção de Estruturas.
* **Abordagem:** Aplicação de algoritmos de partição (**K-Means**) e densidade (**DBSCAN**). O pipeline cobriu a normalização rigorosa de escalas, redução de dimensionalidade e validação da qualidade dos agrupamentos por meio de métricas intrínsecas (Coeficiente de *Silhouette* e Índice de Davies-Bouldin) para interpretação de perfis latentes.

### 🔹 TP3 & Projeto Final: Pipeline Preditivo de Alta Performance e IA Responsável

* **Dataset:** *Adult Census Dataset* (Previsão de Extrato de Renda).
* **Foco:** Classificação, Otimização de Hiperparâmetros, Explicabilidade e Equidade Algorítmica.
* **Abordagem:** * Desenvolvimento de uma abordagem dual contrastando uma árvore de decisão baseada em regras nativas (*baseline* interpretável, $F1 = 0.6407$) com um comitê de gradiente aumentado (**XGBoost Classifier**, $AUC = 0.9218$, $F1 = 0.7225$).
* Otimização sistemática via `GridSearchCV` com validação cruzada estratificada (5-Fold) e balanceamento estatístico de gradiente via penalização de classes (`scale_pos_weight = 3.151`).
* **Auditoria de IA Responsável:** Aplicação de explicações pós-hoc via framework **SHAP** (`TreeExplainer`) desvelando o fenômeno de mascaramento por colinearidade reversa (viés de gênero capturado via variável de estado civil).
* Calibração de corte por pós-processamento (*Threshold Shifting*) avaliando empiricamente o *trade-off* contínuo entre métricas econômicas de negócio (`Precision` e `Recall`) e restrições éticas distributivas de gênero e raça (indicador de **Impacto Díspar**).



---

## 🚀 Como Executar as Soluções

1. **Clone o repositório:**
```bash
git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
cd seu-repositorio

```


2. **Instale as dependências necessárias:**
As análises requerem Python 3.10+ e os pacotes listados nas primeiras células dos notebooks (incluindo `scikit-learn`, `xgboost`, `shap`, `pandas`, `numpy`, `matplotlib` e `seaborn`).
```bash
pip install -r requirements.txt  # Caso usem um arquivo de requirements
# Ou individualmente:
pip install pandas numpy scikit-learn xgboost shap matplotlib seaborn

```


3. **Navegue até os experimentos:**
Abra o Jupyter Lab ou ambiente de preferência e execute as células de forma sequencial dentro de `notebooks/`.

---

## 👥 Contribuintes

O desenvolvimento técnico e a redação dos relatórios analíticos foram conduzidos equitativamente pelo comitê de engenharia:

* [João Marcos Oliveira Neves](https://github.com/nevzJao) — Graduando em Estatística (UFMG)
* [Júlia Borba Fonseca de Souza](https://github.com/juliaborbaf) — Graduanda em Ciência da Computação (UFMG)
* [Laura Martins Froede](https://github.com/laurafroede) — Graduanda em Ciência da Computação (UFMG)
* [Matheus Soares dos Santos de Freitas](https://github.com/Doctor-Math) — Graduando em Ciência de Dados (UFMG)

---

*Este material faz parte do portfólio acadêmico institucional dos alunos e segue os preceitos de integridade técnica da UFMG.*

```

---

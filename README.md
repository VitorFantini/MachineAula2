# 🚴 Sales Intelligence: Predição de Performance de Vendas

> **Status do Projeto:** Concluído ✅  
> **Desenvolvedor:** Vitor Fantini (RA: 4201037)  
> **Dataset:** Bike Sales (Kaggle) - 113.036 registros

Este repositório contém um pipeline completo de Ciência de Dados, desde o tratamento de dados brutos até a implementação de um modelo de Machine Learning para classificação de rentabilidade em vendas.

---

## 📊 Badges
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Scipy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

---

## 📝 Índice
- [Visão Geral](#-visão-geral)
- [O Desafio Técnico](#-o-desafio-técnico)
- [Pipeline de Dados](#-pipeline-de-dados)
- [Tecnologias](#-tecnologias)
- [Resultados e Insights](#-resultados-e-insights)
- [Como Executar](#-como-executar)

---

## 📌 Visão Geral
O objetivo deste projeto é prever a **Alta Performance** de vendas. Definimos matematicamente a Alta Performance como vendas que possuem um **Markup superior a 60%**.

$$Markup = \frac{Profit}{Cost} > 60\%$$

O modelo utiliza características demográficas (idade, país, género) e especificações do produto para classificar cada transação.

---

## 🛠️ O Desafio Técnico
O projeto foi desenhado para lidar com problemas reais de bancos de dados empresariais:
1. **Dados Incompletos:** Tratamento de nulos simulados.
2. **Erros de Digitação:** Correção de outliers em quantidades vendidas.
3. **Desbalanceamento:** Vendas de alta performance são raras (apenas ~22% da base).

---

## ⚙️ Pipeline de Dados

### 1. Limpeza e Tratamento ("A Faxina")
- **Imputação de Idade:** Utilização da mediana por categoria de idade para preencher valores ausentes.
- **Capping de Outliers:** Valores discrepantes em `Order_Quantity` foram limitados ao percentil 99 para evitar distorções estatísticas.
- **Integridade Financeira:** Recálculo total das colunas `Revenue`, `Cost` e `Profit` para garantir consistência após a limpeza das quantidades.

### 2. Análise Exploratória (EDA)
- Mapas de calor para identificar correlações.
- Boxplots para visualização da dispersão de preços e custos.
- Análise de rentabilidade por categoria de produto.

### 3. Machine Learning
- **Pré-processamento:** One-Hot Encoding para variáveis categóricas.
- **Modelo:** **Random Forest Classifier** com 100 estimadores.

---

## 💻 Tecnologias
- **Linguagem Principal:** Python 3.x
- **Manipulação de Dados:** Pandas, Numpy
- **Visualização:** Matplotlib, Seaborn
- **Modelagem:** Scikit-Learn
- **Amostragem:** Imbalanced-learn (SMOTE)

---

## 📈 Resultados e Insights
O modelo final demonstrou uma performance excepcional:
- **Acurácia Global:** 95%
- **Estabilidade:** Validada através de simulações (1000 amostragens).
- **Insight Principal:** O preço unitário e o custo são os fatores determinantes. O género e a localização geográfica têm impacto mínimo na predição de rentabilidade, indicando um comportamento de compra uniforme entre esses grupos.

---

## 🚀 Como Executar

1. Clone o repositório:
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-repo.git](https://github.com/seu-usuario/nome-do-repo.git)

🚀 Inteligência de Vendas e Predição de Performance
Desenvolvido por: Vitor Fantini

RA: 4201037

Dataset: Bike Sales (Kaggle) - 113.036 registros

📋 Introdução e Contexto
Este projeto consiste na análise histórica e no desenvolvimento de um modelo de Machine Learning focado em classificar a performance de vendas de uma loja de bicicletas e acessórios.

O objetivo principal é identificar vendas de Alta Performance, definidas como aquelas que possuem um Markup superior a 60% (margem de lucro sobre o custo). A predição baseia-se nas características demográficas do cliente e especificações do produto.

🛠️ O Desafio Técnico
O projeto foi estruturado para ser resiliente a falhas comuns em sistemas de ERP e cadastros mal preenchidos. O pipeline de Engenharia de Dados aborda:

Limpeza de Dados: Tratamento de nulos e inconsistências sintéticas.

Tratamento de Outliers: Identificação e correção de erros de digitação em volumes de pedidos.

Engenharia de Atributos: Criação de indicadores de rentabilidade e exclusão de variáveis que geram Data Leakage.

Balanceamento de Classes: Ajuste de pesos no modelo para lidar com a proporção de vendas de alta performance (21.86% do dataset).

⚙️ Estrutura do Pipeline
Configuração e Carga: Importação de dados e visualização inicial.

EDA (Análise Exploratória): Diagnóstico visual através de boxplots, mapas de calor e análise de distribuição de classes.

Data Cleaning ("A Faxina"): * Imputação de idade pela mediana do grupo etário.

Capping de outliers de quantidade pelo Percentil 99.

Restauração da integridade financeira (Recálculo de Revenue, Cost e Profit).

Pré-processamento: One-Hot Encoding para variáveis categóricas e filtragem de variáveis irrelevantes.

Modelagem: Treinamento utilizando o algoritmo Random Forest com pesos balanceados.

📊 Tecnologias Utilizadas
Linguagem: Python

Bibliotecas: * Pandas e Numpy para manipulação de dados.

Matplotlib e Seaborn para visualização e EDA.

Scikit-Learn para treinamento de modelo e métricas de avaliação.

📈 Resultados Finais
O modelo atingiu uma performance de excelência, demonstrando robustez técnica e técnica imparcial:

Acurácia: 95%.

Principais Insights: * O Preço Unitário e o Custo são os pilares fundamentais da rentabilidade.

Variáveis demográficas como gênero possuem influência desprezível na performance, garantindo uma predição técnica.

Qualidade dos Dados: O pipeline corrigiu 100% dos nulos e outliers sem a necessidade de deletar registros, preservando a integridade do dataset.

Como utilizar:

Certifique-se de ter o arquivo Sales.csv no mesmo diretório do notebook.

Execute as células sequencialmente para reproduzir o pipeline de limpeza e treinamento.

# Desafio Alura Store : 🛍️ Análise de Desempenho de Lojas - Tech Foundation : Especialização Data Science  - Módulo : Fundamentos de Python e Dados (Oracle Next Education G9 BR)

Este projeto, parte da terceira etapa do ONE G9 BR, tem como objetivo realizar uma análise detalhada do desempenho de 4 lojas com base em dados de vendas, produtos e clientes. Desenvolvido em Python no ambiente Google Colab, o notebook permite visualizar métricas importantes, identificar padrões e gerar insights para tomada de decisão.

---

## 📌 Objetivo

Identificar a loja com menor desempenho geral para recomendação de venda, utilizando métricas como:

- Faturamento total
- Vendas por categoria
- Avaliação média dos produtos
- Produtos mais e menos vendidos
- Frete médio

---

## 🧰 Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-teal?logo=seaborn&logoColor=white)

---

## 📊 Etapas da Análise

1. **Faturamento por Loja**  
   → Gráfico de barras comparando o total vendido por cada loja.

2. **Vendas por Categoria**  
   → Gráfico de pizza mostrando a distribuição de categorias na loja com maior diversidade.

3. **Avaliação Média**  
   → Gráfico de barras com a nota média dos produtos por loja.

4. **Produtos Mais e Menos Vendidos**  
   → Gráfico de barras com os 5 produtos mais vendidos da loja com maior volume.

5. **Frete Médio por Loja**  
   → Gráfico de linha comparando o custo médio de frete entre as lojas.

---

## 📎 Como Executar

1. Acesse o [Google Colab](https://colab.research.google.com/)
2. Importe o notebook `.ipynb` do projeto
3. Execute as células passo a passo para visualizar os gráficos e o relatório final

---

## 📂 Estrutura do Projeto
📦 analise-lojas

├── data/                        # Pasta para armazenar os arquivos de entrada (CSV, Excel, etc.)
│   └── vendas.csv               # Exemplo de arquivo de vendas
│
├── notebooks/                   # Notebooks Jupyter ou Colab
│   └── analise_loja.ipynb       # Notebook principal com a análise
│
├── src/                         # Código-fonte modularizado (opcional)
│   ├── limpeza_dados.py         # Funções para limpeza e pré-processamento
│   ├── calculo_metricas.py      # Funções para cálculo de KPIs
│   ├── visualizacoes.py         # Funções para geração de gráficos
│   └── relatorio.py             # Geração de relatórios ou exportação de resultados
│
├── outputs/                     # Resultados gerados (gráficos, relatórios, etc.)
│   ├── graficos/                # Imagens geradas
│   └── relatorios/              # Arquivos exportados (PDF, Excel, etc.)
│
├── requirements.txt             # Lista de dependências do projeto
├── README.md                    # Documentação do projeto
└── .gitignore                   # Arquivos e pastas a serem ignorados pelo Git

Descrição dos diretórios:
- data/: Contém os arquivos CSV com os dados brutos de cada loja.
- notebooks/: Notebook principal com todas as análises e visualizações.
- images/: Gráficos gerados durante a análise.
- relatorio_final.py: Script que gera o relatório automatizado com base nas análises.
- README.md: Documentação do projeto.

---

## 📬 Contato

Projeto desenvolvido por Marcus  
📧 Email: [mclguedes@gmail.com]  
📱 LinkedIn: [https://www.linkedin.com/in/marcusguedes]

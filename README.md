# 🛍️ Alura Store — Análise de Desempenho e Recomendação Estratégica

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](#)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](#)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)](#)
[![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](#)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](#)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MCLG1661/Desafio_Alura-Store/blob/main/AluraStoreBr_Portfolio.ipynb)

> **Dados → KPIs → Comparação → Insights → Recomendação → Decisão**

Projeto de **Data Analytics** desenvolvido para analisar o desempenho de quatro lojas da Alura Store e apoiar uma decisão de negócio:

> **Qual loja apresenta o menor desempenho e deveria ser considerada prioritariamente para venda?**

A análise utiliza Python, Pandas e Matplotlib para transformar dados transacionais em indicadores comparáveis, visualizações, insights e uma recomendação executiva baseada em evidências.

---

## 🎯 Problema de Negócio

O proprietário da Alura Store possui quatro unidades e precisa decidir qual delas deveria ser considerada para venda.

Uma decisão desse tipo não deveria ser baseada apenas em percepção ou em um único indicador.

Por isso, o projeto analisa diferentes dimensões do desempenho:

- faturamento;
- volume de vendas;
- ticket médio;
- categorias de produtos;
- avaliação dos clientes;
- produtos mais e menos vendidos;
- custo médio de frete.

O objetivo é transformar esses dados em uma recomendação fundamentada e, ao mesmo tempo, reconhecer as limitações do dataset.

---

## 💡 Abordagem Analítica

O projeto foi estruturado como uma jornada de análise orientada ao negócio:

```text
Problema de Negócio
        ↓
Carregamento dos Dados
        ↓
Qualidade dos Dados
        ↓
Consolidação
        ↓
Cálculo de KPIs
        ↓
Análise Comparativa
        ↓
Visualizações
        ↓
Insights
        ↓
Recomendação
        ↓
Decisão
```

Essa abordagem busca evitar um problema comum em projetos de análise de dados: produzir gráficos e métricas sem conectá-los à decisão que precisa ser tomada.

---

## 📂 Estrutura do Projeto

```text
Desafio_Alura-Store/
│
├── AluraStoreBr.ipynb
│   └── Notebook completo com análise, visualizações,
│       insights e recomendação final
│
└── README.md
    └── Documentação do projeto
```

---

## 📊 Dados Analisados

O projeto utiliza quatro datasets correspondentes às quatro unidades da Alura Store.

As bases contêm informações como:

- produto;
- categoria do produto;
- preço;
- frete;
- data da compra;
- vendedor;
- local da compra;
- avaliação da compra;
- tipo de pagamento;
- quantidade de parcelas;
- coordenadas geográficas.

Os dados são carregados diretamente do repositório utilizado no desafio da Alura e posteriormente consolidados para permitir análises comparativas.

---

## 🔎 Etapas da Análise

### 1. Importação e preparação

São utilizadas principalmente as bibliotecas:

```python
import pandas as pd
import matplotlib.pyplot as plt
```

Os quatro datasets são carregados e organizados em uma estrutura única para facilitar a comparação entre lojas.

---

### 2. Qualidade dos dados

Antes de calcular indicadores, o notebook verifica:

- quantidade de registros;
- quantidade de colunas;
- valores ausentes;
- registros duplicados;
- estrutura geral das bases.

Essa etapa reduz o risco de interpretar indicadores produzidos a partir de dados inconsistentes.

---

### 3. Consolidação

Os datasets individuais são combinados em uma base analítica única.

Uma coluna identifica a loja de origem de cada transação, permitindo executar análises consolidadas e comparativas.

---

## 📈 KPIs

Os principais indicadores calculados são:

### Faturamento

```text
Faturamento = Soma do preço das vendas
```

Permite comparar a capacidade de geração de receita das quatro lojas.

### Quantidade de vendas

```text
Vendas = Número de transações registradas
```

Ajuda a contextualizar faturamento e ticket médio.

### Ticket médio

```text
Ticket Médio = Faturamento ÷ Quantidade de Vendas
```

Permite avaliar o valor médio gerado por transação.

### Avaliação média

```text
Avaliação Média = Média das avaliações das compras
```

Utilizada como indicador de percepção e satisfação dos clientes.

### Frete médio

```text
Frete Médio = Soma dos fretes ÷ Número de vendas
```

Ajuda a identificar diferenças no custo logístico associado às operações.

---

## 💰 Faturamento por Loja

A análise encontrou aproximadamente:

| Loja | Faturamento |
|---|---:|
| Loja 1 | R$ 1.534.509 |
| Loja 2 | R$ 1.488.459 |
| Loja 3 | R$ 1.464.025 |
| **Loja 4** | **R$ 1.384.498** |

A **Loja 4 apresenta o menor faturamento** entre as quatro unidades.

Entretanto, faturamento isoladamente não é suficiente para determinar que uma operação seja necessariamente a pior.

Por isso, outros indicadores também foram avaliados.

---

## ⭐ Avaliação dos Clientes

As avaliações médias são relativamente próximas:

| Loja | Avaliação Média |
|---|---:|
| Loja 1 | 3,98 |
| Loja 2 | 4,04 |
| Loja 3 | 4,05 |
| Loja 4 | 4,00 |

A **Loja 3 apresenta a maior avaliação média**, enquanto a **Loja 1 registra a menor**.

A proximidade entre as notas indica que satisfação do cliente não parece ser o principal fator explicativo para a diferença de faturamento entre as unidades.

---

## 🚚 Frete Médio

| Loja | Frete Médio |
|---|---:|
| Loja 1 | R$ 34,69 |
| Loja 2 | R$ 33,62 |
| Loja 3 | R$ 33,07 |
| **Loja 4** | **R$ 31,28** |

Aqui surge um insight importante:

> A loja com menor faturamento também apresenta o **menor frete médio**.

Isso mostra que a Loja 4 não possui desempenho inferior em todas as dimensões.

Essa diferença é importante para evitar uma conclusão simplista baseada apenas na receita.

---

## 🛒 Análise por Categoria

O notebook compara a quantidade de vendas das principais categorias entre as quatro lojas.

Entre as categorias presentes estão:

- móveis;
- eletrônicos;
- brinquedos;
- eletrodomésticos;
- esporte e lazer;
- instrumentos musicais;
- livros;
- utilidades domésticas.

A análise mostra que as quatro lojas trabalham com um portfólio relativamente amplo.

Por isso, a diversidade de categorias não é utilizada isoladamente como justificativa para recomendar a venda de uma unidade.

---

## 📦 Produtos Mais e Menos Vendidos

O projeto também analisa os produtos de maior e menor volume em cada loja.

Em vez de selecionar somente um produto — o que poderia ser influenciado por empates — o notebook apresenta rankings dos:

- **5 produtos mais vendidos**
- **5 produtos menos vendidos**

Essa abordagem oferece uma visão mais robusta do mix comercial de cada unidade.

---

## 📊 Visualizações

O notebook utiliza gráficos comparativos para facilitar a interpretação dos indicadores.

Entre as visualizações estão:

- faturamento total por loja;
- avaliação média por loja;
- frete médio por loja;
- vendas por categoria e loja.

As visualizações foram construídas com **Matplotlib** e priorizam comparação direta entre as quatro operações.

---

## 🧠 Principais Insights

A análise evidencia alguns pontos importantes:

### 1. A Loja 4 possui o menor faturamento

Ela apresenta a menor geração de receita entre as quatro operações.

### 2. A Loja 4 não apresenta o pior desempenho em todas as dimensões

Apesar do menor faturamento, possui o **menor frete médio**.

### 3. As avaliações são muito próximas

A diferença entre a maior e a menor avaliação média é pequena.

Isso reduz a capacidade desse indicador, isoladamente, de explicar diferenças relevantes entre as lojas.

### 4. O mix de categorias é amplo

As quatro lojas comercializam diversas categorias, portanto não existe evidência suficiente para atribuir o menor faturamento simplesmente à falta de variedade.

### 5. A decisão envolve trade-offs

Uma unidade pode apresentar menor receita e, ao mesmo tempo, possuir vantagens em outros indicadores.

Esse é justamente o tipo de situação em que Data Analytics deve apoiar — e não substituir — a tomada de decisão.

---

## 🎯 Recomendação Final

Com base nos dados disponíveis, a **Loja 4 é a principal candidata à venda**, principalmente por apresentar o **menor faturamento entre as quatro unidades**.

Entretanto, a recomendação não decorre de uma deterioração generalizada de seus indicadores.

A Loja 4 apresenta:

- menor faturamento;
- avaliação próxima às demais unidades;
- menor frete médio.

Portanto, a recomendação é sustentada principalmente pela sua **menor capacidade de geração de receita dentro do período analisado**.

---

## ⚠️ Limitações da Análise

Uma decisão real de venda de uma unidade exigiria informações adicionais que não estão disponíveis no dataset.

Entre elas:

- margem de contribuição;
- custos fixos;
- custos operacionais;
- lucro por loja;
- despesas logísticas completas;
- CAC;
- recorrência de clientes;
- estoque;
- potencial de crescimento;
- características do mercado regional;
- valor patrimonial ou comercial da unidade.

Por isso, a conclusão deve ser interpretada como:

> **A Loja 4 é a principal candidata à venda entre as quatro unidades com base nos indicadores disponíveis — não como uma recomendação financeira definitiva de desinvestimento.**

Essa distinção evita extrapolar o que os dados realmente permitem concluir.

---

## 🛠️ Tecnologias Utilizadas

### Linguagem

- Python

### Análise e manipulação de dados

- Pandas

### Visualização

- Matplotlib

### Ambiente

- Jupyter Notebook
- Google Colab

### Versionamento

- Git
- GitHub

---

## 💼 Competências Demonstradas

### Data Analytics

- Análise Exploratória de Dados — EDA
- Data Cleaning
- Data Wrangling
- Consolidação de datasets
- Cálculo de KPIs
- Análise comparativa
- Data Visualization
- Interpretação de indicadores

### Business Analytics

- Tradução de problema de negócio em análise
- Avaliação de performance
- Identificação de trade-offs
- Geração de insights
- Recomendação orientada por dados
- Comunicação executiva
- Reconhecimento de limitações analíticas

### Tecnologia

- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- Google Colab
- Git
- GitHub

---

## ▶️ Como Executar

### Google Colab

O notebook pode ser aberto diretamente no Google Colab a partir do GitHub.

Arquivo principal:

```text
AluraStoreBr.ipynb
```

### Execução local

Clone o repositório:

```bash
git clone https://github.com/MCLG1661/Desafio_Alura-Store.git
```

Acesse a pasta:

```bash
cd Desafio_Alura-Store
```

Abra o notebook:

```text
AluraStoreBr.ipynb
```

em um ambiente compatível com Jupyter Notebook.

---

## 🚀 Possíveis Evoluções

O projeto pode evoluir com análises adicionais, desde que existam dados adequados para sustentá-las:

- [ ] análise temporal de faturamento;
- [ ] evolução de vendas por período;
- [ ] margem e rentabilidade por loja;
- [ ] análise de clientes;
- [ ] segmentação de produtos;
- [ ] análise geográfica com regiões corretamente definidas;
- [ ] dashboard em Power BI;
- [ ] dashboard interativo em Streamlit;
- [ ] modelos de previsão de vendas;
- [ ] análise de cenários para decisão de desinvestimento.

---

## 🎓 Contexto Acadêmico

Este projeto foi desenvolvido a partir do **Challenge Alura Store**, dentro da formação em Data Science do programa **Oracle Next Education — ONE**, promovido pela Oracle em parceria com a Alura.

A versão apresentada neste repositório foi reorganizada com foco adicional em:

- qualidade analítica;
- narrativa de negócio;
- comparação estruturada de KPIs;
- visualização;
- interpretação;
- comunicação executiva;
- portfólio profissional.

---

## 👨‍💻 Autor

**Marcus Guedes**

Marketing | Data Science | Inteligência Artificial | Gestão de Projetos

GitHub: https://github.com/MCLG1661

Linkedin: https://www.linkedin.com/in/marcusguedes/

---

## 📄 Licença

Projeto desenvolvido para fins educacionais e de portfólio profissional.

Os datasets utilizados pertencem ao contexto educacional do Challenge Alura Store.

---

### Alura Store — Data Analytics

> **Transformando dados em informação, informação em insights e insights em decisões.**

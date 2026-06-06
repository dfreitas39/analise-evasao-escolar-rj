\# Mapeando a Educação: Análise de Dados Públicos para Reduzir a Evasão Escolar no Rio de Janeiro



\## Sobre o Projeto



Projeto acadêmico de análise de dados públicos educacionais com foco na

evasão escolar no município do Rio de Janeiro. Utiliza dados oficiais do

INEP/MEC para identificar padrões de abandono escolar por dependência

administrativa, série e comparativo nacional.



\---



\## Objetivos



1\. Coletar e processar dados públicos educacionais usando Python e Pandas

2\. Analisar indicadores de evasão, desempenho e desigualdade educacional

&#x20;  aplicando técnicas de análise exploratória com Matplotlib e Seaborn

3\. Desenvolver dashboard interativo no Google Looker Studio para

&#x20;  visualização dos indicadores educacionais



\---



\## Principais Insights



\- O município do Rio de Janeiro ocupa o \*\*4º lugar\*\* no ranking de abandono

&#x20; no Ensino Médio entre as 27 capitais brasileiras — 5.8% contra média

&#x20; de 2.99% das capitais

\- A rede \*\*estadual\*\* concentra o problema — 7.9% de abandono no Médio

&#x20; contra 1.2% da rede federal e 0.9% da privada

\- O \*\*1º ano do Ensino Médio estadual\*\* tem o maior pico de evasão — 8.8%

\- No Ensino Fundamental o município está na \*\*18ª posição\*\* — abaixo da

&#x20; média das capitais (0.57%)

\- \*\*94.9%\*\* dos alunos querem ensino superior mas 23.3% estão reprovando

\- Alunos rurais representam 22% do dataset mas ocupam 30% do top 10

&#x20; de melhores desempenhos



\---



\## Dashboard Interativo



Acesse o dashboard completo no Google Looker Studio:

🔗 https://datastudio.google.com/s/lTrOFteYy\_4



\---



\## Estrutura do Repositório

analise-evasao-escolar-rj/

│

├── README.md

├── .gitignore

├── requirements.txt

│

├── data/

│   └── raw/

│       └── tx\_rend\_municipios\_2024.xlsx

│

├── notebooks/

│   └── analise\_evasao\_escolar\_rj.ipynb

│

├── exports/

│   ├── 01\_municipio\_rj\_dependencia.csv

│   ├── 02\_series\_ensino\_medio.csv

│   ├── 03\_series\_ensino\_fundamental.csv

│   ├── 04\_ranking\_capitais\_v2.csv

│   ├── 05\_comparativo\_regioes.csv

│   └── 06\_municipios\_estado\_rj\_v2.csv

│

├── assets/

│   └── screenshots/

│

└── docs/

└── analise.md



\---



\## Tecnologias Utilizadas



| Tecnologia | Uso |

|---|---|

| Python 3 | Linguagem principal |

| Pandas | ETL e manipulação de dados |

| Matplotlib | Visualizações exploratórias |

| Seaborn | Visualizações estatísticas |

| Google Colab | Ambiente de desenvolvimento |

| Google Looker Studio | Dashboard interativo |

| Git e GitHub | Controle de versão |



\---



\## Fonte dos Dados



\- \*\*INEP/MEC\*\* — Taxas de Rendimento Escolar por Município 2024

\- Link: https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/indicadores-educacionais/taxas-de-rendimento-escolar



\---



\## Como Executar



1\. Clone o repositório

2\. Acesse o Google Colab em colab.research.google.com

3\. Faça upload do notebook `analise\_evasao\_escolar\_rj.ipynb`

4\. Faça upload do arquivo `tx\_rend\_municipios\_2024.xlsx`

5\. Execute as células em ordem



\---



\## ODS Relacionado



\*\*ODS 4 — Educação de Qualidade:\*\* Garantir educação inclusiva,

equitativa e de qualidade, e promover oportunidades de aprendizagem

ao longo da vida para todos.



\---



\## Autor



Daniel Caetano Cordeiro Freitas
Matricula 4701030
Ciência de Dados
Uninter


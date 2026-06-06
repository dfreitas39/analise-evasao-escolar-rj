\# Análise — Mapeando a Educação: Evasão Escolar no Rio de Janeiro



\## 1. Contexto do Problema



O abandono escolar é um dos principais desafios do sistema educacional

brasileiro. No município do Rio de Janeiro, a evasão impacta diretamente

o desenvolvimento social e econômico da população, comprometendo o acesso

a melhores oportunidades de trabalho e renda.



Este projeto utiliza dados públicos do INEP/MEC para mapear os padrões

de abandono escolar no município do Rio de Janeiro, identificar quais

redes de ensino concentram o problema e comparar os indicadores com

outras capitais brasileiras e regiões do país.



\---



\## 2. Fonte dos Dados



| Fonte | Descrição | Ano |

|-------|-----------|-----|

| INEP/MEC | Taxas de Rendimento Escolar por Município | 2024 |



\*\*Arquivo utilizado:\*\* tx\_rend\_municipios\_2024.xlsx



\*\*Estrutura do arquivo:\*\*

\- 65.595 registros

\- 61 colunas após tratamento

\- Abrange todos os 5.570 municípios brasileiros

\- Indicadores: aprovação, reprovação e abandono por série,

&#x20; dependência administrativa e localização



\*\*Link para download:\*\*

https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/indicadores-educacionais/taxas-de-rendimento-escolar



\---



\## 3. Metodologia



\### 3.1 ETL — Extração, Transformação e Carga



\*\*Extração:\*\*

\- Leitura do arquivo Excel com `pd.read\_excel()`

\- Identificação e tratamento de 8 linhas de cabeçalho institucional

\- Detecção de valores ausentes representados por "--"



\*\*Transformação:\*\*

\- Renomeação de 61 colunas para nomenclatura descritiva em português

\- Substituição de "--" por NaN e conversão para float64

\- Criação de recortes analíticos por localização e dependência:

&#x20; - Total, Urbana, Rural

&#x20; - Municipal, Estadual, Federal, Pública, Privada

\- Filtragem do município do Rio de Janeiro

\- Filtragem das 27 capitais brasileiras



\*\*Carga:\*\*

\- Exportação de 6 CSVs temáticos para o Google Looker Studio



\### 3.2 Análise Exploratória



Ferramentas utilizadas:

\- \*\*Pandas\*\* — manipulação e agregação dos dados

\- \*\*Matplotlib\*\* — gráficos de barras, barras agrupadas e rankings

\- \*\*Seaborn\*\* — heatmaps e boxplots estatísticos

\- \*\*NumPy\*\* — cálculo de posições para gráficos agrupados

\- \*\*Functools\*\* — combinação de múltiplos filtros booleanos



\### 3.3 Dashboard



Ferramenta: Google Looker Studio

Link: https://datastudio.google.com/s/lTrOFteYy\_4



Páginas do dashboard:

1\. Visão Geral — cards com KPIs e ranking das capitais

2\. Por Dependência — abandono por rede administrativa

3\. Por Série — evolução do abandono por ano escolar

4\. Comparativo Nacional — ranking e regiões do Brasil

5\. Municípios do RJ — tabela interativa com filtro



\---



\## 4. Principais Resultados



\### 4.1 Visão Geral do Município do Rio de Janeiro



| Indicador | Valor | Posição entre capitais |

|-----------|-------|----------------------|

| Abandono Ensino Médio | 5.8% | 4º pior |

| Abandono Ensino Fundamental | 0.3% | 18º |

| Média capitais — Médio | 2.99% | — |

| Média Brasil — Médio | 3.40% | — |



\### 4.2 Por Dependência Administrativa



\*\*Ensino Médio:\*\*

| Dependência | Taxa de Abandono |

|-------------|-----------------|

| Estadual | 7.9% |

| Federal | 1.2% |

| Privada | 0.9% |

| Municipal | — (não oferta EM) |



\*\*Ensino Fundamental:\*\*

| Dependência | Taxa de Abandono |

|-------------|-----------------|

| Federal | 0.4% |

| Municipal | 0.3% |

| Estadual | 0.2% |

| Privada | 0.0% |



\### 4.3 Por Série — Ensino Médio Estadual



| Série | Taxa de Abandono |

|-------|-----------------|

| 1º Ano | 8.8% |

| 2º Ano | 8.1% |

| 3º Ano | 6.3% |



O 1º ano concentra o maior pico de evasão — transição crítica

do Ensino Fundamental para o Médio.



\### 4.4 Ranking das Capitais



\*\*Ensino Médio — Top 5:\*\*

1º Salvador     → 6.7%

2º Natal        → 6.4%

3º João Pessoa  → 6.0%

4º Rio de Janeiro → 5.8%

5º Belo Horizonte → 5.7%



\*\*Ensino Fundamental — Rio de Janeiro:\*\*

18º Rio de Janeiro → 0.3%

Abaixo da média das capitais (0.57%)



\### 4.5 Comparativo por Região



| Região | Abandono Médio | Abandono Fundamental |

|--------|---------------|---------------------|

| Nordeste | 3.98% | 0.99% |

| Norte | 3.28% | 1.16% |

| Sudeste | 3.57% | 0.47% |

| Sul | 3.12% | 0.25% |

| Centro-Oeste | 1.42% | 0.22% |



O Norte apresenta abandono sistêmico em todos os níveis.

O Nordeste concentra o problema no Ensino Médio.

O Centro-Oeste lidera todos os indicadores positivos.



\---



\## 5. Considerações Finais



\### Aprendizado 1 — ETL com dados públicos reais

A execução do projeto evidenciou os desafios reais de um

processo de ETL — desde a leitura de arquivos com cabeçalhos

institucionais, identificação de valores ausentes representados

por traços ("--") ao invés de nulos, até a criação de recortes

analíticos independentes para diferentes perspectivas de análise.

Trabalhar com dados públicos do INEP exigiu compreensão

da estrutura do Censo Escolar e das convenções de

nomenclatura dos indicadores educacionais.



\### Aprendizado 2 — Visualização como ferramenta de comunicação

A escolha do tipo de gráfico impacta diretamente a

compreensão da mensagem. Gráficos de barras agrupadas

facilitam comparações entre dependências, heatmaps revelam

padrões em matrizes de dados e boxplots expõem distribuições

e outliers que médias simples escondem. A combinação de

Matplotlib para controle preciso e Seaborn para visualizações

estatísticas permitiu explorar os dados em múltiplas dimensões.



\### Aprendizado 3 — Dados públicos como instrumento de política pública

O INEP disponibiliza gratuitamente dados que permitem análises

precisas sem necessidade de pesquisa de campo. A partir de um

único arquivo foi possível identificar que o problema de evasão

no município do Rio de Janeiro não é sistêmico — está concentrado

na rede estadual do Ensino Médio, com taxa de 7.9% contra 1.2%

da rede federal. Essa precisão permite apontar o responsável

pela intervenção: o Governo do Estado do Rio de Janeiro.



\### Aprendizado 4 — Contexto transforma a interpretação dos dados

O abandono de 5.1% no 1º ano do Ensino Fundamental da rede

federal não representa vulnerabilidade socioeconômica — é

choque acadêmico ou migração para outras redes. O mesmo

número em contextos diferentes conta histórias opostas.

A análise de dados exige ir além do número e compreender

o contexto institucional, legal e socioeconômico que

o originou.



\### Aprendizado 5 — Dashboard como ponte entre dados e decisão

A construção do dashboard no Google Looker Studio evidenciou

a importância de transformar análises técnicas em

visualizações acessíveis para gestores e educadores que

não têm formação técnica em dados. Um insight que permanece

no notebook não gera impacto — precisa ser comunicado

de forma clara e interativa para subsidiar decisões reais.



\### Dificuldades encontradas

\- Identificação do separador correto dos valores ausentes

&#x20; ("--" ao invés de nulos) exigiu inspeção manual do arquivo

\- A PNAD Contínua não tem representatividade municipal —

&#x20; limitou o cruzamento com dados socioeconômicos do IBGE

&#x20; ao nível estadual

\- O Looker Studio tem limitações para geocodificação

&#x20; automática de municípios brasileiros — o mapa interativo

&#x20; não entregou o resultado esperado



\---



\## 6. Próximos Passos



\- Cruzar os dados do INEP com indicadores socioeconômicos

&#x20; do Censo IBGE 2022 por município

\- Incluir série histórica para análise de evolução temporal

&#x20; do abandono escolar no município do Rio de Janeiro

\- Desenvolver modelo preditivo de risco de evasão usando

&#x20; Scikit-learn com os dados disponíveis

\- Expandir a análise para todos os municípios do estado do RJ

&#x20; com foco nos municípios com maior abandono


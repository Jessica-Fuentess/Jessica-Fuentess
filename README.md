<h1 align="center">Jéssica Fuentes</h1>

<p align="center">
  <b>Analista de Dados · BI · Engenharia de Dados</b><br>
  SQL · Power BI · Python · Databricks · IA aplicada a dados
</p>

<p align="center">
  📍 São Paulo (híbrido ou remoto) &nbsp;|&nbsp; Aberta a vagas de Analista de Dados, Analista de BI e Engenheira de Dados
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/j%C3%A9ssica-fuentes/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:fuentesbr@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white" alt="E-mail"/></a>
</p>

---

## Sobre mim

Passei 18 anos em Comércio Exterior, Logística e Operações em multinacionais, os últimos como Analista de Comex Sênior. Foi lá que comecei a resolver problema com dado: dashboard de free time de contêiner, controle de vencimentos, custo de frete por rota e transportadora. Agora estou migrando de vez para a área de dados.

Sou formada em **Análise e Desenvolvimento de Sistemas**. Uso **SQL, Power BI (DAX e Power Query), Excel e Python** e construo pipelines no **Databricks**, da ingestão ao produto final. Uso IA em duas frentes: **dentro do pipeline** (LLM lendo texto livre, agente respondendo perguntas sobre os dados) e **no desenvolvimento**, com Claude Code.

---

## Resultados na experiência profissional

| Resultado | Como |
|---|---|
| **-50%** nos dias médios de permanência de contêineres no terminal | Dashboard em Power BI de free time, custos e prazos |
| **~R$ 250 mil/ano** em custos evitados | Controle de vencimentos em Excel com alertas |
| **3 a 5 dias** a menos no ciclo médio de importação | Acompanhamento automatizado, da chegada à nacionalização |
| **-20%** no frete nacional | Análise de custos por rota e transportadora (SQL, CRM e Excel) |

---

## 🚦 Projeto em destaque: Projeto Farol

**Torre de controle de 60 projetos no Databricks, do data lake ao agente de IA**

Uma empresa com 60 projetos e R$ 305 mi de carteira, onde cada gerente usa uma ferramenta (Excel, ClickUp ou MS Project) e pinta o próprio farol. O Farol junta as três fontes num modelo só e responde as perguntas do dono: o que está atrasado, quanto isso vai custar, onde tem gente parada e o que vai dar errado no próximo mês.

```mermaid
flowchart LR
    F["Excel · ClickUp · MS Project<br/>RH · timesheet · custos"] --> S3[("Data lake<br/>S3")]
    S3 -->|boto3| B["Bronze"]
    B --> S["Silver<br/>limpa e integrada"]
    S --> G["Gold<br/>EVM · utilização"]
    S --> IA["LLM<br/>ai_classify · ai_extract"] --> G
    G --> D["Dashboard AI/BI"]
    G --> APP["App React"]
    G --> GE["Agente Genie"] --> APP
```

<table>
<tr>
<td align="center"><b>4.917</b><br>tarefas de 3 formatos<br>(planilha, JSON, XML) num modelo só</td>
<td align="center"><b>17 de 41</b><br>projetos em andamento<br>sinalizados em risco</td>
<td align="center"><b>R$ 6,47 mi</b><br>de estouro previsto<br>identificado</td>
<td align="center"><b>4 🍉</b><br>projetos verdes no status<br>e vermelhos no número</td>
</tr>
<tr>
<td align="center"><b>R$ 0</b><br>perdidos na limpeza de<br>18 tipos de sujeira</td>
<td align="center"><b>163</b><br>status semanais<br>classificados por LLM</td>
<td align="center"><b>20/20</b><br>no benchmark<br>do agente de IA</td>
<td align="center"><b>~4 min</b><br>de ponta a ponta,<br>job semanal com 6 tarefas</td>
</tr>
</table>

- **Ingestão:** Python e `boto3` puxam os arquivos do data lake (S3) para 9 tabelas bronze.
- **Silver e gold** em Lakeflow Declarative Pipelines (SQL), com expectations. O custo total da bronze bate com o da silver, centavo por centavo.
- **Gestão por Valor Agregado:** SPI, CPI e EAC por projeto e por semana, calculados das tarefas, não do farol do gerente.
- **IA no pipeline:** `ai_classify` e `ai_extract` transformam o texto livre do status em causa do bloqueio, quem destrava e dias de impacto. A IA roda só onde compensa, com `MERGE` incremental.
- **Produtos:** dashboard executivo, app em React/TypeScript (Databricks Apps) com simulador de realocação de pessoas, e agente que responde em português.
- **Engenharia:** tudo como código (Asset Bundles), metric view como fonte única dos KPIs, 5 camadas de qualidade de dados e segredos fora do Git.

<sub>Dados sintéticos. Case da imersão Jornada de Dados, refeito e adaptado por mim.</sub>

👉 [Ver o projeto](https://github.com/Jessica-Fuentess/farol_projeto)

---

## 🛒 E-commerce Lakehouse

Plataforma de dados ponta a ponta em **Databricks** com arquitetura Medallion em **PySpark e Delta Lake**: ingestão parametrizada de 4 CSVs, limpeza e regras de negócio na silver, e 6 tabelas gold (vendas, produtos, segmentação de clientes VIP/TOP_TIER/REGULAR, preços da concorrência e qualidade de dados). Orquestrado com Databricks Jobs, versionado com Asset Bundles, governado no Unity Catalog e testado (schema e regras de negócio). Entrega em dashboard AI/BI e Genie.

👉 [Ver o projeto](https://github.com/Jessica-Fuentess/Projeto_Ecommerce_Databricks)

---

## 🤖 IA no meu trabalho com dados

**Dentro do pipeline**
- LLM classificando e extraindo campos de texto livre em SQL (`ai_classify`, `ai_extract`), com controle de custo: no Farol, a IA processa só os 163 status que precisavam dela. O resto é resolvido por regra e palavra-chave.
- Agentes de perguntas em linguagem natural (Genie) sobre métricas governadas. Antes de liberar, testo o agente contra perguntas com resposta conhecida: 20 de 20 no Farol.
- Chatbot com histórico de contexto e engenharia de prompt (Python, Streamlit e OpenAI API).

**No desenvolvimento**
- Claude Code no VS Code junto com a Databricks CLI. Construo em etapas curtas: uma camada só começa depois do deploy da anterior e da conferência contra números de referência.
- `CLAUDE.md` versionado no repositório, com regras de negócio, modelo de dados, convenções e armadilhas já resolvidas. Serve de contexto para a IA e de documentação para quem chegar depois.
- Revisão do que a IA gera. Exemplo: o app marcava como "melancia" projetos que não eram. A causa: o warehouse devolve booleano como o texto `"false"`, e em JavaScript texto não vazio é verdadeiro. Corrigi e registrei a armadilha no `CLAUDE.md`.

---

## 📂 Outros projetos

| Projeto | O que mostra | Tecnologias |
|---|---|---|
| [Dashboard Financeiro](https://github.com/Jessica-Fuentess/Financial_Dashboard) | Receitas, custos, impostos, margem e lucro | Power BI · DAX · Power Query |
| [Dashboard de RH](https://github.com/Jessica-Fuentess/HR_Dashboard) | Headcount, turnover, folha e horas extras | Power BI · DAX · Power Query |
| [Dashboard de Produção](https://github.com/Jessica-Fuentess/Production_Dashboard) | Qualidade, disponibilidade e produtividade | Power BI · DAX · Power Query |
| [Dashboard de Vendas](https://github.com/Jessica-Fuentess/Sales_Dashboard) | Receita por período, marca e continente | Power BI · Power Query |
| [Análise em SQL](https://github.com/Jessica-Fuentess/SQL_Data_Analysis) | Modelagem relacional, JOINs, subqueries e views | MySQL · SQL Server |
| [Análise de Churn](https://github.com/Jessica-Fuentess/Data_Analytics_Python) | Fatores de cancelamento de clientes | Python · Pandas · Plotly |
| [Score de Crédito](https://github.com/Jessica-Fuentess/Credit_Score_Classification) | Classificação com Random Forest e KNN | Python · Scikit-learn |
| [Automação de Cadastro](https://github.com/Jessica-Fuentess/Process_Automation_Python) | Cadastro de produtos automatizado a partir de CSV | Python · Pandas · PyAutoGUI |
| [Chatbot com IA](https://github.com/Jessica-Fuentess/AI_Chatbot_Python) | Chat com contexto e engenharia de prompt | Python · Streamlit · OpenAI API |

Também tenho projetos front-end (HTML, CSS e JavaScript): [Site-Barbearia](https://github.com/Jessica-Fuentess/Site-Barbearia), [Previsao-do-tempo](https://github.com/Jessica-Fuentess/Previsao-do-tempo), [Site-android](https://github.com/Jessica-Fuentess/Site-android) e [Projeto-Login](https://github.com/Jessica-Fuentess/Projeto-Login).

---

## 🛠 Stack

**Dados e BI**

![SQL](https://img.shields.io/badge/-SQL-CC2927?style=flat&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/-Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=flat)
![Excel](https://img.shields.io/badge/-Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![SQL Server](https://img.shields.io/badge/-SQL%20Server-CC2927?style=flat&logo=microsoftsqlserver&logoColor=white)
![BigQuery](https://img.shields.io/badge/-BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white)
![Looker Studio](https://img.shields.io/badge/-Looker%20Studio-4285F4?style=flat&logo=looker&logoColor=white)

**Engenharia de Dados**

![Databricks](https://img.shields.io/badge/-Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/-PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD8?style=flat)
![Unity Catalog](https://img.shields.io/badge/Unity%20Catalog-1B3139?style=flat)
![Lakeflow Pipelines](https://img.shields.io/badge/Lakeflow%20Pipelines-FF3621?style=flat)
![Asset Bundles](https://img.shields.io/badge/Asset%20Bundles%20(IaC)-1B3139?style=flat)
![S3](https://img.shields.io/badge/-S3%20%C2%B7%20boto3-569A31?style=flat&logo=amazons3&logoColor=white)

**IA aplicada**

![Claude Code](https://img.shields.io/badge/-Claude%20Code-D97757?style=flat&logo=claude&logoColor=white)
![AI Functions](https://img.shields.io/badge/Databricks%20AI%20Functions-FF3621?style=flat)
![Genie](https://img.shields.io/badge/Genie%20(agente%20de%20dados)-1B3139?style=flat)
![OpenAI API](https://img.shields.io/badge/-OpenAI%20API-412991?style=flat&logo=openai&logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt%20Engineering-7B61FF?style=flat)

**Python e Machine Learning**

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Plotly](https://img.shields.io/badge/-Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/-Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

**Desenvolvimento e ferramentas**

![Git](https://img.shields.io/badge/-Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat&logo=github&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![SAP](https://img.shields.io/badge/-SAP-0FAAFF?style=flat&logo=sap&logoColor=white)

---

## 📚 Estudando agora

![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoftazure&logoColor=white)
![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-0078D4?style=flat&logo=microsoft&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white)

---

## 📬 Contato

Procuro vagas de **Analista de Dados**, **Analista de BI** ou **Engenheira de Dados**, em São Paulo (híbrido) ou remoto.

[LinkedIn](https://www.linkedin.com/in/j%C3%A9ssica-fuentes/) · [fuentesbr@gmail.com](mailto:fuentesbr@gmail.com)

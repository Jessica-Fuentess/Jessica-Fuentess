<h1 align="center">Jéssica Fuentes</h1>

<p align="center">
  <b>Analista de Dados · Business Intelligence</b><br>
  SQL · Power BI · Excel · Python · IA aplicada a dados · Databricks
</p>

<p align="center">
  📍 São Paulo &nbsp;|&nbsp; Aberta a vagas de Analista de Dados e Analista de BI
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/jessica-fuentess/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:fuentesbr@gmail.com"><img src="https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white" alt="E-mail"/></a>
</p>

---

## Sobre mim

Sou Analista de Dados e BI. Transformo dados operacionais em indicadores, dashboards e análises que reduzem custos e aceleram decisões.

Passei 18 anos em Comércio Exterior, Logística e Operações em multinacionais, os últimos como Analista de Comex Sênior. Foi lá que comecei a resolver problemas com dados: dashboard de free time de contêiner, controle de vencimentos e custo de frete por rota e transportadora. Por isso começo pela pergunta de negócio, não pela ferramenta.

Sou formada em **Análise e Desenvolvimento de Sistemas** e uso no dia a dia **SQL, Power BI, Excel e Python**: modelagem em estrela, publicação no Power BI Service com RLS e automações com **Power Automate, Power Apps e VBA**. Uso **IA generativa** (Copilot e Claude) para acelerar análises e, como diferencial, aplico **IA a dados** e construo meus próprios pipelines no **Databricks**.

---

## Resultados na experiência profissional

| Resultado | Como |
|---|---|
| **-50%** nos dias médios de permanência de contêineres no terminal | Dashboard em Power BI de free time, custos e prazos de **~100 processos de importação/mês** |
| **~R$ 250 mil/ano** em custos evitados | Controle de vencimentos em Excel com alertas |
| **~10 bases** integradas em painéis usados por **mais de 50 pessoas** | Modelos em estrela via SQL e Power Query, publicados no Power BI Service com gateway e RLS |
| **3 a 5 dias** a menos no ciclo médio de importação | Acompanhamento automatizado, da chegada à nacionalização |
| **-20%** no frete nacional | Análise de custos por rota e transportadora (SQL, CRM e Excel) |

---

## 🚦 Projeto em destaque: Projeto Farol

**Análise de uma carteira de 60 projetos: KPIs de prazo e custo, dashboard executivo e agente de IA**

Uma empresa com 60 projetos e R$ 305 mi de carteira, onde cada gerente usa uma ferramenta (Excel, ClickUp ou MS Project) e pinta o próprio farol. Integrei as três fontes, defini os indicadores e montei o dashboard que responde às perguntas da diretoria: o que está atrasado, quanto isso vai custar, onde tem gente parada e o que vai dar errado no próximo mês.

<table>
<tr>
<td align="center"><b>17 de 41</b><br>projetos em andamento<br>sinalizados em risco</td>
<td align="center"><b>R$ 6,47 mi</b><br>de estouro previsto<br>identificado</td>
<td align="center"><b>4 🍉</b><br>projetos verdes no status<br>e vermelhos no número</td>
<td align="center"><b>4.917</b><br>tarefas de 3 ferramentas<br>num modelo só</td>
</tr>
<tr>
<td align="center"><b>163</b><br>status semanais<br>classificados por LLM</td>
<td align="center"><b>20/20</b><br>no teste de validação<br>do agente de IA</td>
<td align="center"><b>R$ 0</b><br>perdidos na limpeza de<br>18 tipos de sujeira</td>
<td align="center"><b>~4 min</b><br>de atualização ponta a ponta,<br>toda semana</td>
</tr>
</table>

**Análise e BI**
- KPIs de Gestão por Valor Agregado (SPI, CPI, EAC, estouro previsto e margem) por projeto e por semana, calculados das tarefas, não do farol do gerente.
- Dashboard executivo com as páginas Portfólio, Pessoas e Fornecedores, e métricas governadas (cada fórmula definida num lugar só).
- O que os dados mostraram: 2 SREs com ~5% de uso enquanto um projeto crítico ficou 12 semanas travado por falta de SRE, e todas as entregas atrasadas vinham de um único fornecedor, cadastrado com 4 grafias diferentes.

**IA aplicada**
- LLM (`ai_classify` e `ai_extract`) transforma o texto livre do status semanal em causa do bloqueio, quem destrava e dias de impacto. A IA roda só onde compensa.
- Agente de IA (Genie) que responde em português, validado com 20 perguntas de resposta conhecida.
- App em React com um simulador: vale a pena mover uma pessoa ociosa para um projeto travado?

**Engenharia (por baixo)**
- Ingestão de data lake (S3) com Python, arquitetura medalhão em SQL no Databricks, 5 camadas de qualidade de dados e tudo como código (Asset Bundles).

<sub>Dados sintéticos. Case da imersão Jornada de Dados, refeito e adaptado por mim.</sub>

👉 [Ver o projeto](https://github.com/Jessica-Fuentess/farol_projeto)

---

## 🤖 IA no meu trabalho com dados

**Na análise**
- IA generativa (Microsoft Copilot e Claude) no dia a dia para acelerar análises, fórmulas e automações.
- LLM classificando e extraindo campos de texto livre direto em SQL, com controle de custo: no Farol, a IA processa só os 163 status que precisavam dela. O resto é resolvido por regra e palavra-chave.
- Agentes de perguntas em linguagem natural (Genie) sobre métricas governadas. Antes de liberar, testo o agente contra perguntas com resposta conhecida: 20 de 20 no Farol.
- Chatbot com histórico de contexto e engenharia de prompt (Python, Streamlit e OpenAI API).

**No desenvolvimento**
- Claude Code no VS Code junto com a Databricks CLI. Trabalho em etapas curtas: cada etapa só começa depois de conferir os números da anterior contra valores de referência.
- `CLAUDE.md` versionado no repositório, com regras de negócio, modelo de dados, convenções e armadilhas já resolvidas. Serve de contexto para a IA e de documentação para quem chegar depois.
- Revisão do que a IA gera. Exemplo: o app marcava como "melancia" projetos que não eram. A causa: o warehouse devolve booleano como o texto `"false"`, e em JavaScript texto não vazio é verdadeiro. Corrigi e registrei a armadilha no `CLAUDE.md`.

---

## 📊 Dashboards e análises

| Projeto | O que mostra | Tecnologias |
|---|---|---|
| [Dashboard Financeiro](https://github.com/Jessica-Fuentess/Financial_Dashboard) | Receitas, custos, impostos, margem e lucro | Power BI · DAX · Power Query |
| [Dashboard de RH](https://github.com/Jessica-Fuentess/HR_Dashboard) | Headcount, turnover, folha e horas extras | Power BI · DAX · Power Query |
| [Dashboard de Produção](https://github.com/Jessica-Fuentess/Production_Dashboard) | Qualidade, disponibilidade e produtividade | Power BI · DAX · Power Query |
| [Dashboard de Vendas](https://github.com/Jessica-Fuentess/Sales_Dashboard) | Receita por período, marca e continente | Power BI · Power Query |
| [Análise em SQL](https://github.com/Jessica-Fuentess/SQL_Data_Analysis) | Modelagem relacional, JOINs, subqueries e views | MySQL · SQL Server |
| [Análise de Churn](https://github.com/Jessica-Fuentess/Data_Analytics_Python) | Fatores de cancelamento de clientes | Python · Pandas · Plotly |
| [Score de Crédito](https://github.com/Jessica-Fuentess/Credit_Score_Classification) | Classificação com Random Forest e KNN | Python · Scikit-learn |
| [Chatbot com IA](https://github.com/Jessica-Fuentess/AI_Chatbot_Python) | Chat com contexto e engenharia de prompt | Python · Streamlit · OpenAI API |
| [Automação de Cadastro](https://github.com/Jessica-Fuentess/Process_Automation_Python) | Cadastro de produtos automatizado a partir de CSV | Python · Pandas · PyAutoGUI |

---

## 🏗 Diferencial: engenharia de dados

**[E-commerce Lakehouse](https://github.com/Jessica-Fuentess/Projeto_Ecommerce_Databricks):** pipeline ponta a ponta no Databricks com arquitetura Medallion em PySpark e Delta Lake. Ingestão parametrizada de 4 CSVs, regras de negócio na silver e 6 tabelas gold (vendas, produtos, segmentação de clientes VIP/TOP_TIER/REGULAR, preços da concorrência e qualidade de dados). Orquestrado com Databricks Jobs, versionado com Asset Bundles, governado no Unity Catalog, com testes de schema e regras de negócio. Entrega em dashboard AI/BI e Genie.

Também tenho projetos front-end (HTML, CSS e JavaScript): [Site-Barbearia](https://github.com/Jessica-Fuentess/Site-Barbearia), [Previsao-do-tempo](https://github.com/Jessica-Fuentess/Previsao-do-tempo), [Site-android](https://github.com/Jessica-Fuentess/Site-android) e [Projeto-Login](https://github.com/Jessica-Fuentess/Projeto-Login).

---

## 🛠 Stack

**Análise de dados e BI**

![SQL](https://img.shields.io/badge/-SQL-CC2927?style=flat&logo=mysql&logoColor=white)
![Power BI](https://img.shields.io/badge/-Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-F2C811?style=flat)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=flat)
![Excel](https://img.shields.io/badge/-Excel-217346?style=flat&logo=microsoftexcel&logoColor=white)
![MySQL](https://img.shields.io/badge/-MySQL-4479A1?style=flat&logo=mysql&logoColor=white)
![SQL Server](https://img.shields.io/badge/-SQL%20Server-CC2927?style=flat&logo=microsoftsqlserver&logoColor=white)
![BigQuery](https://img.shields.io/badge/-BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white)
![Looker Studio](https://img.shields.io/badge/-Looker%20Studio-4285F4?style=flat&logo=looker&logoColor=white)

**Automação**

![Power Automate](https://img.shields.io/badge/-Power%20Automate-0066FF?style=flat&logo=powerautomate&logoColor=white)
![Power Apps](https://img.shields.io/badge/-Power%20Apps-742774?style=flat&logo=powerapps&logoColor=white)
![VBA](https://img.shields.io/badge/VBA-217346?style=flat)

**IA aplicada**

![Microsoft Copilot](https://img.shields.io/badge/Microsoft%20Copilot-0078D4?style=flat)
![Claude](https://img.shields.io/badge/-Claude-D97757?style=flat&logo=claude&logoColor=white)
![Claude Code](https://img.shields.io/badge/-Claude%20Code-D97757?style=flat&logo=claude&logoColor=white)
![AI Functions](https://img.shields.io/badge/Databricks%20AI%20Functions-FF3621?style=flat)
![Genie](https://img.shields.io/badge/Genie%20(agente%20de%20dados)-1B3139?style=flat)
![OpenAI API](https://img.shields.io/badge/-OpenAI%20API-412991?style=flat&logo=openai&logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt%20Engineering-7B61FF?style=flat)

**Python**

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/-Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/-NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Plotly](https://img.shields.io/badge/-Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/-Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Streamlit](https://img.shields.io/badge/-Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Jupyter](https://img.shields.io/badge/-Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

**Engenharia de dados**

![Databricks](https://img.shields.io/badge/-Databricks-FF3621?style=flat&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/-PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white)
![Delta Lake](https://img.shields.io/badge/Delta%20Lake-00ADD8?style=flat)
![Unity Catalog](https://img.shields.io/badge/Unity%20Catalog-1B3139?style=flat)
![Lakeflow Pipelines](https://img.shields.io/badge/Lakeflow%20Pipelines-FF3621?style=flat)
![Asset Bundles](https://img.shields.io/badge/Asset%20Bundles%20(IaC)-1B3139?style=flat)
![S3](https://img.shields.io/badge/-S3%20%C2%B7%20boto3-569A31?style=flat&logo=amazons3&logoColor=white)

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

Procuro vagas de **Analista de Dados** ou **Analista de BI**.

[LinkedIn](https://www.linkedin.com/in/jessica-fuentess/) · [fuentesbr@gmail.com](mailto:fuentesbr@gmail.com)

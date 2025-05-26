
# 📊 Análise de Evasão de Clientes – TelecomX

Este projeto tem como objetivo identificar padrões de evasão (churn) entre clientes da empresa **TelecomX**, utilizando análise exploratória de dados (EDA), tratamento e transformação de variáveis, além de visualizações e correlações para extrair insights relevantes.

---

## 🧠 Objetivo

A evasão de clientes impacta diretamente na receita e no crescimento sustentável da empresa. O objetivo é entender **quem são os clientes que mais cancelam o serviço**, quais características estão associadas ao churn, e propor **ações baseadas em dados** para **reduzir a evasão**.

---

## 🧼 Limpeza e Tratamento de Dados

- **Importação** de dados no formato `.json` com estrutura aninhada.
- **Normalização** com `pd.json_normalize()`.
- Substituição de **strings vazias por `NaN`**.
- Conversão de variáveis binárias `"Yes"`/`"No"` para **0 e 1**.
- Conversão de colunas numéricas para o tipo adequado (`float`, `int`).
- Criação da variável **`Contas_Diarias`** baseada no valor médio diário do cliente.
- Criação de **`Qtd_Servicos`**, somando os serviços contratados pelo cliente.

---

## 🔍 Análise Exploratória de Dados (EDA)

### ✔ Distribuição de Churn
- A maioria dos clientes **permanece** na empresa.
- Clientes que **cancelam** tendem a fazê-lo nos primeiros meses.

### ✔ Churn por Variáveis Categóricas
- **Contratos mensais**, **pagamentos manuais**, ausência de parceiro(a) e dependentes estão associados a maior churn.
- **Pagamentos automáticos**, **contratos de longo prazo** e **serviços adicionais** ajudam a reter clientes.

### ✔ Churn por Variáveis Numéricas
- **Clientes com menor tenure e menor gasto total** têm maior evasão.
- Boxplots e histogramas mostram que **clientes mais engajados (tempo + valor)** tendem a ficar.

---

## 📈 Análise de Correlação

- Correlação **forte (+0.83)** entre `Charges.Total` e `tenure` (quanto mais tempo, mais gasto).
- Correlações negativas esperadas entre churn e `tenure`/`Qtd_Servicos`.
- Heatmap visualiza relações relevantes entre variáveis para futuras modelagens.

---

## ✅ Conclusões

- **A maior parte da evasão ocorre nos primeiros meses**.
- Perfis com **contratos curtos, poucos serviços e sem relacionamento próximo** com a empresa têm maior propensão ao churn.
- A **qualidade e diversidade dos serviços contratados** influencia diretamente na fidelização.

---

## 💡 Recomendações

- Incentivar **contratos de longo prazo** com benefícios.
- Oferecer **serviços adicionais gratuitos** nos primeiros meses.
- Estimular o uso de **pagamentos automáticos**.
- Implementar ações preventivas com clientes de **baixo engajamento**.
- Utilizar essas variáveis como base para um **modelo preditivo de churn**.

---

## 🧰 Tecnologias utilizadas

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Google Colab / Jupyter Notebook

---

## 📁 Arquivo

- `TelecomX_BR.ipynb`: Notebook com todo o processo de análise e visualizações.

---

## 📬 Autor

Rodrigo Corsini Lueneberg


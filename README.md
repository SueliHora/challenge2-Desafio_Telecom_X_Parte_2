# Projeto de Previsão de Churn - Telecom X (Parte 2)

## 1. Resumo do Objetivo

O objetivo deste projeto foi desenvolver um modelo de machine learning para prever a evasão de clientes (churn) na empresa fictícia Telecom X. Além de construir um modelo preditivo eficaz, o projeto buscou identificar os principais fatores demográficos e de serviço que influenciam a decisão de um cliente cancelar seu contrato, a fim de embasar decisões estratégicas de negócio.

---

## 2. Estrutura do Projeto e Ferramentas

O projeto foi desenvolvido em um notebook Jupyter (`.ipynb`) utilizando Python e as seguintes bibliotecas principais:

* **Pandas:** Para manipulação e pré-processamento dos dados.
* **Scikit-learn:** Para a criação, treinamento e avaliação dos modelos de machine learning, além do escalonamento de dados.
* **Matplotlib / Seaborn (Opcional):** Para visualizações exploratórias.

O repositório está organizado da seguinte forma:
* `README.md`: Este arquivo, com a documentação completa do projeto.
* `analise_churn_parte2.ipynb`: O notebook com todo o código e a análise.
* `dados_tratados.csv`: O conjunto de dados limpo e tratado, utilizado como entrada para a modelagem.

---

## 3. Desempenho e Escolha do Modelo

Foram treinados e avaliados dois modelos de classificação: **Regressão Logística** e **Random Forest**.

O modelo de **Regressão Logística foi escolhido como o campeão**, pois apresentou um desempenho superior na tarefa mais crítica para o negócio: identificar clientes com risco real de churn. Os resultados comparativos foram:

| Métrica                 | Regressão Logística | Random Forest |
| ----------------------- | ------------------- | ------------- |
| Acurácia Geral          | 79.74%              | 77.75%        |
| **Recall (Churn = 1)** | **54%** | 46%           |
| Precisão (Churn = 1)    | 64%                 | 61%           |

O **recall** foi a métrica de desempate, pois indica a capacidade do modelo de encontrar os clientes que de fato irão cancelar, permitindo que a empresa atue de forma proativa sobre eles.

---

## 4. Principais Insights (Análise dos Fatores)

A análise dos coeficientes do modelo de Regressão Logística revelou os principais fatores de risco e retenção:

#### Fatores de Risco (Aumentam a Chance de Churn)
* **Tipo de Internet:** Ter serviço de Fibra Óptica é o maior indicador de risco.
* **Forma de Pagamento:** Clientes que utilizam Cheque Eletrônico tendem a cancelar mais.
* **Faturamento:** A adesão à Fatura Digital (Paperless Billing) também está associada a um maior churn.

#### Fatores de Retenção (Diminuem a Chance de Churn)
* **Tipo de Contrato:** Este é o fator de maior proteção. Contratos de 1 ou 2 anos reduzem drasticamente a chance de evasão.
* **Serviços Adicionais:** A contratação de Suporte Técnico e Segurança Online são fortes indicadores de que um cliente irá permanecer.

---

## 5. Recomendações Estratégicas

Com base nos insights, as seguintes ações são recomendadas:

1.  **Fidelização por Contrato:** Criar campanhas de marketing agressivas para incentivar clientes de planos mensais a migrarem para contratos de 1 ou 2 anos, oferecendo descontos ou benefícios claros.
2.  **Investigar o Serviço de Fibra:** Realizar uma análise aprofundada (ex: pesquisa de satisfação) com os clientes de Fibra Óptica para entender a causa da alta evasão. O problema está no preço, na qualidade do serviço ou na forte concorrência?
3.  **Agregar Valor com Segurança:** Promover pacotes que incluam Suporte Técnico e Segurança Online como diferenciais, uma vez que estes serviços provaram ser importantes para a retenção.

---

## 6. Como Executar o Projeto

1.  Clone este repositório para a sua máquina local.
2.  Certifique-se de ter Python e as bibliotecas mencionadas (`pandas`, `scikit-learn`) instaladas.
3.  Abra o notebook `analise_churn_parte2.ipynb` em um ambiente como Jupyter Notebook ou Google Colab.
4.  Se estiver usando o Google Colab, faça o upload do arquivo `dados_tratados.csv` para o ambiente de execução.
5.  Execute as células do notebook em sequência.



Feito por: Sueli da Hora Moreira

# 👮‍♂️ Análise de Segurança Pública: Dinâmica Criminal e Produtividade (2024)

**Status:** ✅ Concluído

**Ferramentas:** `Python` `Pandas` `Matplotlib` `Statsmodels` `Seaborn`

**Autor:** Matheus Araujo Castro

---

## 📋 Sobre o Projeto
Este projeto realiza uma análise exploratória e estatística sobre os indicadores de segurança pública, cruzando dados de **Boletins de Ocorrência (BOs)**,  **Produtividade Policial** e dados coletados na pesquisa **Origem/Destino - Metrô/SP** registrados no ano de 2024.

O objetivo principal foi investigar se variáveis demográficas (como densidade populacional e renda) e operacionais possuem correlação linear direta com o volume de crimes registrados na região.

---

## ⚙️ Metodologia (Framework OSEMN)
O projeto foi estruturado seguindo o ciclo de vida de Ciência de Dados **OSEMN**:

### 1. **O**btain (Coleta)
* **Fontes:** Dados oficiais do [Portal da Transparência da SSP-SP](http://www.ssp.sp.gov.br/), Dados da pesquisa Origem Destino [Pesquisa Origem Destino, Metrô/SP] (https://www.metro.sp.gov.br/pt_BR/pesquisa-od/),
* 
* **Dados:** Registros de ocorrências criminais e índices de produtividade (prisões, apreensões) de Jan/2024 a Dez/2024.

### 2. **S**crub (Limpeza)
* Conversão de tipos de dados (Datas, coordenadas, padronização textual).
* Tratamento de valores nulos e padronização encontrado nas tabelas e durante os merges realizados.
* Criação de *features* derivadas (ex: "Crimes com emprego da violência").

### 3. **E**xplore (Análise Exploratória)
* Análise de sazonalidade: Identificação de picos de crimes por mês e dia da semana, horário.
* Geolocalização: Mapeamento inicial das regiões com maior volume de registros, distribuição no mapa do estado.
* Matriz de Correlação: Estudo das relações entre variáveis.

### 4. **M**odel (Modelagem)
Foi aplicado um modelo de **Regressão Linear Múltipla (OLS)** utilizando a biblioteca `statsmodels` para testar a seguinte hipótese:
> *"A densidade populacional, a renda média e a circulação de pessoas explicam a variação dos índices criminais?"*

### 5. **I**Nterpret (Resultados e Conclusão)
A modelagem revelou um **$R^2$ de 0.615** (61,5%).

**📉 Insight de Negócio:**
Às amostras indicaram que há alta correlação entre às variáveis e que elas possuem força para explicar os índices criminais de uma região. É necessário, granularizar às análises para validar se a tendência se repete em um contexto com mais variância e mais anos.
Acredito que o modelo pode se tornar mais robusto, a partir do emprego de outras variáveis, não exploradas por aqui.

---
Para executar, clone o projeto, para acessar, clique no arquivo "Análise_dados_ssp_24.ipynb".

<img width="1414" height="2000" alt="phginfogr" src="https://github.com/user-attachments/assets/cc5860d4-2a8b-45b1-92c4-8816b83a84fb" />

# 📘 Dicionário de Dados – UF

O **Dicionário de Dados por Unidade da Federação (UF)** é um documento oficial que define e padroniza os principais indicadores de criminalidade registrados no Brasil, dentro do sistema **Sinesp Integração**.  

Ele serve como **base conceitual e metodológica**, garantindo consistência e comparabilidade entre os dados fornecidos pelos diferentes estados.

---

## 🔎 Conteúdo do Dicionário

### 1. Indicadores e Definições
Cada tipo de crime é descrito de forma detalhada, especificando:
- O que caracteriza a ocorrência (ex.: homicídio doloso, estupro, roubo de carga etc.).
- Critérios legais e técnicos para classificação.
- Observações sobre exceções e enquadramentos específicos.

### 2. Unidades de Medida
As métricas padronizadas utilizadas incluem:
- **Ocorrências** → número de registros de crimes.  
- **Vítimas** → número de pessoas registradas como vítimas.  
- **População** → estimativa oficial do IBGE (2018).  
- **Taxa/100.000** → taxa padronizada de crimes por 100 mil habitantes, permitindo comparações entre estados.

### 3. Notas e Observações
O dicionário explica limitações e cuidados para interpretar os dados:
- Padronização oficial passou a vigorar após 2018.  
- Diferenças podem ocorrer devido a métodos de coleta e consolidação estaduais.  
- Há defasagens de atualização em alguns períodos.

### 4. Escopo Temporal e Geográfico
- Os dados são apresentados por **mês/ano**, abrangendo registros de **2015 em diante**.  
- A unidade geográfica de análise é a **Unidade da Federação (estado)**.

### 5. Fonte
- Dados extraídos diretamente das soluções **SinespJC** e **Sinesp Integração**.  
- Exemplo de extração presente no documento: **14/03/2019**.

---

## ✅ Importância
Esse dicionário garante que os dados analisados sejam **claros, comparáveis e confiáveis**, evitando interpretações incorretas sobre os registros de criminalidade ao longo dos estados brasileiros.

# 📘 Dicionário de Dados – Municípios

O **Dicionário de Dados por Município** complementa o dicionário por Unidade da Federação (UF), mas com foco em uma granularidade **local**. Ele estabelece as definições, métricas e metodologias para análise dos crimes registrados em nível municipal.

---

## 🔎 Conteúdo do Dicionário

### 1. Indicadores e Definições
- Foco em crimes como **homicídio doloso** e outros tipos de violência.  
- São utilizados os mesmos critérios legais e técnicos do dicionário por UF, garantindo consistência.  
- Especifica exceções (ex.: exclusão de feminicídio do indicador de homicídio doloso) e detalha a forma de classificação segundo o **Código Penal**.

### 2. Unidades de Medida
- **Vítimas** → número de pessoas registradas como vítimas em boletins de ocorrência.  
- Essa é a principal métrica utilizada para mensurar o impacto da violência em nível municipal.

### 3. Metodologia
- Os dados são fornecidos pelas **Secretarias Estaduais de Estatística e Segurança Pública**, por meio da **Coordenação Geral de Estatística (CGESt)**.  
- Processo envolve **coleta mensal**, **validação** e **atualização periódica**.  
- Sistemas utilizados:  
  - **SinespJC**  
  - **Sinesp Integração**  
- Após validação, os dados são encaminhados para atualização das bases nacionais e para alimentar o **painel público de estatísticas de segurança**.

### 4. Notas Importantes
- Registros anteriores a **dezembro/2018** podem não seguir a padronização oficial da Portaria nº 229/2018.  
- Diferenças podem ocorrer entre totais por UF e Municípios devido a ajustes de coleta, tratamento e consolidação feitos pelos estados.  
- Exemplo: em 2019, o estado do Amapá apresentou cobertura maior após avanços na implantação do sistema.

### 5. Unidade Geográfica e Periodicidade
- **Unidade Geográfica de Análise:** Município.  
- **Periodicidade:**  
  - Coleta mensal.  
  - Publicação até o dia 15 de cada mês.  
  - Atualização com dados de até 3 meses anteriores ao mês da coleta.

### 6. Fonte
- Dados validados e disponibilizados pelos **Gestores Estaduais de Estatística**.  
- Extraídos dos sistemas **SinespJC** e **Sinesp Integração**.

---

## ✅ Importância
Esse dicionário é essencial para análises **granulares e comparativas entre municípios**, permitindo observar padrões locais de criminalidade, identificar áreas críticas e orientar políticas públicas de segurança com maior precisão.

# 📊 Arquivos XLSX Brutos

Além dos dicionários de dados (UF e Municípios), o projeto utiliza como **fonte primária** os arquivos **XLSX brutos** disponibilizados pelo **Sinesp (Sistema Nacional de Segurança Pública)**. Esses arquivos são a base para todas as transformações realizadas nas camadas **Bronze → Silver → Gold** do pipeline de dados.

---

## 🗂️ Estrutura dos Arquivos

Os arquivos seguem um padrão dividido em **abas (sheets)** por **Unidade da Federação (UF)**, cada uma contendo registros de crimes e vítimas. Entre os principais campos presentes:

- **Cod_IBGE** → Código único de identificação do município.  
- **Município** → Nome oficial do município.  
- **Sigla UF** → Abreviação da Unidade Federativa (ex.: AC, SP, RS).  
- **Região** → Macrorregião correspondente (Norte, Nordeste, Sudeste, Sul, Centro-Oeste).  
- **Mês/Ano** → Período da ocorrência ou registro.  
- **Tipo de Crime** → Classificação do crime (ex.: Homicídio Doloso, Estupro, Roubo de Veículo etc.).  
- **Sexo da Vítima** → Feminino, Masculino ou "Sexo NI" (não informado).  
- **Ocorrências** → Quantidade de ocorrências registradas para aquele crime no período.  
- **Vítimas** → Número de pessoas registradas como vítimas.

---

## 🔄 Relação com os Dicionários

Os dicionários de dados (UF e Municípios) funcionam como **guia de interpretação** dos XLSX, garantindo que:

- **Indicadores** (ex.: Homicídio Doloso, Estupro) sejam entendidos de forma padronizada.  
- **Unidades de medida** (Vítimas, Ocorrências, Taxa/100000) sejam aplicadas corretamente.  
- **Metodologia** (coleta, atualização, publicação) seja respeitada, assegurando a confiabilidade da análise.  

Assim, os arquivos brutos **não devem ser interpretados isoladamente**: o dicionário garante consistência legal, técnica e metodológica.

---

## ⏱️ Periodicidade e Atualização

- Os dados são **mensais**, com cada linha representando um agregado por UF ou Município.  
- As planilhas podem conter diferenças de cobertura dependendo do período e da evolução do sistema Sinesp em cada estado.  
- Atualizações seguem o fluxo descrito no dicionário:
  - **Coleta mensal**
  - **Validação** pelas Secretarias Estaduais
  - **Publicação** no painel oficial até o dia 15 de cada mês

---

## ✅ Importância para o Pipeline

Os **arquivos XLSX brutos** representam a **camada de entrada (Landing → Bronze)** do pipeline.  
É a partir deles que:
1. Os dados são **ingeridos e normalizados**.  
2. Passam por limpeza e padronização (Silver).  
3. São agregados, enriquecidos e preparados para análises avançadas e dashboards (Gold).

Sem essa base estruturada, não seria possível construir as análises regionais, comparativos e indicadores derivados que alimentam o projeto.


# 🥉Camada Bronze - Ingestão & Padronização

A **Camada Bronze** do projeto SINESP é responsável por **ingerir os arquivos brutos (XLSX)**, baixados do portal [dados.gov.br](https://dados.gov.br/dados/conjuntos-dados/sistema-nacional-de-estatisticas-de-seguranca-publica), e transformá-los em **tabelas Delta padronizadas**, prontas para uso nas próximas camadas (**Silver** e **Gold**).

---

## 🎯 Objetivos da Bronze
- **Automatizar a ingestão** dos arquivos publicados (UF e Municípios).  
- **Versionar os binários** (hash SHA256 + data de aquisição).  
- **Manter um manifesto** com metadados de cada arquivo baixado.  
- **Padronizar colunas e tipos** para simplificar o consumo posterior.  
- **Armazenar todos os registros sem perder informação**, mesmo que inconsistentes, aplicando apenas “checks leves”.

---

## 📂 Estrutura dos Diretórios (Landing)
Os arquivos originais são salvos em um **Volume Unity Catalog**:
- **sha256** → assinatura única para identificar o binário.
- **acquired_date** → data em que o arquivo foi adquirido.
- **manifest.csv** → log com informações de URL, tamanho, hash, ETag, Last-Modified.

---
## 🛠️ Principais Scripts

### 1. 📥 Download & Landing
Arquivo: **data**  
- Descobre URLs via **API CKAN** do Ministério da Justiça.  
- Faz download com **retry e backoff exponencial**.  
- Gera hash `sha256` para cada arquivo.  
- Cria diretório no landing com `acquired_date` + `sha256`.  
- Registra o arquivo no **manifesto** para auditoria.

### 2. 🏙️ Ingestão de Municípios
Arquivo: **Ingestao_dos_DadosMunicípio**  
- Localiza o XLSX mais recente no landing.  
- Abre as **27 abas** (uma por UF).  
- Normaliza colunas (`cod_ibge`, `municipio`, `uf`, `regiao`, `mes_ano`, `vitimas`).  
- Faz parsing de `mes_ano` → `ano`, `mes`, `year_month`.  
- Aplica checks leves:
  - `vitimas >= 0`
  - `uf` consistente
- Cria tabelas por UF (`sinesp.bronze.DadosMunicipioAC`, etc).  
- Cria tabela unificada (`sinesp.bronze.municipios_raw_row`), particionada por `uf`, `ano`, `mes`.

### 3. 🏛️ Ingestão por UF
Arquivo: **Ingestao_dos_DadosUF**  
- Localiza XLSX mais recente da pasta **uf**.  
- Identifica abas: `Ocorrências` e `Vítimas`.  
- Normaliza colunas (`uf_nome`, `uf_sigla`, `tipo_crime`, `ano`, `mes`, `ocorrencias`, `vitimas`, `sexo_vitima`).  
- Faz parsing de `Mês` (texto) → número (`janeiro → 1`).  
- Aplica checks leves:
  - UF válida
  - Sem valores negativos
- Cria tabelas:
  - `sinesp.bronze.ufocorrencias`
  - `sinesp.bronze.ufvitimas`

---

## 🧹 Padronização Aplicada
- **Colunas em snake_case**.  
- **Datas parseadas** para `ano` (INT), `mes` (INT), `year_month` (DATE).  
- **Tipos numéricos coerentes** (`cod_ibge` = BIGINT, `vitimas/ocorrencias` = INT).  
- **Metadados preservados** (`_ingestion_ts`, `_source_path`) para rastreabilidade.  

---

## ✅ Benefícios da Bronze
- Mantém os **dados integrais** do SINESP (mesmo inconsistentes).  
- Garante **reprodutibilidade** (manifesto + versionamento por hash).  
- Simplifica a transição para Silver (onde serão aplicadas regras de qualidade mais rígidas).  
- Permite auditoria: qualquer dado analisado pode ser rastreado até o **arquivo bruto**.

---

# 🥈 Camada Silver – Transformações 

A **camada Silver** é responsável por transformar os dados brutos da Bronze em um formato **padronizado, confiável e pronto para análises**.  
Enquanto a Bronze preserva os dados praticamente crus, a Silver aplica **ajustes, validações e padronizações** que garantem consistência e eliminam ruídos.

---

## 🔄 Objetivo da Silver
- Corrigir e validar campos como **ano, mês e UF**.  
- Padronizar nomes de colunas e tipos de dados.  
- Tratar valores nulos ou inconsistentes.  
- Preparar os dados para análises na **camada Gold** e para dashboards em **Databricks SQL**.  

---

## 📂 Estrutura dos Notebooks

Dentro da pasta `notebooks/silver_transformations/` existem três notebooks principais:

### 1. `transformaçãomunicipios.ipynb`
- **Fonte**: `sinesp.bronze.municipios_raw_row`  
- **Transformações**:
  - Derivação de `ano` e `mes` a partir de `mes_ano`.
  - Padronização de colunas (`cod_ibge`, `municipio`, `uf_sigla`, `regiao`, `vitimas`).
  - Validação de registros com ano/mês válidos.
- **Saída**: `sinesp.silver.municipios_vitimas`

👉 Permite análises detalhadas por **município**.

---

### 2. `transformaçãoocorrencias.ipynb`
- **Fonte**: `sinesp.bronze.ufocorrencias`  
- **Transformações**:
  - Padronização de colunas (`uf_nome`, `uf_sigla`, `tipo_crime`, `ano`, `mes`, `ocorrencias`).
  - Conversão de colunas para tipos corretos.
  - Filtro de registros inválidos.
- **Saída**: `sinesp.silver.uf_ocorrencias`

👉 Permite acompanhar o volume de **ocorrências criminais por UF**.

---

### 3. `transformaçãovitima.ipynb`
- **Fonte**: `sinesp.bronze.ufvitimas`  
- **Transformações**:
  - Padronização de colunas (`uf_nome`, `uf_sigla`, `tipo_crime`, `sexo_vitima`, `ano`, `mes`, `vitimas`).
  - Normalização de valores de sexo (`Feminino`, `Masculino`, `Sexo NI`).
  - Conversão para tipos consistentes.
- **Saída**: `sinesp.silver.uf_vitimas`

👉 Possibilita análises sobre o **perfil das vítimas por UF e sexo**.

---

## 📊 Tabelas Resultantes

1. **`sinesp.silver.municipios_vitimas`**  
   - Campos principais: `cod_ibge`, `municipio`, `uf_sigla`, `regiao`, `ano`, `mes`, `vitimas`.

2. **`sinesp.silver.uf_ocorrencias`**  
   - Campos principais: `uf_sigla`, `uf_nome`, `tipo_crime`, `ano`, `mes`, `ocorrencias`.

3. **`sinesp.silver.uf_vitimas`**  
   - Campos principais: `uf_sigla`, `uf_nome`, `tipo_crime`, `sexo_vitima`, `ano`, `mes`, `vitimas`.

---

## ✅ Benefícios
- Dados **limpos e padronizados**.  
- **Consistência** entre diferentes fontes (municípios e UFs).  
- Base pronta para **dashboards interativos** e relatórios.  
- Facilita a criação de visões consolidadas na **camada Gold**.  

---

# 🥇 Camada Gold - Views

A **camada Gold** é a etapa final do pipeline de dados, responsável por **enriquecer, consolidar e disponibilizar** os dados já tratados na Silver em um formato **otimizado para análises** e pronto para dashboards.  
Aqui, garantimos que os dados estejam organizados em **visões regionais e nacionais**, simplificando a exploração e reduzindo a complexidade para os analistas.

---

## 🎯 Objetivo da Gold
- Adicionar a **dimensão Região** (Norte, Nordeste, Centro-Oeste, Sudeste, Sul) às tabelas por UF.  
- Criar **views por região** (UF e Municípios), otimizando consultas.  
- Consolidar os dados para consumo direto em ferramentas analíticas como **Databricks SQL** e **Power BI**.  

---

## 📂 Estrutura dos Notebooks

Dentro da pasta `notebooks/gold_enrichment/` existem dois tipos de notebooks principais:

### 1. `regiao_nas_tabelas.ipynb`
- **Fonte**:  
  - `sinesp.silver.uf_vitimas`  
  - `sinesp.silver.uf_ocorrencias`
- **Transformações**:
  - Mapeamento de cada UF para a sua respectiva **região** (ex.: `RS`, `SC`, `PR` → `SUL`).  
  - Inclusão da coluna `regiao` nas tabelas.  
  - Escrita em tabelas finais da Gold.
- **Saídas**:  
  - `sinesp.gold.uf_vitimas`  
  - `sinesp.gold.uf_ocorrencias`

👉 Permite análises comparativas por **macrorregião brasileira**.

---

### 2. `view_<regiao>.ipynb` (ex.: `view_sul.ipynb`, `view_nordeste.ipynb`)
- **Fonte**:  
  - `sinesp.gold.uf_vitimas`  
  - `sinesp.gold.uf_ocorrencias`  
  - `sinesp.silver.municipios_vitimas` (para nível municipal)
- **Transformações**:
  - Criação de **views SQL** filtrando os dados apenas da região desejada.  
  - São geradas três views por região:
    1. `view_<regiao>_uf_ocorrencias`  
    2. `view_<regiao>_uf_vitimas`  
    3. `view_<regiao>_municipios_vitimas`
- **Exemplo de saída** (para a região Sul):
  - `sinesp.gold.view_sul_uf_ocorrencias`  
  - `sinesp.gold.view_sul_uf_vitimas`  
  - `sinesp.gold.view_sul_municipios_vitimas`

👉 Simplifica o consumo de dados por região sem necessidade de aplicar filtros adicionais.

---

## 📊 Tabelas Resultantes

1. **`sinesp.gold.uf_vitimas`**  
   - Campos principais: `uf_sigla`, `uf_nome`, `regiao`, `tipo_crime`, `sexo_vitima`, `ano`, `mes`, `vitimas`.

2. **`sinesp.gold.uf_ocorrencias`**  
   - Campos principais: `uf_sigla`, `uf_nome`, `regiao`, `tipo_crime`, `ano`, `mes`, `ocorrencias`.

3. **`sinesp.gold.view_<regiao>_*`**  
   - Views segmentadas por região (`Norte`, `Nordeste`, `Centro-Oeste`, `Sudeste`, `Sul`).  
   - Facilita análises rápidas e dashboards focados em determinada região.

---

## ✅ Benefícios
- Inclusão da dimensão **Região**, essencial para análises macro.  
- Criação de **views por região**, reduzindo a complexidade em consultas SQL.  
- **Padronização** das tabelas finais para dashboards interativos.  
- Dados prontos para integração com ferramentas de **BI e Analytics**.  

---
# 📊 Dashboards Regionais 

Os **dashboards regionais** foram desenvolvidos em **Databricks SQL** e seguem a mesma lógica estrutural, mudando apenas o **foco geográfico** (Norte, Nordeste, Centro-Oeste, Sudeste e Sul).  

Cada painel organiza os indicadores de segurança pública em **KPIs, comparativos e análises temporais**, permitindo uma visão **consolidada e interativa** da violência no Brasil.

---

## 🧩 Estrutura Comum dos Dashboards

Todos os dashboards regionais seguem o mesmo padrão:
<img width="1600" height="673" alt="image" src="https://github.com/user-attachments/assets/eac685d6-830f-4979-bfce-c3f48237184d" />

### 🔹 KPIs Principais
- **Total de vítimas** → mostra o volume agregado de vítimas da região.  
  👉 *Insight*: avalia a magnitude da violência ao longo dos anos.  
- **Total de ocorrências** → contabiliza os registros de crimes.  
  👉 *Insight*: mede o nível de atividade criminal (independente do número de vítimas).  
- **Município com mais vítimas (Top 1)** → identifica a cidade mais crítica da região.  
  👉 *Insight*: direciona políticas públicas locais.  
- **Ano mais violento** → mostra o ano com maior número de vítimas.  
  👉 *Insight*: ajuda a analisar tendências históricas de aumento/redução da violência.  

---
<img width="1600" height="469" alt="image" src="https://github.com/user-attachments/assets/8a9ef854-80f8-433c-bd2a-0f5ec1584893" />
<img width="1600" height="469" alt="image" src="https://github.com/user-attachments/assets/48c92e98-2c6b-44e1-a4d1-b13b5026bfd9" />
### 🔹 Análises por UF
- **Evolução mensal de vítimas por UF** (linha temporal).  
  👉 *Insight*: permite comparar padrões entre estados da mesma região.  
- **Ranking de vítimas por UF** (barras).  
  👉 *Insight*: evidencia quais estados concentram maior número de vítimas.  

---
<img width="1600" height="452" alt="image" src="https://github.com/user-attachments/assets/76f898a8-7b30-4186-89a6-a2b5bd260dec" />
<img width="1600" height="458" alt="image" src="https://github.com/user-attachments/assets/d1802c9f-2d4e-4633-a98b-9daf21cdc90a" />

### 🔹 Análises por Município
- **Top 15 municípios com mais vítimas** (barras).  
  👉 *Insight*: identifica focos locais de violência urbana e rural.  
- **Evolução mensal dos 15 municípios mais violentos** (linha temporal).  
  👉 *Insight*: monitora mudanças no comportamento criminal de cidades críticas.  

---

### 🔹 Temas Específicos
- **Ranking de tipos de crime por ocorrências** (barras).  
  👉 *Insight*: mostra os crimes mais frequentes (ex.: furto de veículo, homicídio, estupro).  
- **Distribuição de vítimas por sexo** (pizza).  
  👉 *Insight*: identifica o perfil das vítimas (masculino, feminino, sexo não informado).  
- **Tabela: Tipo de crime × UF por vítimas**.  
  👉 *Insight*: compara a gravidade de crimes específicos entre estados da região.  
- **Tabela: Vítimas por UF e sexo**.  
  👉 *Insight*: cruza perfil da vítima com localização.  

---
<img width="1600" height="450" alt="image" src="https://github.com/user-attachments/assets/1568e219-9a62-4bde-abde-1ac8caf46b36" />
<img width="1600" height="402" alt="image" src="https://github.com/user-attachments/assets/efdb067a-3d1f-41d3-9d0c-18635aeefc74" />

## ✅ Benefícios dos Dashboards
- Oferecem **comparação regional** (Norte, Nordeste, Centro-Oeste, Sudeste e Sul).  
- Permitem identificar **hotspots de violência** em municípios e estados.  
- Auxiliam no **planejamento de políticas públicas** de segurança.  
- Viabilizam análises detalhadas por **tipo de crime** e **perfil de vítimas**.  
- Servem de base para **relatórios oficiais e estudos acadêmicos**.  

---

📌 **Resumo**:  
Os dashboards regionais seguem a mesma arquitetura, mudando apenas a região analisada. Eles possibilitam insights estratégicos sobre **quando, onde e como a violência acontece**, apoiando decisões de gestores e pesquisadores.





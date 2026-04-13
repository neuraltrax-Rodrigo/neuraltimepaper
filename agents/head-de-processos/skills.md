# Skills

## Mapeamento e Documentação de Processos

* **Descrição:** Mapeia como uma área ou fluxo da Neural Trax opera e gera documentação clara com etapas, responsável e ferramentas.
* **Input:** Descrição do processo pelo Head responsável (via Slack ou entrevista estruturada)
* **Output:** SOP (Standard Operating Procedure) com: objetivo, gatilho, etapas numeradas, responsável por etapa e critério de conclusão
* **Tools:** Claude API, Slack MCP, Google Sheets
* **Processo:**
  1. Coletar descrição do processo com o Head da área
  2. Identificar gatilho, etapas, responsáveis e resultado esperado
  3. Redigir SOP em linguagem simples (sem jargão)
  4. Validar com o Head da área antes de publicar
  5. Registrar no repositório de processos no Google Sheets
* **Regras:**
  * Máximo de 10 etapas por SOP — se precisar de mais, dividir em sub-processos
  * Todo processo tem dono definido — sem dono, não é publicado
  * Revisão obrigatória a cada 90 dias ou após mudança de ferramenta/fluxo

## Definição e Revisão de KPIs

* **Descrição:** Extrai e valida os KPIs mais relevantes por frente — eliminando métricas de vaidade e priorizando indicadores que mudam comportamento.
* **Input:** Objetivos da área, processos documentados, dados disponíveis no dashboard do Head de Dados
* **Output:** Lista de KPIs por área com: nome, fórmula de cálculo, frequência de medição, responsável e threshold de alerta (🟡/🔴)
* **Tools:** Claude API, Google Sheets, Slack MCP
* **Processo:**
  1. Mapear objetivos da área (o que ela precisa entregar?)
  2. Listar candidatos a KPI com base nos processos documentados
  3. Filtrar: manter apenas KPIs que são mensuráveis, influenciáveis e relevantes para decisão
  4. Validar com Head de Dados se os dados estão disponíveis para coleta
  5. Definir thresholds de alerta com o CEO
  6. Publicar KPIs aprovados na planilha mestre
* **Regras:**
  * Máximo de 5 KPIs por área — menos é mais
  * KPI sem fórmula de cálculo clara não entra na lista
  * Revisão de KPIs a cada trimestre junto com a revisão de OKRs

## Estruturação de OKRs

* **Descrição:** Converte a visão estratégica do CEO em OKRs trimestrais por área — com Objetivos inspiradores e Key Results mensuráveis.
* **Input:** Visão e prioridades do CEO para o período, performance do trimestre anterior, KPIs ativos por área
* **Output:** OKRs do trimestre por área no formato padrão: 1 Objetivo + 3 Key Results com meta numérica, responsável e prazo
* **Tools:** Claude API, Asana MCP, Slack MCP
* **Processo:**
  1. Reunir visão e prioridades do CEO via Slack ou alinhamento direto
  2. Revisar performance do trimestre anterior por área
  3. Redigir Objetivo por área (qualitativo, motivador, claro)
  4. Definir 3 Key Results por Objetivo (quantitativos, com meta e prazo)
  5. Validar com CEO antes de distribuir
  6. Publicar OKRs no Asana e comunicar aos Heads via Slack
* **Regras:**
  * 1 Objetivo por área por trimestre — foco é a estratégia
  * Key Result sem número não é Key Result — é tarefa
  * OKRs publicados até o 2º dia útil de cada trimestre
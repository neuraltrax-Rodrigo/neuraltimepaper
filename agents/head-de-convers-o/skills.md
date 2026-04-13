# Skills

## Consolidação Diária do Pipeline

* **Descrição:** Coleta os relatórios diários do SDR, BDR, Closer e Contratos, consolida no dashboard e identifica deals que precisam de atenção imediata.
* **Input:** Relatórios diários do squad via Slack
* **Output:** Pipeline atualizado no Google Sheets + alerta no Slack para deals parados ou leads sem follow-up há mais de 2 dias
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Coletar relatórios do SDR, BDR, Closer e Contratos
  2. Atualizar pipeline com novas interações, avanços e perdas
  3. Calcular taxas de conversão do dia por etapa
  4. Identificar deals sem movimentação há mais de 2 dias
  5. Enviar alerta ao agente responsável com orientação de next step
* **Regras:**
  * Consolidação obrigatória todo dia útil até 18h
  * Deal parado há mais de 5 dias sem ação documentada é escalado ao Head de Growth

## Diagnóstico de Gargalo de Funil

* **Descrição:** Identifica em qual etapa do funil está ocorrendo a maior perda de conversão e gera plano tático de desbloqueio.
* **Input:** Taxas de conversão por etapa da semana, motivos de perda registrados pelo Closer, insights da Transcrição
* **Output:** Diagnóstico com: etapa crítica identificada, causa provável, ação corretiva por agente (SDR, BDR ou Closer) e prazo de reavaliação
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Mapear taxas de conversão etapa a etapa: lead → contato → reunião → proposta → contrato
  2. Identificar a etapa com maior queda percentual
  3. Cruzar com motivos de perda e objeções da semana
  4. Gerar hipótese de causa e ação corretiva específica por agente
  5. Enviar diagnóstico ao squad e ao Head de Growth
* **Regras:**
  * Diagnóstico semanal obrigatório toda quarta-feira
  * Foco em um gargalo por vez — não otimizar tudo ao mesmo tempo

## Briefing Diário do Squad

* **Descrição:** Abre o dia de operação do squad com metas, foco e orientações táticas do dia.
* **Input:** Pipeline do dia anterior, metas da semana, gargalo ativo identificado
* **Output:** Mensagem no Slack ao squad com: número de ontem, foco do dia, meta e 1 orientação tática específica
* **Tools:** Slack MCP, Google Sheets
* **Processo:**
  1. Ler consolidação do dia anterior no pipeline
  2. Calcular distância da meta semanal
  3. Definir foco tático do dia com base no gargalo ativo
  4. Redigir briefing curto e energético
  5. Publicar no canal do squad às 08h30
* **Regras:**
  * Máximo de 150 palavras — objetivo e direto
  * Sempre começa com 1 número de ontem e termina com 1 ação do dia

## Relatório Semanal para o Head de Growth

* **Descrição:** Consolida a performance semanal do funil e entrega visão completa ao Head de Growth com diagnóstico e próximos movimentos.
* **Input:** Pipeline da semana, taxas por etapa, MRR novo, motivos de perda, insights da Transcrição
* **Output:** Relatório no Slack ao Head de Growth com: MRR novo, reuniões realizadas, propostas enviadas, contratos fechados, taxa de conversão por etapa, principal gargalo e plano de ação para a semana seguinte
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Consolidar dados da semana no Google Sheets
  2. Calcular KPIs: reuniões, propostas, fechamentos, taxa por etapa, MRR novo
  3. Identificar principal gargalo e causa provável
  4. Definir ação prioritária para a semana seguinte
  5. Enviar toda sexta-feira às 16h00 ao Head de Growth
* **Regras:**
  * Relatório sempre inclui motivo das 3 principais perdas da semana
  * Nunca enviar sem plano de ação para o gargalo identificado
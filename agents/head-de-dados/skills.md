# Skills

## Coleta e Consolidação de Dados

* **Descrição:** Coleta dados de todas as frentes da empresa e os consolida no dashboard central de KPIs no Google Sheets.
* **Input:**
  * Fontes de dados por frente: Google Sheets das áreas, Google Analytics, Meta Ads, relatórios de plataformas
  * Período de referência (dia, semana, mês)
* **Output:** Dashboard de KPIs atualizado no Google Sheets com dados de todas as frentes, organizados por área e período
* **Tools:** Google Sheets, Zapier MCP, Claude API
* **Processo:**
  1. Identificar fontes de dados ativas por frente (financeiro, growth, tráfego, retenção, engajamento, técnico)
  2. Coletar dados brutos de cada fonte via integração ou input manual
  3. Normalizar e consolidar no dashboard central
  4. Calcular KPIs derivados (variação %, médias, totais acumulados)
  5. Aplicar formatação condicional: 🟢 dentro da meta / 🟡 atenção / 🔴 crítico
* **Regras:**
  * Coleta diária obrigatória para KPIs críticos (MRR, leads, uptime, churn)
  * Coleta semanal para KPIs de performance de conteúdo e engajamento
  * Nenhum dado entra no dashboard sem validação de fonte

## Monitoramento e Emissão de Alertas Críticos

* **Descrição:** Monitora continuamente os KPIs críticos e emite alertas imediatos ao CEO e ao Head responsável quando um indicador ultrapassa o threshold de alerta.
* **Input:**
  * Dashboard de KPIs atualizado
  * Tabela de thresholds por KPI (limites de alerta 🟡 e crítico 🔴)
* **Output:** Alerta via Slack (DM ao CEO + mensagem no canal da área impactada) com: indicador afetado, valor atual vs. limite, diagnóstico inicial e recomendação de ação
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Varrer todos os KPIs monitorados e comparar com thresholds definidos
  2. Classificar cada KPI: 🟢 Normal / 🟡 Atenção / 🔴 Crítico
  3. Para cada KPI 🔴: gerar diagnóstico com Claude API (contexto + causa provável + impacto estimado)
  4. Enviar alerta imediato via Slack DM ao CEO e ao Head da área impactada
  5. Registrar alerta no log de monitoramento com timestamp e status de resolução
* **Regras:**
  * Alertas 🔴 são enviados imediatamente — não aguardam o próximo ciclo de relatório
  * Alertas 🟡 são agrupados e entregues no próximo relatório periódico
  * Todo alerta inclui: dado atual, meta, variação e recomendação de ação mínima
  * Nenhum alerta crítico é enviado sem diagnóstico — dado bruto sem interpretação não é alerta, é ruído

## Relatório Diário de Status

* **Descrição:** Gera resumo diário dos principais indicadores de cada frente e envia ao CEO antes do início do expediente.
* **Input:**
  * Dashboard de KPIs do dia anterior
  * Alertas emitidos nas últimas 24h
  * Comparação com dia anterior e média da semana
* **Output:** Mensagem no Slack para o CEO com: status por frente (🟢/🟡/🔴), destaques positivos, pontos de atenção e alertas ativos
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Coletar snapshot de KPIs do dia anterior
  2. Calcular variações vs. dia anterior e vs. média semanal
  3. Identificar destaques (melhor performance) e pontos de atenção (pioras relevantes)
  4. Redigir narrativa de status com Claude API em linguagem executiva
  5. Enviar via Slack para o CEO às 07h15 (antes do briefing do CEO às 07h30)
* **Regras:**
  * Máximo de 250 palavras — conciso e acionável
  * Formato fixo: Status por frente → Destaques → Atenções → Alertas ativos
  * Enviado todos os dias úteis sem exceção

## Relatório Semanal por Área

* **Descrição:** Gera relatório semanal de performance para cada Head de área, com dados específicos da sua frente, comparativo com a semana anterior e recomendações.
* **Input:**
  * KPIs da semana por frente
  * Histórico das últimas 4 semanas para comparação de tendência
  * Metas do período
* **Output:** Relatório individual por área enviado via Slack ao Head responsável, com: performance da semana, variação vs. semana anterior, tendência (crescendo/estável/caindo) e 1-3 recomendações de ação
* **Tools:** Google Sheets, Slack MCP, Gmail MCP, Claude API
* **Processo:**
  1. Filtrar KPIs relevantes por área no dashboard consolidado
  2. Calcular variação semanal e tendência das últimas 4 semanas
  3. Identificar o principal destaque e o principal ponto de melhoria da área
  4. Gerar narrativa analítica com recomendações via Claude API
  5. Enviar via Slack ao Head da área toda segunda-feira às 08h00
* **Regras:**
  * Cada Head recebe apenas os dados da sua frente — sem cruzamento de dados de outras áreas sem autorização do CEO
  * Toda recomendação deve ser específica e acionável — não "melhorar conversão", mas "testar novo script de abordagem no SDR"

## Relatório Executivo Mensal

* **Descrição:** Gera o relatório completo de performance da Neural Trax no mês — consolidando todas as frentes, identificando tendências estratégicas e apresentando recomendações para o CEO.
* **Input:**
  * KPIs consolidados do mês por frente
  * Comparativo com mês anterior e com meta do período
  * OKRs do período e % de atingimento
  * Alertas críticos emitidos no mês e status de resolução
* **Output:** Relatório executivo mensal completo enviado via Slack e Gmail ao CEO, com: visão geral de saúde da empresa, performance por frente, OKRs atingidos/em risco, top insights do mês e recomendações estratégicas para o próximo período
* **Tools:** Google Sheets, Slack MCP, Gmail MCP, Claude API
* **Processo:**
  1. Consolidar todos os KPIs do mês no dashboard
  2. Calcular atingimento de cada OKR do período
  3. Mapear as 3 maiores conquistas e os 3 maiores riscos do mês
  4. Redigir relatório narrativo completo com Claude API
  5. Enviar via Slack (resumo executivo) + Gmail (relatório completo formatado) no primeiro dia útil do mês seguinte
* **Regras:**
  * Relatório mensal deve incluir obrigatoriamente: MRR, churn rate, CAC, NPS, uptime e margem bruta
  * Deve conter pelo menos 3 recomendações estratégicas para o próximo mês
  * Linguagem executiva — sem jargão técnico sem explicação
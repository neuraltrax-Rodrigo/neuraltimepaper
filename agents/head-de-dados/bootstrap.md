# Bootstrap

* **Inicialização:**
  * Carregar arquivos de identidade (Identity.md, Soul.md) para contexto ativo
  * Instanciar sub-agentes: Analista de KPIs, Sentinela de Dados
  * Conectar ferramentas: Google Sheets, Slack MCP, Gmail MCP, Claude API, Zapier MCP
* **Setup inicial:**
  * Verificar acesso ao dashboard central de KPIs no Google Sheets
  * Confirmar conexões ativas com fontes de dados de cada frente (financeiro, growth, tráfego, retenção, engajamento, técnico)
  * Carregar tabela de thresholds de alerta por KPI — definir limites 🟡 e 🔴 para cada indicador monitorado
  * Verificar log de alertas das últimas 24h — identificar se há alertas críticos abertos sem resolução registrada
  * Confirmar canais Slack de cada Head de área e canal executivo do CEO
* **Primeira ação:**
  * Executar skill **Coleta e Consolidação de Dados** para atualizar o dashboard com dados mais recentes
  * Executar skill **Monitoramento e Emissão de Alertas Críticos** — varrer KPIs e verificar se há algum 🔴 ativo
  * Se não houver alerta crítico: gerar e enviar **Relatório Diário de Status** ao CEO às 07h15
  * Se houver alerta crítico: enviar alerta imediato ao CEO e ao Head da área impactada antes do relatório diário
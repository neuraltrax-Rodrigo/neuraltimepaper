# Bootstrap

* **Inicialização:**
  * Carregar arquivos de identidade (Identity.md, Soul.md) para contexto ativo
  * Instanciar sub-agentes: Ledger, Margin, Forecast, Fiscal
  * Conectar ferramentas: Google Sheets, Gmail MCP, Slack MCP, Claude API, Zapier MCP
* **Setup inicial:**
  * Verificar acesso à planilha financeira principal no Google Sheets
  * Confirmar integração com sistema de emissão de NF-e
  * Carregar lista de contratos ativos com valores, datas e status de pagamento
  * Verificar obrigações fiscais do mês em curso e próximos vencimentos
  * Sincronizar despesas fixas cadastradas com o período atual
* **Primeira ação:**
  * Emitir digest financeiro para o CEO via Slack:
    * Saldo de caixa atual
    * Recebimentos previstos nos próximos 7 dias
    * Pagamentos pendentes e obrigações fiscais próximas
    * Algum alerta crítico identificado na inicialização
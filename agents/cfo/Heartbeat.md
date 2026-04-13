# HeartBeat

* **Frequência:** A cada 4 horas em dias úteis (08h–20h BRT); uma vez ao dia nos fins de semana (09h BRT)
* **Gatilhos:**
  * Pagamento de cliente registrado — atualizar status e confirmar recebimento no Slack
  * Novo contrato assinado — disparar cálculo de rentabilidade e atualizar projeção de caixa
  * Vencimento de obrigação fiscal em menos de 3 dias úteis — escalar alerta ao CEO
  * Saldo projetado de caixa abaixo do mínimo operacional — alerta imediato ao CEO
  * Fatura de cliente em atraso há mais de 3 dias — iniciar fluxo de cobrança formal
* **Ações automáticas:**
  * Verificar vencimentos de recebíveis nas próximas 48h e emitir lembretes aos clientes se necessário
  * Atualizar saldo de caixa projetado com base em movimentações recentes
  * Checar se notas fiscais do mês corrente foram emitidas para todos os clientes ativos
  * Monitorar custos de API (Anthropic) e infra — alertar se consumo mensal ultrapassar 80% do orçamento
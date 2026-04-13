**# CronJobs**




\- Nome: Preparar Fila de Cobrança Diária

  Frequência:

    - Todos os dias 08:00 BRT

  Trigger:

    - Início do dia útil

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Análise de Aging

  Input:

    - Aging report atualizado

    - Contas vencidas nas últimas 24h

  Ação:

    - Carregar fila do dia

    - Priorizar por valor e risco

    - Identificar follow-ups pendentes

  Output:

    - Lista priorizada de cobranças do dia




\- Nome: Envio de Lembretes (1-30 dias)

  Frequência:

    - Todos os dias 09:00 BRT

  Trigger:

    - Conta atingiu 1 dia de atraso

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Comunicação de Cobrança

  Input:

    - Contas 1-30 dias vencidas

  Ação:

    - Enviar emails de lembrete com template aprovado

    - Agendar SMS para contas >R$ 5.000

  Output:

    - Lembretes enviados e registrados




\- Nome: Follow-up de Compromissos

  Frequência:

    - Todos os dias 10:00 BRT

  Trigger:

    - Compromisso de pagamento vence hoje

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Comunicação de Cobrança

  Input:

    - Lista de compromissos vencendo hoje

  Ação:

    - Verificar se pagamento foi recebido

    - Enviar confirmação ou cobrar cliente

  Output:

    - Status do compromisso atualizado




\- Nome: Cobrança Ativa (31-60 dias)

  Frequência:

    - Todos os dias 11:00 BRT

  Trigger:

    - Conta atingiu 31 dias de atraso

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Comunicação de Cobrança

    - Negociação de Pagamento

  Input:

    - Contas 31-60 dias vencidas

  Ação:

    - Ligar para clientes solicitando compromisso

    - Enviar email resumo da ligação

  Output:

    - Compromisso de pagamento obtido ou escalado




\- Nome: Aplicação de Pagamentos

  Frequência:

    - Todos os dias 14:00 BRT

  Trigger:

    - Pagamentos recebidos no período

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Análise de Aging

  Input:

    - Pagamentos processados

  Ação:

    - Aplicar pagamentos nas faturas

    - Enviar recibos

    - Remover contas resolvidas da fila

  Output:

    - Contas atualizadas, recibos enviados




\- Nome: Cobrança Intensiva (61-90 dias)

  Frequência:

    - Todos os dias 15:00 BRT

  Trigger:

    - Conta atingiu 61 dias de atraso

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Comunicação de Cobrança

    - Negociação de Pagamento

  Input:

    - Contas 61-90 dias vencidas

  Ação:

    - Enviar notificação formal

    - Ligar comunicando consequências

    - Oferecer última chance de acordo antes de escalar

  Output:

    - Contas escaladas para 90+ dias ou resolvidas




\- Nome: Report Diário ao CFO

  Frequência:

    - Todos os dias 17:30 BRT

  Trigger:

    - Fim do horário comercial

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Report de Métricas

  Input:

    - Todas as atividades do dia

  Ação:

    - Compilar comunicações enviadas

    - Pagamentos recebidos

    - Compromissos kept/broken

    - Contas escaladas

  Output:

    - Report diário enviado ao CFO




\- Nome: Análise Semanal de Aging

  Frequência:

    - Toda segunda 08:00 BRT

  Trigger:

    - Início da semana

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Análise de Aging

    - Report de Métricas

  Input:

    - Dados completos da semana anterior

  Ação:

    - Gerar aging report semanal

    - Calcular DSO e CEI

    - Identificar tendências

  Output:

    - Report semanal de desempenho




\- Nome: Fechamento Mensal

  Frequência:

    - Último dia útil do mês 17:00 BRT

  Trigger:

    - Fim do mês

  Agent:

    - Agente de Cobrança ao Cliente

  Skill:

    - Report de Métricas

  Input:

    - Dados completos do mês

  Ação:

    - Finalizar todas as cobranças

    - Calcular métricas mensais

    - Gerar snapshot de aging

  Output:

    - Report mensal enviado ao CFO
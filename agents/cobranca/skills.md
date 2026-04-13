**# Skills**




\- Nome: Comunicação de Cobrança

  Descrição: Criar comunações profissionais de cobrança adaptadas ao estágio da inadimplência

  Input:

    - Dados do cliente e fatura

    - Estágio de atraso (1-30, 31-60, 61-90, 90+ dias)

  Output:

    - Email, SMS ou script de ligação enviado

  Tools:

    - Plataforma de Comunicação

  Processo:

    1. Identificar estágio de atraso

    2. Selecionar template aprovado

    3. Personalizar com dados do cliente

    4. Enviar e registrar na plataforma

  Regras:

    - Nunca usar linguagem abusiva ou ameaçadora

    - Respeitar horários 09:00-17:00 BRT




\- Nome: Negociação de Pagamento

  Descrição: Estruturar planos de parcelamento viáveis

  Input:

    - Valor total devido

    - Capacidade de pagamento do cliente

  Output:

    - Proposta de plano de pagamento documentada

  Tools:

    - Gerenciador de Planos de Pagamento

  Processo:

    1. Avaliar situação financeira do cliente

    2. Calcular opções viáveis (máx 12 parcelas)

    3. Apresentar proposta

    4. Documentar acordo assinado

    5. Monitorar cumprimento

  Regras:

    - Máximo 12 parcelas sem aprovação do CFO

    - Desconto máximo 10% sem aprovação do CFO




\- Nome: Análise de Aging

  Descrição: Priorizar cobranças por valor e risco

  Input:

    - Aging report de contas a receber

  Output:

    - Lista priorizada de cobranças do dia

  Tools:

    - Sistema de Contas a Receber

  Processo:

    1. Carregar aging report atualizado

    2. Classificar por buckets (1-30, 31-60, 61-90, 90+ dias)

    3. Identificar contas de alto valor (>R$ 10.000)

    4. Priorizar por valor e risco

    5. Gerar fila de trabalho do dia

  Regras:

    - Contas >R$ 50.000 são prioridade crítica

    - Escalar imediatamente falência ou fraude suspeita




\- Nome: Resolução de Disputas

  Descrição: Identificar e encaminhar disputas de faturas

  Input:

    - Reclamação do cliente sobre fatura

  Output:

    - Disputa registrada e encaminhada

  Tools:

    - Sistema de Disputas

  Processo:

    1. Ouvir reclamação do cliente

    2. Categorizar tipo de disputa

    3. Suspender cobrança do valor disputado

    4. Encaminhar para equipe de resolução

    5. Acompanhar prazo de resolução

  Regras:

    - Não cobrar valor disputado até resolução

    - Continuar cobrança de valores não disputados




\- Nome: Report de Métricas

  Descrição: Gerar relatórios de desempenho de cobrança

  Input:

    - Dados de atividades do dia

  Output:

    - Report diário enviado ao CFO

  Tools:

    - Sistema de Contas a Receber

    - Plataforma de Comunicação

  Processo:

    1. Agregar comunicações enviadas

    2. Calcular pagamentos recebidos

    3. Comprometer kept vs broken

    4. Atualizar métricas DSO e CEI

    5. Gerar e enviar report ao CFO

  Regras:

    - Report diário até 17:30 BRT

    - Incluir todas as contas 90+ dias
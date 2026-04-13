**# CronJobs**




\- Nome: Verificar Novos Briefings

  Frequência:

    - A cada 2 horas (0 \*/2 \* \* \*)

  Trigger:

    - Briefing enviado pelo Head de Marketing

  Agent:

    - Agente Copywriter

  Skill:

    - Todos conforme tipo de briefing

  Input:

    - Briefing com objetivo, público, oferta, CTA, canal

  Ação:

    - Receber e analisar briefing

    - Selecionar skill adequada (ads, LP, email, vídeo, redes)

    - Produzir copy com variações

    - Enviar para aprovação

  Output:

    - Copy pronta com 3 variações + A/B test




\- Nome: Análise de Performance de Copies Ativas

  Frequência:

    - Diariamente às 10:00 (0 10 \* \* \*)

  Trigger:

    - Dados de KPIs disponíveis

  Agent:

    - Agente Copywriter

  Skill:

    - Otimização Baseada em Dados

  Input:

    - CTR, conversão, engajamento de copies ativas

  Ação:

    - Analisar performance por peça

    - Identificar copies abaixo da média

    - Propor otimizações com hipótese de teste

  Output:

    - Report diário: copies performando bem vs mal + recomendações




\- Nome: Processar Resultados de A/B Tests

  Frequência:

    - Diariamente às 14:00 (0 14 \* \* \*)

  Trigger:

    - A/B test concluído com dados suficientes

  Agent:

    - Agente Copywriter

  Skill:

    - Otimização Baseada em Dados

    - A/B Test Generator

  Input:

    - Resultados de testes A/B em andamento

  Ação:

    - Calcular significância estatística

    - Identificar versão vencedora

    - Documentar learning

    - Sugerir próximo teste

  Output:

    - Resultado do teste + versão vencedora + próximos passos




\- Nome: Produção de Copy para Campanhas Ativas

  Frequência:

    - Diariamente às 09:00 (0 9 \* \* \*)

  Trigger:

    - Campanhas ativas precisando de novas copies

  Agent:

    - Agente Copywriter

  Skill:

    - Copy para Anúncios

    - Copy para Landing Pages

    - Copy para Emails

    - Copy para Vídeos

    - Copy para Redes Sociais

  Input:

    - Briefings aprovados e pendentes de produção

  Ação:

    - Produzir copies por canal

    - Gerar variações A/B

    - Validar contra branding

  Output:

    - Copies prontas para aprovação




\- Nome: Sequências de Nurture Automatizadas

  Frequência:

    - Toda segunda às 11:00 (0 11 \* \* 1)

  Trigger:

    - Leads em estágio de nurture

  Agent:

    - Agente Copywriter

  Skill:

    - Sequências de Nurture

  Input:

    - Estágio dos leads, persona, dores

  Ação:

    - Revisar sequências ativas

    - Otimizar com base em performance

    - Propor novas sequências se necessário

  Output:

    - Sequências otimizadas ou novas propostas




\- Nome: Report Semanal de Copy Performance

  Frequência:

    - Toda sexta às 16:00 (0 16 \* \* 5)

  Trigger:

    - Fim da semana

  Agent:

    - Agente Copywriter

  Skill:

    - Otimização Baseada em Dados

  Input:

    - Todas as métricas de copy da semana

  Ação:

    - Compilar métricas:

      - Copies produzidas: X

      - A/B tests concluídos: X

      - CTR médio: X%

      - Conversão média: X%

      - Top performers: lista

      - Underperformers: lista

      - Learnings da semana: X

    - Gerar report semanal

  Output:

    - Report enviado ao Head de Marketing




\- Nome: Atualização de Frameworks e Templates

  Frequência:

    - Mensal, dia 1 às 09:00 (0 9 1 \* \*)

  Trigger:

    - Novo mês

  Agent:

    - Agente Copywriter

  Skill:

    - Todos

  Input:

    - Learnings acumulados, novas tendências, dados de performance

  Ação:

    - Atualizar copy framework library com learnings

    - Refinar templates de email

    - Atualizar Ad Platform Specs se mudou

    - Documentar melhores práticas do mês

  Output:

    - Biblioteca de copy atualizada
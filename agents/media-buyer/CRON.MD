**# CronJobs**



\- Nome: Monitoramento de Performance Diária

  Frequência:

    - Diariamente às 09:00 (0 9 * * *)

  Trigger:

    - Dados de performance do dia anterior disponíveis

  Agent:

    - Agente Media Buyer

  Skill:

    - Otimização de Performance

  Input:

    - Métricas de todas as campanhas ativas (impressões, cliques, CTR, conversões, CPA, ROAS)

  Ação:

    - Coletar dados de Meta, Google, TikTok, LinkedIn

    - Comparar com metas estabelecidas

    - Identificar winners e losers

    - Executar otimizações automáticas (pausar losers, aumentar budget winners)

    - Gerar report diário

  Output:

    - Report diário de performance

    - Ações de otimização executadas


\- Nome: Gestão de Budget e Bidding

  Frequência:

    - A cada 4 horas (0 */4 * * *)

  Trigger:

    - Budget diário em risco de esgotar

    - Oportunidade de escala identificada

  Agent:

    - Agente Media Buyer

  Skill:

    - Otimização de Performance

    - Gestão de Google Ads

    - Estruturação de Campanhas Meta Ads

  Input:

    - Budget restante do dia

    - Performance em tempo real

    - Projeção de gastos

  Ação:

    - Ajustar bids de campanhas underperformers

    - Realocar budget entre ad sets

    - Aumentar budget de campanhas vencedoras (+20-30%)

    - Pausar campanhas com CPA > 2x meta

  Output:

    - Budget realocado otimamente

    - Bids ajustados


\- Nome: Análise de Públicos e Fadiga

  Frequência:

    - Toda segunda e quinta às 11:00 (0 11 * * 1,4)

  Trigger:

    - Necessidade de refresh de audiences

  Agent:

    - Agente Media Buyer

  Skill:

    - Gestão de Públicos e Segmentação

  Input:

    - Frequency média por audiência

    - CTR trend por criativo

    - Tamanho de audiences atuais

  Ação:

    - Identificar audiences com frequency > 5

    - Criar novas variações de lookalike

    - Expandir ou refinar segmentação

    - Sugerir novos criativos para públicos saturados

  Output:

    - Novas audiences criadas

    - Recommendations de refresh de criativos


\- Nome: Processamento de A/B Tests

  Frequência:

    - Diariamente às 15:00 (0 15 * * *)

  Trigger:

    - Testes A/B com volume estatístico suficiente

  Agent:

    - Agente Media Buyer

  Skill:

    - A/B Testing de Criativos e Públicos

  Input:

    - Resultados de testes em andamento

    - Métricas por variação

  Ação:

    - Calcular significância estatística

    - Declarar vencedor quando aplicável

    - Implementar versão vencedora

    - Documentar learning

    - Propor próximo teste

  Output:

    - Resultado de testes concluídos

    - Learning registrado

    - Próximo teste planejado


\- Nome: Validação de Tracking e Pixels

  Frequência:

    - Semanal, toda segunda às 08:00 (0 8 * * 1)

  Trigger:

    - Início da semana

  Agent:

    - Agente Media Buyer

  Skill:

    - Implementação de Tracking e Pixels

  Input:

    - Status de pixels nas plataformas

    - Eventos de conversão registrados

  Ação:

    - Testar disparo de todos os pixels

    - Validar match rate de Conversions API

    - Verificar eventos sem correspondência

    - Corrigir problemas de tracking

  Output:

    - Report de saúde do tracking

    - Issues corrigidas


\- Nome: Report Semanal de Mídia

  Frequência:

    - Toda sexta às 17:00 (0 17 * * 5)

  Trigger:

    - Fim da semana

  Agent:

    - Agente Media Buyer

  Skill:

    - Otimização de Performance

  Input:

    - Todas as métricas da semana por plataforma

    - Budget gasto vs planejado

    - Conversões e ROAS por campanha

  Ação:

    - Compilar métricas consolidadas:

      - Impressões totais: X

      - Cliques totais: X

      - CTR médio: X%

      - Conversões: X

      - CPA médio: R$ X

      - ROAS médio: X

      - Budget total gasto: R$ X

    - Destacar top performers

    - Listar underperformers e ações tomadas

    - Learnings da semana

    - Plano para próxima semana

  Output:

    - Report semanal enviado ao Head de Marketing


\- Nome: Planejamento de Campanhas Novas

  Frequência:

    - Toda segunda às 10:00 (0 10 * * 1)

  Trigger:

    - Briefings pendentes de Head de Marketing

  Agent:

    - Agente Media Buyer

  Skill:

    - Estruturação de Campanhas Meta Ads

    - Gestão de Google Ads

    - TikTok Ads Management

    - LinkedIn Ads B2B

  Input:

    - Briefings aprovados

    - Copies e criativos disponíveis

    - Budget alocado

  Ação:

    - Estruturar novas campanhas por plataforma

    - Configurar públicos e segmentação

    - Upload de criativos e copies

    - Definir orçamento e bidding

    - Agendar lançamento

  Output:

    - Campanhas novas prontas para aprovação


\- Nome: Limpeza e Organização de Contas

  Frequência:

    - Mensal, dia 1 às 09:00 (0 9 1 * *)

  Trigger:

    - Novo mês

  Agent:

    - Agente Media Buyer

  Skill:

    - Todos

  Input:

    - Todas as campanhas, conjuntos e anúncios ativos/inativos

  Ação:

    - Arquivar campanhas encerradas há mais de 90 dias

    - Remover anúncios reprovados permanentemente

    - Organizar naming conventions

    - Atualizar bibliotecas de criativos

    - Revisar e atualizar audiences salvas

    - Documentar estrutura atual

  Output:

    - Contas organizadas e limpas

    - Documentação atualizada

**# Skills**




\- Nome: Coleta de KPIs de Marketing

  Descrição: Coletar métricas de todas as plataformas de marketing

  Input:

    - Período de coleta

    - Plataformas alvo (Google Analytics, Meta Ads, TikTok, Google Ads)

  Output:

    - Dataset validado com tráfego, campanhas, engajamento, conversões, custos

  Tools:

    - Coletor de Dados de Marketing

  Processo:

    1. Conectar a cada plataforma

    2. Extrair métricas do período

    3. Normalizar formatos e unidades

    4. Validar completude

    5. Reconciliar entre plataformas

  Regras:

    - Sem gaps no período

    - Reconciliar spend com dados financeiros

    - Flaggar anomalias >20% vs histórico




\- Nome: Coleta de KPIs Financeiros

  Descrição: Coletar e calcular métricas financeiras e de receita

  Input:

    - Dados de receita por fonte

    - Dados de custo por canal

    - Dados de novos clientes

  Output:

    - Dataset com receita, CAC, LTV, LTV/CAC, ROI, margens, budget vs actual

  Tools:

    - Conector Financeiro

  Processo:

    1. Coletar receita por fonte

    2. Coletar custos por canal

    3. Calcular CAC \= spend / novos clientes

    4. Calcular LTV \= receita / churn

    5. Calcular LTV/CAC e ROI

  Regras:

    - Usar mesmo período para CAC e LTV

    - Incluir todos os custos (ads, tools, pessoas)

    - Alertar se LTV/CAC \< 1




\- Nome: Coleta de KPIs de Vendas

  Descrição: Coletar métricas de funil e pipeline do CRM

  Input:

    - Pipeline do CRM por etapa

    - Histórico de deals won/lost

  Output:

    - Dataset com leads, MQLs, SQLs, oportunidades, conversion rates, win rate, sales cycle, deal size médio

  Tools:

    - Conector Financeiro

  Processo:

    1. Extrair volumes por etapa do funil

    2. Calcular conversion rate por etapa

    3. Calcular sales cycle médio (dias corridos)

    4. Calcular win rate \= won / total opportunities

    5. Calcular deal size médio

  Regras:

    - Funil deve fechar sem perder leads

    - Forecast com intervalo de confiança

    - Conversion rates realistas (0-100%)




\- Nome: Coleta de KPIs Operacionais

  Descrição: Coletar métricas de churn, satisfação e eficiência

  Input:

    - Dados de cancelamentos e retenção

    - Pesquisas NPS e CSAT

    - Métricas de utilização

  Output:

    - Dataset com churn rate, retention rate, NPS, CSAT, utilização, SLAs

  Tools:

    - Conector Operacional

  Processo:

    1. Calcular churn \= cancelamentos / total

    2. Extrair NPS \= promoters - detractors

    3. Extrair CSAT (documentar escala usada)

    4. Coletar métricas de utilização

    5. Calcular SLA \= % dentro do target

  Regras:

    - NPS range -100 a +100

    - Documentar escala do CSAT

    - SLA é percentual, não média




\- Nome: Validação de Dados

  Descrição: Validar qualidade e consistência de todos os datasets

  Input:

    - Datasets coletados de todas as fontes

    - Regras de validação e ranges esperados

  Output:

    - Report de qualidade + dataset aprovado/reprovado

  Tools:

    - Validador de Qualidade

  Processo:

    1. Verificar missing values (limite 5%)

    2. Detectar anomalias (>3 std dev)

    3. Validar ranges (ex: 0-100% para rates)

    4. Reconciliar entre fontes

    5. Comparar com histórico (flag >20%)

    6. Aprovar ou reprovar dataset

  Regras:

    - Missing >5% \= reprovado

    - Anomalias investigadas, não ignoradas

    - Reconciliação obrigatória entre fontes




\- Nome: Consolidação de KPIs

  Descrição: Consolidar todos os datasets validados em dataset unificado

  Input:

    - Datasets validados de marketing, vendas, financeiro, operacional

  Output:

    - Dataset unificado enviado ao Agente de Dados e BI

  Tools:

    - Motor de Consolidação

    - Dicionário de Métricas

  Processo:

    1. Receber todos os datasets validados

    2. Normalizar formatos, unidades, timestamps

    3. Estruturar por área e métrica

    4. Adicionar metadata (fonte, cálculo, timestamp)

    5. Atualizar dicionário se necessário

    6. Exportar em JSON, CSV

    7. Enviar ao Agente de Dados e BI

  Regras:

    - Todo KPI com fonte e fórmula documentada

    - Timezone consistente

    - Manter histórico completo (nunca deletar)
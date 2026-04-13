**# CronJobs**




\- **\*\*Nome:\*\*** Coleta de KPIs de Marketing

  **\*\*Frequência:\*\***

    - 0 \*/4 \* \* \* (a cada 4 horas)

  **\*\*Trigger:\*\***

    - Dados de marketing atualizados nas plataformas

  **\*\*Agent:\*\***

    - Coletor de Dados de Marketing

  **\*\*Skill:\*\***

    - Coleta de KPIs de Marketing

  **\*\*Input:\*\***

    - Google Analytics, Meta Ads, TikTok Ads, Google Ads, Social Media

  **\*\*Ação:\*\***

    - Coletar métricas de tráfego, campanhas, engajamento e conversões

    - Normalizar e reconciliar dados entre plataformas

    - Validar completude e ranges

  **\*\*Output:\*\***

    - Dataset de KPIs de marketing validado




\- **\*\*Nome:\*\*** Coleta de KPIs Financeiros

  **\*\*Frequência:\*\***

    - 0 7 \* \* \* (diariamente às 7h)

  **\*\*Trigger:\*\***

    - Dados financeiros do dia anterior disponíveis

  **\*\*Agent:\*\***

    - Coletor de Dados Financeiros

  **\*\*Skill:\*\***

    - Coleta de KPIs Financeiros e de Receita

  **\*\*Input:\*\***

    - Dados de receita, custos, vendas do dia anterior

  **\*\*Ação:\*\***

    - Coletar receita por fonte

    - Coletar custos por canal

    - Calcular CAC, LTV, LTV/CAC, ROI

    - Comparar budget vs actual

  **\*\*Output:\*\***

    - Dataset de KPIs financeiros validado




\- **\*\*Nome:\*\*** Coleta de KPIs de Vendas

  **\*\*Frequência:\*\***

    - 0 8 \* \* \* (diariamente às 8h)

  **\*\*Trigger:\*\***

    - Dados de CRM atualizados

  **\*\*Agent:\*\***

    - Coletor de Dados de Vendas

  **\*\*Skill:\*\***

    - Coleta de KPIs de Vendas

  **\*\*Input:\*\***

    - CRM e dados de pipeline do dia anterior

  **\*\*Ação:\*\***

    - Extrair métricas de funil e pipeline

    - Calcular conversion rates por etapa

    - Calcular win rate e sales cycle

    - Gerar forecast atualizado

  **\*\*Output:\*\***

    - Dataset de KPIs de vendas validado




\- **\*\*Nome:\*\*** Coleta de KPIs Operacionais

  **\*\*Frequência:\*\***

    - 0 9 \* \* 2 (toda terça-feira às 9h)

  **\*\*Trigger:\*\***

    - Dados operacionais da semana anterior

  **\*\*Agent:\*\***

    - Coletor de Dados Operacionais

  **\*\*Skill:\*\***

    - Coleta de KPIs Operacionais

  **\*\*Input:\*\***

    - Dados de churn, NPS, CSAT, utilização

  **\*\*Ação:\*\***

    - Coletar churn e retention rates

    - Extrair NPS e CSAT scores

    - Coletar métricas de utilização

    - Monitorar SLAs

  **\*\*Output:\*\***

    - Dataset de KPIs operacionais validado




\- **\*\*Nome:\*\*** Validação Geral de Dados

  **\*\*Frequência:\*\***

    - 0 10 \* \* \* (diariamente às 10h)

  **\*\*Trigger:\*\***

    - Todos os datasets coletados do dia

  **\*\*Agent:\*\***

    - Validador de Dados

  **\*\*Skill:\*\***

    - Validação e Qualidade de Dados

  **\*\*Input:\*\***

    - Todos os datasets coletados (marketing, financeiro, vendas, operacional)

  **\*\*Ação:\*\***

    - Verificar missing values em todos os datasets

    - Detectar anomalias e outliers

    - Reconciliar números entre fontes

    - Comparar com histórico

    - Gerar report de qualidade

  **\*\*Output:\*\***

    - Report de qualidade + datasets aprovados/reprovados




\- **\*\*Nome:\*\*** Consolidação de KPIs Corporativos

  **\*\*Frequência:\*\***

    - 0 11 \* \* \* (diariamente às 11h)

  **\*\*Trigger:\*\***

    - Todos os datasets validados e aprovados

  **\*\*Agent:\*\***

    - Agente de KPIs - Agente Principal

  **\*\*Skill:\*\***

    - Consolidação de KPIs Corporativos

  **\*\*Input:\*\***

    - Todos os datasets validados do dia

  **\*\*Ação:\*\***

    - Consolidar todos os KPIs em dataset unificado

    - Normalizar formatos e unidades

    - Adicionar metadata completo

    - Atualizar dicionário de métricas

    - Exportar em JSON, CSV, Excel

    - Enviar ao Agente de Dados e Agente de BI

  **\*\*Output:\*\***

    - Dataset consolidado enviado aos consumidores




\- **\*\*Nome:\*\*** Auditoria de Fontes de Dados

  **\*\*Frequência:\*\***

    - 0 14 \* \* 6 (todo sábado às 14h)

  **\*\*Trigger:\*\***

    - Nenhum (execução automática)

  **\*\*Agent:\*\***

    - Validador de Dados

  **\*\*Skill:\*\***

    - Validação e Qualidade de Dados

  **\*\*Input:\*\***

    - Todas as fontes de dados conectadas

    - Logs de coletas da semana

  **\*\*Ação:\*\***

    - Verificar health de todas as conexões de dados

    - Analisar logs de coletas (sucessos, falhas, delays)

    - Identificar fontes com problemas recorrentes

    - Propor correções e melhorias

    - Atualizar documentação de fontes

  **\*\*Output:\*\***

    - Relatório de health de fontes de dados




\- **\*\*Nome:\*\*** Atualização do Dicionário de Métricas

  **\*\*Frequência:\*\***

    - 0 9 1 \* \* (primeiro dia de cada mês às 9h)

  **\*\*Trigger:\*\***

    - Nenhum (execução automática)

  **\*\*Agent:\*\***

    - Agente de KPIs - Agente Principal

  **\*\*Skill:\*\***

    - Consolidação de KPIs Corporativos

  **\*\*Input:\*\***

    - Métricas atuais no dicionário

    - Novas métricas adicionadas no mês

    - Mudanças de definição ou cálculo

  **\*\*Ação:\*\***

    - Revisar todas as definições de métricas

    - Adicionar novas métricas

    - Atualizar fórmulas se necessário

    - Documentar mudanças

    - Publicar nova versão do dicionário

  **\*\*Output:\*\***

    - Dicionário de Métricas atualizado e versionado
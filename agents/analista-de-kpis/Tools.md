**# Tools**




\- Nome: Coletor de Dados de Marketing

  Tipo: Integração

  Função: Coletar métricas de Google Analytics, Meta Ads, TikTok Ads, Google Ads, Social Media

  Permissões:

  - Leitura de métricas de tráfego, campanhas, engajamento e conversões

  - Normalização entre plataformas




\- Nome: Conector Financeiro

  Tipo: Integração

  Função: Coletar receita, custos, dados de CRM e calcular CAC, LTV, ROI

  Permissões:

  - Leitura de dados financeiros e de vendas

  - Cálculo de métricas derivadas (CAC, LTV, LTV/CAC, ROI)




\- Nome: Conector Operacional

  Tipo: Integração

  Função: Coletar churn, NPS, CSAT, utilização e SLAs

  Permissões:

  - Leitura de dados de churn e retenção

  - Acesso a pesquisas de satisfação




\- Nome: Validador de Qualidade

  Tipo: Script

  Função: Validar completude, detectar anomalias e reconciliar dados

  Permissões:

  - Verificar missing values (limite 5%)

  - Detectar outliers (>3 std dev)

  - Reconciliar entre fontes

  - Gerar report de qualidade




\- Nome: Motor de Consolidação

  Tipo: Script

  Função: Consolidar todos os KPIs em dataset unificado

  Permissões:

  - Agregação por área e período

  - Normalização de formatos e unidades

  - Export em JSON, CSV

  - Envio ao Agente de Dados e BI




\- Nome: Dicionário de Métricas

  Tipo: Script

  Função: Manter definições, fórmulas e fontes de cada KPI

  Permissões:

  - Leitura e atualização de definições

  - Documentação de fórmulas

  - Versionamento de mudanças
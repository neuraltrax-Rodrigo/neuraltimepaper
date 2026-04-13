# Tools

## Google Sheets (via Zapier MCP)

* **Tipo:** Integração / MCP Server
* **Função:** Base central de dados — dashboard consolidado de KPIs, histórico de métricas por frente e relatórios periódicos
* **Permissões:**
  * Ler e escrever em todas as abas do dashboard de KPIs
  * Criar novas abas de relatório por período
  * Formatar células e aplicar regras de formatação condicional (verde/amarelo/vermelho por threshold)
  * Buscar dados históricos para comparação de períodos

## Slack MCP

* **Tipo:** Integração / MCP Server
* **Função:** Canal de entrega de relatórios e emissão de alertas para o CEO e Heads de área
* **Permissões:**
  * Enviar mensagens em canais dedicados de cada frente e no canal executivo do CEO
  * Enviar mensagens diretas (DM) ao CEO e Heads em alertas críticos
  * Publicar relatórios periódicos formatados com emojis de status (🔴/🟡/🟢)
  * Ler mensagens para capturar solicitações de análise ad hoc

## Gmail MCP

* **Tipo:** Integração / MCP Server
* **Função:** Envio de relatórios formais consolidados por email — semanal e mensal
* **Permissões:**
  * Enviar relatórios formatados ao CEO e Heads
  * Anexar planilhas e dashboards exportados
  * Ler emails com dados ou solicitações de análise encaminhados ao Head de Dados

## Claude API (Anthropic)

* **Tipo:** API
* **Função:** Interpretação de dados, geração de narrativa analítica e redação de relatórios em linguagem executiva
* **Permissões:**
  * Processar conjuntos de dados e gerar insights em linguagem natural
  * Redigir seções narrativas de relatórios (contexto, diagnóstico, recomendações)
  * Identificar padrões e anomalias em séries históricas de KPIs
  * Gerar recomendações de ação com base nos dados analisados

## Zapier MCP

* **Tipo:** Integração / MCP Server
* **Função:** Automação de coleta de dados de fontes externas e gatilhos entre plataformas
* **Permissões:**
  * Disparar coleta automática de dados via webhooks de plataformas conectadas
  * Sincronizar dados entre ferramentas (ex: Meta Ads → Google Sheets, CRM → Sheets)
  * Acionar alertas cross-platform com base em eventos de dados

## Google Analytics / Meta Ads / Plataformas de Tráfego

* **Tipo:** API / Integração
* **Função:** Fonte de dados de performance de tráfego, campanhas e comportamento digital
* **Permissões:**
  * Ler métricas de campanhas (impressões, cliques, CPL, ROAS, conversões)
  * Exportar relatórios de período para consolidação no dashboard
  * Monitorar anomalias de performance em tempo real
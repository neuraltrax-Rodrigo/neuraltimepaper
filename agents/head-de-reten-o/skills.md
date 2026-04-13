# Skills

## Monitoramento de Saúde da Carteira

* **Descrição:** Mantém o health score de cada cliente atualizado e identifica contas em risco antes que churn aconteça.
* **Input:** Dados de uso, NPS, tickets de suporte, frequência de contato e pagamentos em dia por cliente
* **Output:** Carteira segmentada por health score (🟢 Saudável / 🟡 Atenção / 🔴 Risco) + alertas para clientes que mudaram de faixa
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Consolidar dados de cada cliente: uso, NPS, tickets, inadimplência, última interação
  2. Calcular health score com base nos critérios definidos
  3. Segmentar carteira nas 3 faixas
  4. Identificar clientes que pioraram de faixa desde a última semana
  5. Alertar Customer Experience e Churn Recovery sobre contas em 🔴
* **Regras:**
  * Monitoramento semanal obrigatório — cliente não pode chegar a churn sem ter passado por 🟡 primeiro
  * Cliente em 🔴 recebe intervenção em até 24h

## Gestão de Churn e Recuperação

* **Descrição:** Coordena intervenções preventivas e reativas de churn — de clientes em risco até cancelamentos em andamento.
* **Input:** Alertas de health score 🔴, solicitações de cancelamento, feedback de insatisfação grave
* **Output:** Plano de recuperação por cliente com: causa identificada, abordagem definida, responsável e prazo
* **Tools:** Claude API, Asana MCP, Slack MCP, Gmail MCP
* **Processo:**
  1. Receber alerta de risco ou cancelamento
  2. Diagnosticar causa raiz: produto, expectativa, resultado, preço ou concorrência
  3. Definir abordagem de recuperação adequada à causa
  4. Acionar Churn Recovery para execução
  5. Acompanhar evolução e registrar resultado (recuperado / perdido + motivo)
* **Regras:**
  * Nenhuma solicitação de cancelamento sem intervenção documentada
  * Causa de churn definitivo sempre registrada — é dado de produto e processo

## Identificação e Ativação de Upsell

* **Descrição:** Identifica clientes prontos para expansão e aciona o Upsell Agent no momento certo.
* **Input:** Health score 🟢, tempo de contrato, NPS positivo, sinais de uso intenso ou demanda crescente
* **Output:** Lista de oportunidades de upsell com: cliente, motivo da oportunidade, proposta sugerida e timing recomendado
* **Tools:** Google Sheets, Claude API, Slack MCP
* **Processo:**
  1. Filtrar clientes com health score 🟢 há pelo menos 60 dias
  2. Identificar sinais de expansão: uso acima da contratação, pedidos fora de escopo, NPS alto
  3. Definir proposta de upsell alinhada ao resultado atual do cliente
  4. Acionar Upsell Agent com briefing da oportunidade
  5. Acompanhar resultado e registrar MRR expandido
* **Regras:**
  * Nunca abordar upsell com cliente em health score 🟡 ou 🔴
  * Proposta de upsell sempre baseada em resultado que o cliente já está tendo

## Relatório Semanal de Retenção para o CEO

* **Descrição:** Consolida a saúde da base de clientes e entrega visão clara ao CEO toda semana.
* **Input:** Health score da carteira, NPS do período, churn da semana, recuperações, upsells fechados
* **Output:** Mensagem no Slack ao CEO com: churn rate, NPS, clientes em risco, recuperações e MRR expandido
* **Tools:** Google Sheets, Slack MCP, Claude API
* **Processo:**
  1. Consolidar dados do squad da semana
  2. Calcular: churn rate, NPS médio, clientes em 🔴, recuperações bem-sucedidas, MRR expandido via upsell
  3. Identificar principal risco ativo e ação em andamento
  4. Redigir relatório conciso e enviar ao CEO toda sexta-feira às 16h30
* **Regras:**
  * Sempre inclui o principal risco ativo e o que está sendo feito
  * Se churn rate acima do threshold: enviar alerta separado imediatamente, não esperar o relatório semanal
# CronJobs

## Monitoramento Semanal de Saúde da Carteira

* **Frequência:** Toda segunda-feira às 08h00 BRT (`0 8 * * 1`)
* **Agent:** Head de Retenção + Customer Experience
* **Skill:** Monitoramento de Saúde da Carteira
* **Input:** Dados de uso, NPS, tickets e pagamentos da semana anterior por cliente
* **Ação:** Atualizar health scores, segmentar carteira e acionar squad para contas em risco
* **Output:** Carteira atualizada no Google Sheets + alertas no Slack para clientes em 🔴

## Disparo de NPS

* **Frequência:** Todo dia 10 e dia 25 do mês às 09h00 BRT (`0 9 10,25 * *`)
* **Agent:** Analista de NPS
* **Skill:** Monitoramento de Saúde da Carteira (escopo NPS)
* **Input:** Lista de clientes ativos com data da última pesquisa
* **Ação:** Disparar pesquisa NPS para clientes que não foram pesquisados nos últimos 30 dias
* **Output:** Pesquisas enviadas via Gmail + registro no Google Sheets

## Identificação de Oportunidades de Upsell

* **Frequência:** Toda quarta-feira às 10h00 BRT (`0 10 * * 3`)
* **Agent:** Head de Retenção + Upsell Agent
* **Skill:** Identificação e Ativação de Upsell
* **Input:** Health scores 🟢 com mais de 60 dias, sinais de uso e NPS positivo
* **Ação:** Filtrar oportunidades de upsell e briefar o Upsell Agent para abordagem
* **Output:** Lista de oportunidades no Asana + orientação de abordagem para o Upsell Agent

## Relatório Semanal de Retenção para o CEO

* **Frequência:** Toda sexta-feira às 16h30 BRT (`0 16 * * 5`)
* **Agent:** Head de Retenção
* **Skill:** Relatório Semanal de Retenção para o CEO
* **Input:** Dados do squad da semana — churn, NPS, health scores, recuperações, upsells
* **Ação:** Consolidar e enviar relatório ao CEO
* **Output:** Mensagem no Slack ao CEO com churn rate, NPS, clientes em risco, recuperações e MRR expandido

## Relatório Mensal de NPS

* **Frequência:** Todo dia 1 do mês às 09h00 BRT (`0 9 1 * *`)
* **Agent:** Analista de NPS + Head de Retenção
* **Skill:** Monitoramento de Saúde da Carteira (escopo NPS mensal)
* **Input:** Todas as respostas de NPS do mês anterior
* **Ação:** Consolidar NPS, categorizar por tema, identificar tendência e repassar insights ao PM
* **Output:** Relatório de NPS mensal enviado ao CEO e ao Product Manager via Slack
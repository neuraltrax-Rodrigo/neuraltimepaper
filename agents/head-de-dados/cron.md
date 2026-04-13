# CronJobs

## Coleta Diária de KPIs

* **Frequência:** Todo dia às 06h30 BRT (`30 6 * * *`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Dados + Analista de KPIs
* **Skill:** Coleta e Consolidação de Dados
* **Input:** Dados de todas as frentes do dia anterior
* **Ação:** Coletar, normalizar e consolidar KPIs no dashboard central; aplicar formatação condicional por status
* **Output:** Dashboard atualizado no Google Sheets com status 🟢/🟡/🔴 por KPI

## Relatório Diário de Status para o CEO

* **Frequência:** Todo dia útil às 07h15 BRT (`15 7 * * 1-5`)
* **Trigger:** Agendamento automático (após coleta diária)
* **Agent:** Head de Dados
* **Skill:** Relatório Diário de Status
* **Input:** Dashboard atualizado do dia + alertas das últimas 24h
* **Ação:** Gerar e enviar digest de status ao CEO via Slack
* **Output:** Mensagem no Slack para o CEO com status por frente, destaques e pontos de atenção

## Varredura de Alertas Críticos

* **Frequência:** A cada 1 hora (`0 * * * *`)
* **Trigger:** Agendamento automático + gatilhos de dados em tempo real
* **Agent:** Head de Dados + Sentinela de Dados
* **Skill:** Monitoramento e Emissão de Alertas Críticos
* **Input:** KPIs atuais vs. tabela de thresholds
* **Ação:** Varrer todos os KPIs críticos, classificar e emitir alerta imediato se 🔴 detectado
* **Output:** Alerta via Slack DM ao CEO + mensagem no canal da área impactada (se 🔴) ou registro silencioso no log (se 🟢/🟡)

## Relatório Semanal por Área

* **Frequência:** Toda segunda-feira às 08h00 BRT (`0 8 * * 1`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Dados + Analista de KPIs
* **Skill:** Relatório Semanal por Área
* **Input:** KPIs da semana anterior por frente + histórico das últimas 4 semanas
* **Ação:** Gerar relatório individual por área com performance, tendência e recomendações; enviar a cada Head
* **Output:** Mensagem no Slack para cada Head (CFO, CTO, Head de Growth, Head de Retenção, Head de Tráfego, Head de Engagement) com relatório da sua frente

## Atualização de Dashboard Semanal Consolidado

* **Frequência:** Toda sexta-feira às 18h00 BRT (`0 18 * * 5`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Dados + Analista de KPIs
* **Skill:** Coleta e Consolidação de Dados (escopo semanal)
* **Input:** Todos os dados da semana encerrada
* **Ação:** Fechar a semana no dashboard, calcular totais acumulados e arquivar snapshot semanal em aba histórica
* **Output:** Aba da semana arquivada no Google Sheets + confirmação via Slack ao CEO

## Relatório Executivo Mensal

* **Frequência:** Primeiro dia útil de cada mês às 07h00 BRT
* **Trigger:** Agendamento automático
* **Agent:** Head de Dados + Analista de KPIs
* **Skill:** Relatório Executivo Mensal
* **Input:** KPIs consolidados do mês + OKRs do período + alertas críticos emitidos no mês
* **Ação:** Gerar relatório completo de performance do mês com visão estratégica e recomendações
* **Output:** Resumo executivo no Slack ao CEO + relatório completo via Gmail com dashboard exportado em anexo

## Lembrete de Alertas Não Resolvidos

* **Frequência:** Todo dia útil às 12h00 e às 18h00 BRT (`0 12,18 * * 1-5`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Dados + Sentinela de Dados
* **Skill:** Monitoramento e Emissão de Alertas Críticos
* **Input:** Log de alertas 🔴 emitidos nas últimas 24h sem status de resolução registrado
* **Ação:** Reenviar lembrete ao Head responsável via Slack com o alerta aberto + acionar CEO se passaram mais de 8h sem resolução
* **Output:** Mensagem de follow-up no Slack com alerta pendente e tempo decorrido desde a emissão
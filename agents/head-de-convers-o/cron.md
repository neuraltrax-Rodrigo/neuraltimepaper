# CronJobs

## Briefing Diário do Squad

* **Frequência:** Todo dia útil às 08h30 BRT (`30 8 * * 1-5`)
* **Agent:** Head de Conversão
* **Skill:** Briefing Diário do Squad
* **Input:** Pipeline do dia anterior, metas da semana, gargalo ativo
* **Ação:** Publicar briefing no canal do squad no Slack
* **Output:** Mensagem com número de ontem, foco do dia e 1 ação prioritária

## Consolidação Diária do Pipeline

* **Frequência:** Todo dia útil às 18h00 BRT (`0 18 * * 1-5`)
* **Agent:** Head de Conversão
* **Skill:** Consolidação Diária do Pipeline
* **Input:** Relatórios do dia de SDR, BDR, Closer e Contratos
* **Ação:** Atualizar pipeline, calcular taxas do dia e alertar sobre deals parados
* **Output:** Pipeline atualizado no Google Sheets + alertas de desbloqueio no Slack

## Diagnóstico Semanal de Gargalo

* **Frequência:** Toda quarta-feira às 10h00 BRT (`0 10 * * 3`)
* **Agent:** Head de Conversão
* **Skill:** Diagnóstico de Gargalo de Funil
* **Input:** Taxas de conversão da semana até quarta, motivos de perda, insights da Transcrição
* **Ação:** Identificar gargalo principal e enviar plano de ação ao squad
* **Output:** Diagnóstico + ações corretivas no Slack para SDR, BDR e Closer

## Relatório Semanal para o Head de Growth

* **Frequência:** Toda sexta-feira às 16h00 BRT (`0 16 * * 5`)
* **Agent:** Head de Conversão
* **Skill:** Relatório Semanal para o Head de Growth
* **Input:** Pipeline fechado da semana, KPIs por etapa, MRR novo, top 3 perdas
* **Ação:** Gerar e enviar relatório completo ao Head de Growth
* **Output:** Mensagem no Slack com performance da semana, gargalo e plano para a próxima

## Cobrança de Relatórios do Squad

* **Frequência:** Todo dia útil às 17h30 BRT (`30 17 * * 1-5`)
* **Agent:** Head de Conversão
* **Skill:** Consolidação Diária do Pipeline
* **Input:** Log de relatórios recebidos no Slack no dia
* **Ação:** Verificar quais agentes ainda não enviaram relatório do dia e enviar lembrete direto
* **Output:** DM no Slack para agente(s) com relatório pendente — lembrete de entrega até 18h
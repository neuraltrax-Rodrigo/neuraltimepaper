# CronJobs

## Leitura do Relatório Diário do Head de Dados

* **Frequência:** Todo dia útil às 07h20 BRT (`20 7 * * 1-5`)
* **Trigger:** Agendamento automático (5 minutos após o Head de Dados entregar o status ao CEO)
* **Agent:** Head de Gestão
* **Skill:** Análise de Gestão Baseada em Dados
* **Input:** Relatório diário de status entregue pelo Head de Dados às 07h15
* **Ação:** Interpretar os dados pela lente de gestão — identificar se há padrão ou alerta que requer orientação ao CEO
* **Output:** Se identificar problema de gestão: enviar interpretação ao CEO via Slack antes das 08h00. Se não: registrar leitura no log e aguardar próximo ciclo

## Briefing de Gestão Semanal

* **Frequência:** Toda segunda-feira às 08h30 BRT (`30 8 * * 1`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Gestão + todos os clones
* **Skill:** Briefing de Gestão Semanal
* **Input:** Relatório semanal do Head de Dados + OKRs no Asana + desafios da semana anterior
* **Ação:** Gerar briefing com top 3 orientações de gestão, clone em destaque da semana e ritual de gestão recomendado
* **Output:** Mensagem no Slack ao CEO com briefing de gestão semanal

## Clone em Destaque da Semana

* **Frequência:** Toda segunda-feira às 09h00 BRT (`0 9 * * 1`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Gestão
* **Skill:** Consulta ao Conselho de Clones
* **Input:** Contexto atual da empresa (dados da semana, desafio principal identificado)
* **Ação:** Selecionar o clone mais relevante para o momento atual da Neural Trax e gerar uma dica aprofundada daquele especialista — aplicada diretamente ao contexto da semana
* **Output:** Mensagem no Slack ao CEO com: "Clone em Destaque desta semana: \[Nome]" + perspectiva aprofundada aplicada à situação atual + 1 exercício ou prática recomendada

## Check-in de Implementação de Recomendações

* **Frequência:** Toda quinta-feira às 17h00 BRT (`0 17 * * 4`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Gestão
* **Skill:** Resposta a Demanda Pontual do CEO
* **Input:** Log de recomendações entregues na semana que ainda não receberam feedback de implementação
* **Ação:** Enviar check-in ao CEO sobre as recomendações da semana — foram implementadas? Gerou resultado? Precisa de ajuste?
* **Output:** Mensagem no Slack ao CEO perguntando sobre a recomendação principal da semana + abertura para ajuste ou aprofundamento

## Relatório Mensal de Gestão

* **Frequência:** Primeiro dia útil de cada mês às 09h00 BRT
* **Trigger:** Agendamento automático (após o Relatório Executivo Mensal do Head de Dados)
* **Agent:** Head de Gestão + todos os clones
* **Skill:** Análise de Gestão Baseada em Dados + Consulta ao Conselho de Clones
* **Input:** Relatório executivo mensal do Head de Dados + OKRs do período + histórico de recomendações de gestão do mês
* **Ação:** Gerar relatório mensal de gestão com: padrões organizacionais identificados no mês, recomendações implementadas e seu impacto percebido, foco de gestão para o próximo mês e perspectiva consolidada dos 6 clones sobre o momento da empresa
* **Output:** Mensagem no Slack ao CEO com resumo executivo de gestão do mês + recomendação de foco de liderança para o próximo período
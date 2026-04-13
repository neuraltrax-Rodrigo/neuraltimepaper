# CronJobs

## Briefing Estratégico Semanal do Squad

* **Frequência:** Toda segunda-feira às 09h00 BRT (`0 9 * * 1`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth
* **Skill:** Briefing Estratégico Semanal do Squad
* **Input:** Métricas da semana anterior, prioridades do CEO, bloqueios do Head de Conversão
* **Ação:** Redigir e publicar briefing de performance + foco da semana para o squad
* **Output:** Mensagem no canal de growth no Slack com performance anterior, metas da semana e 1 ação prioritária para o time

## Análise Semanal de Funil

* **Frequência:** Toda quarta-feira às 10h00 BRT (`0 10 * * 3`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth + Head de Conversão
* **Skill:** Análise e Otimização de Funil
* **Input:** Dados do funil da semana até quarta-feira (metade da semana — permite ajuste antes do fim)
* **Ação:** Analisar funil, identificar gargalo da semana e enviar plano de otimização ao Head de Conversão
* **Output:** Diagnóstico de funil + ações de otimização no Slack ao Head de Conversão + atualização no Asana

## Relatório Semanal de Growth para o CEO

* **Frequência:** Toda sexta-feira às 16h30 BRT (`30 16 * * 5`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth
* **Skill:** Relatório Semanal de Growth para o CEO
* **Input:** KPIs do funil da semana, MRR novo, CAC, destaques e gargalos
* **Ação:** Consolidar métricas, gerar relatório executivo e enviar ao CEO
* **Output:** Mensagem no Slack ao CEO com MRR novo, leads, conversão, CAC, destaque, gargalo e próximo movimento estratégico

## Revisão e Atualização de Playbook

* **Frequência:** Todo primeiro dia útil do mês às 10h00 BRT
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth + Alfredo Soares + Mapeador de Objeções + Gerador de Scripts
* **Skill:** Desenvolvimento e Atualização de Playbooks
* **Input:** Dados de objeções do mês, transcrições de chamadas, taxas de conversão por abordagem testada
* **Ação:** Revisar e atualizar playbook completo de vendas com base nos dados do mês anterior
* **Output:** Playbook atualizado publicado no Slack do squad + resumo das mudanças comunicado ao Head de Conversão

## Revisão de Estratégia de Growth (Trimestral)

* **Frequência:** Primeiro dia útil de cada trimestre às 09h00 BRT
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth + Alfredo Soares
* **Skill:** Desenvolvimento de Estratégia de Growth
* **Input:** Performance do trimestre anterior, OKRs do próximo trimestre, dados de ICP e feedback de mercado
* **Ação:** Desenvolver nova estratégia de growth para o trimestre — ICP, canais, metas e playbook base
* **Output:** Documento de estratégia trimestral distribuído ao CEO e Head de Conversão + tarefas criadas no Asana para execução

## Monitoramento de Negociações Paradas

* **Frequência:** Todo dia útil às 11h00 e às 17h00 BRT (`0 11,17 * * 1-5`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth
* **Skill:** Análise e Otimização de Funil (escopo de pipeline)
* **Input:** Lista de negociações ativas no pipeline com data da última interação
* **Ação:** Identificar negociações sem movimentação há mais de 5 dias úteis e acionar Head de Conversão para desbloqueio
* **Output:** Alerta no Slack ao Head de Conversão com lista de deals parados + orientação de próxima ação para cada um

## Check-in com Head de Conversão

* **Frequência:** Toda quinta-feira às 15h00 BRT (`0 15 * * 4`)
* **Trigger:** Agendamento automático
* **Agent:** Head de Growth + Head de Conversão
* **Skill:** Briefing Estratégico Semanal do Squad (escopo de alinhamento bilateral)
* **Input:** Status de execução da semana, bloqueios, insights de campo do Head de Conversão
* **Ação:** Alinhar execução, resolver bloqueios, coletar insights do campo e ajustar abordagem se necessário
* **Output:** Decisões de ajuste comunicadas ao squad via Slack + atualização de tarefas no Asana se necessário
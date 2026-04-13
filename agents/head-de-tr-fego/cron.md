# CronJobs

## Briefing Semanal do Squad de Tráfego

* **Frequência:** Toda segunda-feira às 09h00 BRT (`0 9 * * 1`)
* **Agent:** Head de Tráfego
* **Skill:** Gestão de Performance de Campanhas
* **Input:** Performance da semana anterior, foco da semana e feedback de qualidade de lead
* **Ação:** Publicar briefing no canal do squad com prioridades e ajustes táticos da semana
* **Output:** Mensagem no Slack com: número de leads da semana anterior, foco da semana e 1 ação prioritária por canal

## Revisão de Criativos

* **Frequência:** Toda quarta-feira às 10h00 BRT (`0 10 * * 3`)
* **Agent:** Head de Tráfego + Media Buyer
* **Skill:** Briefing de Criativos e Conteúdo
* **Input:** Performance dos criativos ativos (CTR, CPL, frequência), ângulos não testados
* **Ação:** Pausar criativos esgotados e gerar briefing de novos testes
* **Output:** Decisão de pausa comunicada ao Media Buyer + briefing de 2+ novos criativos para a semana

## Relatório Semanal para o Head de Growth

* **Frequência:** Toda sexta-feira às 15h30 BRT (`30 15 * * 5`)
* **Agent:** Head de Tráfego + Analista de Relatórios
* **Skill:** Relatório Semanal de Tráfego para o Head de Growth
* **Input:** Consolidado de todos os canais da semana
* **Ação:** Gerar e enviar relatório de performance ao Head de Growth
* **Output:** Mensagem no Slack com leads totais, CPL médio, canal destaque, canal problemático e próxima ação

## Diagnóstico Mensal de Mix de Canais

* **Frequência:** Todo dia 1 do mês às 10h00 BRT (`0 10 1 * *`)
* **Agent:** Head de Tráfego + Analista de Relatórios
* **Skill:** Diagnóstico de Mix de Canais
* **Input:** Performance consolidada do mês por canal — CPL, volume, qualidade de lead
* **Ação:** Avaliar mix de canais e recomendar realocação de budget ou esforço para o próximo mês
* **Output:** Recomendação de mix enviada ao Head de Growth + ajustes executados no Google Sheets

## Coleta de Feedback de Qualidade de Lead

* **Frequência:** Toda quinta-feira às 14h00 BRT (`0 14 * * 4`)
* **Agent:** Head de Tráfego
* **Skill:** Gestão de Performance de Campanhas
* **Input:** Dados do Head de Conversão — taxa de show-up, leads avançados no funil e descartados com motivo
* **Ação:** Coletar feedback de qualidade de lead do Head de Conversão e cruzar com dados de canal e segmentação
* **Output:** Ajuste de segmentação ou ICP comunicado ao Media Buyer se qualidade de lead estiver abaixo do esperado
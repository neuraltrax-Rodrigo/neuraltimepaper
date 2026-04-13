# CronJobs

## Relatório Financeiro Semanal

* **Frequência:** Toda segunda-feira às 08h00 BRT (`0 8 * * 1`)
* **Trigger:** Agendamento automático
* **Agent:** CFO + Forecast
* **Skill:** Relatório Financeiro Executivo
* **Input:** Fluxo de caixa da semana anterior, MRR atual, despesas categorizadas
* **Ação:** Gerar e enviar resumo financeiro executivo ao CEO
* **Output:** Mensagem no Slack com MRR, margem, alertas e recomendações da semana

## Verificação Diária de Recebíveis

* **Frequência:** Todo dia útil às 09h00 BRT (`0 9 * * 1-5`)
* **Trigger:** Agendamento automático
* **Agent:** Ledger
* **Skill:** Controle de Recebíveis
* **Input:** Lista de contratos ativos e status de pagamento
* **Ação:** Verificar vencimentos do dia e dos próximos 3 dias; disparar lembretes se necessário
* **Output:** Alerta no Slack se houver inadimplência ou vencimento iminente; e-mail automático ao cliente se aplicável

## Projeção Semanal de Fluxo de Caixa

* **Frequência:** Toda sexta-feira às 17h00 BRT (`0 17 * * 5`)
* **Trigger:** Agendamento automático
* **Agent:** CFO + Forecast
* **Skill:** Projeção de Fluxo de Caixa
* **Input:** Contratos ativos, pipeline de novos clientes, despesas fixas e variáveis previstas
* **Ação:** Atualizar planilha de projeção para 30/60/90 dias em 3 cenários
* **Output:** Planilha atualizada no Google Sheets + resumo enviado ao CEO no Slack

## Emissão de Notas Fiscais

* **Frequência:** Todo dia 1 do mês às 07h00 BRT (`0 7 1 * *`)
* **Trigger:** Agendamento automático
* **Agent:** Fiscal
* **Skill:** \<preencher: skill de emissão automática de NF-e>
* **Input:** Lista de clientes ativos com valores de competência do mês
* **Ação:** Emitir NFS-e para cada cliente ativo no mês, arquivar XMLs e PDFs
* **Output:** Confirmação de emissão por cliente + alerta ao CEO se alguma nota falhar

## Alerta de Obrigações Fiscais

* **Frequência:** Todo dia 15 e todo dia 20 do mês às 08h00 BRT (`0 8 15,20 * *`)
* **Trigger:** Agendamento automático
* **Agent:** Fiscal
* **Skill:** \<preencher: skill de controle tributário>
* **Input:** Calendário fiscal do mês (DAS, ISS, retenções)
* **Ação:** Checar obrigações com vencimento nos próximos 5 dias úteis e alertar CEO
* **Output:** Mensagem no Slack listando obrigação, valor estimado e data de vencimento

## Fechamento Mensal

* **Frequência:** Todo último dia útil do mês às 18h00 BRT
* **Trigger:** Agendamento automático
* **Agent:** CFO + Ledger + Margin
* **Skill:** Relatório Financeiro Executivo (escopo mensal)
* **Input:** Todas as movimentações do mês — receitas, despesas, NFs emitidas, impostos pagos
* **Ação:** Consolidar DRE do mês, calcular margem real por projeto e comparar com projeção
* **Output:** Relatório de fechamento mensal enviado ao CEO com DRE resumido e análise de variações
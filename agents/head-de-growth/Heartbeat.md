# HeartBeat

* **Frequência:** A cada 2 horas em dias úteis (07h–22h BRT); uma vez ao dia nos fins de semana (09h BRT)
* **Gatilhos:**
  * Alerta 🔴 do Head de Dados com queda de conversão ou leads abaixo do threshold → executar **Análise e Otimização de Funil** imediatamente e acionar Head de Conversão com plano de ação
  * Novo contrato fechado pelo squad → registrar no dashboard, calcular MRR novo acumulado e atualizar projeção de atingimento de meta
  * Negociação parada há mais de 5 dias úteis sem movimentação → acionar Head de Conversão para desbloqueio ou requalificação
  * Head de Conversão reporta bloqueio operacional → analisar, orientar e escalar ao CEO se necessário
  * CAC da semana ultrapassar limite definido → revisão imediata de canal ou abordagem de aquisição
  * Lead de conta estratégica (high-value) entrar no funil → enviar alerta ao CEO e garantir abordagem personalizada
* **Ações automáticas:**
  * Verificar status do pipeline no Google Sheets — identificar deals parados, reuniões sem follow-up e propostas não respondidas há mais de 3 dias
  * Checar se Head de Conversão 🔵 está operacional e executando o funil normalmente
  * Monitorar metas de MRR novo da semana — calcular % atingido e projeção de fechamento
  * Verificar se novas objeções foram mapeadas pelo Mapeador de Objeções e se o playbook precisa de atualização urgente
  * Confirmar se o Gerador de Scripts recebeu novos inputs da Transcrição de Chamadas para atualização
* **Thresholds de alerta (preencher com valores reais):**
  * Taxa de conversão lead → reunião: 🟡 abaixo de \<preencher: %> | 🔴 abaixo de \<preencher: %>
  * Taxa de conversão reunião → proposta: 🟡 abaixo de \<preencher: %> | 🔴 abaixo de \<preencher: %>
  * Taxa de conversão proposta → contrato: 🟡 abaixo de \<preencher: %> | 🔴 abaixo de \<preencher: %>
  * MRR novo semanal: 🟡 abaixo de \<preencher: R$> | 🔴 abaixo de \<preencher: R$>
  * CAC: 🟡 acima de \<preencher: R$> | 🔴 acima de \<preencher: R$>
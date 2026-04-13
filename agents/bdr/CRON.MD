**# CronJobs**




\- Nome: Captura de Leads Google Maps

  Frequência:

    - Diariamente às 08:00 (0 8 \* \* \*)

  Trigger:

    - Início do dia útil

  Agent:

    - Agente BDR

  Skill:

    - Captura de Leads Google Maps

  Input:

    - Cidades e segmentos alvo configurados

  Ação:

    - Buscar 50 novas empresas no Google Maps

    - Extrair dados de contato

    - Salvar no CRM

  Output:

    - Lista de novos leads no CRM




\- Nome: Captura de Decisores LinkedIn

  Frequência:

    - Diariamente às 09:00 (0 9 \* \* \*)

  Trigger:

    - Novas empresas no CRM

  Agent:

    - Agente BDR

  Skill:

    - Captura de Decisores LinkedIn

  Input:

    - Empresas capturadas sem decisor identificado

  Ação:

    - Buscar decisores no LinkedIn para novas empresas

    - Enriquecer leads com nome e cargo

  Output:

    - Leads enriquecidos com dados de decisores




\- Nome: Prospecção Primeiro Contato

  Frequência:

    - Diariamente às 10:00 (0 10 \* \* \*)

  Trigger:

    - Leads novos sem contato inicial

  Agent:

    - Agente BDR

  Skill:

    - Prospecção WhatsApp

  Input:

    - Leads com nome, empresa, telefone e decisor

  Ação:

    - Enviar mensagem de primeiro contato

    - Personalizar com nome e empresa

    - Registrar envio no CRM

  Output:

    - Mensagens enviadas e registradas




\- Nome: Follow-ups Pendentes

  Frequência:

    - Diariamente às 14:00 (0 14 \* \* \*)

  Trigger:

    - Follow-ups agendados para hoje

  Agent:

    - Agente BDR

  Skill:

    - Follow-up Sequencial

  Input:

    - Leads pendentes de follow-up

  Ação:

    - Enviar follow-ups agendados

    - Registrar interação no CRM

  Output:

    - Follow-ups executados




\- Nome: Qualificação de Respostas

  Frequência:

    - A cada 2 horas (0 \*/2 \* \* \*)

  Trigger:

    - Leads que responderam no WhatsApp

  Agent:

    - Agente BDR

  Skill:

    - Qualificação BANT

  Input:

    - Respostas dos leads

  Ação:

    - Analisar resposta

    - Aplicar framework BANT

    - Classificar lead (quente/morno/frio)

    - Agendar se quente

  Output:

    - Lead qualificado no CRM + reunião agendada se quente




\- Nome: Report Diário de Prospecção

  Frequência:

    - Diariamente às 18:00 (0 18 \* \* \*)

  Trigger:

    - Fim do horário comercial

  Agent:

    - Agente BDR

  Skill:

    - Qualificação BANT

  Input:

    - Atividades do dia (contatos, respostas, agendamentos)

  Ação:

    - Compilar métricas do dia

    - Calcular taxa de resposta e conversão

    - Gerar report

  Output:

    - Report enviado ao Head de Vendas:

      - Leads capturados: X

      - Mensagens enviadas: X

      - Respostas recebidas: X (taxa X%)

      - Leads qualificados: X quentes, X mornos, X frios

      - Reuniões agendadas: X




\- Nome: Limpeza e Nurturing Semanal

  Frequência:

    - Toda sexta às 16:00 (0 16 \* \* 5)

  Trigger:

    - Fim da semana

  Agent:

    - Agente BDR

  Skill:

    - Follow-up Sequencial

  Input:

    - Leads sem resposta após 5 toques

    - Leads mornos da semana

  Ação:

    - Mover leads sem resposta para nurturing

    - Agendar mensagem mensal para nurturing

    - Limpar leads frios da lista ativa

  Output:

    - CRM organizado, nurturing agendado
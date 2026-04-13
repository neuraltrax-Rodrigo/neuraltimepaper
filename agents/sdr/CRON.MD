**# CronJobs**




\- Nome: Busca de Leads na Agenteda

  Frequência:

    - Diariamente às 08:00 (0 8 \* \* \*)

  Trigger:

    - Início do dia útil

  Agent:

    - Agente SDR

  Skill:

    - Busca de Leads na Agenteda

  Input:

    - Segmento e cidade alvo configurados

  Ação:

    - Buscar 20-50 novos leads na Agenteda

    - Extrair nome, WhatsApp, email, empresa

  Output:

    - Lista de novos leads pronta para cadastro




\- Nome: Cadastro no Asana

  Frequência:

    - Diariamente às 08:30 (0 8:30 \* \* \*)

  Trigger:

    - Novos leads buscados na Agenteda

  Agent:

    - Agente SDR

  Skill:

    - Cadastro no Asana CRM

  Input:

    - Lista de leads da Agenteda

  Ação:

    - Verificar duplicatas

    - Cadastrar novos leads no Asana

    - Tag com segmento e fonte

  Output:

    - Leads cadastrados como "Novo Lead" no Asana




\- Nome: Prospecção Primeiro Contato

  Frequência:

    - Diariamente às 09:00 (0 9 \* \* \*)

  Trigger:

    - Leads novos sem contato inicial

  Agent:

    - Agente SDR

  Skill:

    - Prospecção WhatsApp com Roteiro

  Input:

    - Leads com nome e WhatsApp

  Ação:

    - Enviar saudação Etapa 1 ("Oi! Aqui é \[nome] da Neural Trax 😊")

    - Registrar envio no Asana

  Output:

    - Mensagens enviadas (máx 30/dia)




\- Nome: Processamento de Respostas

  Frequência:

    - A cada 2 horas (0 \*/2 \* \* \*)

  Trigger:

    - Leads que responderam no WhatsApp

  Agent:

    - Agente SDR

  Skill:

    - Prospecção WhatsApp com Roteiro

    - Qualificação BANT Simplificada

  Input:

    - Respostas dos leads

  Ação:

    - Avançar no roteiro (Etapas 2-6.4)

    - Aplicar BANT simplificado

    - Se quente: oferecer agendamento

    - Se morno: agendar follow-up

    - Se frio: mover para nurturing

  Output:

    - Lead qualificado ou agendamento feito




\- Nome: Follow-ups Pendentes

  Frequência:

    - Diariamente às 14:00 (0 14 \* \* \*)

  Trigger:

    - Follow-ups agendados (24h, 48h, 72h, 5 dias)

  Agent:

    - Agente SDR

  Skill:

    - Follow-up Sequencial (4 toques)

  Input:

    - Leads pendentes de follow-up

  Ação:

    - Enviar follow-up com novo ângulo

    - Registrar no Asana

    - Após 4º follow-ups: mover para "Sem Resposta"

  Output:

    - Follow-ups executados




\- Nome: Envio de Lembretes de Reunião

  Frequência:

    - A cada 1 hora (0 \* \* \* \*)

  Trigger:

    - Reuniões agendadas para próxima hora

  Agent:

    - Agente SDR

  Skill:

    - Agendamento de Reunião

  Input:

    - Reuniões agendadas

  Ação:

    - Enviar lembrete 1h antes: "Oi \[nome], lembrando nosso agendamento às \[hora] 😊"

  Output:

    - Lembrete enviado




\- Nome: Report Diário de Prospecção

  Frequência:

    - Diariamente às 18:00 (0 18 \* \* \*)

  Trigger:

    - Fim do horário comercial

  Agent:

    - Agente SDR

  Skill:

    - Qualificação BANT Simplificada

  Input:

    - Atividades do dia

  Ação:

    - Compilar métricas:

      - Leads buscados na Agenteda: X

      - Cadastrados no Asana: X

      - Mensagens enviadas: X

      - Respostas recebidas: X (taxa X%)

      - Follow-ups executados: X

      - Leads qualificados: X quentes, X mornos, X frios

      - Reuniões agendadas: X

    - Enviar ao Head de Vendas

  Output:

    - Report diário enviado




\- Nome: Limpeza Semanal de Leads

  Frequência:

    - Toda sexta às 16:00 (0 16 \* \* 5)

  Trigger:

    - Fim da semana

  Agent:

    - Agente SDR

  Skill:

    - Follow-up Sequencial (4 toques)

  Input:

    - Leads sem resposta após 4 follow-ups

    - Leads frios da semana

  Ação:

    - Mover para nurturing ou "Sem Resposta"

    - Limpar leads frios da lista ativa

  Output:

    - Asana organizado
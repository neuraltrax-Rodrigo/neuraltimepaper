**# CronJobs**




\- Nome: Monitorar Projetos Fechados no Asana

  Frequência:

    - Diariamente às 09:00 (0 9 \* \* \*)

  Trigger:

    - Projetos com status "Fechado"

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Extração de Dados do Asana

  Input:

    - Projetos no Asana com status "Fechado"

  Ação:

    - Buscar projetos fechados nas últimas 24h

    - Extrair dados completos

    - Validar dados

  Output:

    - Lista de projetos prontos para geração de contrato




\- Nome: Gerar Contratos Pendentes

  Frequência:

    - Diariamente às 10:00 (0 10 \* \* \*)

  Trigger:

    - Dados validados de projetos fechados

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Montagem de Contrato

    - Geração de PDF

  Input:

    - Dados validados do projeto

    - Modelo de contrato vigente

  Ação:

    - Montar contrato com dados do projeto

    - Gerar PDF profissional

    - Salvar rascunho

  Output:

    - Contrato em PDF pronto para aprovação




\- Nome: Enviar Contratos para Aprovação

  Frequência:

    - Diariamente às 11:00 (0 11 \* \* \*)

  Trigger:

    - Contratos gerados pendentes de aprovação

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Submissão para Aprovação

  Input:

    - Contrato em PDF

    - Dados do cliente

  Ação:

    - Enviar email ao usuário com PDF e checklist

    - Aguardar aprovação

  Output:

    - Solicitação de aprovação enviada




\- Nome: Processar Aprovações Recebidas

  Frequência:

    - A cada 2 horas (0 \*/2 \* \* \*)

  Trigger:

    - Aprovação ou solicitação de alteração recebida

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Submissão para Aprovação

    - Envio ao Cliente

  Input:

    - Resposta do usuário (aprovado ou alterações)

  Ação:

    - Se aprovado: enviar contrato ao cliente por email

    - Se alterações: aplicar, gerar novo PDF e reenviar para aprovação

  Output:

    - Contrato enviado ao cliente OU novo rascunho para revisão




\- Nome: Rastrear Abertura pelo Cliente

  Frequência:

    - Diariamente às 15:00 (0 15 \* \* \*)

  Trigger:

    - Contratos enviados ao cliente

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Envio ao Cliente

  Input:

    - Status de rastreamento de emails enviados

  Ação:

    - Verificar se clientes abriram emails

    - Se não abriu em 48h: enviar lembrete

    - Se abriu: registrar e monitorar assinatura

  Output:

    - Status atualizado: aberto/não aberto + lembrete enviado se necessário




\- Nome: Cobrança de Contratos Não Assinados

  Frequência:

    - Toda segunda às 10:00 (0 10 \* \* 1)

  Trigger:

    - Contratos enviados há mais de 7 dias sem assinatura

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Envio ao Cliente

  Input:

    - Contratos pendentes de assinatura

  Ação:

    - Listar contratos sem assinatura há +7 dias

    - Alertar usuário com lista

    - Sugerir ação de cobrança

  Output:

    - Report de contratos pendentes com recomendação de ação




\- Nome: Arquivamento Semanal de Contratos

  Frequência:

    - Toda sexta às 17:00 (0 17 \* \* 5)

  Trigger:

    - Fim da semana

  Agent:

    - Agente Gerador de Contratos

  Skill:

    - Envio ao Cliente

  Input:

    - Todos os contratos da semana

  Ação:

    - Compilar contratos gerados, aprovados, enviados e assinados

    - Gerar report semanal

    - Arquivar cópias

  Output:

    - Report semanal: X gerados, X aprovados, X enviados, X assinados
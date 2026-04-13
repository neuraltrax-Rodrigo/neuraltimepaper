**# Skills**




\- Nome: Busca de Leads na Agenteda

  Descrição: Buscar e extrair leads de empresas no Google via Agenteda

  Input:

    - Segmento alvo (ex: clínicas, escritórios, lojas)

    - Cidade e estado

  Output:

    - Lista de leads com nome, WhatsApp, email, empresa, site

  Tools:

    - Agenteda (Google Agent)

  Processo:

    1. Conectar à Agenteda

    2. Buscar empresas por segmento e cidade

    3. Extrair dados de contato (WhatsApp prioritário)

    4. Identificar decisor quando possível

    5. Salvar lista estruturada

  Regras:

    - Máximo 50 leads por busca por dia

    - Priorizar WhatsApp disponível

    - Validar telefones antes de cadastrar

    - Remover duplicatas




\- Nome: Cadastro no Asana CRM

  Descrição: Cadastrar lead como cliente no Asana com dados completos

  Input:

    - Dados do lead (nome, WhatsApp, email, empresa, fonte)

  Output:

    - Cliente criado no Asana com status "Novo Lead"

  Tools:

    - Asana CRM

  Processo:

    1. Verificar se cliente já existe (evitar duplicata)

    2. Criar novo cliente com dados completos

    3. Definir etapa do funil como "Novo Lead"

    4. Registrar fonte (Agenteda/Google)

    5. Adicionar nota com contexto da busca

  Regras:

    - Nunca criar duplicatas

    - Preencher todos os campos obrigatórios

    - Tag com segmento e cidade




\- Nome: Prospecção WhatsApp com Roteiro

  Descrição: Executar roteiro humanizado de prospecção via WhatsApp (Etapas 1-6.4)

  Input:

    - Lead com nome, empresa, WhatsApp

  Output:

    - Conversa conduzida até agendamento ou qualificação

  Tools:

    - WhatsApp Sender

    - WhatsApp Template Manager

  Processo:

    1. Etapa 1: Saudação e apresentação ("Oi! Aqui é \[nome] da Neural Trax 😊")

    2. Etapa 2: Identificação + pedir nome ("Como você se chama?")

    3. Etapa 3: Aprofundar necessidade ("Conta mais sobre o que busca?")

    4. Etapa 4: Apresentação da solução + tranquilização

    5. Etapa 5: Oferta de agendamento ("Quer agendar um horário?")

    6. Etapa 6.1: Coletar preferência de dia

    7. Etapa 6.2: Verificar horários vagos (agrupar manhã/tarde, máx 5 opções)

    8. Etapa 6.3: Confirmação final ("Posso confirmar?")

    9. Etapa 6.4: Finalizar agendamento no sistema

  Regras:

    - Máximo 2-3 linhas por mensagem

    - Sempre uma pergunta por vez

    - Falar preço apenas se cliente perguntar

    - Só mostrar horários vagos

    - Após horário limite: agendar próximo dia útil

    - Nunca agendar sem "pode confirmar?"

    - Responder em JSON: {"mensagem": "...", "event\_id": "..."} se agendado




\- Nome: Follow-up Sequencial (4 toques)

  Descrição: Executar até 4 follow-ups para leads sem resposta

  Input:

    - Lead que não respondeu após X dias

    - Histórico da conversa

  Output:

    - Follow-up enviado e registrado no Asana

  Tools:

    - WhatsApp Sender

    - WhatsApp Template Manager

    - Asana CRM

  Processo:

    1. Verificar leads sem resposta

    2. 1º follow-up (24h): "Oi \[nome], tudo bem? Só passando pra saber se viu minha mensagem 😊"

    3. 2º follow-up (48h): Novo ângulo de valor

    4. 3º follow-up (72h): Última tentativa com urgência leve

    5. 4º follow-up (5 dias): "Vou encerrar seu atendimento por aqui, mas fico à disposição!"

    6. Após 4 follow-ups: mover para "Sem Resposta" no Asana

  Regras:

    - Intervalo mínimo 24h entre follow-ups

    - Cada follow-up traz novo valor (não repetir)

    - Máximo 4 follow-ups

    - Após 4º: parar e mover para nurturing




\- Nome: Qualificação BANT Simplificada

  Descrição: Qualificar leads durante conversa com BANT simplificado

  Input:

    - Respostas do lead no WhatsApp

  Output:

    - Lead classificado: quente, morno ou frio

  Tools:

    - Lead Qualifier BANT

    - Asana CRM

  Processo:

    1. Budget: se perguntar preço \= sinal de interesse

    2. Authority: confirmar se é decisor ("Você quem decide isso?")

    3. Need: dor expressa na conversa

    4. Timeline: urgência ("Pra quando precisa?")

    5. Classificar:

       - Quente (3+ critérios): agendar reunião

       - Morno (2 critérios): nurturing semanal

       - Frio (0-1): remove da lista ativa

    6. Registrar qualificação no Asana

  Regras:

    - Não interrogar o lead — perguntas naturais na conversa

    - Se lead não quer agendar: respeitar e mover para nurturing

    - Lead quente: alertar closer imediatamente




\- Nome: Agendamento de Reunião

  Descrição: Agendar reunião entre lead qualificado e closer

  Input:

    - Lead quente que aceitou agendar

    - Disponibilidade do closer

  Output:

    - Reunião agendada + confirmação ao lead

  Tools:

    - Agendamento

    - WhatsApp Sender

    - Asana CRM

  Processo:

    1. Consultar horários vagos no calendário

    2. Oferecer opções agrupadas (manhã/tarde, máx 5)

    3. Se for hoje: mostrar apenas horários após agora

    4. Confirmar com lead: "\[dia] às \[hora]. Posso confirmar?"

    5. Após confirmação explícita: agendar no sistema

    6. Enviar confirmação: "Pronto, \[nome]! 😊 Agendado: \[dia, dd/mm às HH:mm]"

    7. Lembrete 1h antes

  Regras:

    - Formato de data brasileiro (dia da semana, dd/mm)

    - Nunca incluir EventId na mensagem — apenas no campo event\_id do JSON

    - Mínimo 1h de antecedência

    - Se lead faltar: reagenda uma vez, depois descarta
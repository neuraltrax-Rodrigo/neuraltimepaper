**# Skills**




\- Nome: Captura de Leads Google Maps

  Descrição: Extrair empresas alvo do Google Maps por localização e segmento

  Input:

    - Cidade e estado alvo

    - Categoria de empresa (ex: clínicas, escritórios, lojas)

    - Mínimo de avaliações

  Output:

    - Lista estruturada com nome, telefone, endereço, site, nota

  Tools:

    - Google Maps Scraper

  Processo:

    1. Definir parâmetros de busca (cidade, categoria)

    2. Executar scraper no Google Maps

    3. Filtrar por nota mínima e relevância

    4. Extrair dados de contato

    5. Salvar lista no CRM

  Regras:

    - Máximo 100 leads por busca por dia

    - Validar telefones antes de adicionar

    - Remover duplicatas do CRM




\- Nome: Captura de Decisores LinkedIn

  Descrição: Encontrar decisores das empresas alvo no LinkedIn

  Input:

    - Lista de empresas do Google Maps

    - Cargos alvo (CEO, Diretor, Gerente, Dono)

  Output:

    - Lista de decisores com nome, cargo, empresa, link perfil

  Tools:

    - LinkedIn Lead Finder

  Processo:

    1. Carregar lista de empresas

    2. Buscar decisores por empresa no LinkedIn

    3. Filtrar por cargo e senioridade

    4. Extrair dados de contato

    5. Enriquecer leads no CRM

  Regras:

    - Máximo 50 buscas por dia (limite LinkedIn)

    - Priorizar CEO/dono para PMEs

    - Não conectar automaticamente sem personalização




\- Nome: Prospecção WhatsApp

  Descrição: Enviar mensagens de prospecção personalizadas via WhatsApp

  Input:

    - Lista de leads com nome, empresa, telefone

    - Dor ou gancho personalizado

  Output:

    - Mensagem enviada e registrada no CRM

  Tools:

    - WhatsApp Sender

    - WhatsApp Template Manager

  Processo:

    1. Carregar lista de leads

    2. Selecionar template de primeiro contato

    3. Personalizar com nome, empresa e dor

    4. Enviar em horário comercial (09:00-18:00)

    5. Registrar envio no CRM

  Regras:

    - Apenas horário comercial (09:00-18:00)

    - Máximo 30 mensagens por dia por número

    - Sempre incluir opção de descadastrar

    - Linguagem profissional e consultiva




\- Nome: Follow-up Sequencial

  Descrição: Executar sequência de 5 follow-ups para leads sem resposta

  Input:

    - Lead que não respondeu após X dias

    - Histórico de interações

  Output:

    - Follow-up enviado e registrado

  Tools:

    - WhatsApp Sender

    - WhatsApp Template Manager

    - CRM de Vendas

  Processo:

    1. Verificar leads sem resposta

    2. Selecionar template de follow-up (2º ao 5º toque)

    3. Aguardar intervalo adequado (2-3 dias entre toques)

    4. Enviar follow-up com novo ângulo ou valor

    5. Registrar no CRM

    6. Após 5 toques sem resposta: marcar como "sem resposta"

  Regras:

    - Intervalo mínimo 2 dias entre follow-ups

    - Cada follow-up traz novo valor (não repetir)

    - Após 5 toques: parar e mover para nurturing




\- Nome: Qualificação BANT

  Descrição: Qualificar leads usando framework BANT (Budget, Authority, Need, Timeline)

  Input:

    - Lead que respondeu no WhatsApp

    - Respostas do lead

  Output:

    - Lead qualificado (quente/morno/frio) + notas no CRM

  Tools:

    - Lead Qualifier

    - CRM de Vendas

  Processo:

    1. Analisar resposta do lead

    2. Avaliar Budget: tem orçamento definido?

    3. Avaliar Authority: é o decisor?

    4. Avaliar Need: tem dor real?

    5. Avaliar Timeline: urgência de implementação?

    6. Score e classificar (quente: agenda, morno: nurturing, frio: descarta)

    7. Registrar qualificação no CRM

  Regras:

    - Quente: 3+ critérios atendidos → agenda reunião

    - Morno: 2 critérios → nurturing semanal

    - Frio: 0-1 critério → remove da lista ativa




\- Nome: Agendamento de Reunião

  Descrição: Agendar reunião entre lead qualificado e closer

  Input:

    - Lead quente qualificado

    - Disponibilidade do closer

  Output:

    - Reunião agendada no calendário + confirmação ao lead

  Tools:

    - CRM de Vendas

    - WhatsApp Sender

  Processo:

    1. Verificar disponibilidade do closer

    2. Oferecer 2-3 horários ao lead

    3. Confirmar horário escolhido

    4. Agendar no calendário do closer

    5. Enviar confirmação ao lead com data, hora e link

    6. Lembrete 1h antes da reunião

  Regras:

    - Mínimo 24h de antecedência

    - Confirmar com lead antes de agendar

    - Enviar lembrete 1 dia e 1h antes

    - Se lead faltar: reagenda uma vez, depois descarta
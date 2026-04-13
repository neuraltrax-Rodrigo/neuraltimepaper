**# Skills**




\- Nome: Extração de Dados do Asana

  Descrição: Ler e extrair dados de projeto fechado no Asana

  Input:

    - Projeto com status "Fechado" no Asana

  Output:

    - Dados estruturados: cliente, CNPJ, produtos, automações, valores, prazo de implementação

  Tools:

    - Asana Integration

  Processo:

    1. Monitorar Asana por projetos com status "Fechado"

    2. Extrair dados do cliente (nome, email, CNPJ, telefone)

    3. Extrair escopo (produtos, automações, implementação)

    4. Extrair valores (total, forma de pagamento, parcelas)

    5. Extrair prazos (início, entrega, vigência)

    6. Validar completude dos dados

  Regras:

    - Se dados incompletos: alertar usuário e pausar

    - Validar CNPJ e dados do cliente

    - Valores devem bater com proposta aprovada




\- Nome: Montagem de Contrato

  Descrição: Conectar dados extraídos ao modelo de contrato e preencher cláusulas

  Input:

    - Dados estruturados do projeto (cliente, escopo, valores, prazos)

    - Modelo de contrato vigente

  Output:

    - Contrato completo preenchido em formato estruturado

  Tools:

    - Modelo de Contrato

    - Catálogo de Produtos e Automações

  Processo:

    1. Carregar modelo de contrato vigente

    2. Preencher dados das partes (Neural Trax e cliente)

    3. Preencher cláusula de escopo com produtos e automações

    4. Preencher cláusula de valores e forma de pagamento

    5. Preencer cláusula de prazos e cronograma

    6. Preencer cláusulas de confidencialidade e LGPD

    7. Revisar consistência de todos os dados

  Regras:

    - Usar modelo mais recente (nunca desatualizado)

    - Escopo deve espelhar exatamente o vendido

    - Valores com moeda e forma de pagamento explícitos

    - Incluir cláusulas de rescisão e multas padrão




\- Nome: Geração de PDF

  Descrição: Converter contrato estruturado em PDF profissional

  Input:

    - Contrato preenchido em formato estruturado

  Output:

    - PDF pronto para envio

  Tools:

    - Gerador de PDF

  Processo:

    1. Receber contrato estruturado

    2. Aplicar formatação profissional (logo, fontes, margens)

    3. Gerar PDF

    4. Validar integridade do arquivo

    5. Nomear arquivo padrão: "Contrato\_\[Cliente]\_\[Data].pdf"

  Regras:

    - PDF deve ser legível e profissional

    - Incluir numeração de páginas

    - Logo da Neural Trax no cabeçalho




\- Nome: Submissão para Aprovação

  Descrição: Enviar contrato ao usuário para aprovação antes de envio ao cliente

  Input:

    - Contrato em PDF pronto

    - Dados do cliente para contexto

  Output:

    - Aprovação recebida ou lista de alterações solicitadas

  Tools:

    - Aprovador de Contrato

    - Email Sender

  Processo:

    1. Enviar email ao usuário com PDF em anexo

    2. Incluir checklist de revisão (escopo, valores, prazos, partes)

    3. Aguardar aprovação ou pedido de alteração

    4. Se aprovado: prosseguir para envio ao cliente

    5. Se alterações: aplicar e reenviar para nova aprovação

  Regras:

    - Nunca enviar ao cliente sem aprovação explícita

    - Aguardar no máximo 24h por aprovação

    - Se alterações solicitadas: aplicar e confirmar antes de prosseguir




\- Nome: Envio ao Cliente

  Descrição: Enviar contrato aprovado ao cliente por email

  Input:

    - Contrato aprovado em PDF

    - Email e nome do cliente

  Output:

    - Contrato enviado e rastreado

  Tools:

    - Email Sender

  Processo:

    1. Montar email profissional com apresentação do contrato

    2. Anexar PDF do contrato

    3. Enviar ao cliente

    4. Rastrear abertura do email

    5. Registrar envio no sistema

    6. Se não abrir em 48h: enviar lembrete

  Regras:

    - Email com tom profissional e acolhedor

    - Incluir instruções de assinatura e devolução

    - CC para usuário em todos os envios

    - Arquivar cópia do contrato enviado




\- Nome: Validação de Dados do Projeto

  Descrição: Validar consistência e completude dos dados antes de gerar contrato

  Input:

    - Dados extraídos do Asana

  Output:

    - Dados validados (ok) ou lista de pendências

  Tools:

    - Asana Integration

    - Catálogo de Produtos e Automações

  Processo:

    1. Verificar se todos os campos obrigatórios estão preenchidos

    2. Validar CNPJ do cliente

    3. Validar valores (total \= soma das parcelas)

    4. Validar produtos e automações no catálogo

    5. Validar prazos (início \< entrega \< vigência)

    6. Reportar ok ou pendências

  Regras:

    - Se qualquer dado faltando: alertar e pausar

    - Valores inconsistentes: pedir confirmação

    - Produto não encontrado no catálogo: alertar